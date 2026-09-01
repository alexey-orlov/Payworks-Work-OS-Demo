---
initiatives: [performance-management-discovery]
areas: [performance-management]
updated: 2026-08-31
---

MICRO JOBS BREAKDOWN  |  Payworks  |  Performance Management HR 1.0

# Performance Management HR 1.0 — Micro Jobs Breakdown

Four active jobs cut riskiest-assumption-first from the review cycle backbone; one deferred pending cross-account validation.

| Field | Detail |
|-------|--------|
| **Product / module** | Performance Management (HR 1.0) |
| **Initiative** | [performance-management-discovery](../../initiatives/performance-management-discovery.md) |
| **Release** | HR 1.0 |
| **VP Product Brief** | [performance-management-discovery-product-brief.md](performance-management-discovery-product-brief.md) |
| **Micro Jobs** | MJ-01, MJ-02, MJ-03, MJ-04, MJ-05 (deferred) |
| **Author** | Margaret Foster, Product Manager |
| **Date** | 2026-08-31 |
| **Status** | Draft |

**Evidence key:** `[Evidenced]` source named · `[Partial]` signal, not proof · `[Hypothesis — needs validation]`

> **Platform and tech constraints:** `platform-model.md` and `tech-constraints.md` are both unfilled at this cut. Every constraint assumption below carries `[GAP: platform model unfilled — constraints unverified]` or `[GAP: tech constraints unfilled — feasibility unverified]` where the unfilled state affects the job. Engineering fills both files; the cuts and sequencing do not change on that information alone, but the job specs will need grounding before they are agreed.

---

## 1. THE BACKBONE

**Actors:**
- **HR Administrator** — the buyer; owns the review cycle (setup, configuration, quality check, sharing). At most accounts this is also the HR Manager or a senior admin.
- **Manager** — the reviewer; rates employees, captures notes, carries the adoption risk.
- **Employee** — the self-rater; receives the completed review.
- **Designated Compensation Approver** — CEO, owner, or executive; approves the wage change after the review is shared. *Out of scope for MJ-01 through MJ-04; in scope for MJ-05 (deferred).*

**Core objects:**
- **Review Cycle** — the configured effort: who is reviewed, by whom, on what cadence, with what rating scale and anchors. The central state machine; all other objects attach to it.
- **Review Form** — the per-employee record produced by the cycle: self-rating, manager rating, justification, HR quality-check verdict, share timestamp.
- **Rating Scale** — the configured scale with Administrator-authored anchor definitions displayed at the point of entry.
- **Manager Note** — a time-stamped log entry on an employee, visible to the manager (and optionally to HR); surfaced at review time.
- **Goal** — a configured expectation set at site/team level and cascaded to individual review forms.
- **Notification / Reminder** — system-generated message to an actor at a phase gate; Administrator-configured cadence.
- **Compensation Approval Request** — the record of a wage-change approval step separate from the review share. *Out of scope until MJ-05.*

**Flow:**

```
HR Admin: configure cycle (participants · cadence · rating scale + anchors · goal cascade · peer-feedback toggle)
    ↓
System: open cycle on configured date · notify all participants
    ↓
Employee: complete self-rating on Review Form
    ↓
Manager: view employee self-rating · rate using anchored scale · write mandatory justification · submit
    ↓
HR Admin: quality-check each submitted Review Form · return or approve
    ↓
HR Admin: share approved review with Employee (distinct action from quality-check approval)
    ↓
[MJ-05, deferred] Designated Approver: approve compensation change
    ↓
Loop closes: Employee has received the completed review; HR Admin has a closed cycle record.
```

Notes live alongside this flow (captured any time by Manager on desktop or mobile; surfaced at the Manager-rating step). Goals are set before the cycle opens (HR Admin) and appear in the Employee's review form and the Manager's rating view. Automated reminders fire at each `→` transition.

---

## 2. PROBLEM STATEMENTS THIS VALUE PACKAGE ADDRESSES

### MJ-01 — Review Cycle Skeleton

**Root cause — why this job exists**

