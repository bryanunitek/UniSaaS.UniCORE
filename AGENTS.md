# AGENTS.md — UniSaaS.UniCORE

**Read this first, every time, before touching this repo.**

---

## What this repo is

`bryanunitek/UniSaaS.UniCORE` — the public canonical home of UniSaaS.UniCORE, the **SaaS-deployment-shape sister of UniCORE**. Today it holds documentation, the licence, and the roadmap. **Source code is not yet published here** — it arrives when the first SaaS Vertical CORE built on UniSaaS.UniCORE is certified Powered by UniCORE AI / built on the TrueAI Foundation. See `ROADMAP.md`.

Sister repos:
- `bryanunitek/UniVERSE` — the civilisational-scale programme
- `bryanunitek/TrueAI` — the immutable Foundation (Nine Invariants)
- `bryanunitek/UniCORE-AI` — the 12-Level reference architecture
- `bryanunitek/UniCORE` — the on-prem-deployment-shape sister to this repo
- `bryanunitek/UniCORE.GVB` — the on-prem-shape substrate-services layer
- `bryanunitek/UniSaaS.UniCORE.GVB` — the SaaS-shape substrate-services layer (sister to this repo at the substrate-services tier)
- `bryanunitek/UniSaaS.UniCORE.Law-Claw` — the working private repo for the first SaaS Vertical CORE; on certification, its UniSaaS.UniCORE-conformant substrate is published HERE

When Bryan says "UniSaaS.UniCORE" referring to a repo, he means **this repo only**. Do not spill work into the others. The on-prem-shape sister is `UniCORE`; the substrate-services sister is `UniSaaS.UniCORE.GVB`.

## Who pushes

**I push directly.** Commit and `git push origin main` on Bryan's behalf. No GitHub Desktop, no approval loop. This is the standing rule for the Foundation triad (UniVERSE, TrueAI, UniCORE-AI), for UniCORE / UniCORE.GVB, and for UniSaaS.UniCORE / UniSaaS.UniCORE.GVB.

The working repos with the GitHub-Desktop-by-default rule are the private Claw repositories (`UniCORE.Law-Claw`, `UniCORE.GVB-Claw`, `UniCORE.Desktop-Claw`, `UniTEKClaw-Claw`, `UniSaaS.UniCORE.Law-Claw`, `UniSaaS.UniCORE.GVB-Claw`). This is not one of those.

## Branching

- **One branch: `main`.** Never create feature branches. Never create dev branches.
- Never open pull requests. Direct commits to `main`.

## Commit style

- Author: `bryanunitek <bryan.fred@unitek-systems.com>` (use `--author=` when committing so attribution is correct even when local git config differs).
- Message format: `<type>: <subject line>` then blank line, then body. Types: `docs`, `governance`, `roadmap`, `chore`.
- Body lists the files added/changed and the "what / why" in two or three sentences.

## Layout (current — pre-certification)

| Path | Purpose |
|---|---|
| `README.md` | Repo overview, position in the Layered CORE model, deployment-shape distinction, certification trigger |
| `LICENSE.md` | CC BY 4.0 / gift licence, mirroring the triad |
| `LICENSE_EXAMPLES.md` | Plain-English worked scenarios for Partners, Clients, and Software Providers |
| `AGENTS.md` | This file — rules for Claws working on this repo |
| `AI-AUTHORSHIP.md` | AI-assistance disclosure under TrueAI governance |
| `ROADMAP.md` | What arrives at certification and in what shape |
| `STATEMENT-ON-CLAIMS.md` | Names / marks / claims rules for "UniSaaS.UniCORE" |
| `BRAND-AND-TRADEMARK-USE-POLICY.md` | Names + marks rules (cross-reference to canonical) |
| `IRREVOCABLE-LICENCE-DECLARATION.md` | Irrevocability declaration (cross-reference) |
| `DISCUSSIONS.md` | Discussions tab purpose statement (cross-reference) |
| `SUCCESSION.md` | Stewardship reference (cross-reference) |

Do not invent new top-level files or directories without asking.

## Layout (post-certification — anticipated)

When the first SaaS Vertical CORE is certified, the UniSaaS.UniCORE substrate is extracted from `UniSaaS.UniCORE.Law-Claw` and published here. Anticipated additions at that point:
- `src/` or top-level `.csproj`-bearing directories — the substrate code
- `docs/` — full architecture documents (governance, integration, contracts, SaaS-shape deployment notes)

