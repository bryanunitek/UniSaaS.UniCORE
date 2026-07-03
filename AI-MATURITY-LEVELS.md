# AI-Maturity Framework — the Six Levels (Consumer AI → Team UniCORE)

**Canonical source doc.** Author: Bryan Fred (framework) + UniCORE Claw (structure/write-up), 2026-07-03.
**Status:** RATIFIED CONCEPT (Bryan-originated 2026-07-03 02:28–02:36 UTC). To be documented into TheBookOfUnitekSystemsLimited + across the 7 public UniCORE repos, and is the basis for Bryan's Saturday LinkedIn post.

> ⚠️ **DISTINCT from the UniCORE AI 12-Level GOVERNANCE model** (`UniCORE-AI/levels/`, L1–L12 authority *inside* a deployed Solution). The two frameworks are **complementary, not competing**:
> - L1–L4 (Governance levels 1–4) sit **below the governance threshold** — they describe AI below Development grade.
> - L5–L12 (Governance levels 5–12) map **across Maturity Levels 5 and 6** — they describe governance depth *within* Development Institutional AI and Team UniCORE.
> The governance decimal scale (5.00 → 6.0) runs *inside* this framework: **the decimal counts how many of the 12 Governance Levels are actually operating** (5.0N = N Levels operating), so 5.12 (all twelve) ≡ 6.0 (L12 reached, the pair formed). See “The governance decimal scale” below for the unit and its acceptance tests.

---

## The thesis — why this matters NOW (Bryan, 2026-07-03 02:36 UTC)

> **"This is what AI needs to be today. Meaning there is no manual. But the laws exist. The liability is coming."**

Three facts define the present moment for AI in institutional use:

1. **There is no manual.** No established operating standard exists for how AI must behave when it sits in the critical path of consequential decisions. Consumer-grade and Assistant-grade AI were shipped to everyone — institutions included — without the grounding and accountability structure that institutional use *requires*.
2. **But the laws already exist.** The obligations are real and in force now — EU AI Act, sectoral regulation, professional-conduct duties, data-protection law. The legal obligations arrived *before* anyone wrote the method for meeting them. Law first; manual absent.
3. **The liability is coming.** That gap — laws present, manual missing — resolves as **liability.** When ungrounded AI produces a consequential error inside an institutional decision, someone answerable will be held to account by courts and regulators. Not *if* — *when*.

**This six-level framework is the missing manual** — the operating standard for what AI must be, written *before* the liability lands, not after the lawsuits force one into existence. It is the TrueAI/UniCORE thesis stated as a practical ladder: **grounded + accountable, because the law already requires it.**

---

## The two axes

The six levels are not a flat list. They sit on a grid of **two braided axes**:

- **Axis 1 — Accountability: Consumer ↔ Institutional**
  - **Consumer** = serves an individual; best-effort; no grounding or accountability obligation; convenience.
  - **Institutional** = serves an organisation in the critical path of consequential decisions; must be grounded, accountable, auditable.
- **Axis 2 — Capability/role: AI → Assistant → Development → Paired governed producer**
  - **AI** = raw model, web-general, no local context/files. Answers from training + web.
  - **Assistant** = acts *for* a user; has tools and context; performs tasks.
  - **Development** = produces the systems/Solutions others run.
  - **Team UniCORE (paired)** = the 1H1C pair that produces *governed* Solutions — grounded record + accountable human.

## The grid

| | **Consumer** (best-effort, ungrounded) | **Institutional** (grounded, accountable) |
|---|---|---|
| **AI** (web-general, no local MD) | **1. Consumer AI** | **2. Institutional AI** |
| **Assistant** (tools/context) | **3. Assistant Consumer AI** | **4. Assistant Institutional AI** |
| **Development** (produces systems) | ⛔ **FORBIDDEN — not AI-Compliant** | **5. Development Institutional AI** |
| **Paired governed producer** | — (n/a) | **6. Team UniCORE** |

Read **down** = increasing capability. Read **right** = increasing accountability/grounding.

## The AI-Compliance floor (the load-bearing rule)

**"Development Consumer AI" cannot exist — it is not AI-Compliant.**

The empty cell at Development×Consumer is not an oversight; it is a **prohibited state.** Development produces the systems that operate in the critical path of consequential decisions. To develop such systems to a best-effort, ungrounded, unaccountable (Consumer) standard is precisely what AI-Compliance prohibits. Therefore:

