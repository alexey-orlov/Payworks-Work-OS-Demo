---
initiatives: [performance-management-discovery]
areas: [performance-management]
customers: [northwind-landscaping, harbourview-grocers, maplewood-recreation, cascadia-countertops]
updated: 2026-08-31
---

PRODUCT BRIEF  |  Payworks

# Performance Management — HR 1.0

Managers capture evidence during the year, walk into the review conversation with a shared rating language, and close the cycle on time — without the HR Manager chasing anyone.

| Field | Detail |
|-------|--------|
| **Product / module** | Performance Management (HR 1.0) |
| **Level** | Product Brief (Initiative) |
| **Initiative** | [performance-management-discovery](../../initiatives/performance-management-discovery.md) |
| **Release** | HR 1.0 — Discovery to Definition |
| **Availability** | TBD — admin-enabled per account (the HR Administrator turns on the module and configures the cycle before any participant sees it). `[GAP: confirm whether Performance Management ships as part of the HR module or as a separately purchasable add-on — Owner: VP Product Management]` |
| **Eligible users** | Accounts with the Human Resources module active: 5,277 accounts (12.1% of the active base of 43,550). Expansion reach: 38,273 accounts currently without HR. `[GAP: confirm eligibility rule once pricing/packaging decision is made]` |
| **Pricing** | `[GAP: no pricing model or price point exists in any source — business-info.md → Revenue Model. Owner: VP Product Management / Pricing & packaging initiative]` |
| **Author** | Margaret Foster, Product Manager |
| **Date** | 2026-08-31 |
| **Status** | Approved (Product Leadership) |
| **Links** | Breadth Prototype: None yet · Depth Prototype: None yet · Dev-Ready Prototype: None yet · Micro Jobs Breakdown: None yet · [Assumption Map](reviews/performance-management-discovery-assumption-map.md) · Telemetry: TBD · Dashboard: TBD |

---

## 1. OVERVIEW

Payworks Human Resources today lets an administrator document a performance review — attach a form, record a rating, store it on the employee record. It does not support the process that makes a review: setting expectations, capturing evidence through the year, reminding managers when action is due, or running the rating conversation without a scale argument.

HR 1.0 closes that gap. It is the initiative that turns a record-keeping module into a review process — one that must displace QuickBase, DocuSign, PDF forms on intranets, and Word documents that four of our most engaged design-partner accounts already run. The product this initiative delivers: the first place a Canadian employer can run a full performance review cycle — evidence capture, calibrated ratings, HR quality check, and a compensation-change handoff — inside the system that already knows who reports to whom.

---

## 2. PROBLEM STATEMENT

**The review is built outside the system, argued over in the meeting, and tied to compensation by hand**

Every manager in the design-partner corpus reconstructs six to twelve months of performance from paper journals, self-sent emails, personal spreadsheets, or shared Word documents when a review is due. Nothing in any of those systems connects to the Payworks review form. The reconstruction happens every cycle, at every account, at every seniority level interviewed.

This creates three compounding problems. **First, the evidence lives outside the product.** When the review opens, the manager has a notebook and a form with no connection between them. **Second, the rating scale generates an argument, not a calibration.** Employees self-rate at 4s and 5s; managers rate the same employees at 2s and 3s. Neither party has been given a shared definition of what each number means. The review conversation becomes a negotiation over a digit rather than a discussion of the work. Confirmed at all four accounts — the highest-count finding in the 13-record corpus. **Third, cycles slip every year.** No manager reported receiving an automated reminder. Deadlines exist on paper and are extended in practice. The enforcement mechanism is the HR Manager emailing managers, then managers chasing supervisors. *"On the surface, yes. In reality, no."*

**How often, and what it costs**

- **Frequency** — Annual review cycle at all four accounts; evidence reconstruction begins weeks before each cycle and runs across every manager in scope.
- **Criticality** — Manager time spent reconstructing evidence (estimated multiple hours per employee review, unbasedlined [GAP: establish baseline in next design-partner session]); HR Manager time chasing completion and auditing each submitted form individually [GAP: no time-on-task baseline]; organizational risk of a compensation decision tied to a disputed rating rather than documented evidence.

**The current workaround**

