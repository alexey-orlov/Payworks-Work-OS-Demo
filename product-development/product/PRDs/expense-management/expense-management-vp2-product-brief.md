---
initiatives: [expense-management-vp2]
areas: [expense-management]
customers: [northwind-landscaping, acme-corp, birchbark-books]
updated: 2026-08-31
---

PRODUCT BRIEF  |  Payworks

# Expense Management — VP2, Milestone 1

Field and office staff capture what they spent at the moment they spend it, the right person says yes, and the money arrives on a pay date the claimant can see.

| Field | Detail |
|-------|--------|
| **Product / module** | Expense Management (A/B 2.0) |
| **Level** | VP Product Brief (Value Package) |
| **Initiative** | [expense-management-vp2](../../initiatives/expense-management-vp2.md) |
| **Release** | VP2, Milestone M1 (M2 carries the accountant-and-bookkeeper firm view — §7) |
| **Availability** | Admin-enabled per account: the Administrator turns the module on and configures approval routing before any claimant sees it. Not automatic. |
| **Eligible users** | Every active payroll account is technically eligible — 43,550 accounts (`segmentation-matrix.md`, 2026-08-31 snapshot). The two evidenced shapes are multi-site field services and single-admin small office. [GAP: no source segments the base by expense behaviour or by whether an account already runs expenses elsewhere — needs a question added to the next base report, or an admin survey. Owner: Michelle Tremblay] |
| **Pricing** | [GAP: no pricing model, tier structure or price point exists in any source (`business-info.md` → Revenue Model). Seat treatment for seasonal claimants is an open commercial question — §10. Owner: Pricing & packaging (corporate strategic initiative); Michelle Tremblay to route] |
| **Author** | Michelle Tremblay, Product Lead — Payroll & Expense |
| **Date** | 2026-08-31 |
| **Status** | Approved (Product Leadership) 2026-08-25 — amendment in review following the 2026-08-27 Controller call |
| **Links** | Breadth Prototype: None yet · Depth Prototype: None yet · Dev-Ready Prototype: None yet — Vanessa Lee, after the Translation Checkpoint · [Micro Jobs Breakdown](expense-management-vp2-micro-jobs-breakdown.md) · Telemetry: per-Micro-Job, in each spec's Telemetry Plan · Dashboard: None yet `[GAP: no expense dashboard and no metric definitions exist — analytics/metrics/ is empty. Owner: Michelle Tremblay to run /feature-metrics once MJ-02 locks]` |

---

## 1. OVERVIEW

VP1 gave a limited launch group a mobile expense claim and a first approval step, shipped on 2026-08-21. It proved that a claim can be created on a phone and moved to a person. It did not touch where the money comes from, who is allowed to say yes at what amount, or what happens when the phone has no signal — and it went to a group small enough that we have no instrumented read on any of it.

VP2 Milestone 1 is the package that has to stand on its own inside a real business. It adds the record everything else hangs off, capture that survives a truck and a dead zone, approval routing an employer configures for their own org, and a path for an approved claim onto the pay run without ever behaving like income. What the product becomes: the first place a Canadian employer can run a full expense cycle — spend, capture, approve, pay — without leaving the system that already knows who reports to whom.

---

## 2. PROBLEM STATEMENT

**The receipt and the coding arrive weeks apart, so the money is late and the revenue is lost**

An employee spends their own money away from a desk. The receipt has to physically travel to a finance person, who then has to reconstruct — from a faded piece of paper, weeks later — what it was for and which job it belongs to. Nothing in that chain is instrumented, so nobody can see where a claim is, and no one finds out when it goes wrong.

This creates three compounding problems. **First, the paper does not survive the journey.** Thermal receipts sit on a dashboard in July and arrive blank; envelopes get brought in "or don't". **Second, the coding happens too late to be right.** The person who bought the item knows the site; the person who codes it knows the contract number; they are different people three weeks apart, and a mis-code is silent — there is no error, just a smaller invoice. **Third, the claimant cannot see anything.** They do not know whether the claim arrived, whether it was approved, or when they will be paid, so they phone — and the person they phone is finance.

Approval is the second half of the same problem. Employers already have approval policies; they hold them in a Word document and rebuild the routing by hand every time somebody changes chairs.

**How often, and what it costs**

- **Frequency** — At Northwind Landscaping: **600–650 receipts a month in season (May–October)**, about **250 in February**; median receipt **$60**; roughly **$40,000 a month in season and $15,000 in February**, or **~$350,000 a year** in reimbursements and small purchases, excluding fuel cards. `[Evidenced — 2026-08-27 Controller call]` At Acme Corp (75 employees) the volume is an order of magnitude smaller and the receipts are already digital — PDFs and forwarded confirmation emails, "maybe three" paper photos last month. `[Evidenced — 2026-08-20 Acme call]`
- **Criticality** — Northwind's A/P clerk spends **2.5 days every month end** keying **~400 lines** — "the worst two and a half days to lose", because she is supposed to be closing the month. Unreadable or never-delivered receipts cost **$3,000–$4,000 a year**, reimbursed anyway but un-billable and undefendable in an audit. Mis-coded materials on **eleven municipal contracts** are lost revenue, not lost cost — "if that bag of grass seed doesn't get coded to the right job number, we don't bill for it." A claimant who buys on a Tuesday can wait **a month** for $180 they put on a personal Visa, because A/P's EFT run and its Monday cutoff do not line up with the purchase. `[Evidenced — 2026-08-27 Controller call]`
- **The single most common inbound call to finance** is not about pay. "Not 'where's my paycheque,' they never phone about that, payroll's fine. It's 'where's my ninety bucks from the Home Hardware.'" `[Evidenced — 2026-08-27 Controller call]`

**The current workaround**

An envelope in the glove box, a $200 petty-cash float at each of six yards ("gone by the tenth of the month, always"), and a shoebox on the A/P clerk's desk — "it is a Reebok box, it's been the same box for four years." At the small end it is an Excel file on a shared drive with the year in the filename, so claims arrive on last year's form with last year's mileage rate. At an accounting firm it is the bookkeeper: **three hours per client per month on expense coding, ~120 hours a month across a 40-client book.** The alternative employers evaluate is a standalone expense tool; both accounts that priced one told us what stopped them (§3).

**Who feels this most**

