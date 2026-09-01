---
account: northwind-landscaping
requested: 2026-08-05
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-05.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Launch the whole review cycle automatically, instead of manager-by-manager

**Who asked:** Their HR Manager at Northwind Landscaping, on the 2026-08-05 reverse demo. She volunteered it while explaining why review launch sits with individual managers today — the honest answer being that nobody designed it that way, it is simply how the QuickBase application was built.

**The underlying need:** the cycle should start itself. Managers are the first actor in the chain and nothing moves without them, so a manager who never launches silently stalls their whole team's reviews and self-reviews. HR discovers this half way through the window and then chases by email and phone.

**What they do today instead:** a communications campaign. HR sends a launch email under the Head of HR's signature, runs three or four training webinars over Teams (highly encouraged, not mandatory, attendance tracked but never acted on), and states a target completion date. Each manager then creates each review by hand — an employee cannot start their own. A separate QuickBase report lists people with no review started, which HR uses to chase. The 2025 cycle finished at 173 reviews, 73%, still open months past a target of end-January / early-February.

*"if it was an automatic trigger for all managers to say the review period has started, and poof, the system could generate it itself, that would be a great thing also." — Their HR Manager*

*"Right now, we leave it up to our managers to generate it, to trigger it themselves. And unfortunately, you're right, what happens is, it'll be halfway through that review period we have set up. And we'll go in and we'll say, oh my gosh, Johnny Manager hasn't even started his reviews. He hasn't even launched them for the self-reviews to start." — Their HR Manager*

*"every site probably has managers like that, and we are no different." — Their HR Manager*

**Signal strength:** moderate. Genuine and unprompted, phrased as a want (*"that would be a great thing also"*) rather than a requirement, and it addresses the account's clearest adoption risk after the merit spreadsheet. It is not the reason they would switch — that is the consolidation and merit-handoff asks — but it is the operational relief HR would feel first, and it is cheap evidence in favour of cycle-level orchestration generally.

## Draft ticket

**Objective:** Let an HR administrator open a review cycle once, for a defined population, and have the system create every review in it — removing the per-manager manual launch step and the stall it produces.

**Acceptance criteria seed:**
- HR defines a review cycle (population, form, window, target completion date) and the system generates every review in scope
- Employees and managers are notified when their forms become available, without a manager having to trigger anything
- The population is scoped by rule, not by list — this account reviews salaried and administrative staff only, never the hourly field workforce
- HR sees live completion state for the cycle, including which reviews are unstarted and which are complete but not yet closed off by the manager (the state 27% of this account's last cycle sat in)
- Reminders escalate to the manager, and then to HR, on a configurable schedule before the target date
- A manual per-manager launch remains possible for people added mid-cycle
- Employees joining after the cycle opens are handled explicitly rather than silently missed