Payworks Human Resources today stores review documentation — a form, a rating, a file on the employee record. It does not run a review process: there is no cycle object, no role-differentiated participation, no anchored rating scale, and no distinction between submitting a review and sharing it with the employee. The review process runs outside the product — in QuickBase, DocuSign, PDF forms, and Word — and the cost is an annual scale argument, manual chasing, and compensation hand-offs by email.

**HR Administrator**

When I open the annual review cycle, I want to configure who is reviewed and by whom, set a rating scale whose anchors appear to every rater at the point of rating, and be able to run the HR quality check on each completed form before sharing it with the employee, so I can stop managing a process by email and start reading results.

- **Functional:** Configure cycle (participants, cadence, rating scale + anchors); receive completed forms for quality check; share the approved review with the employee as a distinct action from quality-check approval. `[Evidenced — 4/4 design-partner accounts; synthesis §1, §5]`
- **Social:** *"We want to be part of your pilot to make it right"* — Northwind HR Manager, who asked to be included in the first live run. `[Evidenced — 2026-07-17 Northwind HR leadership call]`
- **Emotional:** Relief that the cycle closes without manual chasing; anxiety that the system is one more thing to set up. `[Partial — synthesis §3 "incumbent tool actively disliked" 3/4 accounts]`
- **Top pain:** Chasing managers every cycle, then reviewing each form by hand — *"I would actually have to go through each manager's review form."* `[Evidenced — synthesis §1]`

**Manager**

When I sit down to rate an employee, I want a rating scale I can explain to the employee — with anchor definitions visible on the form — and a field where I have to write why I gave that rating, so I can stop defending a number and start talking about the work.

- **Functional:** View the employee's self-rating while rating; enter a rating using the anchored scale (anchors displayed at the point of entry, not in a separate legend); submit the mandatory justification field before submission is accepted. `[Evidenced — 4/4 accounts: scale argument 4/4; anchor display named as fix at Northwind; self-rating visibility confirmed as gap at Cascadia]`
- **Social:** Managers who struggle with the scale are perceived as inconsistent by the employees they rate. Defined anchors change the social dynamic. `[Partial]`
- **Emotional:** *"I may have four at one site. They all got the same goals"* — frustration at a one-size form for varied roles; reduced when the form reflects the actual job. `[Evidenced — Northwind regional ops manager, 2026-06-22]`
- **Top pain:** The scale argument. *"Most employees will give themselves 4s or 5s"* — the meeting spends its time on the digit, not the work. `[Evidenced — multiple accounts; synthesis §1]`

**Employee**

When I receive my completed review, I want to see not only the rating but the written justification behind it, so I can understand what the manager actually observed rather than just the number.

- **Functional:** Receive the shared review (self-rating + manager rating + justification) as a distinct event after the HR quality check. `[Evidenced — implied by the three-gate distinction the Cascadia HR Lead named]`
- **Top pain:** Receiving a number with no explanation and no recourse but to ask the manager. `[Partial — no direct quote from an employee perspective; inferred from the scale-argument pattern]`

**Note on scope / direction**

MJ-01 is the minimum end-to-end path: one cycle, all four participants, the review form moves from setup to employee receipt. No notes, no reminders, no goal cascade — those are MJ-02, MJ-03, MJ-04. The mandatory-justification field is in MJ-01, not a later job, because it is the mechanism that breaks the scale argument; without it the skeleton does not test the riskiest assumption.

---

### MJ-02 — Manager Notes

**Root cause — why this job exists**

Every manager across all four accounts has a personal evidence system — paper journals, self-sent emails, Word documents, shared spreadsheets — because there is nowhere in Payworks to put an observation at the moment it happens. When review time comes, the manager reconstructs the year from these sources. Nothing links to the Review Form. The reconstruction is the dominant time cost of the review cycle. `[Evidenced — 4/4 accounts; synthesis §1, theme 2]`

**Manager**

When I observe something worth noting about an employee — at a yard, on the floor, after a customer call — I want to log it in the same system that will show it to me when I write the review, so I can stop maintaining a separate notebook and stop losing observations between the event and the form.

