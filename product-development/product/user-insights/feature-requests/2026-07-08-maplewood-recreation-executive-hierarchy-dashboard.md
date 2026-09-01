---
account: maplewood-recreation
requested: 2026-07-08
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-08-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Executive access to review status, rolled up by hierarchy branch

**Who asked:** their HR Business Partner, on the prototype's HR admin surface (2026-07-08).

**Underlying need.** Their HR model is deliberately disconnected: HR designs the process,
trains on it and launches it, then hands accountability for completion to directors and
executives. So the completion dashboard the prototype offered HR is aimed at the wrong person.
The people who chase stragglers are executives, and they need it scoped to their own branch of
the hierarchy rather than every employee in the company.

*"I'm wondering if this type of view could be accessible to our executives, because, for lack of a better term, I don't… as an HR business partner, I don't really care where they're at in the performance review process." — Their HR Business Partner*

*"And I say that because our structure, our HR model, is we're actually quite disconnected. Our role isn't to keep track of these types of initiatives or processes. We create them, and then we…" — Their HR Business Partner*

*"But I wouldn't be logging in every single day to keep track of it. It'd be really nice for executive to be able to check in as well, especially with their kind of leaders that branch off in the hierarchy, not necessarily every single employee, because that'd be overwhelming, but if we could branch them off." — Their HR Business Partner*

**What they do today instead.** HR sets a deadline and communicates it; nobody tracks
completion centrally. HR would use such a view occasionally, when a live performance-management
issue makes the review timing relevant — described explicitly as a nice-to-know.

**Signal strength.** Deliberately mixed, and that is the finding. Weak as an HR requirement —
she said plainly she would not log in for it. Potentially strong as an *executive* requirement,
but no executive was in the room, so this is second-hand. Their Employee Experience Director has
been offered for a future session; that is the person to test it with.

## Draft ticket

**Objective:** Give executives and directors a review-status view scoped to their own branch of
the reporting hierarchy, distinct from the HR administrator's company-wide view.

**Acceptance criteria seed:**
- A user with the right role sees status for the employees beneath them in the org hierarchy, at any depth.
- The view is roll-up first (counts and stages by team) rather than a flat employee list.
- Access is role-driven and does not require HR administrator permissions.
- The view respects review confidentiality — status is visible, review content is not.
