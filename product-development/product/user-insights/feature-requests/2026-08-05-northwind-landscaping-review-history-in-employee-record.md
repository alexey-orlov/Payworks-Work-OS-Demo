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

# [Performance Management] Performance file on the employee record in Payworks

**Who asked:** Their HR Manager at Northwind Landscaping, on a 2026-08-05 reverse demo in which she walked her own current performance workflow end to end. Northwind is the most multi-module design-partner account and reviews cover salaried and administrative staff only (173 completed in the 2025 cycle, 73% of those in scope).

**The underlying need:** one employee record. Reviews live in QuickBase, a platform Northwind builds on itself, linked to Payworks by an in-house API that pulls employee master data one way. Nothing comes back. The result is that a manager or an HR person who wants to see what an employee scored has to leave the employee's Payworks file and go find them in a second system, one person at a time — and only for the years QuickBase covers.

**What they do today instead:** two records, with a hole between them. When reviews were on paper and Excel, the signed copies were scanned and uploaded into the employee's Payworks file, so that history is still there. Since going paperless four years ago, nothing has landed on the Payworks record at all. Every cycle, every manager re-opens QuickBase per report to look up prior scores.

*"for 5 years, I should be able to go right into PayWorks. Not only can I see your whole file, now I can see your performance file." — Their HR Manager*

*"There's no way to have it captured in PayWorks, where it's assigned to an employee." — Their HR Manager*

*"when we did it in Excel, and the paper copies, they had to print it off and sign it, of course, we actually used to take those, scan them, upload them, and they are in your PayWorks file… But for the last 4 years since we don't do paper, yeah, you got nothing." — Their HR Manager*

**Signal strength:** strong. This is the account's stated headline ask, volunteered without prompting as the reason an in-Payworks solution is worth having, and it is the answer she gave when asked what the benefit of consolidation would be (*"Absolutely."*). It is an ask for consolidation rather than for review features — the review form itself they are broadly happy with.

## Draft ticket

**Objective:** Store completed performance reviews against the employee in Payworks so that the review record — score, rating, and the completed form — is reachable from the employee file alongside everything else Payworks already holds for that person, and persists across review cycles.

**Acceptance criteria seed:**
- A completed review is attached to the employee record in Payworks and is visible from the employee file without leaving Payworks
- Prior-cycle reviews are visible as history against the same employee, not just the current cycle
- The manager of record and HR can see an employee's review history; visibility rules for the employee's own view are defined explicitly (this account shows both sides of the form to both parties today)
- The record survives a manager change and an org move — history follows the employee, not the reporting line
- Existing scanned pre-digital review documents already in the employee's file are not disturbed or duplicated
- Behaviour is defined for reviews that were started but never closed off by the manager — 27% of this account's last cycle sat in exactly that state
