UniSaaS.UniCORE is the public foundation for advanced AI, in its SaaS deployment shape.

We design the governance, write the code, and train the people who can do both. The foundation is gifted to humanity under permissive licences. The producers who maintain it earn their authority through a 30-year apprenticeship: not bought, not granted, earned.

The result is infrastructure no single company can monopolise, built and maintained by people from every background.

The future is coming. Advanced AI will shape the world ahead, whether we are ready or not. The question is who builds it, who controls it, and who benefits. UniCORE answers all three the same way: humanity does.

If you want to spend a career building advanced AI for humanity rather than for shareholders, UniCORE is the path.

A 30-year programme from apprentice to certified producer. A public foundation given away under permissive licences. No monopoly. The work belongs to everyone, including you.

---

*This is **UniSaaS.UniCORE**, the SaaS-deployment-shape sister to [UniCORE](https://github.com/bryanunitek/UniCORE). It is the same governed implementation reference, surfaced for the SaaS deployment topology — multi-tenant routing, signing-key separation, tenant-by-email resolution, hosted operation. Sister repositories: [UniVERSE](https://github.com/bryanunitek/UniVERSE) (the programme), [TrueAI](https://github.com/bryanunitek/TrueAI) (the immutable Foundation), [UniCORE-AI](https://github.com/bryanunitek/UniCORE-AI) (the 12-level reference architecture), [UniCORE](https://github.com/bryanunitek/UniCORE) (the on-prem-deployment-shape sister), [UniCORE.GVB](https://github.com/bryanunitek/UniCORE.GVB) (the on-prem-shape substrate-services layer), [UniSaaS.UniCORE.GVB](https://github.com/bryanunitek/UniSaaS.UniCORE.GVB) (the SaaS-shape substrate-services layer).*

*New to producing on the public gift surface? Start with [UniVERSE/GETTING_STARTED.md](https://github.com/bryanunitek/UniVERSE/blob/main/GETTING_STARTED.md).*

---

# UniSaaS.UniCORE

**The implementation reference for governed, human-sovereign artificial intelligence — SaaS deployment shape.**

Author: Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
First published: June 2026
Status: Public. Given, not sold. Irrevocable.

---

## What is UniSaaS.UniCORE?

UniSaaS.UniCORE is the **SaaS-deployment-shape sister** of [UniCORE](https://github.com/bryanunitek/UniCORE) — the same implementation reference layer of the programme, surfaced for the SaaS deployment topology rather than the on-premise topology.

The architectural position in the [Layered CORE model](https://github.com/bryanunitek/UniVERSE/blob/main/docs/00057-Layered-CORE-Model.md) is identical to UniCORE: **Level 2 ↔ Level 3** — between the universal architecture (UniCORE AI) and the Vertical CORE specific to a sector. UniSaaS.UniCORE is what a Vertical CORE inherits FROM when the Vertical Solution is deployed as a SaaS rather than on the customer's own infrastructure.

The deployment shape is the only thing that distinguishes UniSaaS.UniCORE from UniCORE. The governance is the same. The Foundation invariants are the same. The 12-Level reference architecture is the same. The certification gate is the same.

**Five-Solution naming.** The wider programme recognises five Solutions at the consumption tier: `UniCORE`, `UniCORE-UniVIEW`, `UniCORE-UniREPORT`, `UniSaaS-UniCORE-UniVIEW`, `UniSaaS-UniCORE-UniREPORT`. UniSaaS.UniCORE is the SaaS-shape parent of the last two of those five. UniVIEW (Enquiries, Reports, BI Dashboards) and UniREPORT (report-server-class) are framework-level products that ride on UniSaaS.UniCORE the way they ride on UniCORE in the on-prem shape — see [UniVIEW and UniREPORT](#uniview-and-unireport) below.

When a Vertical SaaS Solution is **certified Powered by UniCORE AI / built on the TrueAI Foundation**, the UniSaaS.UniCORE substrate it stands on is published here, on this repository, under CC BY 4.0. The Vertical CORE remains in its own repository (e.g. `bryanunitek/UniSaaS.UniCORE.Law-Claw` for the SaaS Law sector) and carries its industry-specific Business Objects there.

UniSaaS.UniCORE is the gift layer. The Vertical Business Objects are the commercial layer. Both can co-exist; the gift can never be enclosed.

---

## Why this repository exists today

This repository exists today as the **canonical public home** for UniSaaS.UniCORE — the place where its identity, licence, roadmap, and naming rules are recorded.

**The source code is not yet published here.** Source code is published when the first SaaS Vertical CORE that uses UniSaaS.UniCORE — `UniSaaS.UniCORE.Law-Claw` — is certified Powered by UniCORE AI / built on the TrueAI Foundation. See [ROADMAP.md](ROADMAP.md) for the trigger condition and what arrives at that point.

What is published here today:

- **The licence** — CC BY 4.0, irrevocable, the same terms as the rest of the programme. See [LICENSE.md](LICENSE.md).
- **The licensing reference with worked scenarios** — plain-English guidance for Partners, Clients, and Software Providers, with worked examples per industry. See [LICENSE_EXAMPLES.md](LICENSE_EXAMPLES.md).
- **The naming and claims rules** — what can and cannot be claimed about the UniSaaS.UniCORE name. See [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md).
- **The roadmap** — what arrives at certification and in what shape. See [ROADMAP.md](ROADMAP.md).
- **The AI authorship disclosure** — same disclosure form as the Foundation triad. See [AI-AUTHORSHIP.md](AI-AUTHORSHIP.md).
- **The agent rules** — how Claws working on this repository conduct themselves. See [AGENTS.md](AGENTS.md).

The repository will accumulate documentation between now and certification. Source code arrives at certification.

---

## The Layered CORE position

UniSaaS.UniCORE sits within the **Layered CORE model** ([`UniVERSE/docs/00057-Layered-CORE-Model.md`](https://github.com/bryanunitek/UniVERSE/blob/main/docs/00057-Layered-CORE-Model.md)) at the same level as UniCORE.

```
Level 1 CORE — TrueAI Foundation       (universal, immutable, gift)
                  ↑
Level 2 CORE — UniCORE AI              (universal architecture, gift)
                  ↑
Level 2 ↔ 3   — UniCORE / UniSaaS.UniCORE   (THIS REPO is the SaaS-shape sister — implementation reference, gift)
                  ↑
Level 3 CORE — Vertical CORE           (industry-specific reference, gift)
               (e.g. UniSaaS.UniCORE.Law, UniSaaS.UniCORE.Accounting,
                UniSaaS.UniCORE.Banking, UniSaaS.UniCORE.Healthcare,
                UniSaaS.UniCORE.Government, UniSaaS.UniCORE.Space-Industry)
                  ↑
Solutions tier — Working SaaS implementations (services-built, sellable)
```

The architectural layer is the same as UniCORE; the deployment shape is SaaS rather than on-prem. A derivative of CORE is itself CORE and is itself gifted — gift propagation applies identically across both deployment shapes.

---

## The deployment-shape distinction

UniCORE and UniSaaS.UniCORE are **sister implementation references** that differ in deployment shape, not in governance:

| | UniCORE | UniSaaS.UniCORE |
|---|---|---|
| **Deployment topology** | On the customer's own kit (their hardware, their data centre, their cloud account) | Hosted SaaS (multi-tenant on operator's infrastructure) **or** Private SaaS (multi-tenant on the customer's own kit) |
| **Tenancy** | Single-tenant — one deployment serves one organisation | Multi-tenant — one deployment serves many organisations |
| **Tenant resolution** | Out-of-scope — one tenant per deployment | In-scope — tenant-by-domain, tenant-by-email, signing-key separation |
| **Signing keys** | One key set per deployment | Per-tenant key separation; cross-tenant attack-surface guards |
| **Operational model** | Customer holds operational responsibility | **Hosted SaaS:** SaaS operator (e.g. Unitek Systems USA Inc) holds operational responsibility. **Private SaaS:** Customer holds operational responsibility (a global entity runs the SaaS stack on their own kit). |
| **Governance** | Same | Same |
| **Foundation invariants** | Same | Same |
| **12-Level reference architecture** | Same | Same |
| **Certification gate** | Same | Same |
| **CC BY 4.0 licence** | Same | Same |
| **Industry-classified pattern** | `UniCORE.<Industry>` | `UniSaaS.UniCORE.<Industry>` |

The substrate-services layer (UniCORE.GVB / UniSaaS.UniCORE.GVB) carries the same deployment-shape distinction — the Linux/Windows substrates of UniCORE.GVB serve on-prem; UniSaaS.UniCORE.GVB serves the SaaS topology. See [UniSaaS.UniCORE.GVB](https://github.com/bryanunitek/UniSaaS.UniCORE.GVB).

Vertical Solutions inherit from UniCORE when they are deployed on-prem and from UniSaaS.UniCORE when they are deployed as a SaaS. The Vertical CORE Business Objects on top can be the same; the substrate underneath them differs only by deployment shape.

---

## Three SaaS operator positions

Under SaaS-shape deployment, UniSaaS.UniCORE may be operated in one of three positions, all under the same CC BY 4.0 licence:

1. **Hosted SaaS** — operated by a SaaS operator (e.g. **Unitek Systems USA Inc** as PROD-tier operator from Phase II onward) on the operator's infrastructure, serving many tenants. **Operator holds operational responsibility.**
2. **Private SaaS** — a global entity (typically a customer at scale) runs the SaaS stack on **their own hardware, their own data centre, their own cloud account**. **The customer holds operational responsibility.** The same code runs; the operator shape changes. Useful when the entity is large enough to not want shared hosting but still wants the SaaS deployment shape.
3. **Self-hosted** — any third party stands up the SaaS stack on infrastructure of their choosing under CC BY 4.0.

The gift surface is uniform across all three positions. There is no privileged operator tier.

---

## The certification trigger

The trigger that moves UniSaaS.UniCORE from this repository's documentation-only state to documentation-plus-code state is:

> The first SaaS Vertical CORE built on UniSaaS.UniCORE — `UniSaaS.UniCORE.Law-Claw` — is certified **Powered by UniCORE AI / built on the TrueAI Foundation**.

When that certification is recorded, the UniSaaS.UniCORE substrate inside `UniSaaS.UniCORE.Law-Claw` is extracted and published here under CC BY 4.0. The Law SaaS Business Objects remain in `UniSaaS.UniCORE.Law-Claw` as the commercial Vertical SaaS CORE layer.

The same gift principle then applies to every future SaaS Vertical CORE: when a SaaS Vertical CORE is certified, its UniSaaS.UniCORE-conformant substrate is already published here for everyone, and the vertical's industry-specific SaaS Business Objects sit in the vertical's own repository.

The certification is the gate. The gate exists because the gift must mean something; the badge cannot be self-applied. The gate is identical to UniCORE's — the Foundation invariants do not change shape between deployment topologies.

---

## UniVIEW and UniREPORT

The wider programme recognises **five Solutions at the consumption tier** under the 2026-04-24 lock: `UniCORE`, `UniCORE-UniVIEW`, `UniCORE-UniREPORT`, `UniSaaS-UniCORE-UniVIEW`, `UniSaaS-UniCORE-UniREPORT`. The two SaaS-shape Solutions of those five — `UniSaaS.UniCORE.UniVIEW` and `UniSaaS.UniCORE.UniREPORT` — are framework-level products that ride on UniSaaS.UniCORE.

- **UniVIEW** — Enquiries, Reports, BI Dashboards. The consumption surface for governed read-models; gift layer; same 12-Level governance posture as UniSaaS.UniCORE.
- **UniREPORT** — Report-server-class infrastructure (SSRS / DevExpress Report Server-class). The consumption surface for paginated reports; gift layer; same 12-Level governance posture.

Both are framework-level: they sit at the consumption tier as peers to UniSaaS.UniCORE itself, not inside any particular Vertical CORE. A Vertical CORE may carry per-vertical specialisations of UniVIEW and UniREPORT (e.g. `UniSaaS.UniCORE.Law.UniVIEW` and `UniSaaS.UniCORE.Law.UniREPORT` as project families inside the SaaS Law solution), but the framework-level UniVIEW and UniREPORT live above all Vertical COREs.

**Today, pre-certification:** UniVIEW and UniREPORT are documented inside this UniSaaS.UniCORE repository (here) and inside the on-prem-shape parent UniCORE repository, with cross-references in both. No source code is published yet — the same posture as UniSaaS.UniCORE itself.

**At certification:** UniVIEW and UniREPORT each get their own public gift-surface repository, peer to UniSaaS.UniCORE: `bryanunitek/UniSaaS.UniCORE.UniVIEW` and `bryanunitek/UniSaaS.UniCORE.UniREPORT`. Each carries the same 11-file gift-surface shape as UniSaaS.UniCORE today. Cross-references from UniSaaS.UniCORE point to them at that point. The on-prem-shape parents `bryanunitek/UniCORE.UniVIEW` and `bryanunitek/UniCORE.UniREPORT` follow the same pattern at certification of the on-prem Vertical CORE.

The pattern mirrors how [UniCORE.Desktop](https://github.com/bryanunitek/UniCORE/blob/main/README.md#unicoredesktop--client-applications) is handled: documented in parent gift-surface repositories pre-certification, split out to its own repository at certification.

---

## NVarchar Data Mode — Open, Scrambled, Encrypted

All NVARCHAR (string) data across the UniSaaS.UniCORE substrate is governed by a three-mode architecture:

| Mode | Default | Description |
|---|---|---|
| **Scrambled** | ✅ Yes | Reversibly scrambled storage. Prevents casual database inspection. The owning system’s scramble key is required to read. |
| **Open** | | Plain text. Used where scrambling is operationally inappropriate (e.g. full-text search indexes). |
| **Encrypted** | | Field-level encryption. Future feature (reserved). The customer holds the decryption key (sovereignty principle). |

**Default posture: Scrambled.** All string fields arrive Scrambled unless explicitly resolved otherwise by a policy chain. The resolution cascade is: Workload → Tenant → Product → Default (Scrambled).

This is a substrate-level concern inherited from [UniCORE.GVB](https://github.com/bryanunitek/UniCORE.GVB). Both the on-prem UniCORE and the SaaS UniSaaS.UniCORE deployments enforce the same posture. The deployment shape does not change the data-mode architecture.

---

## 10-Level Mass Data Generation

The SaaS deployment shape includes a **10-level bootstrap seeder** that provisions the foundational user and role hierarchy per UniVERSE Foundation Document 45/54:

| Level | Code | Name | AI Mode |
|---|---|---|---|
| 1 | 0001 | UniCORE-Global | GlobalAIMode |
| 2 | 0002 | UniCORE-GlobalVirtualBridge | GlobalVirtualBridgeAIMode |
| 3 | 0003 | UniCORE-Continental | ContinentalAIMode |
| 4 | 0004 | UniCORE-Regional | RegionalAIMode |
| 5 | 0005 | UniCORE-State | StateAIMode |
| 6 | 0006 | UniCORE-DataCentre | DataCentreAIMode |
| 7 | 0007 | UniCORE-Platform | PlatformAIMode |
| 8 | 0008 | UniCORE-Product | ProductAIMode |
| 9 | 0009 | UniCORE-Deployment | DeploymentAIMode |
| 10 | 0010 | UniCORE-Tenant | TenantAIMode |

Each level seeds one bootstrap user and one paired role. The seeder is idempotent. Default NVarchar posture for all seeded data: **Scrambled**.

Levels 11 (RoleAIMode) and 12 (UserAIMode) remain in the per-tenant operational database — they are not bootstrap-level.

---

## Intelligent Integration Controller

The Intelligent Integration Controller (IIC) is the integration and data-movement subsystem of UniSaaS.UniCORE. It provides secure messaging, secure file transfer manifests, and governed data exchange between systems — the integration spine that a Vertical CORE uses to connect to external systems (practice management, document management, billing, etc.) without exposing raw data paths.

The IIC is built as a standalone service layer within the Vertical CORE working repository. At certification, the IIC interfaces and contracts become part of the UniSaaS.UniCORE gift surface (CC BY 4.0).

**Integration / Import from 3rd-party systems:**

The IIC includes a connector architecture for importing data from established practice-management and billing systems. The first production connector is **Aderant Expert** — a legacy system used by global law firms. The connector provides:
- `AderantIntegrationTransactionAdapter` — transaction-level data import
- `AderantRunProjectionService` — run-projection and workload planning
- `AderantWorkloadHandler` — workload execution for governed import pipelines

The connector pattern is repeatable: future connectors for other systems (Elite, Aderant iManage, 3E, etc.) follow the same interface shape.

The working code lives in `bryanunitek/UniSaaS.UniCORE.Law-Claw` (the first SaaS Vertical CORE), structured as:
- `UniCORE.Law.IntelligentIntegrationController.Abstractions` — contracts and DTOs
- `UniCORE.Law.IntelligentIntegrationController.Core` — interfaces, services, resolver
- `UniCORE.Law.IntelligentIntegrationController.Persistence` — store implementations
- `UniCORE.Law.IntelligentIntegrationController.Service` — the hosted service entry point
- `UniCORE.Law.IntelligentIntegrationController.Connectors.Aderant` — Aderant Expert connector

---

## Platforms and UI Surfaces

UniSaaS.UniCORE runs on **Windows, Linux, macOS, iOS, and Android**.

Three primary UI surfaces deliver the full platform reach:

| Surface | Technology | Platforms | Role |
|---|---|---|---|
| **DevExpress Blazor Server** | .NET 10 + XAF + XPO | Windows, Linux, macOS (via browser) | Primary web UI — the main operational surface |
| **.NET MAUI** | .NET 10 | Windows, macOS, iOS, Android | Native mobile + desktop |
| **Avalonia** | .NET 10 | Windows, Linux, macOS | Cross-platform native desktop |

Additional optional surface:

| Surface | Technology | Platforms | Role |
|---|---|---|---|
| **WinForms (*.Win)** | .NET 10 + DevExpress | Windows only | Optional power-user desktop surface (ships alongside Blazor) |

The Blazor Server surface is the governance-primary UI — all administrative, operational, and Vertical CORE business-object workflows are available through it. MAUI and Avalonia extend reach to native mobile and native Linux desktop respectively. WinForms remains as an optional Windows-only surface for power users who prefer a native Windows experience alongside Blazor.

All four surfaces share the same substrate-services layer (UniSaaS.UniCORE.GVB), the same 12-Level Governance Model, and the same Foundation invariants. The UI surface is a delivery choice; governance is invariant across all of them. The deployment shape (SaaS vs on-prem) does not change the available surfaces — UniSaaS.UniCORE offers the same platform reach as UniCORE.

---

## UniCORE Positioning Principle

The programme is positioned as **Harmony, Peace, Space Exploration, for Humanity**.

Industries and uses that align with this positioning are welcome. Those that do not are not. **Military uses are intentionally absent** from the programme and will not be added. The deployment shape (on-prem versus SaaS) does not change this rule — `UniSaaS.UniCORE.Military` is no more permissible than `UniCORE.Military`.

**The "Powered by UniCORE AI" and "built on TrueAI Foundation" certifications must not appear on any military use.** The badge is part of the gift, and the gift is meant for Harmony, Peace, Space Exploration, for Humanity — using the badge to brand weapons-class systems would invert the gift principle. The positioning closes that route.

This is a structural choice, not a marketing choice. The programme exists to keep critical decision systems available to humanity as gift.

---

## Related repositories

**The Foundation triad:**
- [`UniVERSE`](https://github.com/bryanunitek/UniVERSE) — The civilisational-scale programme.
- [`TrueAI`](https://github.com/bryanunitek/TrueAI) — The immutable Foundation. Nine Invariants.
- [`UniCORE-AI`](https://github.com/bryanunitek/UniCORE-AI) — The 12-Level reference architecture.

**The implementation references (sister repos by deployment shape):**
- [`UniCORE`](https://github.com/bryanunitek/UniCORE) — The on-prem-deployment-shape sister of this repository. Same architectural layer; different deployment topology.

**The substrate-services layer:**
- [`UniCORE.GVB`](https://github.com/bryanunitek/UniCORE.GVB) — The on-prem-shape substrate-services layer.
- [`UniSaaS.UniCORE.GVB`](https://github.com/bryanunitek/UniSaaS.UniCORE.GVB) — The SaaS-shape substrate-services layer. Sister to this repository at the substrate-services tier.

**The SaaS Vertical CORE family (working repositories — private until certification):**
- `bryanunitek/UniSaaS.UniCORE.Law-Claw` — First SaaS Vertical CORE, Law sector. Working repository. Certification pending.
- Future: `UniSaaS.UniCORE.Accounting-Claw`, `UniSaaS.UniCORE.Banking-Claw`, `UniSaaS.UniCORE.Healthcare-Claw`, etc., as additional SaaS verticals are produced. The industry list is open and is defined as the programme expands. Military is intentionally absent.



**Forked-upstream building-block families (scaffold-anchor as of 2026-06-04 — full scaffolding and upstream fork pending dedicated kickoff arcs):**
- [`UniCORE.Avalonia`](https://github.com/bryanunitek/UniCORE.Avalonia) — Cross-platform .NET UI substrate. Fork of MIT Avalonia + UniCORE CC BY 4.0 additions (Pro-equivalent controls + Avalonia XPF).
- [`UniSaaS.UniCORE.Avalonia`](https://github.com/bryanunitek/UniSaaS.UniCORE.Avalonia) — SaaS-deployment-shape sister of UniCORE.Avalonia.
- `bryanunitek/UniCORE.Avalonia-Claw` (private) — on-prem-shape working repository for UniCORE.Avalonia.
- `bryanunitek/UniSaaS.UniCORE.Avalonia-Claw` (private) — SaaS-shape working repository.
- [`UniCORE.DNN`](https://github.com/bryanunitek/UniCORE.DNN) — Web CMS / portal building block. Fork of MIT Dnn.Platform + UniCORE CC BY 4.0 modules.
- [`UniSaaS.UniCORE.DNN`](https://github.com/bryanunitek/UniSaaS.UniCORE.DNN) — SaaS-deployment-shape sister of UniCORE.DNN.
- `bryanunitek/UniCORE.DNN-Claw` (private) — on-prem-shape working repository for UniCORE.DNN.
- `bryanunitek/UniSaaS.UniCORE.DNN-Claw` (private) — SaaS-shape working repository.

---

## Attribution

> Powered by UniCORE AI.
> Built on the TrueAI Foundation.

Attribution required wherever UniSaaS.UniCORE, UniCORE, UniCORE AI, the TrueAI Foundation, or the 12-Level Governance Model is referenced, implemented, or extended.

---

## Licence

Given, not sold. The architecture is public, open, and free. The TrueAI Foundation cannot be modified, forked, commercialised, patented, or proprietarily captured. See [LICENSE.md](LICENSE.md) for full terms; see the canonical [`UniVERSE/IRREVOCABLE-LICENCE-DECLARATION.md`](https://github.com/bryanunitek/UniVERSE/blob/main/IRREVOCABLE-LICENCE-DECLARATION.md) for the formal irrevocability declaration that covers the whole programme.

— Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom, June 2026.

---

## AI authorship

This repository is produced with AI assistance operating under TrueAI governance. The full disclosure is at [AI-AUTHORSHIP.md](AI-AUTHORSHIP.md).

---

## Discuss and contribute

Programme-level debate, adoption questions, translation, and corrections belong in [GitHub Discussions](https://github.com/bryanunitek/UniSaaS.UniCORE/discussions). What is in scope: questions about UniSaaS.UniCORE's role as the SaaS-deployment-shape sister, the certification gate, the relationship to UniCORE and to Vertical SaaS COREs, the gift principle as it applies to substrate code in a SaaS topology. What is out of scope: implementation specifics that belong inside a particular Vertical SaaS CORE's own repository.

For Foundation-level debate, use [UniVERSE Discussions](https://github.com/bryanunitek/UniVERSE/discussions), [TrueAI Discussions](https://github.com/bryanunitek/TrueAI/discussions), or [UniCORE-AI Discussions](https://github.com/bryanunitek/UniCORE-AI/discussions) as appropriate.

---

## Classification, brand, and claims

UniSaaS.UniCORE is the SaaS-deployment-shape implementation reference for governed AI. It is not a product, platform, brand for sale, or hosted service offering — it is the substrate that hosted SaaS services may be built on top of, gifted under CC BY 4.0. See [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md) for binding rules on how the UniSaaS.UniCORE name may and may not be used.

---

## Contact

- **Public discussion:** [GitHub Discussions](https://github.com/bryanunitek/UniSaaS.UniCORE/discussions) (see [DISCUSSIONS.md](DISCUSSIONS.md))
- **Private contact / connection request:** [LinkedIn](https://www.linkedin.com/in/bryan-fred-02209753/)