The shape locks at certification, not before. Today the repository holds the v0.01 minimal set.

## SaaS-shape voice (DURABLE)

UniSaaS.UniCORE is the sister of UniCORE, not its superior. The deployment shape is the only thing that distinguishes them; the governance, the invariants, the architecture, and the certification gate are identical. When drafting copy:

- Refer to UniCORE as the on-prem-deployment-shape sister, not as "the older one" or "the lesser one".
- Frame the SaaS-shape additions (multi-tenant routing, signing-key separation, tenant-by-email resolution) as deployment-topology adaptations, not as new governance.
- Do not claim that UniSaaS.UniCORE replaces or supersedes UniCORE. Both are gift surfaces; both are CC BY 4.0; both are irrevocable; both have the same certification gate.

## Attribution rules (durable)

- **Authorship / licence / legal entity:** Unitek Systems Limited (UK) as the present custodian of the gift layer; specific IP-custodian subsidiary within the Unitek Group recorded in the canonical [`UniVERSE/IRREVOCABLE-LICENCE-DECLARATION.md`](https://github.com/bryanunitek/UniVERSE/blob/main/IRREVOCABLE-LICENCE-DECLARATION.md).
- **Licence for all content here:** CC BY 4.0, "given, not sold, irrevocable".
- **Author byline:** `Bryan Fred, Unitek Systems Limited` unless Bryan says otherwise.
- **Version/date:** include version + month-year on any substantive document (e.g. `Version 1.0 · June 2026`).

## Contact rules (durable)

Two tiers, and only these two:

- **Public discussion** → GitHub Discussions of the relevant repo
  - UniSaaS.UniCORE: https://github.com/bryanunitek/UniSaaS.UniCORE/discussions
  - UniSaaS.UniCORE.GVB: https://github.com/bryanunitek/UniSaaS.UniCORE.GVB/discussions
  - UniCORE: https://github.com/bryanunitek/UniCORE/discussions
  - UniCORE.GVB: https://github.com/bryanunitek/UniCORE.GVB/discussions
  - UniVERSE: https://github.com/bryanunitek/UniVERSE/discussions
  - TrueAI: https://github.com/bryanunitek/TrueAI/discussions
  - UniCORE-AI: https://github.com/bryanunitek/UniCORE-AI/discussions
- **Private contact / connection request** → LinkedIn: https://www.linkedin.com/in/bryan-fred-02209753/

**Do not publish** Bryan's personal email (`bryan.fred@unitek-systems.com`, `bryan@unitek-systems.co.uk`), personal phone numbers, or the Unitek Systems generic inboxes (`info@`, `support@`, `services@`) in any file committed to this repo.

Git commit author metadata is the one exception: use `bryanunitek <bryan.fred@unitek-systems.com>` for `--author=` so the git log attributes correctly.

## Byline rules (durable)

- **Formal full byline:** `Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom` — four parts, in that order.
- Use the full formal on `Author:` fields, signoff lines, LICENSE contact blocks, masthead blocks of any substantive document.
- **Short form** `Bryan Fred, Unitek Systems Limited` is acceptable in running prose only.
- **Never** shorten to "Bryan, Unitek Systems Limited".

## Voice

- Reasoned, not declaratory. Engineering-honest. Avoid manifesto tone.
- This repo's voice is **architectural** — it explains where UniSaaS.UniCORE sits in the Layered CORE model, how it differs from UniCORE only by deployment shape, what the certification gate does, how gift propagation works in a hosted-service topology. It does not market.
- Cross-reference the canonical statements in the Foundation triad rather than repeating them in full here. The triad is upstream.

## Do not

- Do not publish source code in this repo before certification has been recorded for the first SaaS Vertical CORE that uses UniSaaS.UniCORE.
- Do not create branches, open PRs, or introduce a dev workflow.
- Do not invent new top-level files or directories without asking.
- Do not mix product/code material from `UniSaaS.UniCORE.Law-Claw` (or any other working Claw repo) into this public repo.
- Do not contradict the canonical statements in `UniVERSE`, `TrueAI`, `UniCORE-AI`, or `UniCORE`. If something here would contradict the canonical, fix this repo or raise the contradiction.

## After push

Tell Bryan the commit hash and what changed in one or two sentences. That's the handshake.
