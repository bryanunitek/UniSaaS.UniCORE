---
title: "License Examples — Formal Statement and Worked Scenarios"
author: Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
licence: CC BY 4.0
---

# License Examples — Formal Statement and Worked Scenarios

**Author:** Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
**First published:** May 2026
**Living document.** Corrections and clarifications welcome via [GitHub Discussions](https://github.com/bryanunitek/UniCORE/discussions)
**Licence of this document:** Creative Commons Attribution 4.0 International (CC BY 4.0)

> This document is plain-English guidance for Partners, Clients, and Software Providers. Where this document and the canonical [LICENSE.md](LICENSE.md) disagree, the canonical licence text wins.

---

## Purpose

This document is a formal reference you can give to a **Partner, Client, or Software Provider** who asks how the licensing model works across the public CORE corpus.

It explains the licensing of the public CORE corpus, walks through each layer of the architecture, and then gives **worked scenarios** for the most common situations you will be asked about:

- Enterprise software companies serving named industries (Law, Banking, Healthcare, Government, Space Industry)
- Small, Medium, and Large software companies that want **fewer than the standard 12 Levels of Governance** (floor = 4)
- A service company like **Unitek Systems Limited / Unitek Systems USA Inc**
- A hosting company like **Unitek Systems USA Inc**
- A law firm using UniCORE.Law for its own internal practice
- A law firm building its own Law layer from the generic UniCORE implementation reference
- Organisations that require **more than 12 Levels of Governance** (13+)
- Organisations that need **fewer than 4 Levels of Governance** (<4)
- A vendor that forks the CORE and builds proprietary AI on top
- How the licensing structure prevents monopoly capture
- UniCORE.GVB and UniCORE.Desktop — substrate-layer gift, chain-locked, cannot be monopolised, forked, or sold
- Each named industry: Law, Banking, Healthcare, Government, Space Industry

Where this document and the canonical license text disagree, the canonical licence text wins.

---

## 1. The architecture in one diagram

```
Solutions tier — Working implementations (services-built, sellable)
                                  ↓ built on
Level 3 CORE — Vertical CORE (industry-specific reference, gift)
                                  ↓ specialises
   (UniCORE.Law, UniCORE.Accounting, UniCORE.Banking,
    UniCORE.Healthcare, UniCORE.Government, UniCORE.Space-Industry)
                                  ↑
Level 2 ↔ 3 — UniCORE (implementation reference, gift)
                                  ↑
Level 2 CORE — UniCORE AI (universal architecture, gift)
                                  ↑
Level 1 CORE — TrueAI Foundation (universal, immutable, gift)
```

The arrows are **dependency** arrows: the layer above is built on the layer below.

---

## 2. The licensing model in plain English

The CORE corpus is **published as a gift**, under the **Creative Commons Attribution 4.0 International Licence (CC BY 4.0)**.

| You can | You must | You cannot |
|---|---|---|
| Use it commercially | Attribute the author | Sue the author over it |
| Modify it | Keep the licence notice | Imply we endorse your derivative |
| Redistribute it | Indicate what you changed | Add legal or technical restrictions |
| Build a commercial product on top of it | Make the licence link visible | Strip the licence and claim authorship |

The licence is **irrevocable**. Once given, the gift cannot be withdrawn.

The licence is **per-repository**, not per-organisation. Anyone — including a competitor — can use it under the same terms as anyone else, including Unitek Systems Limited and Unitek Systems USA Inc.

### What is "the gift layer"

| Layer | Repository | Licence | Status |
|---|---|---|---|
| Level 1 CORE — TrueAI Foundation | `bryanunitek/TrueAI` | CC BY 4.0 | Public, gift |
| Level 2 CORE — UniCORE AI | `bryanunitek/UniCORE-AI` | CC BY 4.0 | Public, gift |
| Programme umbrella | `bryanunitek/UniVERSE` | CC BY 4.0 | Public, gift |
| Level 2 ↔ 3 — Implementation reference | `bryanunitek/UniCORE` | CC BY 4.0 | Public, gift |
| Substrate services layer | `bryanunitek/UniCORE.GVB` | CC BY 4.0 | Public, gift |
| Level 3 CORE — Vertical CORE | `bryanunitek/UniCORE.Law`, etc. | CC BY 4.0 **upon certification** | Future public, gift |

### What is **not** in the gift layer

The **Solutions tier** — the working, deployed implementations that Unitek and other companies build and sell — is **not** part of the public gift corpus. Those are commercial products.

For Unitek specifically, the commercial line is:

- **The Service** (Unitek-hosted, supported, customised deployments of CORE + Vertical CORE)
- **The Vertical CORE Business Objects** that live inside `UniCORE.Law-Claw`, `UniCORE.GVB-Claw`, etc. (the private working repositories — distinct from the public CORE reference)
- **Professional services, integration, conversion, training**

The same separation applies to any other organisation: the public CORE is gift, what you build on top is yours.

---

## 3. What CC BY 4.0 actually requires

If you take any part of the public CORE corpus and use it — internally, in a product you sell, in a fork, in a paper, in a presentation — you must:

1. **Attribute the author.** The canonical attribution line is:

   > *"Based on [Repository Name], by Bryan Fred, Unitek Systems Limited (CC BY 4.0). https://github.com/bryanunitek/[RepositoryName]"*

   The attribution applies per-repository. If you use multiple public CORE repositories, add a line for each.

2. **Provide the licence notice.** Keep the LICENSE file. Link to it. Do not strip it.

3. **Indicate changes.** If you modified anything, say so clearly. A NOTICE.md or a "Changes from upstream" section is standard.

4. **Not imply endorsement.** Do not say or imply that Bryan Fred, Unitek Systems Limited, or any author of the public CORE endorses, supports, or is responsible for your derivative.

5. **Not impose further restrictions.** You cannot take the public CORE, add DRM or extra legal terms on top, and pass that restricted version to downstream users. Your additions to your own code can carry any licence you like; the underlying CORE portions must remain available under CC BY 4.0.

---

## 4. The 12 Levels of Governance — and the floor / ceiling

UniCORE AI defines a reference governance framework of **12 Levels** — a stack of governance concerns running from the lowest substrate (raw operational data) up to the highest authority (Board / Regulator / Public).

The 12-level model is a **reference**, not a hard constraint of the licence.

| Tier | Practical position |
|---|---|
| **<4 Levels** | Below the recommended minimum. Permitted by the licence, but not certifiable. |
| **4 Levels (floor)** | The minimum we recommend for any serious deployment. |
| **4 to 12 Levels** | Standard band. Most commercial deployments live here. |
| **12 Levels (full reference)** | The complete UniCORE AI reference framework. |
| **13+ Levels (ceiling-extended)** | Permitted. Sometimes required (heavily regulated, multi-jurisdiction, life-safety). |

The licence permits you to take the reference, drop levels you do not need, or add levels you do need.

What the licence does **not** permit:

- Calling your reduced-level deployment "12-Level UniCORE Governance" when it isn't
- Using the **Powered by UniCORE AI** certification mark without certification
- Claiming a Vertical CORE implementation is **certified** when it has not been

---

## 5. Worked scenarios

---

### Scenario 5.1 — Enterprise software company in a named industry

**Profile:** A multi-product enterprise software vendor — examples: a legal-tech vendor serving law firms; a core-banking platform vendor serving banks; an EHR / EMR vendor serving healthcare organisations; a government digital-services vendor; a mission-systems vendor serving space-industry operators. Revenue measured in tens or hundreds of millions. Long sales cycles. Regulated customers.

**What they take from the gift layer:**

- TrueAI Foundation — the Nine Invariants and the universal substrate
- UniCORE AI — the 12-Level Governance architecture
- UniCORE — the implementation reference
- The matching **Vertical CORE** (UniCORE.Law / UniCORE.Banking / UniCORE.Healthcare / UniCORE.Government / UniCORE.Space-Industry) once certified

**What they build on top:**

- Their existing product line, re-architected (in part or in full) onto the Vertical CORE pattern
- Industry-specific business objects, integrations, and workflows that are their own IP
- The commercial Solutions-tier product they sell to their customers

**What the licence requires of them:**

- Carry the attribution line for each public CORE repository they used, in their product's "About" or licence panel and in any technical documentation that describes the architecture.
- Keep their fork of any UniCORE-licensed code under CC BY 4.0 if they redistribute it.
- Indicate, in their changelog or NOTICE, what they have modified.
- Not claim "**Powered by UniCORE AI**" or "**TrueAI-certified**" unless they have gone through the certification process for that named release.

**What they cannot do:**

- Re-licence UniCORE-derived portions under a more restrictive licence.
- Strip out the CC BY 4.0 LICENSE file from their distribution.
- Use a reserved marketing phrase (`UniCORE-certified`, `UniCORE-AI-certified`, `TrueAI-certified`, `Powered by UniCORE AI`, etc.) without certification.
- Use a reserved naming prefix (`UniCORE.Military`, `UniCORE.GVB.Military`, etc. — Military is reserved out of the gift surface).

**Worked example — An enterprise legal-tech vendor:**

A £200M legal-tech vendor with a matter-management platform and billing module takes UniCORE-AI and UniCORE.Law (after certification). They re-architect their billing module so its workflow engine, audit trail, and approval gates conform to the UniCORE pattern. They keep their own conflict-search engine as their commercial differentiator but plug it into the Vertical CORE conflict-clearance contracts.

They ship their platform v8 with a NOTICE.md attributing UniCORE-AI and UniCORE.Law, a LICENSE-3RD-PARTY.md including the CC BY 4.0 text for the UniCORE-derived portions, and a "Built on the UniCORE.Law pattern" line in their product documentation.

None of that revenue is owed to anyone for the public CORE portions — by design, the gift is free for commercial reuse.

If they later want the "**Powered by UniCORE AI**" badge or the "**UniCORE.Law-certified**" badge, they go through the published certification process. Until then, they describe themselves as **building on** the pattern, not as **certified to** it.

---

### Scenario 5.2 — Small, Medium, and Large software companies using fewer than 12 Levels (floor = 4)

**Profile:** A software vendor that does not need the full 12-Level Governance stack — common when the customer base is small-business or mid-market, the regulatory load is light, or the product is point-functional.

#### 5.2a — Small software company (10–50 people, single product, <£10M revenue)

A 20-person SaaS startup building a contract-redlining tool for in-house counsel.

- **Levels used:** 4 (the floor). Authentication, audit, approval, retention.
- **Levels skipped:** Multi-jurisdiction routing, Board-level governance, regulator-facing escalation, etc.
- **Licensing posture:** Permitted. They cite UniCORE AI as the reference framework their 4 levels derive from. They do **not** claim 12-level compliance. They do **not** claim "Powered by UniCORE AI" without certification.

**Attribution line in their product docs:**

> *"This product implements 4 levels of the UniCORE AI Governance Framework (authentication, audit, approval, retention). Based on UniCORE AI by Bryan Fred, Unitek Systems Limited, CC BY 4.0."*

That sentence is honest, sufficient, and licence-compliant.

#### 5.2b — Medium software company (50–500 people, multi-product, £10M–£100M revenue)

A 300-person vertical-SaaS company in the accountancy space.

- **Levels used:** 7 of 12. Includes everything in the floor plus regulator filing audit, multi-entity consolidation, cross-jurisdiction VAT/tax, partner-level approval.
- **Levels skipped:** Board-level governance, Public-facing escalation, life-safety levels (not relevant in accountancy).
- **Licensing posture:** Same shape as 5.2a but with more levels enumerated. Honest scope claim.

#### 5.2c — Large software company (500+ people, multi-product, >£100M revenue)

A 2,000-person enterprise platform vendor selling to mid-market customers.

- **Levels used:** 10 of 12.
- **Licensing posture:** Same shape — list what they implement, list what they don't, attribute correctly, and claim only what they have certified.

**The principle across all three sub-profiles:**

You can stop at any level >= 4. You name the levels you implement. You do **not** misrepresent the scope. The licence does not require you to implement all 12 to use any of them.

---

### Scenario 5.3 — Service company (Unitek Systems Limited / Unitek Systems USA Inc)

**Profile:** A consultancy or service house that takes the public CORE corpus, configures and integrates it for specific clients, runs the deployments, and bills for the service. Unitek itself is the canonical example.

**What they take from the gift layer:**

- The complete public CORE corpus (TrueAI, UniCORE AI, UniCORE, UniCORE.GVB, and any certified Vertical COREs)

**What they build on top:**

- Configured deployments per client (the Solutions tier)
- Their own Vertical Business Objects in private working repositories (`UniCORE.Law-Claw`, `UniCORE.GVB-Claw`, etc. — the commercial differentiator)
- Conversions, integrations, importers, customer-specific workflow
- Professional services, training, support, SLAs

**What the licence requires of them:**

- Attribute each public CORE repository they incorporated into a delivered Solution.
- Keep modifications to public CORE portions under CC BY 4.0 if they are redistributed (e.g., to the client as part of a deliverable).
- Make the licence text accessible to the client (typically as part of the deliverable's documentation pack).

**What they cannot do:**

- Tell the client "this is Unitek IP" when it is in fact derived from the public CORE.
- Claim certification badges they have not earned.
- Stop another consultancy from doing the same thing — the licence is per-repository, not per-organisation. Any of Unitek's competitors can take the same public CORE and offer the same kind of service.

**Where the commercial moat actually lives for a service company:**

1. **Decades of experience** in the vertical — 33 years of Legal IT experience in the case of Unitek (since February 1993)
2. **The Vertical Business Objects** kept in private working repositories — the parts that translate the public CORE into a real, productive Law firm / Accounting firm / Banking deployment
3. **The relationships, the SLAs, the integration capability, the support team**
4. **The Service** — running the deployment for the client so they do not have to

None of those are licence-restricted. They are competitive advantages that exist because the service company has done the work, not because the licence reserves anything to them.

**The principle Unitek operates by, and recommends to other service companies:**

> *"Use the gift under the same terms as everyone else. Build the commercial offer on top. Compete on service, not on access."*

### Scenario 5.4 — Hosting company (Unitek Systems USA Inc on the GVB Production tier)

**Profile:** A company whose business is **operating the runtime** — providing infrastructure, uptime, geographic distribution, hardware, networking, and operational support for deployed Solutions. Unitek Systems USA Inc plays this role on the GVB Production tier.

**What they take from the gift layer:**

- The substrate-services layer (UniCORE.GVB)
- Any Vertical COREs the hosted Solutions depend on
- The underlying CORE stack

**What they build on top:**

- Operational tooling, monitoring, capacity management
- Customer-facing hosting service with billing, support, SLAs
- The data-centre operations themselves

**Crucial distinction — running vs distributing:**

CC BY 4.0 distinguishes between **using** software (running it for yourself or for a customer) and **distributing** it (giving copies to others). For a hosting company:

- **Running the software** for a paying customer is not "distribution" under CC BY 4.0. The hosting company can charge whatever they want for the service of running it. No new licensing obligations are triggered just by hosting.
- **Distributing modified copies** — for example, if the hosting company gives its customer a downloadable artefact that includes their modifications to public CORE — *is* distribution and triggers attribution + licence-text obligations.

**What the licence requires of them:**

- Make the upstream attribution available to their customers (typically as a "Powered by" line in their service documentation or admin console).
- If they distribute artefacts (Docker images, on-prem installers, etc.) that contain modified UniCORE-derived code, ship the LICENSE file and indicate their changes.

**What they cannot do:**

- Claim that the hosted Solution is the customer's exclusive licensed copy — it is not, and the upstream licence is irrevocable.
- Sell the public CORE itself as a product. They are selling the **service of running it**, not the code.

**Worked example — Unitek Systems USA Inc as GVB-tier operator:**

Unitek USA hosts the production-grade UniCORE.GVB deployments at the operator tier. Customers contract with Unitek USA for the hosting service. The hosting agreement names the public CORE components in play and links to their LICENSE files, names Unitek's private Vertical Business Object packages and their commercial licence terms, and separates the **service fee** (hosting + operations + SLA) from any **code licence** (none for CORE, separate commercial agreement for the Vertical Business Objects).

A competitor could in principle stand up the same public CORE and host the same kind of Solution. Unitek's competitive position is on operational quality, hardware ownership, and the 30-year-plus relationship with the underlying business stack — **not** on exclusive access to the code.

---

### Scenario 5.5 — Law firm using UniCORE.Law for itself

**Profile:** An end-user legal practice — partners, associates, support staff — that adopts UniCORE.Law for its own internal practice management. They are not selling software; they are running their law firm on it.

**Two delivery routes — both licence-compliant:**

#### 5.5a — They take the public UniCORE.Law and run it themselves

- They (or their internal IT, or a hired consultancy) clone UniCORE.Law from GitHub.
- They configure it for their firm (matters, clients, billing rules, conflict policies).
- They run it on their own servers or on a cloud account they own.
- They use it internally to run the firm.

**Licence implications:** Internal use. No distribution. They must keep the LICENSE file on the servers running the code, and they should keep an internal record of which UniCORE.Law version they are on. They owe no fee to anyone. If they make modifications for their own internal use, they can keep those modifications private — the licence does not require open-sourcing internal-only modifications (CC BY 4.0 is not ShareAlike).

#### 5.5b — They engage a service company to deploy and operate UniCORE.Law for them

- They sign a services contract with Unitek (or any other service company) to deliver a configured UniCORE.Law Solution.
- The service company configures, deploys, and supports.
- The law firm uses it; the service company maintains it.

**Licence implications:** The law firm does not have to know or care about the licence terms in detail — those obligations sit with the service company. The service company attributes; the firm uses.

**What the firm cannot do (in either route):**

- Re-sell UniCORE.Law as their own product without attribution.
- Add a clickwrap that purports to grant their employees fewer rights to the underlying CC BY 4.0 code than the licence itself grants.

**Worked example:**

A 200-partner UK law firm adopts UniCORE.Law-based practice management. They engage Unitek as the service company. Unitek configures the Vertical Business Objects, deploys onto a Unitek-USA-hosted Solution, and provides SLA-backed support. The firm pays an annual service fee and a per-seat licence fee for Unitek's private Vertical Business Object package. The firm pays nothing to anyone for the public UniCORE.Law portion — that is gift.

---

### Scenario 5.6 — Law firm building its own Law layer from generic UniCORE

**Profile:** A law firm (or a legal-tech team within one) that takes the **generic UniCORE implementation reference**, builds a Law-specific layer on top of it themselves, and runs that for their own internal practice. They are not buying a pre-packaged Vertical CORE; they are constructing their own.

This route is available **today** — before UniCORE.Law as a certified Vertical CORE exists. The generic UniCORE implementation reference is public; a firm with strong internal IT can build their own vertical layer right now.

**What they take from the gift layer:**

- UniCORE — the Level 2↔3 implementation reference
- UniCORE.GVB — the substrate-services layer (mail, file transfer, DNS, federation, tenancy)
- TrueAI Foundation and UniCORE AI — the governance architecture and invariants

**What they build on top:**

- Their own Law-specific Business Objects (matter/client/file hierarchy, time-and-billing rules, jurisdiction-specific workflow, conflict-policy engine)
- Their own integrations to their existing practice management or document management systems
- Their own deployment, configured for their firm's size and topology

**What the licence requires of them:**

- Attribute the public CORE repositories in their internal documentation and any external distribution of their adapted work.
- Keep their UniCORE-derived portions under CC BY 4.0 if they distribute the adapted work.
- Not claim "**UniCORE.Law-certified**" — that badge requires the certified Vertical CORE, which does not yet exist.
- Not claim "**Powered by UniCORE AI**" without going through the certification process.

**What they cannot do:**

- Describe their self-built Law layer as "UniCORE.Law" — that name is reserved for the certified Vertical CORE.
- Claim certification they have not earned.
- Re-sell their adapted work as "UniCORE.Law" without attribution.

**What they can do:**

- Use their adapted work internally for their own firm, licence-free.
- Keep their Law-specific Business Objects proprietary — CC BY 4.0 is not ShareAlike, so their additions are theirs.
- Publish their Law-specific Business Objects under whatever licence they choose (including CC BY 4.0 as a gift to the community).
- Engage Unitek or another service company to help build or maintain the vertical layer, under a standard services agreement.

**The same pattern applies to any vertical:** a hospital network building their own Healthcare layer from UniCORE, an accountancy firm building their own Accounting layer, a government department building their own Government layer. The gift layer is the same; the vertical work is each organisation's own.

---

### Scenario 5.7 — Organisations requiring 13+ Levels of Governance

**Profile:** Heavily regulated, multi-jurisdiction, or life-safety deployments where the 12-level reference is insufficient. Examples: a global investment bank with parallel regulator regimes; a multi-national hospital network with country-specific medical-device approval flows; a space-industry contractor with export-control overlay; a government department with statutory reporting叠加.

**What they take from the gift layer:**

- The full UniCORE AI 12-Level reference

**What they build on top:**

- Additional governance levels — typically jurisdiction-specific, regulator-specific, or domain-specific. Example: Levels 13–15 for an export-control environment might be export-classification review, statutory reporting audit, and cross-border data-flow governance.

**Licensing posture:**

- The additional levels are **their own work** and can be licensed however they choose — proprietary, CC BY 4.0, anything in between.
- If they merge their additional levels back into the public UniCORE-AI repository as a contribution, the merged portion must be CC BY 4.0.
- If they keep their additional levels in a private fork or a separate repository, they can keep that licensed however they wish.

**Attribution line example:**

> *"This deployment implements UniCORE AI 12-Level Governance plus three additional levels (export-control review, statutory reporting audit, cross-border data-flow governance) added by [Organisation Name]. The UniCORE AI 12-Level portion is used under CC BY 4.0; the additional three levels are [Organisation Name], all rights reserved."*

**What they cannot do:**

- Renumber or rename the original 12 levels in a way that creates confusion about what the public reference says.
- Claim the additional levels are part of UniCORE AI as published.
- Use a reserved naming prefix for the extension.

---

### Scenario 5.8 — Vendors that fork the CORE and build proprietary AI on top

**Profile:** A software vendor — potentially large, potentially well-resourced — takes the public CORE, forks it, builds their own proprietary AI implementation with their own governance structure on top, and sells it commercially. They may implement any number of governance levels (3, 4, 7, 12, or more). They may brand it under their own name. This is the scenario most likely to prompt the question: *can someone take this and monopolise it?*

**Short answer: they can take it. They cannot monopolise it.**

**What the licence permits:**

- Fork the public CORE and build proprietary AI on top.
- Implement any number of governance levels (3, 4, 7, 12, 13+, any combination).
- Ship it commercially and charge whatever they want.
- Re-brand it under their own name.
- Keep their proprietary additions proprietary.

**What the licence does NOT permit:**

- Restrict downstream users' rights to the underlying CORE portions (CC BY 4.0 §2(a)(5) — you cannot add legal or technical restrictions that prevent others from doing the same).
- Use reserved marketing phrases without certification (`Powered by UniCORE AI`, `TrueAI-certified`, `UniCORE-certified`, etc.).
- Claim conformance to the TrueAI Foundation or UniCORE AI governance model when their implementation does not satisfy the Nine Invariants.
- Use reserved naming prefixes (`UniCORE.Military`, etc.).

**Governance without Truth is theatre.**

The TrueAI Foundation Nine Invariants are the **Truth bar**. The 12-Level Governance architecture rests on them. A vendor can implement governance levels — even many of them — without being Truth-conformant. That is legally permitted. But it is not the same as being **Built on the TrueAI Foundation**.

The badge — `Powered by UniCORE AI`, `Built on the TrueAI Foundation`, `TrueAI-certified` — is the marker of genuine conformance. It is granted only through the certification process, which verifies that the Nine Invariants are satisfied in operation, not just in documentation.

**What the public corpus does:**

- Publishes the certification process openly. Any vendor can seek certification for any release.
- Reserves the marketing phrases. A vendor that uses them without certification is subject to public refutation.
- Records certification status publicly. A vendor's claims can be verified against the public registry.
- Withdraws certification from parties that engage in market behaviour rising to monopolisation (LICENSE.md monopoly clause; Unitek Systems Limited sole discretion; appeals process via UniVERSE/CERTIFIED-EXPERTS.md §4.3).

**So a vendor that forks and ships their own proprietary AI:**

- **CAN** say: "Based on UniCORE AI / UniCORE / UniCORE.GVB"
- **CANNOT** say: "Powered by UniCORE AI" without certification
- **CANNOT** say: "Built on the TrueAI Foundation" without demonstrating Nine Invariant conformance
- **CANNOT** wrap their proprietary additions in a licence that removes downstream rights to the CORE portions
- **CANNOT** claim certification if they have not been certified

If they behave well: they earn the badge, they compete on quality, the market benefits.

If they behave badly: the badge is withdrawn, their certification claims are publicly refuted, and the irrevocable public CORE remains available to every other vendor — including Unitek's competitors — on the same terms.

---

### Scenario 5.9 — How the licensing structure prevents monopoly capture

**The question:** Can a large vendor take the public CORE, build a proprietary version, and use that to corner the market in governed AI?

**The answer:** The licensing structure makes this structurally impossible to sustain.

**1. The gift is irrevocable and non-exclusive.**

CC BY 4.0 cannot be revoked. Once a version is published under CC BY 4.0, that version is forever available under those terms — to everyone, including every one of that vendor's competitors. No licence agreement, no commercial contract, no clickwrap can retroactively remove what has been given. The vendor cannot close the door they found open.

**2. The vendor cannot restrict downstream rights.**

CC BY 4.0 §2(a)(5) prohibits adding legal or technical restrictions that prevent others from doing the same. If the vendor takes the CORE, builds VendorAI on top, and tries to license VendorAI in a way that would prevent a downstream user from also using the CORE — that restriction is void under the licence. The vendor's proprietary additions can be proprietary; the underlying CORE portions must remain available. The vendor cannot create a situation where using VendorAI requires abandoning the public CORE.

**3. The badge is separate from the licence.**

`Powered by UniCORE AI`, `TrueAI-certified`, `UniCORE-certified` are reserved marks. They exist because the public corpus needs a way to distinguish genuine conformance from structural imitation. The badge is granted only through certification, which requires demonstrating Nine Invariant satisfaction in operation. The vendor can build anything; they cannot claim the badge without earning it.

If the vendor ships VendorAI with a governance structure that does not satisfy the Nine Invariants — no matter how many levels it has — they are not "Built on the TrueAI Foundation." They may say "based on UniCORE AI." They cannot say "Powered by UniCORE AI."

**4. Certification is withdrawable.**

If a certified vendor engages in market behaviour rising to monopolisation — using certification to exclude competitors, imposing restrictions on downstream users that the licence does not permit, or presenting their proprietary version as the only legitimate implementation — the certification is withdrawable under the LICENSE.md monopoly clause (Unitek Systems Limited sole discretion; appeals process via UniVERSE/CERTIFIED-EXPERTS.md §4.3). Withdrawal is a public act. The vendor loses the badge. The public record shows why.

**5. The Generation IT producer pipeline distributes capability.**

The programme's theory of change is that governed AI capability is distributed across many people over 30 years — not concentrated in one vendor. A vendor that attempts to monopolise the market faces not just the licence structure but the entire ecosystem of certified practitioners who have the expertise to build, evaluate, and compete with governed AI implementations. The monopoly is achievable in the short term; it is not sustainable over the 30-year horizon the programme is designed for.

**The principle in one sentence:**

> *A company can take the code. They cannot take the Truth.*

The code is gift under CC BY 4.0. The Truth — the Nine Invariants, the certification, the reserved marks, the public refutation of passing-off — is enforced by the public corpus through mechanisms that operate on reputation, certification, and the irrevocable nature of the gift itself.

---

---

### Scenario 5.10 — Organisations using fewer than 4 Levels of Governance (<4)

**Profile:** A deployment that drops below the recommended floor of 4 levels. Common scenarios: a hobby project, a research prototype, a teaching demo, an internal proof-of-concept that is not meant to go to production.

**What the licence permits:** Anything CC BY 4.0 permits — they can take whichever levels they want, in whatever combination they want, and use them.

**What the public corpus advises against:**

- A production deployment with fewer than 4 levels is not, in the public corpus's published view, a deployment that has earned the right to claim conformance with the UniCORE AI framework.
- A regulator-facing deployment with fewer than 4 levels is not a serious governance posture and should not be described as "Powered by UniCORE AI" or "TrueAI-certified".

**What the public corpus enforces:**

- The reserved marketing phrases (`Powered by UniCORE AI`, `UniCORE-certified`, `UniCORE-AI-certified`, `TrueAI-certified`, etc.) are off-limits without certification — and certification has minimum-level requirements.
- A deployment with fewer than 4 levels will not pass certification.

**Worked example — A university computer-science class:**

A computer science class uses UniCORE AI as a teaching reference for a coursework assignment on governance frameworks. The students implement two levels (audit and approval) as their assignment. They cite UniCORE AI in their bibliography and on a slide.

This is fine. They are not selling a product. They are not claiming certification. They are using the framework as a teaching aid and giving credit, which is exactly what CC BY 4.0 is for.

If, three years later, one of those students tries to commercialise their coursework as a real product with only those two levels, they would be welcome to do so — and the licence permits it — but they would not pass certification, would not be entitled to use the certification marks, and would (in the public corpus's published view) not be running a production-grade governance posture. The public corpus will say so if asked.

---

### Scenario 5.11 — UniCORE.GVB and UniCORE.Desktop — substrate-layer gift, operationally chain-locked

**Profile:** The substrate-services layer (`UniCORE.GVB` — Global Virtual Bridge, providing mail, file transfer, DNS, federation, tenancy, topology) and the client-application layer (`UniCORE.Desktop` — the desktop applications that connect to UniCORE and/or UniCORE.GVB substrate via APIs; installable on user-controlled infrastructure — workstation, internal server, wherever the user runs it) are different in kind from the architectural and Vertical CORE layers. They are **operational substrate**: code that runs in production, carries data, federates between deployments, and serves the desktop clients that humans actually use.

These two repositories are also CC BY 4.0, also gift, also under the same irrevocability and same Positioning Principle as the rest of the public corpus. But because they are operational and runtime-facing, the consequences of misrepresenting them are sharper than for the architectural layers above. This scenario sets out the position explicitly.

**The four principles that apply to UniCORE.GVB and UniCORE.Desktop:**

1. **Cannot be monopolised.** CC BY 4.0 is irrevocable and non-exclusive. No party — including Unitek Systems Limited and Unitek Systems USA Inc — can take exclusive ownership or restrict downstream rights to the public GVB or Desktop substrate. The licensing structure in §5.9 applies to GVB and Desktop on the same terms as every other public CORE repository.

2. **Cannot be forced.** No one can require another party to use a specific deployment, hosting provider, or commercial wrapping of GVB or Desktop. Any Solution that wants to use the gift substrate may do so under CC BY 4.0; no commercial agreement, no certification arrangement, and no service contract can lawfully prevent that.

3. **Cannot be sold as the substrate itself.** The hosting service is sellable (Scenario 5.4). The Vertical Business Objects on top are sellable (Scenario 5.3). The professional services around deployment, customisation, and support are sellable. But the GVB and Desktop substrate code itself is gift — it is not for sale. Anyone offering "exclusive UniCORE.GVB" or "proprietary UniCORE.Desktop" as a product is misrepresenting the gift.

4. **Forking diverges from the chain — and the chain is what makes the badge true.**

   This is the principle that distinguishes substrate from architecture. CC BY 4.0 permits forking. The badge structure does not endorse forks that diverge from the certified chain.

   The certified chain runs: TrueAI Foundation → UniCORE AI → UniCORE **and** UniCORE.GVB → UniCORE.Desktop. UniCORE and UniCORE.GVB are sister substrates — UniCORE is the implementation reference, UniCORE.GVB is the substrate-services layer (mail, file transfer, DNS, federation, tenancy, topology) — and UniCORE.Desktop connects to either or both via APIs. The badge "Powered by UniCORE AI / Built on the TrueAI Foundation" certifies that the entire chain — TrueAI Foundation, UniCORE AI, UniCORE, UniCORE.GVB, and the Desktop clients connecting to them — satisfies the Nine Invariants in operation.

   If a vendor forks UniCORE.GVB (or UniCORE) and ships a divergent version under a similar name, the operational properties of that fork are not the operational properties of the certified substrate. A Desktop client connecting to a forked substrate does not get the audit, identity, federation, and governance guarantees that the badge implies. The fork **looks** like the substrate; it does not **behave** like certified substrate. That is a security risk for the downstream user, and it is dishonest representation.

   The licence permits the fork; the public corpus declines to certify it; the badge is unavailable to it.

**The badge handshake — runtime enforcement of the chain.**

UniCORE.Desktop may be installed locally — on a user's workstation, on an internal server, on whatever infrastructure the user controls. The chain does not require centralised hosting.

But UniCORE.Desktop does not operate in isolation. All communication between the Desktop client and the substrate it serves — UniCORE and/or UniCORE.GVB — flows through APIs, and those APIs require **the badge on both sides** of the connection. The Desktop client carries its certification badge; the substrate endpoint carries its certification badge; the handshake completes only when both are present and current.

This is what makes principle #4 operational rather than aspirational:

- A **forked Desktop** loses its certification badge and cannot complete the handshake with a certified substrate endpoint. Certified UniCORE and UniCORE.GVB deployments will refuse the connection.
- A **forked UniCORE or UniCORE.GVB substrate** loses its certification badge and cannot serve certified Desktop clients. Desktop will refuse to connect to a non-badged substrate.
- A **third-party substrate or client** trying to impersonate the chain without certification cannot complete the handshake either. The badge is the credential; without it, the connection does not establish.

The chain is enforced at runtime, not just in policy. Certification is the architecture, not a sticker on top of it. "Powered by UniCORE AI, built on the TrueAI Foundation" is the badge that has to be present on both sides of every API exchange — and that, in the operating system, is what makes the chain a chain.

**What this means in practice:**

- **Permitted:** read, study, contribute to, deploy, host, integrate with, build Solutions on top of UniCORE.GVB and UniCORE.Desktop. Cite them, attribute them, redistribute them under CC BY 4.0 with appropriate changes-indicated. Add functionality back to the public repositories via Pull Request or Discussion proposal. Engage Unitek or another service company to operate GVB instances on behalf of customers.

- **Permitted but inadvisable:** forking GVB or Desktop for private use. Legally allowed under CC BY 4.0. Operationally the fork loses its certification badge — and once the badge is gone, the runtime API handshake with certified substrate endpoints (if you forked Desktop) or with certified Desktop clients (if you forked the substrate) no longer completes. Security and governance properties expected by users are not guaranteed by a private fork; in many configurations the connection itself simply will not establish. If you fork, you must know what you are doing — these are the operational backbone of governed AI Solutions, not casual reference code.

- **Not permitted under the badge structure:** describing a forked GVB or Desktop as "Powered by UniCORE AI" or "Built on the TrueAI Foundation" without certification. Selling a forked GVB or Desktop as a proprietary substrate product. Forcing downstream users to depend on a private fork instead of the public substrate. Any of these triggers public refutation and certification refusal.

**Contributions are welcome.**

These are gift repositories that grow. Public contributions improve the gift. The public corpus operates on the assumption that the substrate will accumulate functionality over time — added by Unitek, by Generation IT producers, by Solutions providers, by any contributor who has read the AGENTS.md and submits work that satisfies the Foundation invariants. Pull Requests, Discussions proposals, and certification submissions are the routes in.

**The principle in one sentence:**

> *UniCORE.GVB and UniCORE.Desktop are public substrate, contributed to publicly, certified as a chain. Anyone may fork. No fork can claim the badge. The gift remains the gift only while it remains the chain.*


---

## 6. Worked scenarios by named industry

The five industries below are the named verticals on the public roadmap as of 2026-05-22. Other industries follow the same pattern.

---

### 6.1 — Law

**Vertical CORE repository (planned, gift upon certification):** `bryanunitek/UniCORE.Law`

**What's specific to Law:**

- Conflict-of-interest checking is a first-class governance level, not an afterthought.
- The matter / client / file / document hierarchy is the central data model.
- Time-and-billing is the operational engine.
- Privilege, retention, and ethical-wall handling drive the audit and access-control levels.

**Licensing implications when you take UniCORE.Law:**

- Same CC BY 4.0 terms as any other public CORE repository.
- The Vertical CORE pattern is the gift; the Vertical Business Objects (Law-specific time-recording rules, jurisdiction-specific billing formats, firm-specific approval matrices) are typically commercial — kept in private working repositories.

**What is reserved:**

- The "**UniCORE.Law-certified**" badge is reserved for Solutions that have passed certification.
- "**Powered by UniCORE AI**" is reserved similarly.
- The naming prefix `UniCORE.Law.Military` is reserved out — Military is excluded from the public corpus entirely.

**Worked example — A 200-partner UK law firm:**

A 200-partner UK law firm adopts UniCORE.Law-based practice management. They engage Unitek as the service company. Unitek deploys UniCORE.Law (gift, CC BY 4.0) plus its private `UniCORE.Law-Claw` Vertical Business Object package (commercial, separately licensed). The deployment runs on Unitek USA's GVB Production tier.

The firm pays: (a) the hosting service fee, (b) the Vertical Business Object licence fee, (c) the implementation and ongoing professional services fee. They pay nothing for the public UniCORE.Law portion — that is gift.

If the firm later wants to switch service providers, or take operations in-house, or run a parallel deployment with another vendor — the UniCORE.Law licence permits all of those. Their commercial relationship with Unitek is service-based, not licence-based.

---

### 6.2 — Banking

**Vertical CORE repository (planned, gift upon certification):** `bryanunitek/UniCORE.Banking`

**What's specific to Banking:**

- Multi-jurisdiction regulator overlay (FCA, PRA, OCC, FDIC, ECB, FINMA, MAS, HKMA, etc.)
- Capital-adequacy and stress-testing reporting as governance levels
- Anti-money-laundering / know-your-customer flow as a separate audit track
- Real-time payments and settlement-finality semantics

**Licensing implications when you take UniCORE.Banking:**

- Same CC BY 4.0 terms.
- A core-banking vendor implementing UniCORE.Banking will typically need 13+ levels because of the multi-jurisdiction regulator overlay — the licence permits that.
- The vendor's own implementations of regulator-specific filings are their own work and can be proprietary or otherwise licensed at their discretion.

**Who uses it:**

- Core-banking platform vendors
- Challenger banks running their own stack
- Regulatory-tech (RegTech) vendors building governance and reporting tools
- Banks running internal compliance tooling

**Worked example — A challenger bank's compliance stack:**

A 5-year-old challenger bank with banking licences in three EU countries runs its compliance and audit stack on UniCORE.Banking. They implement 14 levels — the standard 12 plus two for SEPA-specific settlement-finality forensics and one for cross-border tax-information-exchange (CRS / FATCA).

Their attribution line in their compliance documentation:

> *"Compliance stack based on UniCORE.Banking by Bryan Fred, Unitek Systems Limited (CC BY 4.0). Two additional governance levels added for SEPA settlement-finality forensics and cross-border tax-information-exchange. [Organisation Name], all rights reserved on the additions."*

The bank pays nothing for the public UniCORE.Banking portion. They invest engineering effort to integrate, configure, and maintain it. If the bank's compliance tooling becomes good enough to spin it out as a sellable RegTech product, they can do so under CC BY 4.0 — same terms, same attribution requirements, same freedom to commercialise.

---

### 6.3 — Healthcare

**Vertical CORE repository (planned, gift upon certification):** `bryanunitek/UniCORE.Healthcare`

**What's specific to Healthcare:**

- Patient-record privacy (HIPAA in the US, GDPR + national law in the EU, equivalents elsewhere) drives the audit and access-control levels
- Medical-device interoperability and the FDA / MHRA / EMA approval lifecycle
- Clinical decision support — where AI in the critical path of consequential decisions is most acute
- Cross-border clinical trial governance

**Licensing implications when you take UniCORE.Healthcare:**

- Same CC BY 4.0 terms.
- Healthcare deployments commonly need 13+ levels to handle device-specific regulator approvals as their own governance level.
- The Nine Invariants (from TrueAI Foundation) are particularly important here — Healthcare is one of the original motivating examples for "AI in the critical path of consequential decisions."

**Who uses it:**

- EHR / EMR vendors
- Hospital networks running internal clinical governance tooling
- Medical-device manufacturers building software-as-a-medical-device (SaMD)
- Public-health authorities running surveillance and reporting platforms

**Worked example — A regional hospital network:**

A 12-hospital network in the EU adopts UniCORE.Healthcare for its clinical governance and safety reporting. They implement 13 levels — the 12 reference levels plus a 13th for medical-device-incident escalation under the EU Medical Devices Regulation.

They run it on infrastructure they own, supported by an internal IT team. They use the gift; they owe no fee to anyone for the code.

When they publish a peer-reviewed paper on the reduction in adverse-event reporting latency they observed, they cite UniCORE.Healthcare and TrueAI Foundation in the methods section. CC BY 4.0 is the appropriate licence for academic citation, and the citation requirement is exactly what the licence calls for.

If a vendor later wants to use the same hospital network's adapted level-13 framework, the hospital can publish that level-13 framework under whatever licence they choose — including CC BY 4.0 as a contribution to the global healthcare community. Their choice; the licence does not force them either way.

---

### 6.4 — Government

**Vertical CORE repository (planned, gift upon certification):** `bryanunitek/UniCORE.Government`

**What's specific to Government:**

- Statutory reporting and regulatory compliance as governance levels
- Multi-tier authority structures (departmental, cross-government, parliamentary / legislative)
- Public-interest obligations and freedom-of-information regimes
- Cross-border data sharing between government agencies (domestic and international)
- Citizen-facing service delivery with audit and accountability requirements

**Licensing implications when you take UniCORE.Government:**

- Same CC BY 4.0 terms.
- Government deployments commonly need 13+ levels to handle the statutory reporting叠加 and cross-agency coordination complexity — the licence permits that.
- Government-specific Business Objects (statutory-reporting formats, public-records management, citizen-data handling under privacy law) are typically developed as part of the deployment and can be kept proprietary or contributed back to the public corpus.

**Who uses it:**

- Central government departments and agencies
- Local and regional government bodies
- Public-sector procurement frameworks
- Government IT suppliers building on behalf of public-sector bodies

**Worked example — A national government's digital services agency:**

A national government's digital services agency adopts UniCORE.Government as the governance foundation for its citizen-services platform. The platform handles interactions across multiple departments — taxation, social welfare, immigration, healthcare registration. Each department has its own regulatory regime; the platform must present a unified citizen-facing interface while maintaining department-specific audit trails.

They implement 15 levels — the 12 reference levels plus three for statutory-reporting aggregation across departments, cross-border data-sharing governance under applicable privacy treaties, and parliamentary-oversight audit access.

They run the platform on government-owned infrastructure. Their attribution line:

> *"Citizen services platform based on UniCORE.Government by Bryan Fred, Unitek Systems Limited (CC BY 4.0). Three additional governance levels added for statutory-reporting aggregation, cross-border data-sharing governance, and parliamentary-oversight audit access. [Agency Name], all rights reserved on the additions."*

The government agency pays nothing for the public UniCORE.Government portion. They invest engineering effort to configure and maintain the platform. If a neighbouring government's agency later wants to adopt the same framework, they can — the licence is the same, the attribution is the same, the freedom to build on top is the same.

---

### 6.5 — Space Industry

**Vertical CORE repository (planned, gift upon certification):** `bryanunitek/UniCORE.Space-Industry`

**What's specific to Space Industry:**

- Export-control overlay (ITAR / EAR in the US, the EU Dual-Use Regulation in Europe, equivalents elsewhere)
- Mission-critical / life-safety levels (crewed missions add another layer of severity)
- Long-duration mission planning — governance windows measured in years or decades, not minutes or hours
- Multi-agency coordination across civil space agencies and commercial operators

**The Positioning Principle:**

The public CORE programme is positioned for **Harmony, Peace, Space Exploration, and Humanity**. `UniCORE.Military` and any military-named industry prefix is **deliberately reserved out** of the public corpus. Space Industry as named here means civil and commercial space, not weapons systems.

**Licensing implications when you take UniCORE.Space-Industry:**

- Same CC BY 4.0 terms.
- Space-industry deployments commonly need 13+ levels (export-control review, mission-readiness sign-off, post-flight forensic and lessons-learned).
- The Positioning Principle is enforced at the public corpus level, not at the licence level. CC BY 4.0 itself does not restrict use to non-military purposes — but the public statements, the named-industry list, and the reserved-prefix list make the position clear: these are published for civil and commercial space, and certification and badge endorsement will not be granted for military-classified derivatives.

**Who uses it:**

- Civil space agencies' contractors and subcontractors
- Commercial launch providers
- Satellite operators (Earth observation, communications, scientific research)
- Crewed-mission operators
- University and research-laboratory aerospace programmes

**Worked example — A commercial Earth-observation satellite operator:**

A commercial constellation operator (roughly 80 satellites in low Earth orbit, 24/7 imagery service to civilian customers) adopts UniCORE.Space-Industry for its mission-control governance and customer-data audit framework. They implement 14 levels — 12 reference + 1 for export-control on imagery distribution + 1 for orbital-debris-mitigation reporting.

They publish a NOTICE.md attributing UniCORE.Space-Industry, UniCORE-AI, and TrueAI Foundation. Their levels 13–14 are kept internal and proprietary because they are commercially sensitive.

They pay nothing for the public CORE portion. They sell their imagery service commercially. The licence permits this.

If the operator later wins a defence contract, the defence work is outside the scope of the public UniCORE.Space-Industry positioning. They can fork privately — the licence permits the fork — but they cannot describe the defence-classified deployment as "Powered by UniCORE AI" if the public corpus's reserved-marketing-phrase rules disqualify defence applications.

---

## 7. Things the licence does not do

Common misconceptions worth correcting up front when you are asked:

- **"CC BY 4.0 means it's only for non-commercial use."** False. CC BY 4.0 explicitly permits commercial use. The "BY" stands for "Attribution", not "non-commercial".
- **"If I modify the code I have to give my modifications back."** False. CC BY 4.0 is not ShareAlike. You can keep modifications private. The only obligation is attribution if you redistribute.
- **"The licence covers the trademarks too."** False. CC BY 4.0 covers copyright, not trademarks. The "Powered by UniCORE AI" mark and the certification marks are governed separately by the published statement-on-claims and certification policy.
- **"If I use this I have to publicise that I'm using it."** Partly true. The attribution requirement applies when you distribute — when you ship a product, publish a paper, host a public service. Internal-only use does require keeping the LICENSE file with the code but does not require external publicity.
- **"Unitek can revoke the licence later."** False. CC BY 4.0 is irrevocable. Once a version is published under CC BY 4.0, that version is forever available under those terms.

---

## 8. Things the public corpus enforces beyond the licence

CC BY 4.0 itself does not cover everything. Some matters are enforced by the public corpus through statements, conventions, and refusal to certify or endorse:

| Matter | Enforced by | Mechanism |
|---|---|---|
| Reserved marketing phrases | STATEMENT-ON-CLAIMS in each public repository | Public refutation if used incorrectly; certification policy |
| Reserved naming prefixes | STATEMENT-ON-CLAIMS | Public refutation |
| The Positioning Principle (Harmony / Peace / Space Exploration / for Humanity) | The public corpus's published position | Refusal to certify or badge derivatives that conflict |
| Certification gates | The certification policy | The certification process itself |
| Honest scope claims | Published guidance and the certification gate | Certification refusal; public clarification if asked |

These are not licence terms — they are conventions of the public programme. They function on the basis of public statement and reputation, not contract.

---

## 9. The short version (for if you're asked verbally)

If a Partner, Client, or Software Provider asks you in person and you have 60 seconds:

> *"The public CORE — TrueAI Foundation, UniCORE AI, UniCORE itself, and the Vertical COREs once certified — is published under Creative Commons Attribution 4.0. That means anyone can use it, modify it, and build a commercial product on top of it. The only obligations are: attribute the author, keep the licence text with the code, indicate what you changed if anything, and don't claim certifications or marks you haven't earned. The licence is irrevocable — once given, it stays given. Unitek operates under the same licence as everyone else. Our commercial position is the service, the implementation experience, and the private Vertical Business Objects we keep in our working repositories — not exclusive access to the public CORE."*

That's the elevator answer. Send them this document for the detail.

---

## 10. References

- **Canonical licence text:** `LICENSE` in each public repository (`bryanunitek/UniVERSE`, `bryanunitek/TrueAI`, `bryanunitek/UniCORE-AI`, `bryanunitek/UniCORE`, `bryanunitek/UniCORE.GVB`)
- **CC BY 4.0 in full:** [https://creativecommons.org/licenses/by/4.0/legalcode](https://creativecommons.org/licenses/by/4.0/legalcode)
- **Reserved marketing phrases and naming prefixes:** `STATEMENT-ON-CLAIMS.md` in each public repository
- **Certification process:** `00057-Layered-CORE-Model.md` and the certification documents in `UniCORE-AI/docs/`
- **The Positioning Principle:** `HORIZON.md` and `FULL_FORMAL_STATEMENT.md` in the Foundation triad
- **Author and contact:** Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom — public discussion via the Discussions tab on each public repository

---

## Document status

| Field | Value |
|---|---|
| First published | May 2026 |
| Author | Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom |
| Licence of this document | Creative Commons Attribution 4.0 International (CC BY 4.0) |
| Review status | Living document — corrections and clarifications welcome via [GitHub Discussions](https://github.com/bryanunitek/UniCORE/discussions) |
| Companion documents | [LICENSE.md](LICENSE.md) · [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md) · [ROADMAP.md](ROADMAP.md) · [IRREVOCABLE-LICENCE-DECLARATION.md](IRREVOCABLE-LICENCE-DECLARATION.md) |