- **Functional:** Log a time-stamped note on an employee from desktop or mobile (capture and light check-ins on mobile; note is stored in Payworks and associated with the employee). View all notes for an employee when the rating window opens. Configure note visibility (private to manager, or visible to HR if Administrator enables). `[Evidenced — 4/4 accounts (workaround present); explicit ask 2/4; mobile must-have: Cascadia (single-account, strong signal); corroborated at Northwind for mobile-native capture]`
- **Social:** The manager who cannot recall what happened six months ago loses authority in the review conversation. A note log restores it. `[Partial]`
- **Emotional:** *"I have a notebook… almost like a journal"* — pride in the personal system, and reluctance to add a new step. The note surface must cost less than writing on paper. `[Evidenced — Northwind director, 2026-06-22]`
- **Top pain:** Reconstructing a year of observations at review time from scattered sources. `[Evidenced — 4/4 accounts; synthesis §1, theme 2]`

**Note on scope / direction**

Mobile scope: note capture and check-ins on mobile. Formal review actions (submitting a rating, HR quality check) stay on desktop — this is the rule Cascadia's HR Lead stated and Northwind's pattern supports. The mobile surface does not exist in HR today `[GAP: tech constraints unfilled — feasibility unverified; Engineering to confirm mobile infrastructure state]`. If mobile is more than 8 weeks away, de-scope to desktop notes in MJ-02 and treat mobile as MJ-02.1 (first release against a real user group).

---

### MJ-03 — Automated Cycle Reminders

**Root cause — why this job exists**

Review cycles slip every year because no one is reminded by the system. The enforcement mechanism is the HR Manager emailing managers and managers chasing supervisors — a manual escalation that consumes HR Manager time and still fails. *"On the surface, yes. In reality, no"* — Northwind on whether their cycle completes on time. `[Evidenced — 3/4 accounts; synthesis §1, theme 3]`

**HR Administrator**

When I open a cycle, I want the system to send timed notifications to every participant at each phase gate, so I can stop spending my own time chasing people and know the system is holding the deadline.

- **Functional:** Configure reminder cadence (which phase gates trigger a notification, how many reminders, how spaced) at cycle setup. System sends notifications to employees (self-rating due), managers (rating due), and HR (quality-check due) at each configured gate. `[Evidenced — 3/4 accounts; synthesis §1, theme 3]`
- **Social:** An HR Administrator who no longer chases managers gains time for substantive HR work. `[Partial]`
- **Emotional:** *"We don't get, like, automated replies"* — resignation that the deadline will slip. `[Evidenced — Northwind HR Manager, synthesis §1]`
- **Top pain:** Manual email chains as the only enforcement mechanism; cycles slip anyway. `[Evidenced — 3/4 accounts]`

**Manager**

When my rating window opens, I want a notification so I do not have to track the deadline myself.

- **Functional:** Receive a timely, actionable notification when the rating window opens and before it closes. `[Evidenced — 3/4 accounts; no direct manager quote but the HR-Manager-chasing-managers pattern implies the manager is not self-tracking]`
- **Top pain:** Finding out the review is overdue from the HR Manager rather than from the system. `[Partial]`

**Note on scope / direction**

Notification infrastructure likely exists elsewhere in Payworks `[GAP: tech constraints unfilled — Engineering to confirm whether the existing notification service covers this; do not re-implement]`. If a shared notification service exists, MJ-03 is an Integration job (surfacing it for HR) — substantially lower Engineering effort. If it does not exist, MJ-03 is Net new and its effort estimate changes materially.

---

### MJ-04 — Goal Cascade

**Root cause — why this job exists**

At accounts with multiple sites or team structures, managers carry review forms with the same goal set for every employee at the site — but type those goals individually per employee. *"I may have four at one site. They all got the same goals"* — the operations manager at Northwind, on his own experience. `[Evidenced — 2/4 accounts, Northwind and Maplewood; synthesis §3, demand item 5]`

**HR Administrator**

When I set up a cycle for a multi-site or team-based organisation, I want to define goals once at the site or team level and have them cascade to each employee's review form, so I do not have to type the same goal twelve times.

