---
status: active
note: "In definition — no VP Product Brief yet; the Controller conversation is the open evidence gap"
updated: 2026-08-31
owner: "Michelle Tremblay"
areas: [expense-management]
features: []
customers: [northwind-landscaping]
---

# Expense Management VP2 (A/B 2.0)

## Snapshot

- The second Value Package of the Expense Management module — the wallet-share expansion bet named in the FY27 strategy alongside Perform, Onboarding and Comp. VP1 shipped mobile-first to a limited group; VP2 is the package that has to stand on its own with clients and through the accountant-and-bookkeeper channel.
- **In definition.** No VP Product Brief exists yet. What exists is a thin problem statement, VP1's shipped scope, and one first-hand customer thread.
- **The evidence base is deliberately narrow, and saying so matters.** Across thirteen design-partner records, expense management appears in exactly one: the 2026-08-05 Northwind reverse demo, for roughly ninety seconds at the end of the call. Everything else this initiative might claim about expense behaviour is currently unbacked.
- What that one thread gives us: claims route **claimant → approver → accounts payable**, *not* through payroll; the claimant is satisfied (*"I usually get my expense account in a relatively fast manner, so I have no complaints"*); expense support currently sits in QuickBase alongside safety and claims tracking; and the pain, if any, is on the A/P side and unmeasured.
- What it does **not** give us: receipts, mobile capture, corporate cards, approval thresholds, reimbursement volumes or cycle times. None of those words appear on any record. They are hypotheses.
- "Done" for VP2 = a Value Package a Payworks client and a channel firm can both run expenses on end to end, with the payroll-side and A/P-side boundaries settled rather than assumed.

## Scope & goal

