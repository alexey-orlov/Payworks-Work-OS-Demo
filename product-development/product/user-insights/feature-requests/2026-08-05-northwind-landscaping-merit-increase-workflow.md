---
account: northwind-landscaping
requested: 2026-08-05
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-05.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Carry review scores into the merit increase step, instead of re-keying them into a spreadsheet

**Who asked:** Their HR Manager at Northwind Landscaping, on a 2026-08-05 reverse demo. She shared her screen and walked the entire merit chain, including the live workbook at the centre of it, on the condition that no names were spoken. The Head of HR owns the workbook; the HR Manager describes herself as her second set of eyes.

**The underlying need:** a completed review score should reach the increase decision, and then payroll, without a human retyping it. Every step of Northwind's merit workflow exists only because the score cannot move. Note this spans two modules — the score starts in Performance Management and ends in Payroll — and it is the boundary the Performance Management discovery explicitly holds in scope, distinct from compensation management as a module.

**What they do today instead — the full chain, in order:**

1. Reviews close in QuickBase in January, before any merit conversation starts.
2. Payroll pulls a salaried extract out of Payworks with a requested column set (employee number, payroll group, status, name, occupation, employee type, start and seniority dates, earnings, effective date, prior-year rate changes, cost centre, reports-to).
3. The Head of HR splits the extract by department or senior leader into one tab per manager, saves a copy per manager and emails each one out. She is *"the keeper of the spreadsheet."* Packs are regional — the one shown was Ontario only.
4. Each manager opens QuickBase, reads their people's scores off screen and **re-types them into their tab** — QuickBase has no export. They also enter a recommended percentage increase and verify the employee data on the tab.
5. Tabs come back one email at a time and are reassembled by hand; names are re-checked, employment status re-verified, missing entries chased.
6. Eligibility (employed before June 1; a promotion after that date disqualifies) is applied by reading hire and rate-change dates row by row.
7. The Head of HR reconciles rating against recommended percentage **by eye, one employee at a time**. An anomaly triggers a phone call to the manager rather than a look at the review. No report exists to check the sheet against QuickBase, and whether that check ever happens is unknown even to the HR Manager.
8. A company merit pool (*"2.5% or 3%"*) gives each manager a total percentage to allocate and not exceed; managers may depart from the rating-to-percentage guideline.
9. The executive/ownership team reviews the workbook and **the Owner signs it personally**.
10. The signed sheet goes back to payroll and the Payroll Administrator re-uploads the increases and retros into Payworks — into the system that produced the extract in step 2.
11. The last round landed against a hard cutoff: signed sheet from the Owner Monday night, payroll cutoff Wednesday at noon, payday Friday.

*"Aha! So here's the biggest challenge. I mean, this is… this is a bit barbaric to what I know you can create for us." — Their HR Manager*

*"I have to take all those scores and get them into our… another spreadsheet to be able to say, here's what the scores are" — Their HR Manager*

*"It's gotta be the worst spreadsheet you've ever experienced." — Their HR Manager*

*"it's that whole other nightmare of trying to get these scores, and then next year we're gonna do the exact same thing." — Their HR Manager*

*"Just going through… it's just very manual. It's just a very manual process." — Their HR Manager*

**Signal strength:** strong, and it is the pain that motivated the customer to run the session at all. She proposed the walkthrough herself, narrated the workflow as the answer to "what's not working today," and volunteered to bring her manager group back for a separate session on this step specifically — *"we'll still use those same managers to walk us through How they find that horrible process."* Two of the four risks on this account's portfolio entry come from this workflow. Caveat for ranking: Northwind's compensation model (company pool, per-manager percentage allocation, manager discretion over the recommendation) is one of four incompatible models across the design partners, so the handoff must be built to be model-agnostic rather than to this account's shape.

## Draft ticket

**Objective:** Make a completed review score usable by the merit/increase step inside Payworks — so that the rating, the recommended increase, the approval trail and the resulting pay change move through one system rather than through a spreadsheet, email and re-entry.

**Acceptance criteria seed:**
- Completed review scores are available to the increase workflow without any manual re-entry by a manager
- A manager enters a recommended percentage increase for each of their people against a budget they cannot exceed, and can see their remaining allocation as they go
- Rating-versus-recommended-increase mismatches are surfaced to HR automatically rather than found by reading two columns
- HR can pull a reconciliation view of scores as recorded in the review against what reached the increase sheet — the report that does not exist today
- Eligibility rules (an employment-date cutoff, and treatment of promotions and rate changes inside the cycle) are configurable and applied by the system, not by hand
- Approval routes through a defined chain ending in a single named sign-off, with the approved state recorded — this account ends at the Owner
- The approved increase reaches payroll without a second manual upload, carries an effective date, and handles retro amounts
- The workflow supports regional/segmented packs and per-manager scope, since managers must not see each other's people
- The model is not hard-wired to one compensation shape; pool-and-allocate is one of at least four models seen across design partners