- **Functional:** Create goals at site/team level during cycle setup. Goals appear in the relevant employees' review forms automatically. Manager can annotate per-employee (e.g. goal does not apply to this role). `[Evidenced — 2/4 accounts; Northwind (strong signal); Maplewood (corroborated in shape)]`
- **Top pain:** Typing identical goals per employee across large review groups. `[Evidenced — Northwind regional ops manager, 2026-06-22]`

**Manager**

When I open an employee's review form, I want to see the goals that were set for this employee's site or team, so I can rate against something we both knew going in — not something I have to reconstruct.

- **Functional:** View site/team goals in the review form; annotate where a goal does not apply or was modified for this employee. `[Partial — Northwind signal; probe at Harbourview and Maplewood before spec]`
- **Top pain:** Explaining to an employee why their goals on the review form are different from what they remember being told. `[Hypothesis — needs validation]`

**Note on scope / direction**

Goal cascade is a scope expander on MJ-01's review form — not a different backbone. It runs parallel to MJ-02 and MJ-03 once MJ-01's review form structure is live. What MJ-04 defers: goal libraries (reusable templates across cycles), goal tracking through the year (check-ins on goal progress) — these are next-release scope.

---

## 3. THE MICRO JOBS

| ID | Micro Job | Type | Riskiest assumption it tests | Depends on | Priority — why | Effort | Status |
|----|-----------|------|------------------------------|------------|----------------|--------|--------|
| MJ-01 | Review Cycle Skeleton — end-to-end review cycle with anchored scale, mandatory justification, and HR quality check | Net new | H1: Anchored scales + mandatory justification will reduce the scale argument (High confidence, still unshipped; kills the riskiest product-level assumption) | — | **Must ship first** — MJ-02, MJ-03, and MJ-04 all depend on the Review Cycle and Review Form objects this job creates. Tests the highest-count pain in the corpus (4/4 accounts). | [Eng to confirm] | not-drafted |
| MJ-02 | Manager Notes — continuous in-system evidence capture (desktop + mobile capture) | Net new | H2: In-system notes displace paper journals (Med confidence); H4: Mobile capture is the adoption gate for deskless managers (Med confidence, single-account must-have) | MJ-01 (Employee record + Review Form structure) | **Should — depends on MJ-01** · Can ship the day MJ-01 is live · Tests the second-highest-count pain (4/4 accounts have the workaround) · Mobile is a single-account must-have — if mobile infra is > 8 weeks, de-scope to desktop notes first | [Eng to confirm] | not-drafted |
| MJ-03 | Automated Cycle Reminders — system notifications at each phase gate, Administrator-configurable | Integration (if shared notification service exists) / Net new (if not) | H3: Automated reminders close cycle-slippage gap (High confidence — 3/4 accounts; lower risk than H1 and H2 but dependent on shared infra state) | MJ-01 (Review Cycle state machine) | **Should — depends on MJ-01** · Can run in parallel with MJ-02 once MJ-01 ships · Engineering to confirm whether the shared notification service covers this before typing as Integration vs Net new | [Eng to confirm] | not-drafted |
| MJ-04 | Goal Cascade — site/team-level goal setup cascaded to individual review forms | Net new | Whether goal cascade reduces the per-employee goal-typing burden at scale (2/4 accounts, evidenced; not cross-validated at the remaining two) `[Partial]` | MJ-01 (Review Form structure where goals appear) | **Could — depends on MJ-01** · Can run in parallel with MJ-02 and MJ-03 · Lowest reach of the four active jobs (2/4 accounts signalled it; 38,273 accounts without HR still to validate) · No compliance, money, or irreversibility flag | [Eng to confirm] | not-drafted |
| MJ-05 | Compensation Approval Gate — configurable three-gate step (manager submits → HR approves quality → designated approver approves wage change) | Net new | Whether the three-gate model reflects the actual workflow across accounts (Low confidence — single-account data point at Cascadia; 3 accounts not yet asked) | MJ-01 (Review Form share-state) | **Won't-now — deferred** · Single-account evidence is insufficient for a structural workflow change that is hard to reverse · Probe compensation approver model at Northwind, Harbourview, Maplewood before spec · Revisit when 3+ accounts confirm the three-gate model fits their workflow · High-risk job: affects compensation process; extra QA time required when it does ship | [Eng to confirm] | deferred |