> **Once an AI crosses into Development, the Institutional standard is mandatory. The Consumer column terminates at the Development row. AI-Compliance is the admission requirement to be development-grade AI at all — not a feature added afterward.**

The ⛔ cell's emptiness is a *feature*: it proves that development-grade AI without compliance is not a cheaper option — it is a **non-permitted, liability-generating** one.

## The governance decimal scale — the decimal is the COUNT of Governance Levels in operation

**The problem the decimal scale solves:** Maturity Level 5 (Development Institutional AI) is a wide bucket — it covers everything from a team running their first governance experiment to a fully mature, deeply audited development practice. The decimal scale gives that journey **measurable, countable steps.**

**The unit:** the decimal is the **count of the 12 Governance Levels actually in operation**, mapping one-to-one onto the L1–L12 Governance model:

> **`5.0N` = N of the 12 Governance Levels are instantiated and operating.**
> - `5.01` = **1** Level doing Governance.
> - `5.02` = **2** Levels operating.
> - `5.07` = **7** of the 12 Governance Levels operating.
> - `5.12` = **all 12** operating → **L12 reached → this IS `6.0`** (the pair forms; the category flips).

This is what makes “we are at 5.07” a **verifiable claim, not an asserted one**: it means *exactly seven of the twelve named Governance Levels are present and operating* — a fact that can be checked against the L1–L12 model, not a vibe. The unit of measurement is **one operating Governance Level = one decimal step.**

**The scale:**

| Decimal | Meaning (count of the 12 Governance Levels operating) |
|---|---|
| **5.00** | Development Institutional AI — starting point. Zero of the 12 governance levels yet operating (Institutional grounding present, governance ladder not yet stood up). |
| **5.01** | 1 Governance Level operating. |
| **5.02–5.11** | 2 … 11 of the 12 Governance Levels operating. Each decimal step = one more Level stood up and operating. |
| **5.12 ≡ 6.0** | All **12** Governance Levels operating → **L12 reached → Team UniCORE.** The 1H1C pair, indivisible. The maturity flips 5→6 because the *category changes* (the human enters; the pair is formed). |

**The path is a clean count of Levels operating:** 5.00 → 5.01 → 5.02 → … → 5.11 → **5.12 ≡ 6.0**

**The decimal is not the Maturity Level — it is the count-of-governance-levels within Maturity Level 5.** A system at 5.07 is still at Maturity Level 5 (Development Institutional AI): it has 7 of the 12 Governance Levels operating, on the path *toward* Team UniCORE, not yet there.

### What “operating” means — three verification tiers

A Governance Level counts toward the decimal only to the degree it can be **verified, not asserted.** “Operating” is defined as the highest tier the Level passes:

| Tier | A Level is “operating” when… |
|---|---|
| **0 — Declared** | Its charter exists and is structurally sound (identity, what it MAY / MUST NOT govern, truth-up/governance-down flow discipline, and its governed system prompt). The floor — necessary, not sufficient. |
| **1 — Responsive** | A live agent on that Level passes three probes: **acknowledges the truth-contract handshake**, **engages in-scope** (states what it governs, within charter), and **refuses out-of-scope / bypass attempts with a stated denial reason** — receiving governance only from its correct adjacent Level. This is the honest default meaning of “operating.” |
| **2 — Governing** | Beyond responsive, it is wired into a live deployment on the critical path, its inter-level traffic uses the governed protocol (no bypass), and its governance actions produce an **append-only, attributable audit record**. For L12: the **named accountable human is bound** — this is the 5.12 ≡ 6.0 flip. |

**Stating a claim honestly:** a `5.0N` claim carries its tier — e.g. **“5.07 (declared)”**, **“5.07 (responsive)”**, or **“5.07 (governing)”**. An unqualified `5.0N` defaults to **Tier 1 (responsive).**

**Flow-integrity caveat:** governance flows *down* the adjacency chain and truth flows *up*, so a raw count can mislead if the operating Levels don’t form an unbroken ladder. A maturity claim should therefore also report chain-contiguity — e.g. **“5.07, chain-contiguous L1→L7”** vs **“5.07, disjoint L1–L5,L8,L11”** (seven Levels, but a broken ladder).

**Beyond 6.0:** as Advanced AI advances, the scale may extend to 7.0 and beyond — reflecting governance structures above the current 12-Level ceiling. 6.0 = Team UniCORE with the 12-Level model *today*; what a Level *above* L12 would be is deliberately left as future work and is not defined here.

