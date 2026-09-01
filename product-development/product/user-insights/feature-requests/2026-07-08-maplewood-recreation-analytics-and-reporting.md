---
account: maplewood-recreation
requested: 2026-07-08
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-08-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Review-process status reporting with CSV export, for payroll

**Who asked:** their Payroll Manager, unprompted, in the closing minutes (2026-07-08).

**Underlying need.** The payroll function is checklist-driven and its questions are all about
process state, not people: which reviews are in, which increases have been actioned, who has
been paid, who is owed retro pay. They need a working list they can filter and take away —
CSV export was the thing that made the prototype's analytics view land.

*"A possibility of, analytics?" — Their Payroll Manager*

*"For, like, the payroll side, we're a very checklist. Checklist-driven, as you've seen in some of my responses on other things. So, for us, we need to know, like, who's been submitted, when we've done their increase, have they been paid, do they… are they owed retro pay, or anything like that? So, like, I guess I could use, like, the dashboard screen, just to kind of see what's pending, what's outstanding, what's new, what's completed." — Their Payroll Manager*

*"Yeah, and even the list of employees, like, if that's… oh, there's export to CSV, then that's perfect, because then we can see exactly where people are." — Their Payroll Manager*

**What they do today instead.** Reviews arrive through the company intranet; the Payroll
Manager opens each one, scans it, flags anything odd to HR, and tracks the rest by her own
checklist.

**Signal strength.** Strong for payroll, and important for scoping: when this account says
"analytics" they mean **process status and export**, explicitly not people analytics — Margaret
confirmed the distinction on the call and the answer was *"stats and data, yeah."* Do not read
this record as demand for competency or performance analytics. The reporting itself may end up
served by the Workforce Analytics module rather than built inside Performance Management.

## Draft ticket

**Objective:** Give payroll and HR a status view of a review cycle — pending, outstanding, new,
completed, per employee — with CSV export.

**Acceptance criteria seed:**
- A cycle status view lists every employee in the cycle with their current stage.
- Filters cover stage, manager, and population (permanent / seasonal).
- The list exports to CSV with the same columns as the on-screen view.
- Compensation-relevant state (increase actioned, paid, retro owed) is representable, without the review itself deciding the increase.
