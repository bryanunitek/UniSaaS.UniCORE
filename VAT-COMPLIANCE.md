# VAT Compliance

**What this document covers:** the UniCORE cross-vertical VAT and consumption-tax compliance infrastructure — the 178-jurisdiction gate architecture, the VAT resolver engine, the Making Tax Digital (MTD) digital-links gate, and the honest-fixture posture that governs what the substrate does and does not claim.

**What this document does not cover:** jurisdiction-specific filing procedures, tax authority portal credentials, filing calendars, or VAT return computation. Those are operational matters for the Vertical CORE and its host.

---

## Status

This document describes the **Tier-4 VAT Compliance** infrastructure as implemented in the UniCORE substrate. The implementation covers 178 consumption-tax jurisdictions across the world. Coverage is complete for non-EU jurisdictions. EU VAT remains in scope — see §EU VAT below.

---

## Coverage overview

UniCORE's VAT compliance infrastructure covers **178 distinct jurisdictions** across every continent. Each jurisdiction has a dedicated gate interface (`I<Country>VatSubmissionGate` or equivalent) that validates a dossier of prescribed invoice data against that jurisdiction's current rules.

The infrastructure is a **cross-vertical substrate** — the same gate architecture serves every Vertical CORE built on UniCORE. A Vertical CORE for law firms, accounting firms, or any other vertical inherits the same 178-gate infrastructure without modification.

### Coverage by region

| Region | Approximate count | Notes |
|---|---|---|
| Europe | ~50 | EU Member States + EEA + microstates + UK + Switzerland |
| Asia Pacific | ~45 | GCC + South Asia + Southeast Asia + East Asia + Oceania |
| Middle East | ~8 | Including UAE, Saudi, Qatar, Oman, Bahrain, Kuwait, Israel, Jordan |
| Africa | ~40 | Sub-Saharan + North Africa + island jurisdictions |
| Americas | ~35 | North America, Central America, South America, Caribbean |

Exact counts shift as jurisdictions update their tax regimes. The substrate is versioned with each gate change; the matrix in the repository root tracks the current authoritative count.

### What "coverage" means

Coverage means the gate **interface exists** and the **validation logic is implemented** for the current statutory rules. Coverage does not mean the gate has been tested against every possible real-world scenario in every jurisdiction — that would require live filings in every country, which is not possible from a single jurisdiction.

The honest-fixture posture (see §Honest-fixture posture below) governs what the substrate claims about real-world identifiers.

---

## Architecture

### One gate per jurisdiction

Each jurisdiction has a single gate interface. The interface name follows the pattern:

```
I<Country><TaxType>SubmissionGate
```

Examples: `IVietnamVatSubmissionGate`, `IBhutanGstSubmissionGate`, `IUkMtdDigitalLinksGate`