QuickBase at Northwind (actively disliked — *"You can feel my pain"*), DocuSign at Harbourview, PDF forms on an intranet at Maplewood (rolled back from a digital system after a confidentiality exposure), Word documents and paper at Cascadia. All four accounts are displacing an incumbent — none is starting from zero. Three of four rated the Payworks prototype above their incumbent tool on first contact: *"You sold me. I'm good to go."*

**Who feels this most**

- **Administrator / HR Manager** — owns the cycle, chases completion, runs the HR quality check on each submitted form, and manages the compensation hand-off by email. The buyer at every design-partner account.
- **Manager (all tiers)** — reconstructs evidence per employee at review time, argues the scale in every review conversation, and carries the follow-up on disputed ratings. The adopter whose friction determines whether the cycle closes at all.

**The trigger moment**

It is October. The annual review cycle opens. A manager opens Payworks to begin writing reviews for eleven employees and finds that eleven months of observations live in a colour-coded paper notebook on their desk and in a folder of self-sent emails — none of it in the form they are now filling in.

**Evidence**

- *"I have a notebook… almost like a journal"* — Northwind director, unprompted
- *"Most employees will give themselves 4s or 5s"* — multiple accounts; confirmed 4/4
- *"We don't get, like, automated replies"* — Northwind HR Manager on deadline reminders
- *"You can feel my pain"* — Northwind on QuickBase; 3/4 accounts rated prototype above incumbent on first contact
- 4/4 accounts: evidence lives outside the system. 4/4: undefined rating scale. 3/4: no automated reminders. 3/4: incumbent tool actively disliked.

---

## 3. CUSTOMER & MARKET CONTEXT

**Target users**

Administrators and HR Managers at Canadian SMBs — the buyers who own the review cycle — and Managers at all tiers who complete the reviews. Today: 5,277 accounts on the Human Resources module (12.1% of the active base of 43,550 — `segmentation-matrix.md`, 2026-08-31 snapshot). The four design partners span Micro to Mid size band:

| Account | Vertical | Size band | Incumbent | Key signal |
|---|---|---|---|---|
| Northwind Landscaping | Other Services | Mid | QuickBase | Multi-site; merit workflow walked end-to-end in reverse demo; 6-person east/west pilot ready |
| Harbourview Grocers | Retail | Small–Mid | DocuSign | ~1,000 review setups/year; BOS ratings; hire-date-driven cadence |
| Maplewood Recreation | Arts, Entertainment | Small | PDF on intranet | Board-governed comp; PDF rollback after confidentiality exposure |
| Cascadia Countertops | Manufacturing | Micro–Small | Word / paper | Deskless managers; mobile as adoption gate; dollar-per-hour increases |

ARR for the HR segment is unavailable — the customer base report carries no revenue field. `[GAP: billing export needed to size the retention and expansion levers in dollar terms]`

**How they work today**

HR Manager sets the cycle manually, emails a deadline, and chases stragglers. Managers reconstruct evidence from personal systems and submit ratings on a scale with no shared anchor definitions. The HR Manager reviews each form individually. The compensation step is a separate email chain to the CEO, owner, or executive team — at no account does review submission automatically trigger or inform the compensation change. The full cycle at a 14-employee account takes weeks; at Harbourview, the setup volume alone is ~1,000 records a year.

**Design partners**

Four accounts co-creating this initiative across 13 sessions (2026-06-22 → 2026-08-12). Northwind is furthest along: six interviews plus one reverse demo of the full merit workflow plus one HR leadership call. Northwind's 6-person east/west pilot group is being stood up for prototype testing. Harbourview, Maplewood, and Cascadia have each seen the prototype; follow-up sessions are pending (Maplewood: Employee Experience Director availability; Harbourview: BOS review form and manager access; Cascadia: next session TBD).

**Competitive landscape**

`[GAP: no competitive research has been run for the Performance Management module. The 39% HR win-loss gap is the only quantified competitive fact in any current source — the products accounts are leaving for are not named in any win-loss record. Run /competitor-analysis before Planning Review circulation. Owner: Margaret Foster]`

---

## 4. BUSINESS GOALS & USER OUTCOMES

**North Star**

Managers complete annual reviews inside Payworks — evidence captured, ratings calibrated, cycle closed — so HR administrators stop managing a process and start reading results.

**Business goals**

