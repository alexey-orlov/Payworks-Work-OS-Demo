---
initiatives: [initiative-slug]
---

# Micro Jobs Breakdown Template

> **House format.** Derived 2026-08-30 from a real filled Jobs-to-be-Done document and the
> dependency structure of the Micro Job set it produced, the Product Development Workflow SOP
> (Chat 2 — 3–5 validated Micro Jobs, the four pressure tests, riskiest-assumption sequencing,
> the PM pipeline rule, the Exception List) and the Terminology Proposal (Initiative → Value
> Package → Milestone → Micro Job; Problem Statement). This file is the document contract:
> section order, table shapes and status vocabulary come from here.
>
> **File name and location.** Keep the machine name: copy to
> `PRDs/{area}/{initiative-slug}-micro-jobs-breakdown.md` — the `-micro-jobs-breakdown.md` suffix is how the
> repo finds it (`governance/link-schema.yaml`). One breakdown per initiative, edited in place
> as Micro Jobs get drafted, locked and handed off. Fill the frontmatter above. For guided
> creation run `/micro-jobs-breakdown`; it reads this file fresh every run.
>
> **What this document is.** The cut — one Value Package broken into independently shippable
> Micro Jobs, sequenced riskiest assumption first. It sits between the Product Brief (why this
> bet) and the per-job Micro Job specs (`/micro-job-draft` — the buildable contract). The job
> table is the live status board: it is where anyone looks to see what is drafted, what is
> locked, and what has gone to the BA.
>
> **How many.** 3–5 Micro Jobs per Value Package. Fewer usually means the cut is too coarse to
> ship incrementally; more usually means the Value Package should be split across Milestones.
>
> **Voice.** Plain language, grade-6 reading level. Personas by role. Date everything
> (YYYY-MM-DD). Every priority states its reason in dependency or risk language — never a bare
> Must or Should. Honest unknowns written out loud and paired with
> `[GAP: what's missing — how to close it]`.
>
> `>` blockquotes are guidance to the drafting agent — never emitted into the document.

---

MICRO JOBS BREAKDOWN  |  [ORG]  |  [Product / module] [Release]

# [Value Package] — Micro Jobs Breakdown

[One line: what this Value Package delivers, and the logic of how it is cut.]

| Field | Detail |
|-------|--------|
| **Product / module** | [module] |
| **Initiative** | [name — link to `product/initiatives/{slug}.md`] |
| **Release** | [Value Package, and Milestone if the VP ships in parts] |
| **VP Product Brief** | [link] |
| **Micro Jobs** | MJ-01, MJ-02, MJ-03… |
| **Author** | [name, role] |
| **Date** | [YYYY-MM-DD] |
| **Status** | Draft / Agreed / Handed off |

**Evidence key:** `[Evidenced]` source named · `[Partial]` signal, not proof · `[Hypothesis — needs validation]`

---

## 1. THE BACKBONE

> The Value Package's end-to-end story as users live it — activities left to right, every actor
> named (including out-of-scope personas), core objects listed. Rebuilt from the Product Brief
> and its evidence — interview quotes, current-state facts, code answers — never invented. This
> is the seam the Micro Jobs are cut from; every job below traverses part of it.

**Actors:** [everyone who touches this flow, including out-of-scope personas]
**Core objects:** [the nouns — each needs its lifecycle verbs in some Micro Job]
**Flow:** [activity] → [activity] → [activity] → [the loop closes: outcome lands]

---

## 2. PROBLEM STATEMENTS THIS VALUE PACKAGE ADDRESSES

> One block per Micro Job, in the order the jobs ship. Each block opens with the root cause —
> **why this job exists**, in the user's world, with current-state facts — then gives the
> Problem Statement per persona in the house sentence form, then the four reads below. Every
> claim carries an evidence label; a persona with no evidence behind it is a
> `[Hypothesis — needs validation]`, not a fact. With no evidence at all, name the persona,
> attach the GAP, and leave the block empty — do not write a labelled sentence you made up.
> A labelled guess is still a guess.
>
> This section is where the breakdown earns its keep: it is the evidence base Design reads
> before deciding how anything should work, and the reason each Micro Job survives the
> Before/After pressure test. A job with no Problem Statement here is not ready to be cut.
>
> Name the provenance behind each label: Design Partner co-creation calls, customer interviews,
> support volume, analytics. `[Evidenced]` means a source can be named — "three customers said
> this independently", not "we believe".

### MJ-[NN] — [Micro Job name]

**Root cause — why this job exists**

[What is broken or missing today, and what happens to people because of it. Where the
capability or data already exists somewhere in the product, say so — the job is then surfacing
an existing signal in the right place, not building new detection.]

