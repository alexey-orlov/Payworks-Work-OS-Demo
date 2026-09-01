---
account: acme-corp
requested: 2026-08-20
area: employee-self-service
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Employee Self Service] Employee-visible expense claim history

Their HR Manager raised this herself at the end of the call, prefacing it as probably outside what we are building: an employee should be able to look up their own claims — what was submitted, whether it was approved, when it was paid, and the receipt — without going through either of the two people who run the back office.

**It is contested inside the account, and the disagreement is the most useful part of the record.** Their Payroll Administrator does not believe anyone will use it, and has four years of counter-evidence: employees come to her desk to ask their vacation balance while it is on screen in front of them in self-service. She reads that as behaviour rather than discoverability — people would rather ask a person. Their HR Manager's rebuttal, which the administrator accepted, is that the habit is partly self-inflicted because they always answer.

A ranking should treat this as a deflection bet with a named adoption risk attached, not as a straightforward request. If the deflection assumption fails here it likely fails across the small-employer segment this account represents.

**Who asked:** Their HR Manager. Explicitly doubted by Their Payroll Administrator in the same exchange.

**Today instead:** Every "what happened to my claim" and "what was that amount" question routes to one of two people; the administrator retrieves the answer from old email.

**Signal:** Weak-to-moderate as demand and explicitly self-scoped as out of the current build, but valuable as evidence — it is the clearest statement in the corpus that shipping a self-service surface does not by itself produce deflection.

*"Employees seeing their own history. So somebody can go in and see, I submitted this, it was approved, it was paid on the fifteenth, here's the receipt. Without asking either of us." — Their HR Manager*

*"They won't. They'll come to my desk. They come to my desk to ask what their vacation balance is and it's on the screen in front of them in the self-service." — Their Payroll Administrator*

*"They've been told it's there for four years. At some point it's not a discoverability problem, it's that people would rather ask a person." — Their Payroll Administrator*

*"Well, some of that's on us for always answering." — Their HR Manager*

## Draft ticket

**Objective:** Let an employee see the status and history of their own expense claims in self-service — submitted, approved, paid, with the receipt — without contacting HR or payroll.

**Acceptance criteria seed:**
- An employee sees their own claims only, with current status and the date each was paid.
- The attached receipt is retrievable from the historical claim.
- Where the claim was reimbursed through payroll, the entry links to the pay run that paid it (pairs with `2026-08-20-acme-corp-pay-statement-expense-detail.md`).
- The entry point is reachable from where employees already go for pay information, not a separate destination they must be told about.
- Instrument usage before assuming deflection — this account expects nobody to use it, and that prediction is the thing worth testing.
