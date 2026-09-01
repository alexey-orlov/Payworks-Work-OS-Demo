---
date: 2026-08-31
type: synthesis
areas: [performance-management, human-resources, employee-self-service, payroll]
features: []
initiatives: [performance-management-discovery]
customers: [northwind-landscaping, maplewood-recreation, cascadia-countertops, harbourview-grocers]
owner: "Margaret Foster"
sessions_covered: 13
corpus_window: "2026-06-22 → 2026-08-12"
---

# Performance Management — Cross-Interview Synthesis

**Basis:** 13 filed records across 4 design-partner accounts, 2026-06-22 → 2026-08-12.
Sessions covered: [2026-06-22 (×3 Northwind)](2026-06-22-interview-insights.md) ·
[2026-06-23 (Northwind)](2026-06-23-interview-insights.md) ·
[2026-06-24 (Northwind)](2026-06-24-interview-insights.md) ·
[2026-07-08 (Maplewood)](2026-07-08-interview-insights.md) ·
[2026-07-10 (Northwind)](2026-07-10-interview-insights.md) ·
[2026-07-15 (Cascadia)](transcripts/2026-07-15-cascadia-countertops-interview.md) ·
[2026-07-17 (Northwind)](transcripts/2026-07-17-northwind-landscaping-call.md) ·
[2026-07-22 (Cascadia)](2026-07-22-interview-insights.md) ·
[2026-07-29 (Harbourview)](transcripts/2026-07-29-harbourview-grocers-interview.md) ·
[2026-08-05 (Northwind)](transcripts/2026-08-05-northwind-landscaping-call.md) ·
[2026-08-12 (Harbourview)](transcripts/2026-08-12-harbourview-grocers-interview.md)

Related initiative: [performance-management-discovery](../initiatives/performance-management-discovery.md).
No Product Brief exists yet — this synthesis is an input to it.

> **Evidence discipline.** Every count below is across distinct accounts (not interviews)
> unless labelled otherwise. A theme that appeared at only one account is labelled
> *single-account* and should be probed before it enters a Product Brief as a requirement.
> Verbatim quotes are from the interview-insights reports and are not re-verified here.

---

## Headlines — what the corpus settles

**1. The rating scale is the most pervasive pain in this corpus.**

The 1–5 scale is misread on both sides of every review at every account that uses a
numerical scale. Employees give themselves 4s and 5s; managers rate the same employees
2s and 3s; neither party has been given an agreed definition of each number. The review
conversation becomes an argument about the digit rather than the work. Confirmed across
**all four accounts** — the highest-count finding in the corpus.

Implication for the Product Brief: the scale's anchors must be surfaced at the point of
rating (not in a separate legend page), and a mandatory written justification for a rating
is the mechanism that most participants named as the fix.

**2. The evidence a review is built on lives entirely outside every Payworks surface.**

Paper journals (colour-coded, tabbed), emails sent to oneself, personal spreadsheets,
shared Word documents, monthly folders on a laptop — every manager in every account has a
personal system, and not one of them links to the review form. When a review is due, the
manager reconstructs six to twelve months of performance from these sources. Confirmed
across **all four accounts**, at every seniority level interviewed. The pattern is not an
edge case.

Implication: a notes feature that lives in Payworks and can be found at review time is the
single change that addresses the largest block of manager time in this corpus.

**3. Nothing in the current tool reminds anyone that a review is due. Cycles slip every year.**

No manager in the corpus reported receiving an automated reminder. Deadlines exist on paper
and are extended in practice ("On the surface, yes. In reality, no" — Northwind). The
mechanism today is the HR Manager emailing, then managers chasing their supervisors.
Confirmed at **3 of 4 accounts**; Harbourview was not asked directly.

**4. Mobile access is the adoption gate for manager-facing surfaces — but only where
managers are away from a desk.**