- **The Employee / claimant (field)** — fronts their own money, has no desk, cannot see the claim's state, waits weeks
- **The Manager / approver** — approves on paper in a tray with nothing to prompt them; routing breaks whenever a person changes role
- **The Administrator** — re-keys, re-codes, and answers the "where's my money" calls
- **The Business Owner** — is the top approval tier and the slowest one: "a five thousand dollar approval can sit for eleven days"
- **The Accountant / Bookkeeper (channel)** — absorbs the coding work across a whole book of clients, and is the front line for a product they do not own
- **Finance, internally to the customer (A/P clerk)** — 2.5 days a month and the audit exposure. [GAP: the A/P clerk is not one of Payworks' seven personas and has never been interviewed; the Controller has offered to bring her to the next session. Owner: Michelle Tremblay]

**The trigger moment**

A crew is on a municipal site and the mower throws a belt. They are not driving back to the yard, so they buy the part at the supply place down the road — on a company card if the supervisor has one, otherwise on somebody's personal Visa. The receipt goes in the glove-box envelope, and from that second onwards the information that makes it billable — which site it was for — exists only in one person's head. Once this ships, that same moment is where the claim is created: the photo, the amount and the site are captured at the counter, and everything downstream inherits a coded claim instead of reconstructing one.

**Evidence**

- **2026-08-27 — Northwind Landscaping, Controller + HR Manager** (raw record in `inbox/2026-08-27-northwind-landscaping-expense-call.txt`; summary pending `/process-meeting`). Volumes, dollars, clerk time, thresholds, cutoffs, taxability and register-lock conditions, offline behaviour, notification reach. `[Evidenced]`
- **2026-08-20 — Acme Corp, HR Manager + Payroll Administrator** (raw record in `inbox/2026-08-20-acme-corp-call.txt`). 75 employees, one administrator, already-digital receipts, the auto-approve-floor disagreement, and an explicit request that mobile approval be blocked rather than discouraged. `[Evidenced]`
- **2026-08-18 — Birchbark Books & Accounting, Firm Principal + Senior Bookkeeper** (raw record in `inbox/2026-08-18-birchbark-books-call.txt`). Channel volumes and the firm-level access problem. `[Evidenced]`
- **2026-08-05 — Northwind Landscaping reverse demo** (`inbox/payworks-source-material/2026-08-05-northwind-landscaping-client-call-reverse-demo.vtt`). The one first-hand expense record that existed before this month: claims route claimant → Head of HR → accounts payable, *not* payroll, and the claimant "has no complaints". `[Evidenced]`

Four sources across three accounts, above the SOP's bar of three. Two of the three are single-account voices on their own segment shape; the field-services picture rests on Northwind alone. [GAP: no second multi-site field-services account has been interviewed on expense — the pattern could be Northwind-specific. Close with one more field-services design partner before MJ-02 locks. Owner: Margaret Foster]

---

## 3. CUSTOMER & MARKET CONTEXT

**Target users**

Canadian SMB payroll accounts that already run Payworks. The nominal denominator is **43,550 active accounts**, of which **93% have under 100 employees** (`segmentation-matrix.md`; `business-info.md` → ICP). Within that base, the two shapes this Milestone is designed against are:

- **Multi-site field services** — crews away from any desk, purchases at a counter, job- or contract-level cost coding. Closest available proxies in the base: Construction **1,941 accounts**, Other Services **6,125**, Other **5,285** (Northwind itself files under `Other` — grounds maintenance, NAICS 561730). These are vertical counts, *not* a count of accounts with this expense shape.
- **Single-admin small office** — one Administrator doing payroll, expenses, benefits and T4s; receipts already digital. Acme-shaped. The Small band (20–99 employees) is **14,284 accounts**; Micro (1–19) is **26,020**.
- **The channel** — **2,983 accounts (6.9%)** carry the `Accountant` tag, concentrated in BC (1,018) and Ontario (836), with only **86 in Québec** against a 3% provincial share target.

[GAP: **ARR by segment cannot be produced.** The August 2026 Customer Base report carries no revenue, price or contract-value field of any kind (`segmentation-matrix.md` banner), so every revenue-weighted claim in this brief is a count, not a dollar. Close by providing a finance export keyed on `CustID` and re-running the matrix recipe. Owner: unassigned — `segmentation-matrix.md` has no owner either.]

**How they work today**

At the field-services end: about sixty trucks across two provinces, six yards, eleven municipal contracts, a fuel card per truck (clean — one statement, ~$28,000 a month, and explicitly not the problem), a $200 petty-cash float per yard, and everything else on a company or personal card. Approval policy today, at Northwind, in the Controller's own words: under $500 the regional manager, $500–$2,500 the Controller, over $2,500 the Controller plus the Ops Director, over $5,000 the Owner. Six to eight claims a year cross the top tier. A/P pays by EFT every second Thursday with a Monday cutoff; payroll runs biweekly on the *opposite* Thursday.

At the small-office end: an Excel claim template on a shared drive, emailed to the payroll administrator — or to a manager first, "depending on who taught them, which is not consistent" — with PDF receipts attached. One approval for everything, and the administrator believes that is correct at 75 people.

At the firm end: a bookkeeper reviewing (not approving — "those are different words") forty clients' coding at eight in the morning on two monitors, at 120 hours a month across the book, billed at $75 while the advisory work they turn down bills at $180.

**Design Partners**

Three engaged, against the house range of 3–5.

| Partner | Profile | What they have seen | What is still going to them |
|---|---|---|---|
| **Northwind Landscaping** | Multi-site field services, ON + BC; Controller is the primary Payworks contact, HR Manager is the champion | Nothing built — the 2026-08-27 session was current-state discovery only | A Breadth Prototype in 3–4 weeks; the Controller has asked to bring his A/P clerk, and Michelle has accepted |
| **Acme Corp** | 75 employees (76 as of 2026-08-24), one office plus six remote; one Payroll Administrator owns expenses | Nothing built — 2026-08-20 was a listening call | The same prototype round, to test whether the tiering model reads as configuration burden at their size |
| **Birchbark Books & Accounting** | Six-person bookkeeping firm, ~40 SMB clients | Nothing built — 2026-08-18 was a research call | M2 (firm view). They asked for two weeks' notice of any client-visible change — "we're the people who absorb it" |

The standing cadence is not yet agreed. [GAP: no Design Partner cadence, no co-creation call schedule, and no written partner agreement exists for this initiative. Owner: Michelle Tremblay, before the prototype round.]

**Competitive landscape**

There is no competitor research to draw on. `product/competitive-research/` contains no teardowns, and `business-info.md` records that **no source names a single expense competitor** — the only rival named anywhere in Payworks' material is Wagepoint, and that is from Payroll Hub material, not expense. What we have instead is two first-hand, customer-reported evaluations of a standalone expense tool:

- **Northwind priced one at $9 per user per month with a 200-seat minimum — $21,000–$22,000 a year.** The cost was not the blocker: "I could defend twenty-two thousand against two and a half days of clerk time." What stopped it was that **it did not talk to payroll and it did not know what a job number was** — meaning a CSV export into job costing anyway. "So I'd be paying twenty-two grand to move the problem." `[Evidenced — 2026-08-27]`
- **Acme priced one at about $9 a head — roughly $8,000 a year for 75 people** — and rated it a good product. `[Evidenced — 2026-08-20]`

That is the whole differentiation argument for this Value Package, and it is the same one the company sells: one suite, one database, no rekeying. The Controller stated it himself without prompting — "the system already knows who reports to who. Payroll knows. It's just, expense doesn't ask payroll."

No capability matrix is included, because filling one would mean naming products nobody has checked. [GAP: **zero of the SOP's expected 3–5 competing products have been reviewed.** Close with `/competitor-analysis` scoped to expense capture and approval workflow, and file the teardowns in the shared competitors home. Owner: Michelle Tremblay. Needed before any external positioning claim, and before the M1 launch gate.]

---

## 4. BUSINESS GOALS & USER OUTCOMES

**North Star**

A Payworks client can run a whole expense cycle — spend, capture, approve, pay — inside Payworks, and the claimant never has to ask where their money is.

**Business goals**

- Make Expense the next module an existing payroll client turns on, contributing to **multi-module adoption 32% → 35%** (FY27 KR 1.4)
- Move **NRR toward 105%+** (FY27 KR 2.3) by giving renewal conversations something to add rather than a number that went up — the Controller named this as his own reason for taking the call
- Defend the **94%+ retention bar** (FY27 KR 1.3) in accounts where a standalone expense tool would otherwise establish a second system of record next to payroll
- Give the accountant-and-bookkeeper channel a reason to bring a book of clients — the channel is 6.9% of the base and thinnest in Québec, exactly where the FY27 share target sits (M2, not M1)

**User outcomes**

- **The claimant** can capture a receipt at the counter, on a phone, with no signal, and afterwards can see the claim's state and its pay date without phoning anyone
- **The Administrator / Controller** can write their own approval policy — by dollar band, by location, by position — and have it survive a person changing chairs
- **The approver** gets prompted where they actually are, including when they have no company email address
- **The Administrator** sees the expense total on the payroll register, clickable to the claim, *before* the register locks

**Strategy fit**

Expense Management (A/B 2.0) is named on the FY27 24-month roadmap under Accounting & Bookkeeping, and sits in the **wallet-share expansion** half of the portfolio — "Deliver more value for every client", whose measure is multi-module adoption (`current-quarter.md`). It is the right expression of that bet now because the competitive objection our own design partner raised — "it didn't talk to payroll" — is the one thing a standalone tool structurally cannot fix and the one thing "six integrated modules, one shared database" is supposed to mean.

**Hypothesis**

If we let a claimant capture a receipt *and its site code* at the point of purchase on a phone, then the finance-side coding effort per claim will fall far enough to remove the month-end keying block (2.5 days at Northwind) and the claim-to-paid interval will fall from weeks to one pay cycle, because the only moment the site is reliably known is the moment the person is standing at it.

**Key hypotheses** — full inventory in [`reviews/expense-management-vp2-assumption-map.md`](reviews/expense-management-vp2-assumption-map.md) once it exists.

| Hypothesis | Risk lens | Confidence | Validation route | Priority |
|------------|-----------|------------|------------------|----------|
| A crew member will code the site at the counter rather than skip it — capture without coding just relocates the shoebox | Desirability | Low | Breadth Prototype with Northwind supervisors, then instrumented in MJ-02 | 1 `[GAP: unranked — run /assumption-map]` |
| A reimbursement can ride a pay run without touching taxable, pensionable or insurable earnings, and without breaking register lock | Feasibility | Low | `/code-qa` on the payroll repo, or an engineering consult — no code access is configured today | 2 `[GAP: unranked — run /assumption-map]` |
| Employers want a *fence* on mobile approval above a threshold, not more mobile | Desirability | Med | Two accounts asked for it independently (2026-08-20, 2026-08-27); test with a third | 3 `[GAP: unranked — run /assumption-map]` |
| One employee record can carry pre-hire, unposted and active claimants on one axis without becoming a nullable trap every module has to check | Feasibility | Med | MJ-01 Translation Checkpoint; settled in part by the 2026-08-26 decision | 4 `[GAP: unranked — run /assumption-map]` |
| Employers will configure their own approval tiers correctly, and configurability will not become the burden a 75-person account says it is | Usability | Low | Prototype the configuration step with Acme specifically | 5 `[GAP: unranked — run /assumption-map]` |

**Impact by lever**

| Lever | Primary? | Estimate | Basis |
|-------|----------|----------|-------|
| Acquisition | not this bet | — | M1 targets the existing payroll base; the channel-led acquisition story is M2 |
| Activation | not this bet | — | Module activation matters, but the bet is not sized on it |
| Retention | **yes** | Accounts where a standalone tool would become a second system of record | [GAP: no churn-risk baseline; retention 94%+ is a stated FY27 bar, not a current reading (`business-info.md` → Key Metrics). Cannot be sized without it. Owner: Michelle Tremblay via `/impact-sizing` once a baseline exists] |
| Expansion / LTV | **yes** | Contribution to multi-module 32% → 35% | Reach denominator is real (43,550 active accounts; 26.6–28.9% multi-module on the computed definitions). [GAP: ARR unavailable, so no dollar figure; and Payworks' own definition of "multi-module" is not stated in any source, so the 32% and the computed 26.6/28.9% are not yet the same metric] |
| Cost to serve | not this bet | — | The 2.5 days a month is the *customer's* cost, not ours; it is a value claim, not a Payworks cost saving |

---

## 5. KPI FRAMEWORK

> Baselines below are largely absent by fact, not by omission: Expense is not in market, `analytics/metrics/` is empty, and VP1's limited launch was not instrumented. Payworks' own house rule applies — *"where a baseline is not yet available the metric is marked 'Coming soon' — do not fabricate numbers"* (`business-info.md` → Metric Reporting Conventions). Product Leadership accepted the framework on that basis at the 2026-08-25 approval.

**Tier 1 — Outcome Metrics** (the business result)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| Expense module attach rate on the existing payroll base | 0 — not in market (`feature-index.yaml`: Expense Management, "not yet in market") | [GAP: no attach target set — needs the multi-module definition confirmed first; VP, Product Management to set. Owner: Michelle Tremblay to escalate] | 2 quarters post-launch | Lagging |
| Contribution to multi-module adoption (FY27 KR 1.4) | 32% stated in the FY27 strategy; independently computed 26.6% / 28.9% depending on definition (`segmentation-matrix.md`) | 35% company-wide; Expense's share of that unallocated | FY27 | Lagging |
| Retention in accounts that adopt Expense vs matched non-adopters | Coming soon [GAP: no retention baseline is stated anywhere — 94%+ is a bar to defend, not a reading. Owner: analytics, once a metric doc exists] | Hold 94%+ | 2 quarters post-launch | Lagging |

**Tier 2 — Product Metrics** (adoption and engagement)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| **Capture-at-source rate** ★ — share of claim lines whose receipt was captured within 24h of the purchase timestamp | Coming soon — no product exists to measure | [GAP: threshold unset — no baseline; Michelle Tremblay sets it from the first 30 days of MJ-02 telemetry] | Day 30 | Leading |
| Coding-at-capture rate — share of captured lines carrying a site/job code at capture | Coming soon | [GAP: threshold unset — same route] | Day 30 | Leading |
| Claim-to-paid interval (median and p90), purchase → money received | Northwind today: up to ~1 month for a purchase that misses the A/P Monday cutoff `[Evidenced — 2026-08-27]`; no product baseline | One pay cycle for pay-run claims | Day 60 | Lagging |
| Approval cycle time, submission → final approval (median, and p90 for the top tier) | Northwind today: top-tier approvals "can sit for eleven days", 6–8 times a year `[Evidenced]` | [GAP: threshold unset — set with Northwind at the prototype round] | Day 60 | Leading |
| Claimant status checks per claim (a proxy for "did it go through") | Coming soon | Falling over time | Day 90 | Leading |

**Tier 3 — Quality Metrics** (stability and performance)

| KPI | Baseline (source) | Target | Timeline | Type |
|-----|-------------------|--------|----------|------|
| Offline capture loss rate — receipts captured on-device that never reach the server | Coming soon | 0 | Day 7 | Leading |
| Register integrity defects — pay runs where the expense total changed after the register was approved | Coming soon | 0 — any occurrence is a stop-ship | Day 7 | Leading |
| Taxability defects — reimbursements posted to taxable, pensionable or insurable earnings, or to a T4 box | Coming soon | 0 — any occurrence is a stop-ship | Day 7 | Leading |
| Expense-tagged support ticket volume | Coming soon [GAP: support ticket volume is not currently tagged by module in any source available to this repo. Owner: Michelle Tremblay with Service] | [GAP: threshold unset] | Day 60 | Lagging |

★ = the primary metric for this release.

**Guardrails** (must not harm)

- **Payroll run success rate** must not fall at all — watched on every run in the first two months, and at the Day 7 checkpoint
- **Median mobile approval decision time** must not fall below the point where an approval stops being a decision — the "tap yes in a parking lot" risk the Controller named. [GAP: threshold unset — no baseline for what a considered approval takes; Michelle Tremblay to set from the first 30 days, with Vanessa Lee]
- **Administrator configuration abandonment** — accounts that begin approval-tier setup and do not finish must not exceed [GAP: threshold unset]; watched because Acme told us configurability is itself a cost at 75 people
- **Claims paid but not billed on** — mis-coded billable materials must not rise above today's rate. [GAP: today's rate is unmeasurable at Northwind; the Controller's own estimate of unreadable/lost receipts is $3,000–$4,000 a year]

**Kill metrics**

- Coding-at-capture below [GAP: threshold unset] at Day 60 → we built a digital shoebox. Diagnose whether the site step is too slow or the site list is wrong; if it is wrong on both, stop before MJ-04 and re-cut.
- Capture-at-source below [GAP: threshold unset] at Day 60 → capture is not happening at the counter, which is the whole bet. Diagnose device, signal, or habit; pause MJ-03 scope growth until it is understood.
- **Any** register-integrity or taxability defect in production → stop the pay-run path immediately, fall back to the A/P destination, and do not resume until root cause is closed. No threshold; one is too many.

**Checkpoint schedule**

| Checkpoint | What we're checking |
|------------|---------------------|
| Day 7 | Zero taxability and register defects; offline queue drains; no critical capture failures |
| Day 30 | First capture-at-source and coding-at-capture read against target |
| Day 60 | Approval cycle time, claim-to-paid interval, and the mobile-approval guardrail |
| Day 90 | Attach rate, retention read on adopters, and whether status-check volume is falling |

**Prior-release baseline (reference)**

| KPI | Result | Type |
|-----|--------|------|
| VP1 (mobile-first claim + first approval step, shipped 2026-08-21 to a limited group) | [GAP: **no results exist.** VP1 shipped before this OS instance was populated and carries no launch-gate verdict, no telemetry plan and no metric definitions (`expense-management-vp1.md`). The only recorded outcome is a support case three weeks in — a new salaried hire expensed a hotel before their first pay run, which is why MJ-01 carries an `unposted` state. Owner: Michelle Tremblay — decide whether a retrospective read is worth the effort before M1 launch] | — |

---

## 6. PROPOSED SOLUTION

**How it works**

A claimant records what they spent at the moment they spend it — on a phone, at the counter, with or without signal — and answers one question the finance side cannot answer later: which site or job this was for. The claim then routes to whoever the employer's own policy says should see it, by dollar band, by location and by position rather than by person, escalating on its own if nobody acts. When it is approved it becomes money: either on the pay run as a reimbursement that never behaves like income, or through the employer's existing accounts-payable path. Throughout, the claimant can see the claim's state and, once it is scheduled, its pay date.

Two surfaces are being created (mobile capture, approval routing) and one is being extended (the payroll run and its register). The register today shows regular pay and overtime and is approved and locked by the Administrator before transmission; this release adds an expense total to it that is visible before the lock, clickable through to the claims behind it, and impossible to change after the lock.

**Feature set — Capture**

| Feature | Description |
|---------|-------------|
| Capture at source | The claimant records a receipt image, an amount and a site or job code at the point of purchase, from a phone. The site is the load-bearing field: it is the only thing the buyer knows and finance does not. |
| Offline-tolerant capture | If the device has no connection the claim is held on the device and the claimant can see that it is held and how many are waiting. Nothing is ever lost to a "try again". |
| Mileage without a receipt | A mileage line is kilometres × a rate, with no image at all. A different shape of claim, not a special case of a receipt. |
| Claim status for the claimant | Every claim carries a state the claimant can read, including — once scheduled — the pay date it will land on. |

**Feature set — Approval**

| Feature | Description |
|---------|-------------|
| Employer-configured approval tiers | Bands of dollar amount, scoped by location, routing to a position. An employer writes their own policy instead of choosing from ours. A band may route to nobody, which is how an auto-approve floor is expressed. |
| Position-based routing | Approval authority hangs off a position ("regional manager, Ontario west"), so replacing the person in the chair does not require rebuilding the routing. |
| Escalation on inaction | After an employer-set number of business days a pending approval moves on, with a notification and a permanent record of where it went and why. Never silent. |
| Approval-surface policy | An employer can require that approvals above a set amount be completed on a desktop session, and have that enforced rather than suggested. |
| Reaching approvers who have no email | Notification by in-app badge as well as email, because half of one design partner's field staff have no company email address on file. |

**Feature set — Where the money lands**

| Feature | Description |
|---------|-------------|
| Reimbursement on the pay run | An approved claim can post to the employee's pay run as a non-taxable reimbursement — never on a T4, never in pensionable or insurable earnings. |
| Register visibility before lock | The expense total appears on the payroll register before the Administrator approves it, as a total that opens into its underlying claims in one step. |
| Register lock integrity | Once the register is approved, no expense can enter that run. Claims that miss the cutoff roll to the next run automatically, and the claimant sees the new pay date. |

**Why this beats the current workaround**

Against the shoebox it wins outright on paper survival, and it wins on coding for the first time — the workaround has no mechanism at all for capturing the site while the buyer still knows it. Against a standalone expense tool it wins on exactly the two grounds our design partner used to reject one: it knows the reporting line already (it is the same database as payroll), and it can put the money on the pay run.

Where it does **not** win, and we should say so: for an account like Acme, whose receipts are already PDFs in email, the capture story lands flat — their problem is people not submitting for four months, and a phone camera does not solve that. For Northwind on day one it does not win on money movement either, because their expenses come out of accounts payable and the A/P destination is M2 (§7). And an approval chain is a thing an employer has to configure; at 75 people that is a cost, not a benefit, and the Acme HR Manager said so plainly.

**Access & eligibility**

- Admin-enabled per account: an Administrator turns the module on and must configure at least one approval tier before any claimant can submit
- A claimant must have an employee record on the account and be able to sign in; MJ-01 defines which record states can hold a claim
- Employees outside the configured scope see nothing — the module does not appear for them
- [GAP: whether ~200 seasonal crew members at a single account need paid seats, and what happens to those seats in February, is an open commercial question — §10]

**Alternatives considered**

- **Extend VP1's claim as-is and skip a foundation Micro Job** — rejected: the same employee record is the seam that Onboarding and, next in the queue, Time and Absence build on. Doing it inside receipt capture would have produced a claimant-only record and forced three modules to fork it later.
- **Ingest fuel-card and corporate-card statements as the primary capture route** — rejected for M1: at Northwind the fuel card is already clean ("one file", ~$28,000 a month) and card feeds do not carry the site code, which is the thing that actually costs money.
- **Automatic extraction (OCR) of amount and vendor from the receipt image** — rejected for M1: it addresses the field the buyer already knows and not the field they don't. Revisit once capture volume exists to train against.
- **Route everything through accounts payable only, matching how our design partner works today** — rejected as the M1 target: the claimant-visible pay date and the "it didn't talk to payroll" objection both live on the payroll side. A/P remains real and is scheduled for M2, and this is a genuine cost carried in §7 and §10.

---

## 7. SCOPE & BOUNDARIES

**In this release (VP2, M1)**

- The employee-profile and expense-claim foundation, including the record states a claim can attach to — MJ-01
- Capture at source on a phone, offline-tolerant, with site/job coding at capture, and mileage as its own claim shape — MJ-02
- Employer-configured, position-based approval routing with escalation, the approval-surface policy, and badge notification — MJ-03
- Posting an approved claim to the pay run as a non-taxable reimbursement, with register visibility before lock and lock integrity after — MJ-04

**Scope boundary — documented but not included**

- **The accountant-and-bookkeeper firm view** (one login across a book of clients, firm-level roles such as "can code expenses, cannot transmit payroll") — **VP2 Milestone M2**. It is real and evidenced (Birchbark, 2026-08-18) and it is the channel half of the strategy, but it needs the claim object and the approval model to exist first.
- **The accounts-payable destination and its cutoff behaviour** — **VP2 Milestone M2**. Northwind pays expenses from A/P today and will keep doing so through M1. Carried as a named risk in §10.
- **Expense-to-GL mapping and journal-entry export** — **VP2 Milestone M2**. Approved claims mapped to employer GL account codes and exported as journal entries to the accounting system, so the Administrator and the bookkeeper can reconcile expense spend against the general ledger without a rekeying step. The Payroll module already ships `gl-integration` (live — journal entries and GL account mapping exported to the accounting system); this extends that pattern to approved expense claims. Deferred to M2 because it requires the claim record, approval model, and pay-run or A/P destination (M1 + M2a) before there is a settled claim object to export — and because the bookkeeper firm view (M2) is the primary consumer: the reconciliation output is most valuable when a bookkeeper can see all clients' expense GL state in one place, not client by client. [GAP: whether the existing `gl-integration` export format and account-mapping model extends to expense claims without schema change is unverified — requires Engineering confirmation before MJ-level scoping. Owner: Michelle Tremblay with Payroll Engineering.] [GAP: no customer evidence exists yet for GL reconciliation as an explicit ask — Northwind's Controller described job-code mis-coding as lost revenue, not a GL-reconciliation problem; Birchbark's bookkeeper described coding time (120 hrs/month), not a reconciliation gap. First-hand confirmation needed from the bookkeeper or A/P side before this feature enters M2's locked scope. Owner: Michelle Tremblay — add to the next Northwind and Birchbark sessions.]
- **Corporate card issuance** — deliberately never in this initiative (`expense-management-vp2.md`).
- **General ledger redesign** — deliberately never in this initiative (`expense-management-vp2.md`).
- **Fuel-card and corporate-card statement ingestion** — future Value Package. The one account with real volume says its card statements are already clean.
- **Automatic amount/vendor extraction from images (OCR)** — future Value Package; see §6.
- **Location-derived site suggestion** — deliberately out of M1. The Controller raised it himself and then ruled it out himself: "I don't want to be creepy about tracking guys… that's a whole other conversation with our union side." Revisit only with a customer-side labour-relations conversation completed first.
- **Recurring-subscription detection** (Acme's eleven monthly software subscriptions arriving as personal claims "for years") — named, not built. Future Value Package.
- **Seat and licence model for seasonal claimants** — not a product scope item; routed to Pricing & packaging (§10).

**Tradeoffs accepted**

- **Three to four weeks of MJ-02 slip**, accepted on 2026-08-26 in exchange for MJ-01 carrying a pre-hire state before it goes dev-ready. The alternative was Employee Onboarding building a second person record, costed at 11–12 weeks of two engineers and, more importantly, a second org chart under a "one shared database" promise.
- **Our most-evidenced design partner cannot use M1 end to end for money movement**, because their money leaves through A/P and A/P is M2. We accept that M1's pay-run path is validated against the *ask* rather than against their current process, and we revisit if the prototype round says the A/P gap makes the whole thing unusable for them.
- **Configuration burden at the small end.** The tiering model is built for the Controller's four bands; a 75-person account told us tiers add a thing to configure rather than oversight. We accept that and mitigate with a single-tier default, rather than shipping two different approval models.

> **Exception List.** This section is the brief-level statement. The build-level Exception List — one entry per locked Micro Job — is assembled in the [Micro Jobs Breakdown](expense-management-vp2-micro-jobs-breakdown.md) and travels in the Dev-Ready Bundle.

---

## 8. USER EXPERIENCE PRINCIPLES

**Capture must survive the worst moment it will meet.**

The moment a receipt exists in someone's hand is the only moment it is guaranteed to exist at all. Everything after that is decay: fading, envelopes, three weeks, a truck. So capture has to work with no signal, in a hurry, one-handed, and it has to visibly hold what it captured. If a claimant ever loses a receipt because the product told them to try again, that is a product gap, not an expected workflow. This rules out any capture flow that requires a round trip to succeed, and it rules out silent retry.

**A claimant should never have to ask whether it went through.**

The most common question finance receives is not "approve this", it is "did the thing I did land somewhere". Every claim therefore carries a state the claimant can read without asking anyone, and once it is scheduled it names its pay date. This rules out states that exist only in an administrator's view. If a claimant has to phone to learn where their claim is, that is a product gap.

**An approval must be an actual decision, and the product may enforce that.**

Where an employer says a decision needs attention, the product makes it need attention rather than encouraging it. This rules out treating "more mobile" as automatically better: an approval that can be granted without seeing what is being approved is a control that does not control anything, which is worse than no control. It also rules out the opposite mistake — forcing every approval to a desktop. The employer draws the line; we hold it.

**Authority follows the position, not the person.**

Approval routing is defined against a role in an org, and the org already lives on the payroll record. If a customer has to rebuild a routing table because somebody changed chairs, or maintain a Word document to remember who approves what, that is a product gap. This rules out per-person approver assignment as the primary model.

**Money that is not income never behaves like income.**

A reimbursement must not touch taxable, pensionable or insurable earnings, must not appear on a T4, and must not alter a payroll register after it has been approved. This is not a preference and it is not tunable; it outranks any convenience anywhere in the flow. If the two conflict, the flow gives way.

---

## 9. KEY DECISIONS & TRADEOFFS

**Decisions made**

**Mobile-first was right for capture and is wrong for high-value approval.**  VP1 chose mobile-first on 2026-08-06, over desktop-first parity and responsive web, for the reason that the people who spend the money have no desk (`expense-management-vp1.md`). That call stands and is reinforced — a route supervisor's office is a truck, and "anything you build for that layer of the company that assumes a browser on a desk is already dead. Not 'less good.' Dead." But two accounts independently asked for the *opposite* on approvals above a threshold: Acme's HR Manager wanted mobile approval blocked, not discouraged ("if you can approve it at a red light, you're not reading it"), and Northwind's Controller asked for it as an enforced setting ("if it's optional I'll do it in the parking lot… make it a setting I turn on, and then make it stick"). Both cited the same mechanism — approval quality collapses when the surface removes the context. The decision: mobile-first for capture and low-value approval; an employer-configurable, enforced desktop requirement above a threshold. [GAP: the standalone decision record for the VP1 mobile-first call is not yet filed in `product/decisions/` — Michelle Tremblay to file it via `/decision-log-entry` so the two-read lookup works. Its date and attendees come from that record.]

**Employee Onboarding reuses this Value Package's employee-profile foundation; MJ-01 grows a pre-hire state before it goes dev-ready.**  Decided 2026-08-26 (Michelle Tremblay, Claire Sutton, Margaret Foster, Vanessa Lee). The rejected option was Onboarding building its own person record in the HR module, costed at 11–12 weeks of two engineers. It was rejected for three reasons in this order: two records means two org charts under a product sold as "six integrated modules, one shared database"; the cost; and design drift — two records become two screens that diverge, and the person looking at them is a new hire in their first week. Research supported it — two design partners independently described the same wall, where an employee is real in one system and not in another. In exchange, MJ-01 gains a pre-hire state and a named extension point so Onboarding can add its own fields without shipping an expense release. The price is 3–4 weeks in front of MJ-02, accepted.

**An expense run above $5,000 on an employer with more than 150 employees requires a second approval before the payroll register can lock.**  A cross-module rule: it is an expense policy that constrains a payroll action. It exists because the register-lock guarantee is only as good as the review behind it, and because at scale the aggregate is where the exposure sits, not the individual claim. The $5,000 figure is deliberately the same round number our design partner uses for their own top tier — "round numbers are easy to remember and people actually follow rules they can remember." [GAP: the `expense-approval-threshold` decision record is not yet filed in `product/decisions/`. Michelle Tremblay to file via `/decision-log-entry`, with the payroll-side impact stated; the 150-employee boundary needs a rationale on the record — no source in this repo explains where it came from.]

**Tradeoffs**

- **Enforcing a desktop requirement costs speed for the approvers most likely to be away from a desk.** The Controller and the Acme HR Manager both accepted that trade explicitly ("some decisions should be slightly annoying"). We would revisit if approval cycle time at the top tier gets *worse* than today's eleven days.
- **Position-based routing means expense authority depends on the accuracy of the payroll org chart.** Whoever owns the HR record now indirectly owns who can approve money. That is the right seam, and it is also a new failure mode; §10 carries it as a risk.
- **Building the foundation as its own Micro Job costs a release cycle before anything visible ships.** Paid deliberately, because Time and Absence are next in the queue for the same record and a fork would leave them choosing whichever version finished first.

---

## 10. OPEN QUESTIONS, RISKS & DEPENDENCIES

**Open questions**

- [ ] Does the approval threshold apply to a single receipt or to the whole report? — @Michelle Tremblay — Northwind applies it to the report today and their Controller believes that is probably wrong, because it produces split submissions to stay under a tier ("it's not fraud… it's a guy who doesn't want to wait for the Ops Director"). Decide with two more accounts at the prototype round; it changes MJ-03's rule set.
- [ ] Is an auto-approve floor (a tier routing to nobody) right, or does it destroy a signal a manager needs? — @Michelle Tremblay — Acme's Payroll Administrator wants $250 and under to "just go"; Acme's HR Manager objects that the manager then loses the only window into what their people are buying. Test the middle option: the manager sees it without having to click.
- [ ] Do seasonal claimants need paid seats, and what happens to them in February? — @Michelle Tremblay to route to Pricing & packaging — one account alone would add ~200 people who have no login today, roughly half of them April-to-November. A cost answer changes who can submit, which changes MJ-03's persona set.
- [ ] Who is the A/P clerk, and what does her job actually require? — @Michelle Tremblay — she is the person absorbing 2.5 days a month, has never been interviewed, is not one of Payworks' seven personas, and the Controller has offered to bring her. Route: `/interview-guide` then `/process-meeting`.
- [ ] What is the mileage rate policy — per employer, or the CRA rate maintained by us? — @Michelle Tremblay — one account uses the CRA rate (72¢ for the first 5,000 km) and another was still on a prior year's rate because the claim form was a spreadsheet with the year in its filename. If we maintain it, it becomes a compliance obligation.
- [ ] Which record states may hold a claim? — @Michelle Tremblay — settled in MJ-01's draft (`unposted` exists; pre-hire being added) but not yet confirmed against what the payroll platform actually enforces.

**Risks**

**Risk — the digital shoebox.**  Capture succeeds and coding does not, so finance receives 650 photos a month with no site codes and still spends 2.5 days keying. The Controller named this himself: "I've moved the shoebox, I haven't emptied it." **Mitigation:** coding-at-capture is a Tier 2 metric with a kill threshold at Day 60; the site step is designed as one short list, not a search; and the Breadth Prototype tests the counter moment with actual supervisors before MJ-02 locks. Owner: Michelle Tremblay, with Vanessa Lee.

**Risk — a reimbursement is treated as income.**  A single claim landing in pensionable or insurable earnings, or on a T4, is a correctness failure in the one area Payworks sells as its moat. "If it does that once we'd have a very bad year." **Mitigation:** a stop-ship guardrail at zero occurrences; the atomic-transaction and earning-code questions are engineering confirmations that must be answered before MJ-04 leaves draft; and the fallback is the A/P destination. Owner: Michelle Tremblay with Engineering.

**Risk — the register stops meaning anything.**  If expenses can enter a pay run after the Administrator has approved the register, then the approval was not an approval. **Mitigation:** register lock is an acceptance criterion on MJ-04, not a quality goal; claims that miss the cutoff roll forward automatically and the claimant is told the new date. Owner: Michelle Tremblay.

**Risk — approvals reach nobody.**  Half of one design partner's field staff have no company email address on their Payworks file — the same root cause that stops their review system pulling an employee. An email-only notification story silently excludes exactly the people this release is for. **Mitigation:** in-app badge notification is in MJ-03's scope, not deferred. Owner: Michelle Tremblay.

**Risk — our best-evidenced partner cannot use M1.**  Northwind's money leaves through accounts payable, and the A/P destination is M2. If the prototype round says the pay-run path alone is unusable for them, M1's validation set drops to accounts with far less volume. **Mitigation:** ask that question directly at the prototype round and be willing to pull the A/P destination forward into M1. Owner: Michelle Tremblay.

**Risk — the org chart becomes a money control.**  Position-based routing makes expense authority depend on payroll's reporting lines being current. A stale reporting line now misroutes money, not just a task. **Mitigation:** escalation on inaction bounds the damage, and every routing decision is recorded with who it went to and why. [GAP: whether the payroll record actually carries a position — as distinct from a person and a manager — is unverified. Engineering confirmation required before MJ-03 leaves draft.]

**Dependencies**

- **MJ-01, the employee-profile and claim foundation** — everything in this Milestone attaches to it. Owned by: Michelle Tremblay / Engineering. Required by: MJ-02, MJ-03 and MJ-04 all start from it. Estimated at 11 weeks of two engineers from the Translation Checkpoint, plus 3–4 weeks for the pre-hire state.
- **The payroll register and pay-run mechanics** — MJ-04 extends an existing surface rather than creating one. Owned by: Payroll engineering. Required by: MJ-04. [GAP: **no code access is configured** — `engineering/code-repos.yaml` registers no repo, so no claim in this brief about what the payroll platform does today has been verified against code. Close with `/connect-code` and then `/code-qa`. Owner: Michelle Tremblay.]
- **A non-taxable reimbursement earning code** — must exist, or must be created, and must be excluded from T4, pensionable and insurable earnings. Owned by: Payroll engineering / Compliance. Required by: MJ-04. [GAP: existence unverified.]
- **Employee Onboarding** — consumes MJ-01's extension point and has a November pilot that depends on MJ-01 landing. Owned by: Claire Sutton. Required by: MJ-01 dev-ready.
- **Design capacity for the Breadth Prototype** — Owned by: Vanessa Lee (Curtis Boyd, Design lead). Required by: the 3–4 week commitment made to Northwind on 2026-08-27. Vanessa also owns the profile-screen extension-point layout question, to be settled before the MJ-02 Dev-Ready Bundle.
- **Pricing & packaging** — the seat question for seasonal claimants. Owned by: [GAP: no owner named for the Pricing & packaging corporate initiative in any source]. Required by: before M1 launch conditions can be written.

---

## 11. ROLLOUT & ITERATION PLAN

**VP2 M1 — date TBD**

It waits on MJ-01 going dev-ready, which waits on the Translation Checkpoint and on the pre-hire state added by the 2026-08-26 decision. No launch date is committed; VP2 has already moved once, from the June milestone to the September one.

- Rollout shape: incremental per Micro Job as each completes, not a single release. MJ-01 ships invisibly; MJ-02 is the first thing a claimant meets.
- Who gets it and when: Design Partners first, on invitation, then admin-enabled availability. General availability is not part of M1.
- Configuration required: yes, and it is not optional — an Administrator must configure at least one approval tier before any claimant can submit.

**Launch conditions**

- [ ] Zero taxability defects and zero register-integrity defects in staging, tested explicitly rather than assumed
- [ ] Offline capture verified with the network genuinely unavailable, including the visible pending count and drain-on-reconnect
- [ ] A non-taxable reimbursement earning code confirmed by Engineering as existing and correctly excluded from T4, pensionable and insurable earnings
- [ ] Approval routing verified against a real customer org, including a position with no person in it
- [ ] Monitoring and escalation plan agreed for the first four pay runs that carry expenses
- [ ] Comms plan agreed with the channel — Birchbark asked for two weeks' notice of any client-visible change
- [ ] `/competitor-analysis` run and at least three competing products reviewed, so the positioning claim is grounded
- [ ] `/product-brief-challenge` run against this brief and its ranked assumptions folded into §10

**VP2 M2 — accounts-payable destination, firm view, and GL reconciliation**

Already known to be deferred here: the A/P destination with its own cutoff behaviour; the accountant-and-bookkeeper firm view (one login across a book of clients, firm-level roles that separate coding rights from payroll-transmit rights, and a way to see which clients are falling behind before February); and **expense-to-GL mapping and journal-entry export** — approved claims mapped to GL account codes and exported as journal entries to the accounting system, extending the live `gl-integration` pattern in Payroll. The GL reconciliation scope is the most evidence-light of the three; it requires both first-hand confirmation (see §7 gap) and Engineering feasibility input before it can be broken into Micro Jobs. Its scope will be informed by the M1 prototype round, by whether Northwind's A/P gap proves blocking, and by the next Northwind Controller and Birchbark Bookkeeper sessions.

**Future expansion**

Card-feed ingestion, automatic extraction from images, recurring-subscription detection, and site suggestion from device location — the last only if a customer-side labour-relations conversation clears it. Directional, not committed.

---

## 12. APPENDIX

**Changelog**

| Date | Change | Who |
|------|--------|-----|
| 2026-08-31 | Added GL reconciliation (expense-to-GL mapping and journal-entry export) to VP2 M2 scope boundary in §7 and M2 rollout description in §11. Two gap markers placed: Engineering format-compatibility unverified; no first-hand customer signal yet for this specific capability. Catalog entries for the expense-management area proposed (gated — awaiting PM yes). | Michelle Tremblay |
| 2026-08-31 | Amended after the 2026-08-27 Controller call: added the register-lock and taxability conditions, position-based routing, the approval-surface policy, offline capture, and the notification-reach risk. Reopened §5 targets and §7's A/P boundary. | Michelle Tremblay |
| 2026-08-26 | §9 records the employee-profile foundation decision and the 3–4 week MJ-02 cost accepted with it. | Michelle Tremblay |
| 2026-08-25 | Product Leadership Approval recorded. KPI Framework accepted with baselines marked "Coming soon" per the house rule, given the module is not in market. | Michelle Tremblay |
| 2026-08-21 | VP1 shipped mobile-first to a limited group; §1 rewritten to state what VP1 established. | Michelle Tremblay |

**Impact sizing detail** (the funnel behind §4's reach numbers)

| Funnel stage | Users | Drop-off reason |
|--------------|-------|-----------------|
| Sees it | 43,550 active payroll accounts | — |
| Eligible | [GAP: unknown — no source identifies which accounts have expense volume, or already run expenses elsewhere] | Accounts with no expense process at all, or one they will not move |
| Engages | [GAP: no baseline — the module is not in market and VP1's limited launch was not instrumented] | Administrator does not complete approval-tier configuration |
| Completes | [GAP: no baseline] | Claimants do not capture at source; coding step skipped |

The funnel is deliberately empty below the first row. Run `/impact-sizing` once an attach baseline exists; a modelled number here would be an invention, not an estimate.

**Source material**

- `inbox/2026-08-27-northwind-landscaping-expense-call.txt` — Controller + HR Manager; the primary evidence base for §§2, 5, 6, 9 and 10. Raw record; summary pending `/process-meeting`
- `inbox/2026-08-20-acme-corp-call.txt` — HR Manager + Payroll Administrator; the small-office counter-case and the mobile-approval objection
- `inbox/2026-08-18-birchbark-books-call.txt` — Firm Principal + Senior Bookkeeper; the channel evidence behind the M2 boundary
- `inbox/2026-08-26-internal-product-sync.txt` — the employee-profile foundation decision and MJ-01's estimate
- `inbox/payworks-source-material/2026-08-05-northwind-landscaping-client-call-reverse-demo.vtt` — the A/P routing fact and the Controller introduction
- `product/strategy/current-quarter.md` — FY27 objectives, the roadmap position of A/B 2.0, and the strategic refusals
- `product/strategy/business-context/business-info.md` — ICP, the seven personas, the channel motion, Key Metrics and the Metric Reporting Conventions this brief's §5 follows
- `product/strategy/business-context/segmentation-matrix.md` — every account count in §3, and the standing ARR gap
- `product/initiatives/expense-management-vp1.md` — the 2026-08-06 mobile-first decision and VP1's shipped scope
- `product/initiatives/expense-management-vp2.md` — scope, goal and the open loops this brief inherits

---

Payworks Confidential  |  Updated 2026-08-31
