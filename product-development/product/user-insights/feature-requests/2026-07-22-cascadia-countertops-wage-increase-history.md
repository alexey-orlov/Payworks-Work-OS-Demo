---
account: cascadia-countertops
requested: 2026-07-22
area: performance-management
type: improvement
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-22-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Show wage-increase history at the point a manager recommends an increase

Managers at this account have access to their reports' wages and make the increase
recommendation themselves. What they lack at that moment is the recency of the last one — a
manager who is pleased with someone may recommend an increase without knowing one landed
recently, and recognition might be better given some other way. She was explicit that this
does not need to be prominent: a pointer to the latest increase is enough, and Payworks
already has an earnings-history view it could link to.

*"I mean, ideally, it would be great to see the, like, the history of increases." — Their HR Lead*

*"Because if the employee just not long ago got an increase, and the employee just doing great, it will be good to remind the manager that they've got an increase, that it's too early for maybe the next one, unless it's, like, a major change." — Their HR Lead*

*"Or at least it may be, like, for example, linked to… because there is a nice, function in PayVox right now that shows history of earnings." — Their HR Lead*

*"It may not necessarily pop up in here right away, but it should be a, like, reminder if you want to see the" / "History of increases, so maybe show just latest increase." — Their HR Lead*

**Today instead:** HR benchmarks the ask against other branches when the request reaches
her; the manager makes the recommendation without that context. **Signal strength:**
moderate and self-limited — she volunteered that it need not be surfaced prominently, which
is why it is filed nice-to-have rather than must-have.

## Draft ticket

**Objective:** Give a manager the recency and size of the employee's last wage increase at
the moment they enter a recommendation.

**Acceptance criteria seed:**
- The recommendation step shows the date and amount of the most recent increase.
- Full increase history is reachable in one click, linking the existing earnings-history view rather than duplicating it.
- The panel is secondary on the screen — it must not compete with the recommendation input.
- Nothing here is visible to the employee.
