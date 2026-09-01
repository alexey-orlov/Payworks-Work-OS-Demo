---
initiatives: [initiative-slug]
features: []
---

# Product Brief Template

> **House format.** Derived 2026-08-30 from three real filled VP Product Briefs, the Product
> Development Workflow SOP (Chat 1 — the 8-section brief, KPI tier structure, Product
> Leadership Approval gate) and the Terminology Proposal (the 8 named sections, the
> Initiative / Value Package / Milestone hierarchy). This file is the document contract:
> section order, meta fields, table shapes and voice come from here.
>
> **File name and location.** Keep the machine name: copy to
> `PRDs/{area}/{initiative-slug}-product-brief.md` — one per initiative, edited in place. `{area}` is the
> module the initiative primarily serves. Fill the frontmatter above — `initiatives:` carries
> exactly one slug, bare kebab-case in a one-item list (`initiatives: [payment-links]`); link
> contract: `governance/link-schema.yaml`. For guided drafting run `/product-brief-draft`; it reads this
> file fresh every run.
>
> **`[ORG]`.** The token in the banner and the footer — replace both with the company name
> exactly as it appears in `strategy/business-context/business-info.md`.
>
> **Two levels, one format.** A **Product Brief** scopes the Initiative — the parent strategic
> effort that closes only when all its Value Packages have shipped or it is deprioritized. A
> **VP Product Brief** scopes one Value Package — the shippable, client-facing release inside
> it. Same sections, same order; set the **Level** row in the meta table and write at that
> altitude. Most briefs in practice are VP Product Briefs.
>
> **Length.** Start short and grow with the bet. A first brief at direction-setting is
> 300–500 words. The brief that goes to Product Leadership Approval is 1500–2000 words.
> Expand as you learn, not before. Detail that outgrows a section moves to the Appendix.
>
> **Voice.** Plain language, grade-6 reading level. Real numbers with their source, or an
> explicit TBD — never an adjective standing in for a measurement. Personas by role, never by
> individual name (the Author row is the one exception). Date everything (YYYY-MM-DD).
> No UI prescriptions — screens, buttons and layout are Design's to decide.
>
> **Honest unknowns.** The house writes them out loud: "TBD — baseline to be established
> post-launch", "pending confirmation with the team", "owned by Data/Engineering; timing to be
> determined". Pair each with the OS marker so automation can age it:
> `[GAP: what's missing — how to close it]`. `/wiki-lint` ages these and
> `/feature-launch-gate` blocks a launch while any remain.
>
> `>` blockquotes are guidance to the drafting agent — never emitted into the document.

---

PRODUCT BRIEF  |  [ORG]

# [Product / module] — [Release]