At Cascadia Countertops (manufacturing, managers frequently on the floor), mobile was
named as the single condition of adoption: *"a lot of our managers are constantly on the
go."* This is the strongest single-account signal in the corpus. At Northwind (multi-site
operations, yard-based managers), the regional operations manager confirmed a mobile-native
notes capture was the only condition under which he would use a notes feature at all.
Not every account in the corpus is mobile-primary — desk-based HR administrators at several
accounts expressed no mobile preference and some explicitly chose desktop tasks for
sensitive work. The distinction is manager role and work location, not company size.

**5. The relationship between a review, an approval, and a compensation change is
misunderstood — and the current product conflates steps that participants treat as separate.**

At Cascadia, the HR Lead distinguished three independent gates: the manager's rating
(manager owns), the HR quality check (HR owns), and the wage change (CEO owns, one at a
time by email today). *"If I, as HR, click approve and share, it doesn't mean that this is
approved."* Submitting a review is not approving a pay increase; they are different
decisions with different approvers. This distinction was not surfaced at every account, but
the Cascadia account's HR function runs compensation, which makes her the most direct
informant on the workflow.

---

## Ranked Themes — validated, single-account, and contested

### VALIDATED across 3–4 accounts

| Theme | Count | First surfaced | Key evidence |
|---|---|---|---|
| Self-rating inflation / undefined scale | 4/4 accounts | 2026-06-22 (Northwind) | *"most employees will give themselves 4s… 4 or 5s"* |
| Evidence lives outside the system (paper, personal files) | 4/4 accounts | 2026-06-22 (Northwind) | *"I have a notebook… almost like a journal"* |
| No automated reminders; cycles slip | 3/4 accounts | 2026-06-22 (Northwind) | *"we don't get, like, automated replies"* |
| Incumbent tool (QuickBase or equivalent) actively disliked | 3/4 accounts | 2026-06-22 (Northwind) | *"You can feel my pain"*; *"Not well"* |
| Prototype preferred to incumbent on first contact | 3/4 accounts | 2026-06-22 (Northwind) | *"You sold me. I'm good to go."* |
| Cross-department / dual-report contributions invisible | 2/4 accounts | 2026-06-22 (Northwind) | *"that's not currently acknowledged anywhere"* |
| Private vs. shareable manager notes is a real distinction | 2/4 accounts | 2026-06-22 (Northwind) | *"usually go through me"* (on sensitive content) |
| Goals typed per employee instead of set once for a site | 2/4 accounts | 2026-06-22 (Northwind) | *"I may have four at one site. They all got the same goals"* |

### SINGLE-ACCOUNT — probe before treating as requirements

| Theme | Account | Strength |
|---|---|---|
| Manager mobile as the adoption gate | Cascadia | Strong (stated twice, once unprompted, once on direct probe) |
| Dollar-per-hour compensation, not percentage | Cascadia | Must-have (their field is unusable with percentage-only input) |
| Review approval ≠ compensation approval (three separate gates) | Cascadia | Strong — HR Lead is the compensation owner at this account |
| Mandatory rating justification (character minimum) | Northwind | Must-have from the regional operations manager who writes both sides today |
| Rating anchors shown at the point of rating | Northwind | Must-have, named the prototype as the fix |
| Goal cascade to roles where the goal cannot apply | Northwind | Named by regional operations manager; corroborated in shape by Maplewood |
| Succession / readiness signal on the review | Northwind | Named unprompted; out of current initiative scope |
| Managers blind to self-review progress | Northwind | Named by district manager |
| Summary tab on the employee record for review preparation | Northwind | Named by operations manager |
| Check-in notes as HR documentation | Northwind | Named by operations manager |

### CONTESTED — do not average; hold as a design decision

| Theme | Position A | Position B |
|---|---|---|
| Peer / 360 feedback | District Manager (Northwind) and Regional Ops Manager (Northwind): want it — recognition and dual-report visibility | HR Manager (Northwind): *"we don't plan on going down that route"* — wants one-up manager collaboration instead. **HR Manager is the buyer.** |
| Employee access to check-in content | HR Manager (Northwind) and District Manager (Northwind): want employees to see it | Operations Manager (Northwind): *"I would say don't give the access to the employees"* |
| Peer feedback routing | Cascadia HR Lead: positive feedback can be visible; constructive must go through HR first | (No other account tested this routing model) |