- Close the 39% HR gap in win-loss exits (FY27 KR 2.2) — the module is losing deals it should win; a review process is the capability gap
- Defend the 94%+ retention floor (FY27 KR 1.3) by making the HR module worth staying for
- Grow HR module adoption from 12.1%, contributing to the 32% → 35% multi-module KR (FY27 KR 1.4)

**User outcomes**

- Administrator / HR Manager: the cycle runs without manual chasing; the HR quality check is one step, not a form-by-form audit; the compensation conversation is clearly separated from the review.
- Manager: captures evidence at the moment it happens, finds it at review time, enters a rating conversation with shared scale definitions, and completes the cycle without a paper notebook.

**Strategy fit**

HR 1.0 is the retention-floor bet in the FY27 portfolio alongside Time and Absence. The FY27 strategy labels HR, Time, Scheduling, and Absence as *"retention floor"* modules — not wallet-share expansion. The 39% win-loss gap means HR is losing deals it should be winning on compliance and integration grounds. Winning those deals requires a review process; more review documentation does not close that gap.

**Hypothesis**

If we build a Payworks-native review cycle with in-system evidence capture, anchored rating scales, and mandatory rating justification, then managers will complete reviews on time and HR Managers will spend less time chasing and auditing, because the evidence-reconstruction burden and the undefined scale are the two mechanisms that make performance review season fail today — and both are solvable in product.

**Key hypotheses** — the beliefs this bet rests on; full map in [`reviews/performance-management-discovery-assumption-map.md`](reviews/performance-management-discovery-assumption-map.md).

| Hypothesis | Risk lens | Confidence | Validation route | Priority |
|---|---|---|---|---|
| Anchored scales + mandatory justification reduces the scale argument | Desirability | High | Northwind 6-person pilot; present revised prototype, observe rating-conversation outcome | 1 |
| In-system notes displaces paper and email journals | Desirability | Medium | 2 design-partner sessions with note-capture prototype; ask if it replaces the notebook | 2 |
| Automated reminders close the cycle-slippage gap | Desirability | High | Probe cadence needs with Harbourview HR Manager (1,000 reviews/year is highest-stakes validator) | 3 |
| Mobile capture is the adoption gate for deskless managers | Usability | Medium | Probe Harbourview + Northwind site supervisors on work location before generalising from Cascadia | 4 |
| Separate comp-approval step reflects actual workflow across accounts | Usability | Low | Probe comp approver model at Northwind, Harbourview, Maplewood before making it structural default | 5 |

**Impact by lever**

| Lever | Primary? | Estimate | Basis |
|---|---|---|---|
| Retention | **Yes** | `[GAP: ARR unavailable. Reach: 5,277 HR accounts. Baseline churn rate by module not established — run /retention-analysis once warehouse is connected]` | segmentation-matrix.md (account count) |
| Expansion / LTV | **Yes** | `[GAP: ARR unavailable. Reach: 38,273 accounts without HR module. Run /impact-sizing once billing export and churn baseline land]` | segmentation-matrix.md (account count) |
| Acquisition | Not this bet | — | — |
| Activation | Not this bet | — | — |
| Cost to serve | Not this bet | — | — |

---

## 5. KPI FRAMEWORK

**Tier 1 — Outcome Metrics** (the business result)

| KPI | Baseline (source) | Target | Timeline | Type |
|---|---|---|---|---|
| HR win-loss gap rate | 39% (`current-quarter.md` — measurement date not stated) | TBD — set at Planning Review `[GAP: Owner: VP Product Management]` | 2 quarters post-launch | Lagging |
| Client retention rate (HR module accounts) | TBD — baseline to be established; no module-level churn data in any source `[GAP: /retention-analysis once warehouse is connected]` | 94%+ (FY27 floor) | Rolling 12-month | Lagging |
| HR module adoption rate | 12.1% of active base (5,277 / 43,550 — `segmentation-matrix.md`, 2026-08-31) | TBD — set at Planning Review | 4 quarters post-launch | Lagging |

**Tier 2 — Product Metrics** (adoption and engagement)

