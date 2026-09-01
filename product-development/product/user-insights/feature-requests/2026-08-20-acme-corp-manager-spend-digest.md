---
account: acme-corp
requested: 2026-08-20
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Manager team-spend list — tell the manager what their team spent, in-product, instead of asking them to approve

Their HR Manager's objection to an auto-approval floor is that the approval email is the only channel that tells a manager anything about their team's spending. She concedes managers do not read those emails, but argues they still *see* them, and that peripheral awareness is what lets her notice a pattern — someone expensing parking three times a week — and start a conversation about workload. Remove the approval and that signal disappears. She accepted the threshold once the PM reframed it as approval-versus-visibility: under the floor the claim pays, and the manager is **told rather than asked**.

She then set a hard constraint on the telling: not email. An FYI email at her volume is a deleted email. She wants a list she encounters when she is already in the product — "here's what your team spent this month" — reviewed once rather than twenty times.

Both attendees then realised the same list solves their invisible-spend problem: eleven personal-card software subscriptions arrive as monthly expense claims, roughly $400 a month, each approved once about 22 months ago and never re-decided, because at $29 a time nothing under $50 is ever looked at twice.

**Who asked:** Their HR Manager (the shape and the no-email constraint); Their Payroll Administrator endorsed it as the fix for the recurring-subscription leak.

**Today instead:** Per-claim approval emails. Recurring small charges are invisible because each one is individually trivial.

**Signal:** Strong, and load-bearing — this is the condition on which their HR Manager accepts the auto-approval floor. Ranking the threshold without this is ranking half a package.

*"They're not reading, but they are seeing. That's the real reason. The thing the manager gets out of that email isn't a control, it's information." — Their HR Manager*

*"And if you auto-approve everything under two-fifty, that entire signal disappears from the manager's world. It goes to you, and you're brilliant, but you're not their manager, you're not going to know that means something." — Their HR Manager*

*"Told, but not in an email, please. I get a hundred and something emails a day and a 'for your information' email is a deleted email." — Their HR Manager*

*"I'd want it as a list. Like, when I go in to do something else, there's a 'here's what your team spent this month' and I look at it once. That's a much better shape than twenty emails." — Their HR Manager*

*"Because eleven twenty-nine-dollar things in a list looks like something. Eleven separate emails over a month looks like nothing." — Their Payroll Administrator*

## Draft ticket

**Objective:** Give a manager an in-product view of what their direct reports claimed in the current period — including auto-approved claims that never required their action — so that removing the approval step does not remove their awareness of team spend.

**Acceptance criteria seed:**
- A manager sees a per-period list of their team's claims: claimant, date, amount, category, and approval route (auto-approved vs approved by them).
- The view is reached in-product on the manager's normal path, not delivered as a per-claim email; email notification, if offered at all, is off by default.
- Repeated claims from the same claimant and merchant are visibly grouped or counted, so recurring monthly charges read as a pattern rather than as separate entries.
- The period total is shown, so a manager can answer "what did my team spend this month" without adding it up.
- Auto-approved claims appear here with no action affordance — the view informs, it never holds the money (*"if it genuinely doesn't hold the money"* — Their Payroll Administrator).
