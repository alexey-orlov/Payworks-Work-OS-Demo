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

# [Expense Management] System-owned reminder to submit a stale claim

Their written policy gives claimants 60 days to submit. It has never once been enforced, because the only enforcement available is refusing to reimburse a colleague for a hotel — so the rule is, in their Payroll Administrator's word, decorative. The consequence is claims that arrive four months late, spanning a quarter that has already closed, and always from the same three people.

Half of the day and a half she spends on expenses each month is chasing. Her ask is a nudge at around day 15 — but the requirement is as much about *who sends it* as about the reminder existing. She is currently the reminder, which makes her the nag, and at 75 people in one building that is a standing relationship cost she pays personally.

**Who asked:** Their Payroll Administrator. Their HR Manager corroborated the pattern (*"It's always the same person, too."*).

**Today instead:** She chases by email and in person; the 60-day rule is never applied.

**Signal:** Strong, quantified by the requester herself — she estimates a system-sent nudge removes about ninety percent of the chasing. The social framing (not from me, from the system) is the part a build must not lose.

*"And I've never once enforced it. Because what am I going to do, not pay somebody back for a hotel?" — Their Payroll Administrator*

*"So the rule's decorative. If the system nudged them at day fifteen — not me, the system — I think ninety percent of it goes away." — Their Payroll Administrator*

*"A reminder that isn't from me. Because right now the reminder is from me, and then I'm the nag, and that's a relationship cost in a company this size. You see these people at lunch." — Their Payroll Administrator*

*"It's not that the receipt's hard to get, it's that somebody hasn't submitted anything since May and then in August I get four months in one go." — Their Payroll Administrator*

## Draft ticket

**Objective:** Have the system remind a claimant to submit an ageing expense before the client's submission deadline, so the administrator is not the enforcement mechanism.

**Acceptance criteria seed:**
- A client can set a submission window (theirs is 60 days) and a reminder point within it (they suggested day 15).
- The reminder is attributed to the system, not to the administrator who configured it — no "from" that makes a colleague the nag.
- Reminders target the claimant, not the manager or the administrator.
- A claim spanning a closed prior period is flagged to the administrator on receipt, since late claims are the ones that cross a closed quarter.
- Reminder cadence is bounded (a claimant who ignores it is not mailed indefinitely) and the administrator can see who has been reminded.