| KPI | Baseline (source) | Target | Timeline | Type |
|---|---|---|---|---|
| ★ Review cycle completion rate (% of cycles opened that close on schedule) | TBD — post-launch baseline; design-partner estimate to be established in next session `[GAP]` | TBD — set at Planning Review | Day 90 | Leading |
| Manager note-capture rate (% of active managers logging ≥1 note before their review window opens) | 0 (feature does not exist today) | TBD | Day 60 | Leading |
| Time-to-cycle-close (days from cycle open to last review submitted) | TBD — historical estimate from design partners `[GAP: ask in next session]` | ↓ from baseline | Day 90 | Leading |

★ = primary metric for this release.

**Tier 3 — Quality Metrics** (stability and performance)

| KPI | Baseline (source) | Target | Timeline | Type |
|---|---|---|---|---|
| Review form error rate (missing required fields at submission) | TBD — post-launch | < 5% | Day 30 | Leading |
| Mobile session success rate (note capture, no crash or data loss) | TBD — post-launch | ≥ 99% | Day 7 | Leading |

**Guardrails** (must not harm)

- Existing HR module engagement (document storage, onboarding checklists, other HR features in market) must not decline past the pre-launch baseline — watched at Day 30 and Day 60.
- Payroll run success rate must hold at its existing level through any shared-database schema changes — watched at Day 7.

**Kill metrics**

- Review cycle completion rate below 30% at Day 90 → diagnose whether the UX, the required fields, or adoption of the cycle-setup step is the blocker; freeze expansion rollout and convene a design-partner session.
- Mobile session crash rate above 2% at Day 7 → roll back mobile access; revert to desktop-only while Engineering resolves.

**Checkpoint schedule**

| Checkpoint | What we're checking |
|---|---|
| Day 7 | Critical defects; mobile stability; can the full cycle be opened, rated, HR-checked, and closed end to end? |
| Day 30 | First adoption read — which accounts activated the module; manager note-capture early signal |
| Day 60 | Engagement read — are managers using notes before review time? Is the scale argument appearing in support tickets? |
| Day 90 | Business outcome read — cycle completion rate vs baseline; HR Manager time-on-task vs design-partner estimate |

---

## 6. PROPOSED SOLUTION

**How it works**

The HR Administrator sets up a review cycle: who is reviewed, by whom, on what cadence, and using which rating scale — with anchor definitions written into the setup that will appear at the point of rating for every participant. The cycle opens automatically on the configured date and notifies all participants. Managers capture notes on their direct reports throughout the year from desktop or mobile; those notes appear alongside the employee's self-rating when the manager's rating window opens. The employee completes a self-rating; the manager sees it, rates against the same anchored scale, and must provide a written justification before submission. The HR Manager runs a quality check on each submitted review and either approves it or returns it to the manager. The reviewed employee then receives the completed review — an explicit share step, separate from the HR quality-check approval. Where the account has enabled it, a compensation-change approval step sits after the review is shared, owned by the account's designated approver (CEO, executive, or HR, depending on account configuration).

On mobile: note capture and check-ins are available on a phone. Formal review actions — submitting a rating, running the HR quality check — stay on desktop. This is the scope Cascadia's HR Lead defined (*"serious and disciplinary wording goes through HR"*) and that Northwind's pattern of deskless notes but desk-based review completion supports.

**Feature set**