---

## Demand Ranking — features by signal strength across the corpus

This ranking weights: (a) how many accounts named the need, (b) whether it was raised
unprompted before seeing the prototype, (c) whether it was rated must-have, and
(d) whether it addresses a pain confirmed at 3+ accounts.

1. **Rating-scale anchors at the point of rating** — 4/4 accounts, prototype-tested,
   directly addresses the highest-count pain. Must-have.
2. **Mandatory written justification for a rating** — 3/4 accounts (the fourth was not
   asked), raised unprompted at Northwind as the mechanism that stops double-writing.
   Must-have where self-rating inflation is present, which is everywhere.
3. **Automated reminders** — 3/4 accounts, unprompted, consistently described as the
   fix for a broken deadline culture. Must-have.
4. **Manager notes captured in Payworks, visible at review time** — 4/4 accounts by
   presence of the workaround (paper, email, Word); the notes-in-system ask was explicit at
   2/4 accounts, implicit at the other two. Must-have at mobile-primary accounts if mobile
   is available; desktop notes would still serve desk-primary accounts.
5. **Goal-cascade for a site or team** — 2/4 accounts, strong signal from the manager
   carrying the largest review load (12 reviews, identical goals across a site). Must-have
   for multi-site managers; nice-to-have otherwise.
6. **Manager access to the employee's self-rating while rating** — named at Cascadia as
   a prototype gap; implied at Northwind ("I compare them"). Must-have; easy win.
7. **Manager mobile for notes and check-ins** — single-account must-have (Cascadia);
   strong corroboration from one Northwind participant. Scoped to notes and check-ins;
   formal review actions stay desktop at Cascadia HR's own request.
8. **A compensation approval step separate from the review share** — single-account
   must-have. Probe at the remaining accounts before making it the default workflow model.
9. **Peer / cross-department feedback** — contested. Hold as a configurable feature
   (opt-in by account); the buyer at the most-researched account explicitly declined it as
   default. Design to the HR Manager's resolution: *"you probably have that as an option
   that either you want this option or you don't."*

---

## Open Questions for the Product Brief

1. **Does the mandatory-justification requirement hold at accounts that currently have no
   justification field at all, or only where the current tool already has one?** Northwind
   operates QuickBase — the behaviour there may not generalise to a from-scratch deployment.
2. **What is the right mobile boundary — which review actions belong on a phone and which
   stay on a desktop?** Cascadia gave a clear rule (capture and light check-ins on mobile;
   serious disciplinary wording goes through HR). Other accounts have not been asked.
3. **Where does the compensation approval step actually sit across accounts?** One HR Lead's
   workflow is one data point. Three accounts have not been asked who approves a wage change
   and how.
4. **How is the current QuickBase / spreadsheet workflow being replaced, and does the data
   migrate?** Four accounts have personal notes in Word, spreadsheets, and email. A notes
   feature that requires starting from zero will see low early adoption.

---

## Recommended Actions

1. **Use this synthesis as the input to the Performance Management Product Brief** — the
   ranked feature table and the open questions are the starting state. Owner: Margaret
   Foster — Due: 2026-09-07.
2. **Probe the three unanswered questions (mobile boundary, compensation approver, data
   migration) in the next design-partner session before a Product Brief draft is circulated**
   — each shapes a structural decision that is hard to reverse. Owner: Margaret Foster —
   Due: 2026-09-12.
3. **Carry the peer-feedback divergence into the Product Brief as an admin-configurable
   switch, with the default set to off** — the HR Manager's words provide the resolution.
   Owner: Claire Sutton — Due: 2026-09-14.
4. **Verify the mandatory-justification finding across the remaining corpus before making it
   a hard requirement** — it is a must-have at Northwind; probe Maplewood and Harbourview
   before generalising. Owner: Margaret Foster — Due: 2026-09-07.