- **Goal:** move multi-module adoption toward the FY27 target of **32% → 35%** and NRR **toward 105%+** by making Expense the next module an existing payroll client turns on. The module-level measure is attach rate on the existing base; the Value Package measure is whether a client can run a full claim cycle without leaving Payworks.
- **In scope:** claim submission and the approval chain; where an approved claim lands (the A/P vs payroll boundary — Northwind's runs to accounts payable, and that is the fact to design against); the channel view for a firm administering expenses across client databases.
- **Out of scope for VP2:** anything VP1 already shipped (see [expense-management-vp1](expense-management-vp1.md)); corporate card issuance; general ledger redesign.
- **Unresolved, and blocking scope:** whether receipt capture, approval thresholds and mobile access belong in VP2 at all. They are the recurring asks in the plan of record, but no design-partner record states them. The Controller conversation is what turns them from hypotheses into scope.

## Instructions

- Expense claims at Northwind route to accounts payable, not payroll — never assume a payroll path. First-hand evidence is one ~90-second thread in the 2026-08-05 reverse demo; the Controller conversation has not happened. Mark anything beyond it with a gap marker rather than borrowing from the performance corpus.

## Sources

- [2026-08-05 Northwind reverse demo](../../inbox/payworks-source-material/2026-08-05-northwind-landscaping-client-call-reverse-demo.vtt) — the only first-hand expense evidence in the corpus; the expense thread is at the end of the call
- [expense-management-vp1](expense-management-vp1.md) — what shipped, and the scope decisions behind it
- [strategy/current-quarter.md](../strategy/current-quarter.md) — the FY27 test and the win-loss gaps this work is measured against
- [strategy/business-context/business-info.md](../strategy/business-context/business-info.md) — personas, channel motion, portfolio role of the expansion modules
- [strategy/business-context/segmentation-matrix.md](../strategy/business-context/segmentation-matrix.md) — segment denominators for any sizing
- [customers/accounts/northwind-landscaping](../customers/accounts/northwind-landscaping/account-context.md) — the account the Controller referral came from

## Artifacts

- VP Product Brief: [PENDING: product/PRDs/expense-management/expense-management-vp2-product-brief.md]
- Assumption map: -
- Challenge report: -
- Micro Jobs Breakdown: [PENDING: product/PRDs/expense-management/expense-management-vp2-micro-jobs-breakdown.md]
- Micro Jobs: -
- Impact sizing: -
- User insights: -
- Competitive analysis: -
- Pre-mortem: -
- Eng plan: -
- Metrics: -
- Experiments: -
- Launch checklist / gate verdict: -

## Decisions

- 2026-08-06 — [Expense Approval Threshold](../decisions/2026-08-06-expense-approval-threshold.md) — $5k default, 150-employee auto-on, cross-module into Payroll
- 2026-08-26 — [Onboarding Profile Foundation](../decisions/2026-08-26-onboarding-profile-foundation.md) — MJ-01 shared with employee onboarding; gains pre-hire state + named extension point; MJ-02 (receipt capture) pushed right 3–4 weeks

## Open loops

- **CLOSED 2026-08-27** — Controller call held. Receipt capture, approval thresholds, payroll register integration, and status visibility are now first-hand evidence, not hypotheses. See [2026-08-27 call summary](../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md).
- **Mine** — Resolve threshold scope question: per-receipt or per-report? Controller said today it is per-report and "probably not right." Owner: Michelle Tremblay. Due: 2026-09-10.
- **Mine** — Validate non-taxable payroll treatment with Engineering: T4, CPP, EI implications. Hard go/no-go for register integration. Owner: Michelle Tremblay. Due: 2026-09-10.
- **Mine** — Define seasonal licensing model for ~200 crew-member submitters (April–November). Cost question flagged by Controller. Owner: Michelle Tremblay. Due: 2026-09-10.
- **Mine** — MJ-02 (receipt capture) has been pushed right 3–4 weeks to accommodate the pre-hire state addition to MJ-01. Owner: Michelle Tremblay to update MJ-02 milestone date.
- **Mine** — the Expense Management module carries no feature entries in the catalog (`features: {}`). The first VP2 brief has to propose them as `status: planned` in the same gated change. Owner: Michelle Tremblay.

## Activity

- 2026-08-27 — Controller expense discovery call with Northwind Landscaping: first substantive client-side evidence on receipt capture (site attribution is the unlock, photo is table stakes), approval chain (position-based, per-yard, auto-escalate, desktop-enforce above threshold), payroll register integration (non-taxable, pre-lock visible, clickable drill-down, auto-roll at cutoff), and status visibility ("approved, paying on the 11th"). Four feature-request records filed. Renewal horizon confirmed; A/P clerk invited to next session in 3–4 weeks. ([summary](../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md))
- 2026-08-31 — GL reconciliation (expense-to-GL mapping and journal-entry export) added to VP2 M2 scope boundary in the Product Brief (§7, §11). Two gap markers placed: Engineering format-compatibility unverified; no first-hand customer ask on record yet. Catalog entries for the expense-management area proposed (gated).
- 2026-08-31 — Request triage: "Match submission/approval to device", "Define approval routing without rulesets burden", and "Attach receipts in form they arrive" routed Act Now ([board](../strategy/feature-requests-expense-management-vp2.md)); receipt capture and approval-threshold hypotheses confirmed from both channel (birchbark-books) and direct-client (acme-corp) sides.
- 2026-08-31 — Initiative page created; scope framed against VP1 and the single expense record, with the evidence gap stated rather than filled.
- 2026-08-05 — Expense surfaced unprompted on the Northwind reverse demo: current flow is claimant → Head of HR → accounts payable, and the Controller was offered as the next conversation.
- 2026-08-26 — Internal product sync: MJ-01 profile foundation agreed as shared with employee onboarding; gains pre-hire state + named extension point; MJ-02 (receipt capture) pushed right 3–4 weeks. Acme visit surfaced second signal against mobile approvals and physical capture assumptions. ([summary](../meetings/other/summaries/2026-08-26-internal-product-sync.md))
