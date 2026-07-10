---
title: "UniSaaS.UniCORE — Roadmap"
author: Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
version: "Version 1.0 · June 2026"
status: v1.0 (DRAFT v0.01)
licence: CC BY 4.0
---

# UniSaaS.UniCORE — Roadmap

**What arrives here, when, and under what trigger condition. The SaaS-deployment-shape sister of [UniCORE/ROADMAP.md](https://github.com/bryanunitek/UniCORE/blob/main/ROADMAP.md).**

---

## Status today

This repository holds the canonical public identity of UniSaaS.UniCORE — the SaaS-deployment-shape sister of UniCORE. The licence, the architecture position, the certification trigger, and the naming rules. **Source code is not yet published.**

The implementation work is being done in the private working repository `bryanunitek/UniSaaS.UniCORE.Law-Claw` and (for the substrate-services layer) `bryanunitek/UniSaaS.UniCORE.GVB-Claw`. Source code becomes public on certification, not before.

---

## The certification trigger

The trigger that moves UniSaaS.UniCORE from documentation-only to documentation-plus-code is:

> The first SaaS Vertical CORE built on UniSaaS.UniCORE — `UniSaaS.UniCORE.Law-Claw` — is **certified Powered by UniCORE AI / built on the TrueAI Foundation**.

When that certification is recorded, the UniSaaS.UniCORE substrate inside `UniSaaS.UniCORE.Law-Claw` is extracted and published in this repository under CC BY 4.0. The Law SaaS Business Objects remain in `UniSaaS.UniCORE.Law-Claw` as the commercial Vertical SaaS CORE layer.

The certification gate is not a marketing milestone. It is a quality threshold. The badge ("Powered by UniCORE AI / built on the TrueAI Foundation") is a claim about Foundation conformance. Source code arriving here before that claim is earned would dilute the badge.

The gate is identical to UniCORE's gate. The Foundation invariants do not change shape between deployment topologies.

---

## What arrives at certification

When `UniSaaS.UniCORE.Law-Claw` is certified, this repository receives:

### Source code
- The UniSaaS.UniCORE substrate code extracted from `UniSaaS.UniCORE.Law-Claw` — the industry-agnostic, SaaS-deployment-shape layer that satisfies the UniCORE AI 12-Level reference architecture.
- The build files (`.sln`, `.csproj`, `Directory.Packages.props`, `Directory.Build.props`) that compile the substrate.
- Tests for the substrate.

The Vertical SaaS CORE Law layer continues to mature ahead of certification. Vertical-CORE-side feature work — the multi-payor billing model, the multi-jurisdiction VAT resolver engine, the protected-bank-detail workflow, and the SaaS-shape additions (multi-tenant routing, signing-key separation, tenant-by-email resolution) — lives inside `UniSaaS.UniCORE.Law-Claw` rather than in this UniSaaS.UniCORE substrate, and remains there at certification. The substrate is the cross-vertical layer; the Vertical SaaS CORE features stay with the Vertical SaaS CORE.

### Documentation
- `docs/` — full architecture documents: governance integration, contracts, integration points, conformance claims, SaaS-shape deployment notes.
- `IRREVOCABLE-LICENCE-DECLARATION.md` — formal irrevocability declaration (mirror of, or reference to, the canonical UniVERSE declaration).
- `BRAND-AND-TRADEMARK-USE-POLICY.md` — names + marks rules.
- `DISCUSSIONS.md` — purpose of the GitHub Discussions tab.
- `SUCCESSION.md` — stewardship reference.

### Continuous publication
- After certification, every release of UniSaaS.UniCORE substrate in any SaaS Vertical CORE working repository is mirrored here on push.

---

## What does NOT arrive at certification

- **Vertical SaaS CORE Business Objects** stay in their own repositories. UniSaaS.UniCORE.Law's Business Objects stay in `bryanunitek/UniSaaS.UniCORE.Law-Claw` as the commercial Vertical SaaS CORE layer.
- **Hosted-service operational state** stays with whoever operates the service. UniSaaS.UniCORE is the substrate code. Unitek Systems USA Inc, when it operates a UniSaaS.UniCORE-based hosted service, does so as one consumer of this gift among many — under the same CC BY 4.0 licence as everyone else. The operational state of any specific hosted service is not part of the gift surface.
- **Solutions-tier code** stays with the Solution producer. A specific client's working SaaS implementation is a services-built deliverable; it is not part of the gift.
- **Working-state churn** stays in the private working repository. This repository is not a mirror of work-in-progress; it receives published, certified releases.

---

## Five-Solution naming and the UniVIEW / UniREPORT split-out

Under the 2026-04-24 five-Solution lock, the consumption tier carries five Solutions: `UniCORE`, `UniCORE-UniVIEW`, `UniCORE-UniREPORT`, `UniSaaS-UniCORE-UniVIEW`, `UniSaaS-UniCORE-UniREPORT`. UniSaaS.UniCORE is the SaaS-shape parent of the last two.

**Today, pre-certification:** UniVIEW and UniREPORT are documented inside this repository's [README.md §"UniVIEW and UniREPORT"](README.md#uniview-and-unireport) and inside the on-prem-shape parent UniCORE repository.

**At certification:** UniVIEW and UniREPORT each get their own public gift-surface repository, peer to UniSaaS.UniCORE: `bryanunitek/UniSaaS.UniCORE.UniVIEW` and `bryanunitek/UniSaaS.UniCORE.UniREPORT`. Each carries the same 11-file gift-surface shape. Cross-references from UniSaaS.UniCORE will be updated to point to them at that point.

This pattern mirrors how `UniCORE.Desktop` is handled in UniCORE's roadmap — documented in parent gift-surface repositories pre-certification, split out to its own repository at certification. Pre-creating four repositories before there is source code to host would stand up empty canonical homes; the certification gate is a natural moment to split out at, after which each carries real content.

---

## Sequence of certification

The certification arc is roughly:

1. **Build** — `UniSaaS.UniCORE.Law-Claw` and `UniSaaS.UniCORE.GVB-Claw` are built privately to the level the Foundation invariants require, including the SaaS-shape additions (multi-tenant routing, signing-key separation, tenant-by-email resolution).
2. **Self-assessment** — the Generation IT producer pair self-assesses against the Nine Invariants and the 12-Level reference architecture, including the SaaS-shape adaptations.
3. **Solution Review** — independent Solution Review by a [Certified Expert](https://github.com/bryanunitek/UniVERSE/blob/main/CERTIFIED-EXPERTS.md) (or by the producer pair where they themselves hold the certification, per the rule in `UniVERSE/docs/00059-Solution-Review.md`).
4. **Certification recorded** — the Solution Review outcome is recorded; the certification claim ("Powered by UniCORE AI / built on the TrueAI Foundation") becomes valid for the SaaS-shape Solution.
5. **Public publication** — the UniSaaS.UniCORE substrate is extracted and published here. The Vertical SaaS CORE Business Objects remain in the Vertical SaaS CORE's own repository.

The exact procedural detail of the certification is governed by the canonical material in [`UniVERSE/docs/10002-Certification-Before-Layered-Governance.md`](https://github.com/bryanunitek/UniVERSE/blob/main/docs/10002-Certification-Before-Layered-Governance.md) and [`UniVERSE/docs/00059-Solution-Review.md`](https://github.com/bryanunitek/UniVERSE/blob/main/docs/00059-Solution-Review.md).

---

## Why DRAFT v0.01 today

The programme as a whole is in DRAFT v0.01. Versioning across the public repositories does not turn on until the first GitHub Discussion is opened in any of the public programme repositories — see [`UniVERSE/HORIZON.md`](https://github.com/bryanunitek/UniVERSE/blob/main/HORIZON.md) for the canonical statement.

This repository inherits that posture. The `Version: 1.0` line in the header is a placeholder. Substantive change is tracked in git history; programme-level versioning will be enabled when the corpus moves out of draft.

---

## Time horizon

The same horizon that applies to the wider programme applies here. UniSaaS.UniCORE source publication depends on the certification arc, which depends on the substrate being honestly built to satisfy the invariants in the SaaS deployment shape. That is decade-shaped work.

For the canonical horizon statement, see [`UniVERSE/HORIZON.md`](https://github.com/bryanunitek/UniVERSE/blob/main/HORIZON.md). UniSaaS.UniCORE does not publish a separate horizon — the programme horizon governs.

---

## What readers can do today

- **Cite the architecture** — the position of UniSaaS.UniCORE as the SaaS-deployment-shape sister to UniCORE, and the certification trigger, are public and citable now.
- **Read the canonical material** — the Foundation triad ([UniVERSE](https://github.com/bryanunitek/UniVERSE), [TrueAI](https://github.com/bryanunitek/TrueAI), [UniCORE-AI](https://github.com/bryanunitek/UniCORE-AI)) is fully published; the technical reference for what UniSaaS.UniCORE substrate must satisfy is there. The on-prem-shape sister [UniCORE](https://github.com/bryanunitek/UniCORE) is published at the same documentation-only state today.
- **Build their own UniSaaS.UniCORE-conformant substrate** under CC BY 4.0 — the architecture is open. Independent producers building Foundation-aligned SaaS substrates are exactly what the gift principle exists to enable.
- **Discuss** — open a thread on this repository's [Discussions tab](https://github.com/bryanunitek/UniSaaS.UniCORE/discussions) when adoption questions, architectural critique, or translation work has begun.

---

## Versioning of this document

| Version | Date | Notes |
|---|---|---|
| v1.0 | June 2026 | First publication. Repository created public; certification trigger recorded; source code held until first SaaS Vertical CORE certification. |

Revisions tracked in git history.

---

## Contact

- **Public discussion:** [GitHub Discussions](https://github.com/bryanunitek/UniSaaS.UniCORE/discussions)
- **Private contact / connection request:** [LinkedIn](https://www.linkedin.com/in/bryan-fred-02209753/)

— Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom, June 2026.

---

## Document history

- 2026-06-03 (6c489cf) — docs: initial 11-file public surface — UniSaaS.UniCORE

*Back-filled from git log on 2026-07-10 21:33 UTC. Kind 2 versioning (dated change notes) — see HORIZON.md § Evolution and versioning. Kind 1 (formal `Version:` bumps) remains OFF until first GitHub Discussion.*