[One line: the value this release delivers, in the customer's own terms.]

| Field | Detail |
|-------|--------|
| **Product / module** | [module this sits in] |
| **Level** | Product Brief (Initiative) / VP Product Brief (Value Package) |
| **Initiative** | [name — link to `product/initiatives/{slug}.md`] |
| **Release** | [Value Package, and Milestone if the VP ships in parts — e.g. VP2, M1] |
| **Availability** | [how a customer gets it — automatic, on invite, opt-in, feature-flagged] |
| **Eligible users** | [who qualifies, and the count behind it] |
| **Pricing** | [included at no cost / paid tier / usage-based] |
| **Author** | [name, role] |
| **Date** | [YYYY-MM-DD] |
| **Status** | Draft / In review / Approved (Product Leadership) / Shipped |
| **Links** | [Breadth Prototype]() · [Depth Prototype]() · [Dev-Ready Prototype]() · [Micro Jobs Breakdown]() · [Telemetry]() · [Dashboard]() |

> **Meta rules.** Every row gets a value or an explicit TBD — a blank row reads as an
> oversight. **Availability**, **Eligible users** and **Pricing** are house-required and rarely
> live in the repo: `/product-brief-draft` asks for them at intake. **Status** lives here, never in the
> frontmatter (that carries links only). It reads `Draft` on creation and moves to `Approved
> (Product Leadership)` only when VP, Product Management and Senior Manager, Product
> Management have signed off — the gate that must clear before Micro Jobs are written. Every
> status move gets an Appendix changelog row and a bumped **Date**.
>
> **Links** carries one entry per artifact that exists; no artifact yet → `None yet` +
> `[GAP:]`, never an empty link — a `[Name]()` reads as filled and points nowhere.
>
> **One date, two places.** **Date** is this brief's last-updated date — it is the row
> `/product-brief-draft` calls **Last Updated** — and the footer's `Updated [YYYY-MM-DD]` carries the
> same value. Bump the two together; they must never disagree.

---

## 1. OVERVIEW

[Two paragraphs. What this release is, what came before it, and what changes because of it.
Name the prior release and what it established, then what this one adds. Close on the
one-sentence statement of what the product becomes.]

> The house opener is comparative: "[prior release] gave [users] X. [This release] adds Y."
> It orients a reader who has never seen the initiative before. No evidence here — this is
> the summary; §2 carries the proof.

---

## 2. PROBLEM STATEMENT

**[Name the problem in a short declarative heading]**

[What is broken or missing today, in the user's world. Two to three paragraphs. Where the
problem has more than one strand, use a numbered breakdown — "This creates three compounding
problems. First… Second… Third…" — so each strand can be traced to a solution element later.]

**How often, and what it costs**

- **Frequency** — [how often it bites, as a number with its source. "Often" is not a frequency;
  unsourced, it carries `[GAP:]`.]
- **Criticality** — [what it costs when it hits — time, money, risk, churn — with its source.
  "Significant" is not a cost; unsourced, it carries `[GAP:]`.]

**The current workaround**

[What people do about it today — the manual process, the competitor, the spreadsheet, or
nothing-and-suffer. This is what the solution must beat, and §6 has to say why it does.]

**Who feels this most**

- [Persona / segment] — [how the pain shows up for them]
- [Persona / segment] — [how the pain shows up for them]
- [Internal team, when they absorb the cost] — [what they absorb]

**The trigger moment**

[The specific moment the problem bites — a user is in this situation, trying to do this, and
hits this wall. One paragraph, concrete and dateable. Name what changes in that same moment
once this ships.]

**Evidence**

- [A quote, a number or a volume — and where it came from: research synthesis, call summary,
  support tickets, analytics query.]
- [Second source.]
- [Third source. The readiness bar is 3 or more customers or sources; with fewer, say how many
  you have and carry `[GAP:]` — never pad the list.]

> **Slot routing** — `/product-brief-draft` problem-side: problem, frequency (how often it bites, with
> the source), criticality (what it costs when it hits), today's alternative, and the
> supporting evidence — real quotes and numbers from `user-insights/`, call summaries, and
> support volume. Segment sizing belongs in §3, not here. "Often" is not a frequency and
> "significant" is not a cost: an unsourced claim carries `[GAP:]`.
>
> Every Problem Statement traces to a validated opportunity on the Opportunity Solution Tree,
> and the SOP's readiness bar wants evidence from 3 or more customers or sources — a brief
> resting on one complaint is not ready for Product Leadership Approval. Where a Problem
> Statement is written in the structured form, use the house sentence:
> *"When I [situation], I want to [motivation], so I can [expected outcome]."*

---

## 3. CUSTOMER & MARKET CONTEXT

**Target users**

[Who this is for, by role — with the account count and ARR behind the segment, from
`strategy/business-context/segmentation-matrix.md`. "Everyone" is not a segment.]

**How they work today**

[The workflow this release sits inside — the volume they handle, the tools they hold open,
what a heavy day looks like. Enough that a designer can picture the desk.]

**Design Partners**

[The 3–5 named external clients co-creating this initiative — who they are by role and
profile, what they have already seen (Breadth Prototype, prior release), and the standing
cadence. Name what they have shaped so far and what is still going to them. Distinct from
Early Access participants: Design Partners commit to the co-creation calls and shape the
roadmap. None engaged yet → say so and carry `[GAP:]`.]

**Competitive landscape**

[What comparable products do about this problem — from `product/competitive-research/`.
Name where the market is at parity, where a competitor is ahead, and where this release goes
further. Competitor claims are researched, not assumed: an unverified one carries `[GAP:]`.]

| Capability | Us today | [Competitor] | [Competitor] | After this release |
|------------|----------|--------------|--------------|--------------------|
| [capability] | [state] | [state] | [state] | [state] |

> The SOP's readiness bar expects 3–5 competing products reviewed before the brief is drafted.
> No research yet → omit the table and carry the `[GAP:]` in the prose; a competitor name you
> have not checked is an invention, and an empty matrix row reads as a finding.
> Findings feed §6 (Proposed Solution) and §9 (Key Decisions) — the differentiation argument
> lives there; this section is the evidence base for it. Deep-dive: `/competitor-analysis`.

---

## 4. BUSINESS GOALS & USER OUTCOMES

**North Star**

[One sentence: what is true for the customer and for the business when this has worked.]

**Business goals**

- [What the company is trying to achieve — measurable, not aspirational. Say why now, not later.]
- [Second goal.]
- [Third goal.]

**User outcomes**

- [What a user can do after this ships that they could not do before — per persona named in §2.]
- [Second outcome.]

**Strategy fit**

[Which strategic bet or pillar this serves, and why this release is the right expression of it
now. Ties to `product/strategy/current-quarter.md`.]

**Hypothesis**

If we [build X], then [Y metric] will [change by Z], because [assumption about behavior].

**Key hypotheses** — the beliefs this bet rests on; full inventory in
[`reviews/{initiative-slug}-assumption-map.md`](reviews/{initiative-slug}-assumption-map.md).

| Hypothesis | Risk lens | Confidence | Validation route | Priority |
|------------|-----------|------------|------------------|----------|
| [falsifiable statement — one observation could break it] | Desirability / Viability / Feasibility / Usability | High / Med / Low | [cheapest probe that moves the belief, and who runs it] | 1 |

> At most five rows, ranked. Rows come FROM `/assumption-map` — it owns surfacing, rating and
> ranking; this table is the headline, never the method. Import its **Test First** rows first,
> then its *kill criterion + monitor* rows until you reach five. Priority is the validate-first
> rank (1 = validate first), not a scope tier. No map yet → one row per hypothesis you can
> state, each carrying `[GAP: unranked — run /assumption-map]`. Lens vocabulary: the map's
> **Value** category is **Desirability** here; an initiative-mode map adds Ethics,
> Go-to-Market, Strategy & Objectives and Team & Org, which keep their own names.

**Impact by lever**

| Lever | Primary? | Estimate | Basis |
|-------|----------|----------|-------|
| Acquisition | yes / no / not this bet | [new accounts / conversion Δ] | [source or `[GAP:]`] |
| Activation | yes / no / not this bet | [Δ in reaching value] | [source or `[GAP:]`] |
| Retention | yes / no / not this bet | [ARR retained] | [source or `[GAP:]`] |
| Expansion / LTV | yes / no / not this bet | [ARR added] | [source or `[GAP:]`] |
| Cost to serve | yes / no / not this bet | [cost avoided] | [source or `[GAP:]`] |

> Name **at most two primary levers**; mark the rest "not what this bet is for." Each named
> lever needs a number built as *reach × baseline × expected change* (method:
> `/impact-sizing`). A lever with no baseline gets a `[GAP:]`, never a guess.

---

## 5. KPI FRAMEWORK

> The three-tier structure, per the SOP. **Tier 1 — Outcome Metrics:** the business result,
> what leadership cares about most. **Tier 2 — Product Metrics:** how clients use the feature —
> adoption and engagement. **Tier 3 — Quality Metrics:** how well it works — stability and
> performance. **Every tier carries at least one metric** — an empty tier is a `[GAP:]`, not a
> blank row, and Product Leadership Approval expects all three populated with a baseline data
> source named wherever one exists.
>
> Vetted definitions live in `analytics/metrics/{area}/` via `/feature-metrics` — link, don't
> restate. Where the team has recorded its own tier names in `business-info.md` → Metric
> Reporting Conventions, those win over the labels below.

**Tier 1 — Outcome Metrics** (the business result)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| [metric] | [value (source), or TBD — how the baseline gets established] | [goal] | [Day 30 / Day 90 / 2 quarters post-launch] | Leading / Lagging |

**Tier 2 — Product Metrics** (adoption and engagement)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| [metric] ★ | [value (source), or TBD — how the baseline gets established] | [goal] | [when] | Leading / Lagging |

**Tier 3 — Quality Metrics** (stability and performance)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| [metric] | [value (source), or TBD — how the baseline gets established] | [acceptable range] | [when] | Leading / Lagging |

★ = the primary metric for this release.

**Guardrails** (must not harm)

- [Metric — behavioural, quality or cost] must not [rise / fall] past [threshold, or "TBD — who
  sets it and when"] — watched at [checkpoint or dashboard]
- [Second guardrail.]

**Kill metrics**

- [Metric] below [threshold, or "TBD — who sets it and when"] at [checkpoint] → [what we
  diagnose, and what we do about it]
- [Metric] below [threshold, or "TBD — who sets it and when"] at [checkpoint] → [what we
  diagnose, and what we do about it]

**Checkpoint schedule**

| Checkpoint | What we're checking |
|------------|---------------------|
| Day 7 | [critical defects? is the entry point working? early signal?] |
| Day 30 | [first adoption read against target] |
| Day 60 | [engagement and satisfaction read] |
| Day 90 | [business outcome read] |

**Prior-release baseline (reference)**

| KPI | Result | Type |
|-----|--------|------|
| [metric carried over from the previous release, and where it landed] | [value] | Leading / Lagging |

> Include this block whenever a prior release set the benchmark this one is measured against.
> When targets genuinely cannot be set yet, say so in the house form — "TBD — baseline to be
> established post-[prior release] launch" — and pair it with `[GAP:]` naming who sets it and
> when. A guessed target is worse than an honest TBD.
>
> **Slot routing** — `/product-brief-draft` proof-side: success metrics with baselines and targets,
> guardrails (the **Guardrails** block above — a guardrail can be behavioural, not only
> stability or performance, so it need not be a Tier 3 KPI), and kill criteria (the kill
> metrics above). Experiment-specific metric validity: `/experiment-metrics`.

---

## 6. PROPOSED SOLUTION

**How it works**

[Two paragraphs. What is being built and how a user meets it — capability and intent, no
layout, no components, no copy. Where a surface is being extended rather than created, say
what it does today and what changes.]

**Feature set**

| Feature | Description |
|---------|-------------|
| [name] | [what it does and what it changes for the user — one to three sentences] |

> When the release spans more than one surface, group the table by surface with a subheading
> each ("Feature set — [surface]"), the way the house writes multi-surface releases.

**Why this beats the current workaround**

[The workaround named in §2 — when and for whom this wins over it, and where it doesn't. An
honest "doesn't win here" is stronger than a claim that it always does.]

**Access & eligibility**

- [How access is granted — automatic, invite-triggered, admin-enabled, flagged]
- [What a user must have or be to qualify]
- [What users outside the criteria see — nothing, a read-only view, or an explanation]

**Alternatives considered**

- [Option we evaluated and rejected] — not doing it because [reason]
- [Option we evaluated and rejected] — not doing it because [reason]

> These are options *we* rejected. The customer's current alternative is §2's workaround —
> keep the two apart; conflating them hides the competitive argument. Not §9 either: that
> section records the calls we *made* and the live tradeoffs they carry, while this is the
> shortlist of whole approaches evaluated and dropped, leaving nothing to manage.

### AI Behavior Contract

> **This sub-section only for AI/ML features** — delete it otherwise, and drop it in place of
> the flow description when the contract covers the same ground. Full guidance:
> `.claude/skills/product-brief-draft/reference/ai-product-brief.md`.

| Dimension | Specification |
|-----------|--------------|
| **Primary task(s)** | summarize / extract / classify / generate / route |
| **Inputs available** | [fields, context, tools, sources] |
| **Constraints and guardrails** | [voice, privacy rules, compliance] |
| **Disallowed** | [PII echo, policy violations, jailbreak classes] |
| **Params (if fixed)** | temperature, max tokens, tool-call policy |
| **Latency budget** | P50: [X]ms / P95: [Y]ms |

| Scenario | Input | Expected output | Rejection criteria |
|----------|-------|-----------------|--------------------|
| Happy path | [example] | [what should happen] | N/A |
| Edge case | [example] | [graceful handling] | N/A |
| Should reject | [example] | [refusal] | [why] |

---

## 7. SCOPE & BOUNDARIES

**In this release**

- [What ships — one line per element, matching a row of §6's feature set]

**Scope boundary — documented but not included**

- [Item] — [why it is out, and where it goes instead: a named future release, or "deliberately never"]
- [Item] — [why it is out, and where it goes instead]

**Tradeoffs accepted**

- [What we are knowingly giving up, and what we get for it]

> **Exception List.** The scope boundary above is the brief-level statement. The build-level
> Exception List — one entry per locked Micro Job, each naming the excluded item and why —
> is assembled as Micro Jobs lock and travels in the Dev-Ready Bundle. It lives with the
> Micro Jobs Breakdown, not here; this section is what it must stay consistent with. When in
> doubt about whether something is in scope, the house default is the Exception List: it is
> easier to add scope later than to manage scope creep mid-build.
>
> **Slot routing** — `/product-brief-draft` solution-side: scope boundary and non-goals. Keep non-goals
> specific and each one reasoned; a bare list of exclusions tells a builder nothing.

---

## 8. USER EXPERIENCE PRINCIPLES

**[Principle as a short declarative sentence.]**

[One paragraph of reasoning. What the principle rules in, what it rules out, and — the house
formulation — what it means when the product violates it: "if [X happens], that is a product
gap, not an expected workflow."]

**[Second principle.]**

[Reasoning.]

**[Third principle.]**

[Reasoning.]

> Three to five principles. They are the standing arbitration rules for the hundred decisions
> the brief will never mention — Design and Engineering read them when this document does not
> answer their question. A principle that could not be violated is not a principle; each one
> should rule something out. Performance and consistency-with-an-existing-surface are
> legitimate principles here, not just experience ones.

---

## 9. KEY DECISIONS & TRADEOFFS

**Decisions made**

**[The decision as a claim sentence.]**  [Why it was made, what was considered instead, and
what evidence or review settled it. Where a decision reversed an earlier direction, say what
the original model was and what changed.]

**[Second decision.]**  [Rationale.]

**Tradeoffs**

- [What the decision costs, who feels that cost, and under what condition we would revisit it.]

> A decision worth recording names the option not taken. Decisions that will outlive this
> brief also get filed with `/decision-log-entry` into `product/decisions/` — this section is
> the release-scoped summary, that folder is the durable record. Competitive findings from §3
> belong in the rationale here.

---

## 10. OPEN QUESTIONS, RISKS & DEPENDENCIES

**Open questions**

- [ ] [Question] — @[owner] — [how it gets answered, and by when]

**Risks**

**Risk — [short name].**  [What could go wrong and what it would cost.] **Mitigation:** [what
reduces it, who owns that, and what we watch to know whether it worked.]

**Risk — [short name].**  [Description.] **Mitigation:** [action.]

**Dependencies**

- **[Dependency]** — [what it is and what it blocks]. Owned by: [team, or TBD — who confirms
  the owner and by when]. Required by: [release or date, or TBD — what pins it]. [Interim
  workaround, if there is one.]

> Every dependency names an owner and a required-by, or an explicit TBD naming who confirms
> each — an unowned, unmarked dependency is a hope.
> `/product-brief-challenge` writes its ranked unverified assumptions into **Open questions** with owners
> and next research steps; those are questions, not beliefs — standing beliefs live in §4's
> Key hypotheses table.

---

## 11. ROLLOUT & ITERATION PLAN

**[This release] — [timing, or "date TBD" with what it waits on]**

- [Rollout shape — broad release, phased, incremental per Micro Job as each completes]
- [Who gets it and when]
- [Configuration required, or explicitly none]

**Launch conditions**

- [ ] [What must be true before this ships — QA complete, a specific behavior tested and verified, comms plan in place, a monitoring and escalation plan agreed]
- [ ] [Second condition]

**[Next release] — [theme]**

- [What is already known to be deferred here, and what will inform its scope]

**Future expansion**

[Where this could go beyond the current customer set or use case — the extension paths the
architecture already allows. Directional, not committed.]

> Phased rollouts get a table: Phase | Audience | Duration | Pass criteria. Where Design
> Partners see it before general availability, say so here and name what their feedback gates.
> Launch conditions are the brief's half of the gate; the filled checklist and the gate record
> live in `product/launches/` via `/launch-checklist` and `/feature-launch-gate`.

---

## 12. APPENDIX

**Changelog**

| Date | Change | Who |
|------|--------|-----|
| [YYYY-MM-DD] | [what changed] | [name] |

**Impact sizing detail** (the funnel behind §4's reach numbers)

| Funnel stage | Users | Drop-off reason |
|--------------|-------|-----------------|
| Sees it | [number] | — |
| Eligible | [number] | [reason] |
| Engages | [number] | [friction] |
| Completes | [number] | [friction] |

**Source material**

- [Where the evidence in this brief came from — research syntheses, call summaries, competitive teardowns, analytics queries]

---

[ORG] Confidential  |  Updated [YYYY-MM-DD]

---

## Product Brief Quality Checklist

> **Template file only** — delete this section, with the comment block below it, when filling
> a copy. It is the standing bar, not part of the brief.
>
> The single quality checklist — `/product-brief-draft` checks against it before presenting a draft; use
> it yourself before sharing. Check the items that apply at your current status. An item
> satisfied by an explicit TBD + `[GAP:]` counts as checked at every gate before Product
> Leadership Approval — that gate is where the TBDs have to be real answers.

### Every draft (hygiene)

- [ ] Saved as `PRDs/{area}/{initiative-slug}-product-brief.md`, frontmatter names exactly one initiative
- [ ] Registered: folder CLAUDE.md row appended; catalog entry proposed for a new feature or module; initiative page created or updated
- [ ] Meta table complete — Level, Availability, Eligible users, Pricing all answered or explicitly TBD
- [ ] Length matches the gate you are heading into (see Length at the top); overflow moved to the Appendix
- [ ] Every thin section carries `[GAP:]`, not silence
- [ ] Plain language, grade-6 reading level; no UI prescriptions; personas by role
- [ ] Dated inside and in the changelog

### Before it goes for review

- [ ] Problem stated in 2–3 sentences: who has it, what the pain is, what it costs them
- [ ] Evidence from 3 or more customers or sources — not a single complaint
- [ ] Segment named with account count / ARR behind it
- [ ] Frequency and criticality stated with a source
- [ ] The current workaround described — this is what §6 must beat
- [ ] 3–5 competing products reviewed; the differentiation claim is grounded
- [ ] Hypothesis is testable ("If we… then… because…")
- [ ] Key hypotheses table filled — lensed, rated, routed, ranked (or `[GAP:]`-marked)
- [ ] At most two primary impact levers named; the rest marked "not this bet"
- [ ] Every business goal is measurable

### Before Product Leadership Approval

- [ ] All sections complete — no placeholder sections remaining
- [ ] KPI Framework populated across all three tiers, each metric with a baseline source or an explicit TBD and a named owner for setting it
- [ ] Kill metrics defined — would the team actually act at these thresholds?
- [ ] Scope boundary explicit, each exclusion reasoned and routed
- [ ] Every risk carries a mitigation; every dependency an owner and a required-by
- [ ] Launch conditions listed and testable
- [ ] Decisions record what was considered and rejected
- [ ] `/product-brief-challenge` run; its ranked assumptions sit in §10 with owners

### Before the Micro Jobs are written

- [ ] Product Leadership Approval recorded (Status + changelog row)
- [ ] Every planned Micro Job traces to a validated opportunity and to a Problem Statement in §2
- [ ] §7's scope boundary is stable enough for the Exception List to be built against it
- [ ] No `[GAP:]` markers remain in §§2, 5 or 7

<!--
Template rules (template file only — delete this comment when filling a copy):
- Living doc: edit in place, bump Date and add a changelog row. Challenge reports live in
  `PRDs/{area}/reviews/`, never inside this file.
- The section order is the reading order Design and Engineering rely on: overview → problem →
  who and market → goals → measures → solution → scope → principles → decisions → risks →
  rollout. Don't re-order per release.
- Section-name map, for anyone tracing the SOP's 8-section brief through this file:
  Problem Statement §2 · Business Goals §4 · Customer & Market Context §3 ·
  Proposed Solution §6 · Scope & Boundaries §7 · Key Decisions §9 · KPI Framework §5 ·
  Open Questions & Risks §10. §1, §8 and §11 are house additions the real briefs all carry.
- A Milestone (M1, M2) inside a large Value Package does not get its own brief — it is named
  in the Release row and scoped in §7 and §11.
-->
