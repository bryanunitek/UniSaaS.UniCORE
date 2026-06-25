# Localisation

**What this document covers:** the UniCORE cross-vertical localisation infrastructure — the governance, architectural layers, and integration surface that any Vertical CORE built on UniCORE inherits.

**What this document does not cover:** Vertical CORE-specific localisation business logic, jurisdiction-specific display conventions, or per-tenant localisation policy configuration. Those live with the Vertical CORE.

---

## Status

This document describes the **Tier-1 Localisation** infrastructure as implemented in the UniCORE substrate. The implementation is complete and published as part of the cross-vertical substrate layer.

Vertical Cores built on UniCORE inherit this infrastructure by default. Hosts and Vertical CORE producers can override every axis.

---

## The five-axis localisation model

UniCORE localises consequential outputs (bills, reports, regulatory filings, audit trails) across five independent axes. Each axis is governed by its own policy chain and resolved at render time, not at data-entry time. Internal storage is always canonical (UTC timestamps, ISO 4217 currency codes, BCP 47 language tags).

| Axis | Internal form | Display form | Example |
|---|---|---|---|
| Language | BCP 47 tag (`en-GB`) | Translated output | DeepL-rendered bill in French |
| Currency | ISO 4217 alpha-3 (`GBP`) | Local symbol + format | `£1,234.56` |
| Date / time | UTC | Locale-formatted | `25/06/2026` vs `06/25/2026` |
| Translated badge | Boolean | Localised badge text | "Propulsé par UniCORE AI · Fondé sur TrueAI" |
| DeepL policy | Enum | Per-deployment policy | `HardDeny`, `AskUser`, `Allow` |

All five axes compose into a `LocalisedBillPresentationEnvelope` that wraps every render call. The envelope carries the resolved policy for each axis so the renderer receives everything it needs in a single structure.

---

## Language axis

### Catalogue

54 languages are supported in the substrate seed data. The catalogue is the `UniCoreLanguage` business object, stored with ISO 639-1 alpha-2 as primary code, ISO 639-2/3 alpha-3 as secondary, and BCP 47 as the operational tag.

Language selection follows a three-level override chain:

1. **User-level override** — per-user language preference (highest priority).
2. **Tenant-level override** — per-organisation language policy.
3. **Deployment default** — host-configured default, used when neither user nor tenant is set.

### Translation chain

Translation is provided via a `ILocalisationTranslator` port. The default production implementation calls the DeepL API. The chain:

```
Render request → LocalisedBillPresentationEnvelope
  → ITranslatedBadgeResolver (badge text, DeepL-rendered)
    → ILocalisationTranslator.Denormalise(sourceText, targetLanguage)
      → DeepL HTTP API (or mock in dev/test)
```

A `DenyByDefaultLocalisationTranslator` is also provided — returns the source text unchanged, for deployments where external API calls are not permitted.

### Policy: when does DeepL fire?

The `EffectiveDeepLPolicy` on the presentation envelope is resolved from the `Deployment` → `Tenant` → `User` override chain. The three policy values:

- **`HardDeny`** — no DeepL call. Source text returned. Badge text rendered from local fallback strings.
- **`AskUser`** — prompt the user before sending text to DeepL. Supports consent workflows.
- **`Allow`** — DeepL fires normally. Default in production SaaS deployments.

---

## Currency axis

### Storage vs display

Currency amounts are stored as integers in the smallest unit (pence, cents, centsimes) alongside an ISO 4217 alpha-3 currency code. The substrate never stores floating-point amounts.

Display formatting is a render-time concern, resolved from the `LocalisedBillPresentationEnvelope`:

```
Money(4250, "GBP") → LocaleCurrencyFormatter.Format(amount, "GBP", locale)
  → "£42.50"  (en-GB locale)
  → "42,50 £" (fr-FR locale)
```

### Zeroamount and absent balances

`ZeroAmount` is represented as `0` in the smallest unit — not `null`, not a separate flag. The renderer formats `0` as `£0.00` or its locale equivalent. Absent or not-yet-set balances are represented as `null` and render as a dash or blank, never as `£0.00`.

---

## Date / time axis

### Storage: always UTC

All dates and times in the substrate are stored as UTC `DateTimeOffset`. No local-time storage anywhere in the data model. This is non-negotiable — cross-border billing, matter management, and regulatory filing all require a consistent anchor.

### Display: locale-formatted at render time

The `LocalisedBillPresentationEnvelope` carries the display locale. The renderer calls:

```
DateTimeOffset.UtcNow → LocaleDateFormatter.Format(utc, displayLocale)
  → "25/06/2026"  (en-GB)
  → "06/25/2026"  (en-US)
  → "2026/06/25"  (ja-JP)
```

### Time zones vs display

Time zone conversion is the host's responsibility at the presentation layer. The substrate provides UTC; the host applies the display time zone. This prevents the substrate from accumulating time zone state.

---

## Badge axis

### The badge claim

Every UniCORE-powered output carries the attribution badge:

> Powered by UniCORE AI · Built on the TrueAI Foundation

### Translated badge

The badge text is translated through the same DeepL chain as bill content. The `ITranslatedBadgeResolver` returns the badge in the display language, governed by the `ShowTranslatedBadge` axis of the presentation envelope.

When `ShowTranslatedBadge = false`, the badge renders in English regardless of display language. When `true`, it renders in the display language via DeepL.

### DI wiring

The badge services are wired via `AddLawBadgeAndAttribution()` and `AddLawBadgeConformanceCheck()`. A host can replace either service with a custom implementation before calling these methods, using standard Microsoft.Extensions.DependencyInjection removal-and-replacement patterns.

---

## Architectural notes for Vertical CORE producers

### The substrate handles the cross-vertical layer

The five-axis localisation model is **cross-vertical infrastructure**. Vertical CORE producers building on UniCORE do not need to implement language detection, currency formatting, or UTC storage discipline — it is provided. What the Vertical CORE owns is the **business-object layer** that supplies the raw data into the envelope.

### Override points

Every axis has a defined override point. The override chain (User → Tenant → Deployment → Hardcoded default) means that in a multi-tenant SaaS deployment, each tenant can have a different display locale without affecting any other tenant.

### Testing

The localisation infrastructure is tested at three levels:

1. **Unit tests** — each resolver, formatter, and translator in isolation.
2. **DI wire-in tests** — `AddLawBadgeAndAttribution()` and `AddLawBadgeConformanceCheck()` register the correct services.
3. **Integration tests** — full render cycle with a `LocalisedBillPresentationEnvelope` carrying all five axes.

### Relationship to EU AI Act obligations

Translated outputs do not alter the AI system's obligations under the EU AI Act. The translation is a **faithful rendering** of the underlying canonical text — the authoritative record remains the source-language version. Transparency about the use of AI-generated translation (Article 13) is addressed at the system level, not at the translation axis.

---

## Version

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | First publication. Describes Tier-1 Localisation as implemented in the UniCORE substrate. |