The gate takes a **dossier** (a structured record of the invoice's prescribed data) and returns a **report** (a structured record of every criterion checked). No gate returns a raw boolean — the report always carries the granular result of each criterion.

### Gate interface pattern

Every gate implements the same pattern:

```csharp
public interface I<Country><TaxType>SubmissionGate
{
    <Country><TaxType>SubmissionReport Validate(
        <Country><TaxType>Dossier dossier,
        DateTime utcNow);
}
```

The dossier captures the prescribed data fields for that jurisdiction. The report captures:

- Each individual criterion result (`bool`)
- An overall compliance flag
- The jurisdiction's authority name
- The regulatory anchors (statute citations)
- Whether the gate applied the current rate or a historical rate

### No central resolver — interface-discovered

There is no central `IVatResolver` that routes to a specific gate. Vertical Cores access the gate they need by requesting the interface directly from DI:

```csharp
IVietnamVatSubmissionGate gate = serviceProvider
    .GetRequiredService<IVietnamVatSubmissionGate>();
var report = gate.Validate(dossier, DateTimeOffset.UtcNow);
```

This means the Vertical CORE explicitly names the jurisdiction it is filing to. There is no ambiguity about which gate handled a given submission.

---

## Non-EU consumption taxes

The primary coverage scope is **non-EU consumption taxes** — VAT, GST, and equivalent indirect taxes in jurisdictions outside the EU. These are implemented as a flat list with no EU-specific assumptions.

Examples (selected):
- Australia GST (`IAustraliaGstSubmissionGate`)
- New Zealand GST (`INewZealandGstSubmissionGate`)
- Canada GST/HST (`ICanadaGstSubmissionGate`)
- India GST (`IIndiaGstSubmissionGate`)
- Vietnam VAT (`IVietnamVatSubmissionGate`)
- Brazil ICMS (`IBrazilIcmsSubmissionGate`)
- South Africa VAT (`ISouthAfricaVatSubmissionGate`)

Each gate encodes the current statutory rate, the prescribed invoice fields, the filing trigger conditions, and the currency of record.

### Rate accuracy

Rates are encoded as constants in the gate implementation. When a jurisdiction changes a rate (as India did with its GST slabs, as Vietnam did with its temporary 8% reduction, as as the UK did with the MTD threshold changes), the gate implementation is updated in the next substrate release.

Historical rate transactions are handled by passing a historical `utcNow` to the gate — the gate selects the rate that was in force on that date.

---

## EU VAT

EU VAT is handled separately from the non-EU consumption-tax axis.

The EU VAT gates validate B2B intra-community supplies, reverse-charge mechanisms, and the VAT information exchange (VIES) consistency checks. The EU VAT regime is distinct from single-country consumption taxes in that it operates under a single administrative framework with country-specific filing portals.

EU e-invoicing under EN 16931 (Peppol BIS Billing 3.0) is supported via the Peppol/UBL e-invoicing infrastructure in the substrate.

---

## UK MTD digital links

The UK Making Tax Digital regime introduces a specific **digital-link chain** requirement. The `IMtdDigitalLinksGate` validates that a declared chain of submission stages satisfies the digital-links rule:

- No manual re-typing between any step
- No copy-paste or spreadsheet transposition
- Each step connected by an approved digital link
- Submission window respected for the box period

This gate is structural — it validates the chain architecture, not the values themselves. Value validation is handled by the computation layer.

---

## E-invoicing: Peppol/UBL support

The substrate supports Peppol BIS Billing 3.0 (EN 16931) for cross-border e-invoicing. Peppol is not a VAT compliance check — it is a document format and transport standard. The VAT compliance gate runs **after** the Peppol document has been parsed and its fields placed into the gate dossier.

Supported profiles:
- Peppol BIS Billing 3.0 (EN 16931)
- Extended profile with tax breakdown
- Peppol府 and multipart messages

---

## Honest-fixture posture

The VAT compliance infrastructure takes a strict approach to real-world identifiers:

**Every candidate real-world identifier (e.g. a real company VAT number) is tested against the algorithm before being used as a fixture.** If the identifier fails the algorithm, it is dropped from the fixture set — the algorithm is not adjusted to accept it.

This means:

- The substrate ships with **algorithmic validators** (the check-digit and format rules) for every jurisdiction where those rules are publicly documented.
- **Synthetic fixtures** (made-up identifiers that pass the algorithm) are used in testing.
- **Real-world fixtures** are included only where a real identifier has been independently verified to pass the algorithm.
- No real-world identifier is named as a fixture unless it passes.

This posture prevents the substrate from accumulating incorrect validation logic to accommodate incorrect fixture data.

---

## Architectural notes for Vertical CORE producers

### Gates are additive

A new jurisdiction gate is added by creating a new interface + implementation in the `Services.Vat` namespace. No existing code needs to change. The new gate is immediately available for DI injection.

### Gate access is explicit

The Vertical CORE names the jurisdiction explicitly when requesting a gate. There is no "give me the right gate for this invoice" routing — the developer decides which jurisdiction the filing is for and requests that gate specifically.

### Compliance reports are attestable

Every gate returns a structured report, not a boolean. The report is the attestable evidence that the submission was checked. Storing the report satisfies the record-keeping obligations that most tax authorities impose.

### Threshold monitoring is the Vertical CORE's responsibility

Gate implementations do not monitor filing thresholds,voluntary registration triggers, or deregistration events. Those are business-logic concerns that belong to the Vertical CORE's own operations layer.

---

## Version

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | First publication. Describes Tier-4 VAT Compliance as implemented in the UniCORE substrate — 178 jurisdictions, interface-driven architecture, honest-fixture posture, UK MTD digital-links gate, and Peppol/UBL e-invoicing support. |

---

## Document history

- 2026-06-25 (24877ec) — docs: add VAT-COMPLIANCE.md — sister-mirror of unicore_public c16b942

*Back-filled from git log on 2026-07-10 21:34 UTC. Kind 2 versioning (dated change notes) — see HORIZON.md § Evolution and versioning. Kind 1 (formal `Version:` bumps) remains OFF until first GitHub Discussion.*
