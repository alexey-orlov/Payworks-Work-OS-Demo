---
status: active
note: "Cross-module scoping — origin evidence is one customer artifact and a 45-second exchange; the offboarding half is still owed"
updated: 2026-08-31
owner: "Claire Sutton"
areas: [onboarding, human-resources, payroll, employee-self-service]
features: []
customers: [maplewood-recreation]
---

# Employee Onboarding (HR 2.0)

## Snapshot

- Onboarding as its own module — HR 2.0 on the 24-month roadmap, sitting beyond the onboarding checklists Human Resources ships today. Cross-module by nature: a hire touches the **HR** record, **Payroll** setup, and the **Employee Self Service** surface the new person actually sees, and today those are three separate acts.
- **The origin is real, and it is small.** This initiative exists because of a 45-second exchange at the very end of the 2026-07-08 Maplewood Recreation interview — after an hour on performance management, Margaret Foster raised the onboarding/offboarding workstream and the customer's **Payroll Manager** turned out to have already sent in an artifact.
- What that exchange actually established, and nothing more: Payworks is looking at onboarding and offboarding with the goal of *"how can we simplify the experience"*; the Payroll Manager had emailed *"a massive Excel spreadsheet"* mapping their onboarding process; Payworks has read it, shared it internally, and queued it — *"that's next on our bucket"*; and the **offboarding equivalent is promised but unfinished**, held up by seasonal volume: *"We just did 300 plus on the SPR side, so we're just trying to do ROEs and get everything all dialed up for that."*
- What it did **not** establish: any pain, any current-state process detail, any system inventory, any requirement. Recording that honestly is the point — an initiative born from a passing mention is exactly the kind that gets over-scoped from a single line of transcript.
- "Done" for the discovery phase = the two process maps in hand, read against what the product does today, with a scoped problem statement that says which of the three modules owns which step.

## Scope & goal

- **Goal:** close part of the **39% HR gap** in win-loss exits by making the hire-to-first-payroll path a single flow instead of three, and add Onboarding to the wallet-share expansion set that carries the **32% → 35%** multi-module target.
- **In scope:** the hire-to-first-pay path across HR record creation, payroll setup and the new hire's self-service experience; the offboarding mirror of it, including the ROE trigger that seasonal employers live and die by.
- **Out of scope:** recruiting and applicant tracking (HR 3.0, and Applicant Tracking is already live); learning management; anything that turns this into a general HR-records rebuild.
- **Not yet scoped, on purpose:** which module owns which step. That is the first real decision and it needs the process maps, not a whiteboard.

## Instructions

- Origin evidence is thin and must not be inflated: one 45-second exchange plus an onboarding process map supplied by Maplewood's payroll manager. The offboarding map is promised, not delivered. Any pain narrative or requirement needs a source beyond the 2026-07-08 record. Cross-module by nature — check the HR, Payroll and ESS surfaces before scoping a step.

## Sources

- [2026-07-08 Maplewood Recreation interview](../../inbox/payworks-source-material/2026-07-08-maplewood-recreation-interview.vtt) — the origin exchange, at the very end of the call
- Maplewood's onboarding process map (Excel, emailed to Margaret Foster) — **not in the repo**; hold the file until it can be folded in through `/context-update`
- [customers/accounts/maplewood-recreation](../customers/accounts/maplewood-recreation/account-context.md) — the account, its seasonal workforce and its ROE volume
- [strategy/current-quarter.md](../strategy/current-quarter.md) — HR 2.0 on the roadmap and the 39% HR win-loss gap
- [strategy/business-context/business-info.md](../strategy/business-context/business-info.md) — the seven personas, and what "the Administrator" already carries at hire time

## Artifacts

- Product Brief: [PENDING: product/PRDs/onboarding/employee-onboarding-product-brief.md]
- Assumption map: -
- Challenge report: -
- Micro Jobs Breakdown: -
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

- 2026-08-26 — [Onboarding Profile Foundation](../decisions/2026-08-26-onboarding-profile-foundation.md) — reuses expense VP2 MJ-01; MJ-01 gains pre-hire state + named extension point; MJ-02 pushed 3–4 weeks
- 2026-08-26 — [Onboarding Pilot ESS Scope](../decisions/2026-08-26-onboarding-pilot-ess-scope.md) — pilot scoped to ESS only (new hire self-serve); admin side deferred; target November; sequencing call, not a ranking of problems

## Open loops

- **Theirs** — Maplewood's Payroll Manager to send the **offboarding** process map; blocked behind a 300+ seasonal ROE batch as of 2026-07-08. Owner: Claire Sutton to follow up through the account.
- **Mine** — Payworks committed to come back to them when the onboarding map is worked: *"we will ping you as well when we get to that."* That promise is outstanding. Owner: Claire Sutton. **Partial progress 2026-08-26:** Claire Sutton committed to read the spreadsheet and respond this week.
- **Mine** — the onboarding Excel map is not in the repo. Fold it in through `/context-update` so the initiative stops depending on an email attachment. Owner: Claire Sutton.
- **Mine** — no second account has spoken to onboarding yet. One customer's process map is a map, not a pattern. Owner: Claire Sutton.
- **Mine** — who owns the org chart? Both 2026-08-26 decisions assume the org relationship lives on the payroll record and everything else copies it. Payroll did not confirm this. Add to Open Questions & Risks on the Product Brief. Owner: Claire Sutton.
- **Mine** — new hire user experience is unresearched. All 13 summer interviews involved HR/payroll managers; zero new hires. The ESS pilot will address this, but no current evidence base exists. Owner: Claire Sutton.

## Activity

- 2026-08-31 — Initiative page created; origin recorded from the Maplewood record with the evidence limits stated on the page.
- 2026-07-08 — Origin: the Maplewood onboarding/offboarding exchange; onboarding process map received, offboarding map promised.
- 2026-08-26 — Two decisions made at internal product sync: onboarding reuses expense VP2 MJ-01 profile foundation (pre-hire state + named extension point added); pilot scoped to ESS only targeting November. ([summary](../meetings/other/summaries/2026-08-26-internal-product-sync.md))