| Feature | Description |
|---|---|
| Review cycle setup | Administrator configures participants, cadence, rating scale, and anchor text per scale point. Peer feedback is a toggle, default off (HR Manager at Northwind explicitly declined as default; configurable per the HR Manager's own resolution: *"you probably have that as an option"*). |
| Anchored rating scale | Scale anchors are displayed at the point of entry — not in a help page, not in onboarding. Anchor text is set by the Administrator at cycle setup; a default set ships for common scales (1–5, 1–4) that the Administrator can override. |
| Mandatory rating justification | A character-minimum written field required before a manager can submit a rating. Prevents a scale number from standing without context. |
| In-system manager notes | A running note log per employee. Visible to the manager; visible to HR only if the Administrator enables it. Appears alongside the employee's self-rating when the manager's rating window opens. Private-vs-shareable distinction configurable by Administrator. |
| Automated cycle reminders | System reminders at each phase gate: self-rating due, manager rating due, HR quality-check due. Cadence and frequency set by the Administrator. |
| Goal cascade | Administrator sets goals at a site or team level; those goals populate into individual employee reviews. Manager can annotate per-employee where a goal does not apply. |
| Manager-side self-rating visibility | Manager sees the employee's self-rating while completing their own — confirmed as a prototype gap at Cascadia; implied at Northwind (*"I compare them"*). |
| Mobile note capture | Manager can log a note from a phone. Formal review submission stays on desktop. |
| Compensation approval step | A gate between review share and compensation change, owned by the account-configured approver. Configurable; default off pending cross-account validation. |

**Why this beats the current workaround**

QuickBase, DocuSign, and PDF forms share the structural weakness that makes them the current alternative: no connection to Payworks, so any compensation or payroll consequence requires a manual hand-off out of the review system and into the payroll system. A Payworks-native cycle eliminates that hand-off — the person who approved the review is in the same system as the person who runs payroll.

The incumbent does not lose on every dimension. Accounts with years of historical data in their current tool face a migration cost that a net-new Payworks cycle cannot immediately offset — this is an adoption risk in the first cycle (§10). Accounts with established peer-feedback workflows will find the default-off position limiting; the configurable-on option is the minimum viable hedge.

**Access & eligibility**

- Admin-enabled per account: the HR Administrator turns on Performance Management and configures the cycle before any manager or employee sees it.
- Eligible: accounts with the Human Resources module active. `[GAP: confirm whether Performance Management ships as part of HR or as a separately billed add-on — Owner: VP Product Management]`
- Users outside the criteria: no entry point; no read-only view in V1.

**Alternatives considered**

- **Enhance the existing HR review documentation fields** — not doing it because the existing feature stores a completed form, not a process; adding more fields cannot address reminders, note capture, or scale calibration — the three structural gaps the corpus confirms.
- **Peer / 360 feedback as the default** — not doing it because the buyer at the most-researched account explicitly declined: *"we don't plan on going down that route."* Configurable on/off is the resolution.

---

## 7. SCOPE & BOUNDARIES

**In this release**

- Review cycle setup and administration
- Anchored rating scale with mandatory justification
- Manager notes, captured throughout the year, visible at review time
- Automated phase-gate reminders
- Goal cascade to site or team
- Manager-side self-rating visibility during rating
- Mobile note capture (formal review actions: desktop only)
- Compensation approval gate (configurable, default off pending cross-account validation)

**Scope boundary — documented but not included**

- **Compensation management (HR 4.0)** — setting rates, budgets, and pay bands is a separate roadmap module with its own business case; the compensation approval gate in HR 1.0 is the handoff point, not the compensation system itself.
- **Peer / 360 feedback as default** — out by buyer decision at Northwind (the most-researched account); ships as configurable on/off.
- **Data migration from legacy tools** — accounts have years of historical performance data in Word, spreadsheets, and email. A migration path is an adoption-risk open question (§10), not in scope for V1.
- **Succession and readiness signals** — named unprompted at Northwind (single-account signal); deliberate next-release candidate.
- **Summary tab on the employee record for review preparation** — named at Northwind; next-release scope.
- **Full-cycle on mobile** — formal review submission and HR quality-check stay on desktop in V1.
- **Recruiting (HR 3.0), LMS (HR 5.0), Compensation Management (HR 4.0)** — separate roadmap modules.

**Tradeoffs accepted**

- Deferring peer/360 feedback as a default may cost deals where it is a buying criterion. The configurable-on option is the minimum viable hedge; revisit after observing how accounts use the toggle in the first release.
- Deferring migration tooling means early adopters start the first cycle from zero. This is the highest adoption risk in V1 for accounts with rich legacy data (Northwind has three years of QuickBase records).
- Desktop-only formal review actions mean the full cycle cannot be completed on a phone. If a larger share of accounts proves to be fully mobile-primary, this boundary will need to move in v1.1.

---

## 8. USER EXPERIENCE PRINCIPLES

**Evidence capture must cost less than a paper notebook.**

A manager who finds it faster to write on paper will keep writing on paper. The note-entry surface must be reachable in two taps from the manager's home screen and must work without a signal on mobile. If adding a Payworks note takes longer than a paper entry, that is a product gap, not an expected trade-off.

**The scale is shared before the rating happens, not explained after.**

Anchor definitions appear at the point of entry, every time, for every rater — not in a help page, not in onboarding, not explained by the HR Manager before the cycle opens. If a manager or employee has to navigate away from the rating field to understand what a number means, that is a product gap.

**Completing a review is not the same as approving a raise.**

The product surfaces three distinct acts as three distinct steps: the manager submits the rating, the HR Manager approves the review quality, and the compensation change is separately approved by the designated approver. Conflating any two of these is a product gap. *"If I, as HR, click approve and share, it doesn't mean that this is approved"* — Cascadia HR Lead — is the sentence the product must make impossible.

---

## 9. KEY DECISIONS & TRADEOFFS

**Peer feedback is an admin-configurable switch, default off.**

The district manager and regional ops manager at Northwind want peer recognition and cross-department visibility in the review. The HR Manager at Northwind — the buyer — explicitly declined: *"we don't plan on going down that route."* Resolution from the same account: *"you probably have that as an option that either you want this option or you don't."* The default is the HR Manager's position; the on-state is for accounts whose buyers choose it.

Tradeoff: accounts that want peer feedback will need to discover and enable the setting. Surface the toggle prominently in cycle setup to avoid burying a feature that some accounts will consider table-stakes.

**Mobile access is scoped to note capture and check-ins; formal review actions stay on desktop.**

Cascadia's HR Lead defined the clearest rule: light capture on mobile, serious wording through HR on desktop. Northwind's pattern (deskless notes, desk-based review completion) corroborates. This is the narrowest mobile scope that unblocks adoption for deskless managers without moving sensitive HR actions onto a form factor the HR function itself declined.

Tradeoff: accounts that are fully mobile-primary — beyond Cascadia's profile — may find desktop-required formal steps to be a friction point. Revisit the boundary at the first design-partner cycle-completion read.

**The compensation approval gate ships as configurable, default off.**

A single account (Cascadia) provides the evidence for a three-gate model (manager submits → HR approves quality → designated approver approves wage change). Three accounts have not been asked whether this model fits their workflow. Shipping it as a mandatory step before cross-account validation would impose a workflow that the corpus cannot yet support as universal. Default-off with Administrator enablement is the minimum viable hedge.

---

## 10. OPEN QUESTIONS, RISKS & DEPENDENCIES

**Open questions**

- [ ] What is the right mobile boundary across accounts beyond Cascadia? — @Margaret Foster — probe Harbourview and Northwind site supervisors before Solution Review. Due: 2026-09-12
- [ ] Where does the compensation approval step sit across accounts? Three accounts not yet asked who approves a wage change and how. — @Margaret Foster — probe in next design-partner session. Due: 2026-09-12
- [ ] Does the mandatory-justification requirement hold at accounts that currently have no justification field (Maplewood, Harbourview)? — @Margaret Foster — probe before making it a hard requirement. Due: 2026-09-07
- [ ] Is Performance Management priced as part of HR or as a separately purchasable add-on? — @[GAP: VP Product Management] — blocks Eligible users and Pricing rows. Due: TBD
- [ ] What competitors do accounts switching away from HR name? — @Margaret Foster — run `/competitor-analysis`. Due: before Planning Review circulation
- [ ] What is the HR Foundation dependency and does it block HR 1.0? — @[GAP: Engineering] — confirm whether HR Foundation (position/occupation, effective dating, skills & certifications) is a prerequisite or a parallel workstream. Due: before XFN Kickoff

**Risks**

**Risk — Migration friction.** Four accounts have years of historical performance data in Word, spreadsheets, and email. A Payworks cycle that requires starting from zero will see low early adoption in the first review cycle. **Mitigation:** Scope a lightweight import path (CSV or document upload) for historical review records; assess Engineering feasibility before locking the V1 scope boundary. If infeasible for V1, communicate to design partners before the cycle opens and offer manual-assist onboarding for the first cycle.

**Risk — Anchor text quality.** The anchored scale reduces the rating argument only if the Administrator writes meaningful anchor text. If accounts leave anchors at defaults or copy generic text, the scale argument recurs in a new form. **Mitigation:** Ship a curated default anchor set for common scales (1–5, 1–4) that the Administrator can override — not a blank — so the worst-case starting state is usable, not empty.

**Risk — Peer feedback discovery gap.** Default-off means accounts that want peer feedback must find the toggle. If it is buried in advanced settings, it effectively does not exist for most accounts. **Mitigation:** Surface the peer feedback toggle prominently in the cycle-setup flow, not in settings.

**Risk — Mobile infrastructure unknown.** Mobile HR access for note capture and check-ins assumes mobile infrastructure that may not yet exist in the HR module. **Mitigation:** Run `/code-qa` as soon as `engineering/code-repos.yaml` has a reachable HR repo; if mobile is 6+ months away, de-scope mobile to v1.1 and ship desktop-first.

**Dependencies**

- **HR Foundation (position/occupation, effective dating, skills & certifications)** — named on the 24-month roadmap as a shared foundation. Whether it is a prerequisite for HR 1.0 is not stated in any source. Owned by: Engineering `[GAP: confirm owner]`. Required by: HR 1.0 XFN Kickoff. Interim: proceed with definition assuming HR Foundation is parallel; revisit if Engineering confirms it as a blocker.
- **Mobile platform (note capture)** — mobile infrastructure for HR module actions; current state unknown. Owned by: Engineering `[GAP]`. Required by: HR 1.0 Solution Review. Interim: `/code-qa` as soon as a reachable HR repo is registered.
- **Pricing & packaging decision** — determines Eligible users, Pricing, and availability model. Owned by: VP Product Management / Pricing & packaging initiative. Required by: HR 1.0 Planning Review. No interim workaround — the brief cannot clear Planning Review with Pricing as TBD.

---

## 11. ROLLOUT & ITERATION PLAN

**HR 1.0 — date TBD (waits on Planning Review approval and Engineering scope confirmation)**

- Rollout: design-partner accounts first — Northwind's 6-person east/west pilot group as the first live test; Harbourview, Maplewood, and Cascadia as the second wave once the pilot read is in
- Configuration required: Administrator sets up cycle, rating scale and anchors, goal cascade, and approval routing before any participant sees the module
- Peer feedback: configurable, default off
- Compensation approval gate: configurable, default off

**Launch conditions**

- [ ] HR Foundation dependency confirmed resolved or de-scoped
- [ ] Mobile boundary confirmed across at least 3 accounts
- [ ] Compensation approval model validated at 2 additional accounts beyond Cascadia
- [ ] Default anchor set tested with Northwind pilot and confirmed usable
- [ ] Pricing and eligibility row resolved in the meta table
- [ ] `/feature-launch-gate` cleared; no `[GAP:]` markers remaining in §§2, 5, or 7

**HR 1.0 v1.1 — theme: migration and mobile completeness**

- Lightweight import of historical review data (CSV / document upload)
- Expanded mobile surface based on design-partner cycle-completion read
- Succession / readiness signal — if validated at a second account

**Future expansion**

The compensation approval gate, once validated broadly, is the natural bridge into HR 4.0 (Compensation Management). The check-in notes and goal-cascade features are the foundation for a continuous-performance model beyond annual cycles. The peer-feedback surface, once adoption data arrives, may move from default-off to default-on in accounts above a size threshold.

---

## 12. APPENDIX

**Changelog**

| Date | Change | Who |
|---|---|---|
| 2026-08-31 | Product Leadership Approval recorded; status moved to Approved | vladyslav.butenko@payworks.ca |
| 2026-08-31 | Direction approved at intake; brief created at Planning Review stage | vladyslav.butenko@payworks.ca |

**Source material**

- [`product/user-insights/performance-management-2026-08-31.md`](../../user-insights/performance-management-2026-08-31.md) — cross-interview synthesis, 13 records, 4 accounts; the primary evidence base for this brief
- [`product/initiatives/performance-management-discovery.md`](../../initiatives/performance-management-discovery.md) — initiative page: scope, design-partner corpus, open loops
- [`product/strategy/current-quarter.md`](../../strategy/current-quarter.md) — 39% HR win-loss gap (KR 2.2), 94%+ retention (KR 1.3), multi-module 32% → 35% (KR 1.4)
- [`product/strategy/business-context/segmentation-matrix.md`](../../strategy/business-context/segmentation-matrix.md) — 5,277 HR accounts (12.1% of 43,550 active accounts)
- [`product/strategy/business-context/business-info.md`](../../strategy/business-context/business-info.md) — seven personas; product principles; FY27 strategy framing

---

Payworks Confidential  |  Updated 2026-08-31