---

## 4. SEQUENCING RATIONALE

**The walking skeleton:** MJ-01 ships first because the Review Cycle and Review Form objects it creates are the shared foundation every other job attaches to. It also tests H1 — the riskiest assumption in the assumption map (highest confidence, but completely unshipped; if the anchored scale and mandatory justification do not change behaviour in a live pilot, the entire product direction needs revisiting). The skeleton is the minimum loop: setup, self-rate, manager-rate, HR check, share. No notes, no reminders, no goals — those widen the skeleton once it is proven.

**What can run in parallel:** Once MJ-01 ships, MJ-02, MJ-03, and MJ-04 can all run concurrently — they each depend only on MJ-01's data model (employee record, review form, cycle state machine). Engineering can pick up all three in the sprint following MJ-01's handoff, or sequence them by team capacity.

**What must wait, and why:**
- MJ-02, MJ-03, MJ-04: each waits on MJ-01's data model. No workaround.
- MJ-05 (deferred): waits on cross-account validation of the three-gate compensation model. A structural workflow change that touches compensation is high-risk and hard to reverse; the single-account evidence does not justify locking it into the default flow before Margaret Foster's 2026-09-12 probe sessions.

**Pipeline commitment:** the PM stays 1–2 Micro Jobs ahead of Engineering at all times. With four active jobs, the spec pipeline is: MJ-01 spec in week N → Engineering picks up MJ-01 → PM drafts MJ-02 and MJ-03 in parallel (they are independent once MJ-01's model is clear) → handoff MJ-02 and MJ-03 as MJ-01 nears completion.

> Sequencing discussed with BA and Designer before the order is locked. MJ-03's Integration vs Net new typing changes its effort substantially — confirm with Engineering before writing MJ-03's spec.

---

## 5. PRESSURE TEST RESULTS

| Micro Job | Before/After | Standalone | Vertical / Horizontal | Scope sanity | False thin slice | INVEST | Verdict |
|---|---|---|---|---|---|---|---|
| MJ-01 | **Pass** — Before: no digital review process in Payworks; scale argument, manual chasing, email-chain compensation. After: HR Admin can open a cycle, every participant has a clear role, rating conversation has shared anchors and mandatory justification. | **Pass** — if the initiative were killed after MJ-01 shipped, accounts with no digital review process would keep the cycle end-to-end. | **Pass** — traverses the full backbone (setup → self-rate → manager-rate → HR check → share); minimum at every station. | **Pass** — includes all actors and all backbone steps, but defers notes, reminders, and goals. Width is warranted: the riskiest assumption cannot be tested without closing the loop. | **Pass** — the loop closes: Employee receives the shared review. | **Pass** — I (depends on nothing), N (how the anchors render is Design's call), V (outcome-changing for all four personas), E (Engineering can estimate from the backbone), S (weeks for a scoped v1 cycle), T (pilot can observe whether the scale argument reduces). | **Cut stands** |
| MJ-02 | **Pass** — Before: manager evidence lives in paper notebooks, email chains, personal spreadsheets — nothing in Payworks. After: manager logs observations in Payworks; they appear in the Review Form at rating time. | **Pass** — notes deliver value between cycles (the observation log persists year-round). | **Pass** — traverses the notes backbone: create note → store → surface at review time. | **Pass** — scoped to note create/view/privacy settings + mobile capture. Defers goal tracking, check-in records, and the summary tab. | **Pass** — notes are stored AND surfaced at review time; not just "create note and stop there." | **Pass** — I (depends on MJ-01 declared), N, V, E, S, T (adoption rate of note-capture vs paper is the test signal). | **Cut stands** |
| MJ-03 | **Pass** — Before: HR Manager emails manually; cycles slip. After: system sends timed notifications to all participants at each phase gate. | **Pass** — reminders deliver value independent of whether notes or goals are live. | **Pass** — one capability (notifications), all actors, triggered by cycle state. | **Pass** — scoped to notification creation and scheduling based on cycle phase. Does not include custom notification channels (Slack, SMS) or digest summaries — those are next-release scope. | **Pass** — reminders fire at real phase-gate events, not at an arbitrary time. | **Pass** — depends on MJ-01 (declared); Engineering types as Integration or Net new after checking notification infra. | **Cut stands** |
| MJ-04 | **Pass** — Before: Manager types identical goals per employee individually across a whole site. After: Administrator sets goals once at site/team level; they cascade to individual review forms. | **Pass** — goal cascade delivers value independent of notes and reminders at multi-site or team-based accounts. | **Pass** — traverses from goal setup (HR Admin during cycle configuration) through to goal display in the Employee's review form and the Manager's rating view. | **Pass** — scoped to goal creation, cascade, and per-employee annotation. Defers goal libraries (cross-cycle reuse) and goal progress tracking. | **Pass** — goals appear in the review form and are visible to both Manager and Employee; the loop closes at the form. | **Pass** — depends on MJ-01 (declared); 2/4 accounts signal confirms reach; estimable from the cascade data model; testable (does the manager type fewer goals per-employee?). | **Cut stands** |
| MJ-05 | Deferred — not gated at this cut; will be gated when cross-account validation supports it. | — | — | — | — | — | **Deferred** |

---

## 6. CROSS-JOB DECISIONS & OPEN QUESTIONS

| # | Decision / question | Affects | Owner | Needed by | Status |
|---|---|---|---|---|---|
| 1 | What is the right mobile boundary — which actions belong on a phone and which stay on desktop? Cascadia gave a clear rule (capture on mobile; serious review actions on desktop); the other 3 accounts have not been asked. | MJ-02 (mobile scope), MJ-05 (deferred) | Margaret Foster | Before MJ-02 spec is agreed — Due: 2026-09-12 | Open |
| 2 | Does the existing Payworks notification service cover HR cycle phase gates, or does MJ-03 require Net new infrastructure? The type and effort of MJ-03 change materially depending on this answer. | MJ-03 (type: Integration vs Net new; effort) | Engineering `[GAP: tech constraints unfilled — Engineering to confirm notification service coverage]` | Before MJ-03 is handed off | Open |
| 3 | Is Performance Management priced as part of the HR module or as a separately purchasable add-on? Determines eligibility rules in MJ-01's access and configuration surface. | MJ-01 (access model), MJ-04 (same) | VP Product Management | Before MJ-01 spec is agreed | Open |
| 4 | What does the HR Foundation provide and does it affect MJ-01's data model? HR Foundation (position/occupation, effective dating, skills & certifications) is on the roadmap; if it precedes HR 1.0, the Review Form's employee-record linkage may depend on it. | MJ-01, MJ-02, MJ-04 | Engineering | Before MJ-01 spec is agreed | Open |
| 5 | Compensation approval gate (MJ-05): does the three-gate model (manager submits → HR approves quality → compensation approver approves wage change) fit the actual workflow at Northwind, Harbourview, and Maplewood? | MJ-05 (deferred) | Margaret Foster | 2026-09-12 (design-partner probe sessions) | Open |
| 6 | `[GAP: platform model unfilled — constraints unverified]` Access model, permission sets, and self-access rules are not described in `platform-model.md`. MJ-01's role differentiation (Administrator vs Manager vs Employee) relies on a platform mechanism not yet confirmed. Owner: PM (fill `platform-model.md`). | MJ-01, MJ-02, MJ-03, MJ-04 | PM (fill `platform-model.md`) | Before any spec is agreed | Open |
| 7 | `[GAP: tech constraints unfilled — feasibility unverified]` Stack, mobile posture, API conventions, and do-not-re-implement registry are absent from `tech-constraints.md`. MJ-02 (mobile), MJ-03 (notification infra), and MJ-04 (cascade data model) each depend on a constraint that cannot be verified until Engineering fills this file. Owner: Engineering. | MJ-02, MJ-03, MJ-04 | Engineering (fill `tech-constraints.md`) | Before MJ-02, MJ-03, MJ-04 are agreed | Open |

---

## 7. COVERAGE CHECK

- **Covered:** Review cycle setup (participants, cadence, rating scale) → MJ-01
- **Covered:** Anchored rating scale (displayed at point of entry) → MJ-01
- **Covered:** Mandatory rating justification (character-minimum field, required before submission) → MJ-01
- **Covered:** Manager-side self-rating visibility (manager sees employee's self-rating while rating) → MJ-01
- **Covered:** HR quality-check step (distinct from review share) → MJ-01
- **Covered:** Review share with employee (distinct action from quality-check approval) → MJ-01
- **Covered:** In-system manager notes (continuous capture, visible at review time) → MJ-02
- **Covered:** Mobile note capture (manager logs from phone; formal review actions stay on desktop) → MJ-02
- **Covered:** Private vs shareable note visibility (Admin-configurable) → MJ-02
- **Covered:** Automated cycle reminders (phase-gate notifications, Administrator-configurable cadence) → MJ-03
- **Covered:** Goal cascade (site/team-level goal setup cascaded to individual review forms; manager annotation) → MJ-04
- **Covered:** Peer feedback toggle (default off, configurable by Administrator) → MJ-01 (cycle setup configuration; the feature itself is off by default so no additional spec surface beyond the toggle)
- **Explicitly out:** Compensation approval gate — MJ-05 deferred until cross-account validation at Northwind, Harbourview, and Maplewood. Ships as configurable when ≥ 3 accounts confirm the three-gate model.
- **Explicitly out:** Data migration from legacy tools (QuickBase, Word, spreadsheets) — deferred to v1.1. Accounts start the first cycle from zero. Mitigation: manual-assist onboarding for Northwind's first cycle (per Margaret Foster's open loop).
- **Explicitly out:** Succession and readiness signals — single-account signal (Northwind); deliberate next-release candidate.
- **Explicitly out:** Summary tab on employee record for review preparation — named at Northwind; next-release scope.
- **Explicitly out:** Full-cycle on mobile (formal review submission, HR quality check on mobile) — out per Cascadia HR Lead's stated rule and Northwind's pattern; desktop-only for formal actions in V1.
- **Explicitly out:** Goal libraries (cross-cycle reuse, reusable templates) and goal-progress tracking (check-in updates against goals) — next-release scope after MJ-04's cascade behaviour is in market.
- **Explicitly out:** Compensation management (HR 4.0), LMS (HR 5.0), Recruiting (HR 3.0) — separate roadmap modules.

**Exception List status:** Not yet initiated — the PM initiates once each Micro Job is locked; the BA extends it during the deep dive. Locked jobs to initiate from: none yet (all jobs at `not-drafted`).

---

**Quality gate:**

- [x] 3–5 Micro Jobs — 4 active + 1 deferred = 5 total; deferred job is explicitly reasoned
- [ ] Every Micro Job passes the four pressure tests, recorded in §5 — **partial**: MJ-05 not gated (deferred); MJ-02 mobile scope carries a feasibility GAP pending Engineering confirmation
- [x] No false thin slice: MJ-01 traverses the backbone end to end and closes the loop (employee receives the completed review)
- [x] Every job in §3 has a Problem Statement block in §2, with evidence labels on its claims
- [x] Every job traces to a validated opportunity — all four active jobs trace to Problem Statements in §2 of the Product Brief (anchored in the 13-record corpus)
- [x] Every priority states its reason in dependency or risk language
- [x] Effort cells carry `[Eng to confirm]` — no PM estimates
- [x] Coverage check is clean — every Product Brief scope item covered, explicitly out, or deferred with reasoning
- [x] A variation whose backbone differs end to end became its own Micro Job — no variation-backbone cases identified; peer feedback (default off, configurable) is a configuration switch within MJ-01's cycle setup, not a different backbone
- [x] High-risk jobs flagged in Priority cell — MJ-05 (deferred): *"High-risk job: affects compensation process; extra QA time required when it does ship"*
- [ ] Statuses reflect reality — all jobs at `not-drafted`; specs not yet linked (correct for first cut)

---

Payworks Confidential  |  Updated 2026-08-31
