---
account: acme-corp
requested: 2026-08-20
area: payroll
type: improvement
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: [pay-statements]
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Payroll] Show which claims a reimbursement covers on the pay statement

Reimbursement at this account rides the pay run — semi-monthly, 15th and last business day, cutoff two business days before. The claim itself works; the pay statement is where it falls down. The statement shows a single unlabelled amount, so the employee cannot reconcile it and asks a person instead, and the administrator has to go back to an email from three weeks earlier to answer.

She believed this happened two or three times a pay. On the call her HR Manager revealed she fields the same questions and forwards them on, so the real volume is roughly five or six per pay across the two of them. The administrator attached explicit willingness to pay to the fix — the strongest priority language anyone used on the call.

This is a payroll-module improvement rather than expense-module scope, but it is generated entirely by the expense flow and sits on the payroll-side boundary `expense-management-vp2` names as in scope.

**Who asked:** Their Payroll Administrator; corroborated by Their HR Manager as a shared, under-counted cost.

**Today instead:** The statement reads as a bare amount; both attendees answer the resulting questions manually from old email.

**Signal:** Strong on wording, moderate on severity — it is a recurring interruption every pay, not a blocker to running expenses. Small, and it removes work from both people who run the back office.

*"The pay statement just says a number. It says 'expenses, three hundred and forty dollars.' And then somebody comes to my desk and says, what's the three-forty, and I have to go back to their email from three weeks ago." — Their Payroll Administrator*

*"Two or three times a pay. Not everybody. But enough that I'd pay real money for the statement to just say which claims it was." — Their Payroll Administrator*

*"All the time. I just forward them to you and you think it started with you." — Their HR Manager*

## Draft ticket

**Objective:** Identify the expense claims behind a reimbursement amount on the pay statement, so an employee can reconcile it without asking the administrator.

**Acceptance criteria seed:**
- A reimbursement on the pay statement itemises the claims it covers — claim reference or description, date, and amount — rather than showing one aggregate figure.
- The itemisation appears wherever the employee reads the statement, including self-service.
- Multiple claims paid in one run are listed separately and sum to the reimbursement line.
- The claim reference shown matches what the claimant sees on their own submitted claim, so the two can be tied together.
- Behaviour is unchanged for clients who do not reimburse through payroll.