**[Persona]**

When I [situation], I want to [motivation], so I can [expected outcome].

- **Functional:** [what they must be able to do] `[Evidenced]` · [second capability] `[Partial]`
- **Social:** [how it changes how they are seen — or "none — this is an internal workflow job"] `[Evidenced]`
- **Emotional:** [what they feel about it today, and how strongly] `[Partial]`
- **Top pain:** [the single worst part of today] `[Evidenced]`

**[Second persona, when a second one has a distinct job]**

When I [situation], I want to [motivation], so I can [expected outcome].

- **Functional:** … · **Social:** … · **Emotional:** … · **Top pain:** …

**[The business, when it carries a cost of its own]**

[What the current state costs internally — support volume, compliance exposure, manual work
that should never require a person. Name the success condition in the same breath.]

**Note on scope / direction**

[The thing a builder would otherwise get wrong: what this job deliberately does not do, why a
signal navigates rather than resolves, why a state is session-only, why an action is
irreversible, or that a data source already exists and must not be re-implemented.]

---

## 3. THE MICRO JOBS

> One row per Micro Job. **Type:** Integration (existing components surfaced or connected —
> feasibility verification is the critical path) · Net new (new objects or flows — earns a
> full-depth spec) · Enhancement (existing behavior changed). Type comes from what the code
> actually does, not from hope. **Priority** carries its reason in dependency or risk language
> ("Must ship first — MJ-02 and MJ-03 depend on [surface] being live"), never a bare label.
> **Status:** `not-drafted` → `drafted` → `agreed` → `handed-off`; a Won't-now job rests at
> `deferred`. ("Locked" is the house word for `agreed`: all four pressure tests passed and the
> PM agreed the spec.) Link each drafted spec from its row.

| ID | Micro Job | Type | Riskiest assumption it tests | Depends on | Priority — why | Effort | Status |
|----|-----------|------|------------------------------|------------|----------------|--------|--------|
| MJ-01 | [name] | [type] | [assumption] | — | Must ship first — [what depends on it] | [Eng to confirm] | not-drafted |
| MJ-02 | [name] | [type] | [assumption] | MJ-01 | [reason, and whether it can run parallel to another] | [Eng to confirm] | not-drafted |

> **Effort** is Engineering's number, not the PM's — the column carries `[Eng to confirm]` until
> they fill it. A high-risk job (irreversibility, money, privacy) says so in its Priority cell
> so the extra QA time is planned, not discovered.

---

## 4. SEQUENCING RATIONALE

> **Riskiest assumption first — not by feature area, user-journey order, or what feels most
> logical.** The goal is to surface the most uncertain decisions early, so they can be resolved
> before they become build blockers. Say why this order and not another.

**The walking skeleton:** [which job goes first and why — the thinnest path across the whole
backbone, minimum at every station, loop closed. Where the riskiest capability mechanically
depends on a prior loop being live, the skeleton ships first as the smallest cut that unblocks
it, and the risky job scopes to the seam. Riskiest-first means the risk is *reached* fastest,
not that its job jumps its dependency.]

**What can run in parallel:** [which jobs are independent once their shared dependency is live]

**What must wait, and why:** [the sequencing constraints that are real, with the reason]

**Pipeline commitment:** the PM stays 1–2 Micro Jobs ahead of Engineering at all times (or 2–3
sprints, whichever is greater) — fully specified and prototype-ready. If that cadence slips,
escalate to Product Leadership rather than letting the build run dry.

> Sequencing is discussed with the BA and the Designer before the order is locked. A sequencing
> claim with no evidence behind it is marked `[Hypothesis — needs validation]`.

---

## 5. PRESSURE TEST RESULTS

> All four tests must pass before a Micro Job is locked. Record the verdict here so the whole
> cut can be audited at a glance; the reasoning lives in each spec. A job failing the same test
> three or more times is a scoping problem — re-cut it, or flag it with the PM Lead.

| Micro Job | Before/After | Standalone | Vertical/Horizontal | Scope sanity | False thin slice | INVEST | Verdict |
|-----------|--------------|------------|---------------------|--------------|------------------|--------|---------|
| MJ-01 | Pass / Fail | Pass / Fail | Pass / Fail | Pass / Fail | Pass / Fail | Pass / Fail | Cut stands / Locked / Re-cut — [why] |

> **Verdict vocabulary:** `Cut stands` — the gates pass and the cut holds, but the spec is not
> yet drafted or agreed (the normal state at first cut). `Locked` — all gates passed AND the PM
> agreed the spec. `Re-cut` — a gate failed; say which and why. Never mark a job `Locked` at
> first cut just because its gates pass.

