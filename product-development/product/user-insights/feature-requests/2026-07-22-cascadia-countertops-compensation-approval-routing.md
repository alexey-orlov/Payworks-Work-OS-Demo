---
account: cascadia-countertops
requested: 2026-07-22
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-22-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Compensation approval routed to the CEO as its own step, separate from HR's approve-and-share

The single clearest workflow correction of the session. In their process there are two
different approvals with two different owners, and the prototype merged them into one
button. HR approves that the review is *done* and can be shared with the employee; the CEO
approves the *money*, individually, and only then does HR action it into a pay period.
Today the compensation hop is an email with the review attached — which means no task for
the approver, no audit trail, and HR chasing.

She also does not want the manager's unapproved recommendation persisted where it might
surface: the CEO may decline it, and an employee seeing a recommendation that never
happened is worse than not recording it.

*"What is important for me to emphasize is that if I, as an HR, click approve and share, it doesn't mean that this is approved." — Their HR Lead*

*"should trigger… some kind of, task for the CEO," — Their HR Lead*

*"see, or I can see that this manager requested a raise based on, like, this performance review, all these comments. That is what's happening right now, but by mail." — Their HR Lead*

*"But it might not happen. CEO may not approve it, so why even put this in there?" — Their HR Lead*

*"Yeah, one at a time, because it's a serious decision about wage increase." — Their HR Lead*

**Today instead:** the manager completes the review, attaches it to an email to the CEO and
copies HR; HR benchmarks but does not approve; the approved increase is entered into the
next pay period. **Signal strength:** high — she interrupted the walkthrough to insist on
the distinction, and returned to it twice more. Note for prioritisation: this account will
not batch-approve, so a list-of-employees approval screen does not serve them.

## Draft ticket

**Objective:** Model review approval and compensation approval as two distinct gates, and
route the compensation gate to a named approver as a task.

**Acceptance criteria seed:**
- HR's approve-and-share shares the review with the employee and does not approve any compensation change.
- A recommendation with a compensation change raises a separate approval task for the configured approver.
- The approver sees the outcome and the recommendation, and can approve or decline one employee at a time.
- The compensation section is never visible to the employee at any stage.
- HR can return the review to the manager for revision with comments, without touching the compensation gate.
- The approval decision and its date are recorded against the employee.