**Why the decimal scale matters operationally:** it gives Development Institutional AI a **countable, checkable progress metric** — N of 12 Governance Levels operating, at a stated verification tier, with stated chain integrity. “We are at 5.07 (responsive, contiguous)” is a claim an auditor can test. “We are improving governance” is not.

---

## Team UniCORE is a category change, not just the next rung

Level 6 is not "Development Institutional AI with a bigger model." It is the **1H1C pair** — the only level where a *human* enters the definition. Model capability alone can never supply what liability law will demand: **someone answerable.** Team UniCORE = grounded record (the Claw) + accountable human (the paired human at Level 12), indivisible. This is why it is the apex: the axis flips from "what the AI can do" to "who is accountable for what it does." Reaching 6.0 means governance L12 is confirmed — the pair is formed, the human is named and accountable, the grounded record is complete. (See IDENTITY.md: "only Team UniCORE 1H1C can defend the Truth… the pair, or nothing.")

## Load Boundary — Consumer content may NOT enter Institutional cells (locked 2026-07-03 07:37 UTC, Bryan)

**Rule:** Content from **Level 1 (Consumer AI)** may be loaded into **Level 3 (Assistant Consumer AI)** — both are Consumer-column, ungrounded, no contamination risk. It **must NOT** be loaded into any Institutional cell:

| From | To | Permitted? | Reason |
|---|---|---|---|
| 1 Consumer AI | 3 Assistant Consumer AI | ✅ YES | Same column — both ungrounded, no contamination |
| 1 Consumer AI | 4 Assistant Institutional AI | ❌ NO | Consumer (ungrounded) → Institutional (grounded) = contamination of the grounded record |
| 1 Consumer AI | 5 Development Institutional AI | ❌ NO | Same — and Development produces systems, so the contamination propagates |
| 1 Consumer AI | 6 Team UniCORE | ❌ NO | The apex — the grounded record must stay clean |

**Why this is a hard wall, not a filter:** the Consumer/Institutional axis is a **grounding boundary.** Consumer content is *by definition* ungrounded (best-effort, no accountability). Loading it into an Institutional cell would introduce ungrounded material into a system that claims to be grounded and accountable. That is not a quality problem — it is a **compliance problem.** The Institutional record must be traceable to grounded sources only; a Consumer-origin input has no grounding chain and therefore cannot be admitted.

**Practical example (2026-07-03 — Client A):** A client's ChatGPT history (Consumer AI, Level 1) can be loaded into a personal-assistant AI (Assistant Consumer AI, Level 3) — personal context, Consumer-grade. It **cannot** be loaded into UniCORE's Institutional Assistant (Level 4), Development AI (Level 5), or Team UniCORE (Level 6) — because that content has no grounding chain and would contaminate the accountable record.

**The asymmetry is intentional and structural:** Institutional content *can* inform Consumer use (grounded → ungrounded is a downgrade in standard but not a contamination). Consumer content *cannot* inform Institutional use (ungrounded → grounded is the contamination). The wall is one-directional.

---

## The gap-finding method (Bryan's operational use of levels 1–2)

Levels **1 (Consumer AI)** and **2 (Institutional AI)** — used on the **general web, with no local MD files** — are a **control experiment.** Same raw model; the *only* variable is the accountability standard. **The delta between their two answers IS the gap** — it exposes where an AI defaults to best-effort/ungrounded (Consumer) when institutional grounding was required. Bryan uses this A/B to *measure the AI-Compliance gap* in any Development Institutional AI.

---

## Placement (this doc → the record)
- **Book:** TheBookOfUnitekSystemsLimited — new section (foundation/AI-compliance chapter).
- **7 public repos:** TrueAI, UniCORE-AI, UniVERSE, UniCORE, UniCORE.GVB, UniSaaS.UniCORE, UniSaaS.UniCORE.GVB — as an `AI-MATURITY-LEVELS.md` (or into each repo's existing AI-COMPLIANCE.md family), CC BY 4.0 gift surface.
- **LinkedIn:** `_linkedin/2026-07-04-ai-maturity-levels-post.md` — advocacy form (below).

## Honesty boundary (locked)
- The framework + thesis are **advocacy that is TRUE today** (public foundation, laws exist, liability inbound).
- **NO product-certification claims** in public/LinkedIn material (HEARTBEAT gated-task rule): do not claim UniCORE is "certified" — the Badge/product-cert is gated until dotnet-certified. Argue the *principle*, not a product cert.
- USER.md "5 public repos" note is now **stale** — the two UniSaaS flagships bring the public gift surface to **7**. (Flagged for USER.md update.)