> Common failures, so a re-cut targets the real problem: **Before/After** — too vague to
> describe a meaningful change in capability. **Standalone** — depends on a job that has not
> been defined. **Vertical/Horizontal** — too broad; the work belongs in several specs.
> **Scope sanity** — a whole Value Package disguised as one job, or so small it delivers no
> value on its own. A variation whose backbone differs end to end becomes its own Micro Job —
> never a footnote inside someone else's.

---

## 6. CROSS-JOB DECISIONS & OPEN QUESTIONS

> Decisions that span Micro Jobs — shared objects, shared states, who owns a boundary — and
> questions no single spec can settle. Each one has an owner and a by-when. Settled ones move to
> `product/decisions/` via `/decision-log-entry` and stay linked from here.

| # | Decision / question | Affects | Owner | Needed by | Status |
|---|---------------------|---------|-------|-----------|--------|
| 1 | [question] | MJ-[NN], MJ-[NN] | [name/role] | [job or date it blocks] | Open |

> Also lands here as owned rows: **context gaps** carried in from the platform model and tech
> constraints (the health check the breakdown starts from), **end-to-end variations considered
> but not cut into their own Micro Job** (say which, and why they stayed inside one), and any
> §7 coverage item recorded as unresolved.

---

## 7. COVERAGE CHECK

> Every scope item in the VP Product Brief lands in a named Micro Job above (or an explicitly
> reasoned split), or is named here as explicitly out — with why, and where it goes instead (a
> future Micro Job, a later Value Package, or "deliberately never"). Nothing silently dropped,
> and nothing forced into a job just to make the list look clean: an item with no home yet is
> recorded as unresolved with an owner, never invented into a destination. The explicitly-out
> rows are the seed of the Exception List that travels in the Dev-Ready Bundle.

- **Covered:** [Product Brief scope item] → MJ-[NN]
- **Covered, split:** [item] → MJ-[NN] ([part]) + MJ-[NN] ([part]) — [why the split]
- **Explicitly out:** [item] — [why] — [future Micro Job / later Value Package / never]
- **Unresolved — no home yet:** [item] — no Micro Job covers it and no destination is decided — owner: [name], see §6 #[n]

**Exception List status:** [one entry per locked Micro Job — where it stands, and who is still
owed rows. The PM initiates; the BA extends it with implementation-level exceptions during the
deep dive.]

---

**Quality gate** (checked by `/micro-jobs-breakdown` before presenting; recheck on manual edits):

> A box that cannot honestly be true yet stays unchecked, with its reason and an owner beside
> it. An unchecked box blocks *locking*, not filing — a first cut with a genuinely undecided
> scope item is a real breakdown, not a failed one. Never check a box to make the gate look clean.

- [ ] 3–5 Micro Jobs — fewer means the cut is too coarse, more means the Value Package should be split across Milestones
- [ ] Every Micro Job passes the four pressure tests, recorded in §5 (checklists: `.claude/skills/micro-jobs-breakdown/references/gates-and-cuts.md`)
- [ ] No false thin slice: the first job traverses the backbone end to end and reaches an outcome
- [ ] Every job in §3 has a Problem Statement block in §2, with evidence labels on its claims
- [ ] Every job traces to a validated opportunity — no Micro Job, and no prototype, without one
- [ ] Every priority states its reason in dependency or risk language
- [ ] Effort cells carry `[Eng to confirm]` or Engineering's own number — never a PM estimate
- [ ] Coverage check is clean — every Product Brief scope item covered or explicitly out, with where it goes
- [ ] A variation whose backbone differs end to end became its own Micro Job, not a footnote in another
- [ ] High-risk jobs (irreversibility, money, privacy) are flagged in their Priority cell so extra QA is planned
- [ ] Statuses reflect reality — drafted specs are linked from their rows

<!--
Template rules (template file only — delete this comment when filling a copy):
- One breakdown per initiative, edited in place; §3 is the live status board.
- Micro Job IDs (MJ-01…) are stable once assigned — specs, the Exception List, the BA Handoff
  and the feature index all reference them. Never renumber; a dropped job rests at `deferred`.
- Link each drafted spec from its row:
  `[MJ-02 spec]({initiative-slug}-mj-02-{job-slug}-micro-job.md)`.
- Status vocabulary in §3 is lowercase and machine-read: not-drafted / drafted / agreed /
  handed-off / deferred. The document-level Status in the meta table uses the title-case
  ladder (Draft / Agreed / Handed off), matching the Micro Job spec header.
- A Value Package too large to ship at once is split into Milestones (M1, M2). Keep one
  breakdown for the Value Package and mark each job's Milestone in its Priority cell, rather
  than splitting the board.
-->
