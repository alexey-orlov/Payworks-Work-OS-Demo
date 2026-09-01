---
account: acme-corp
requested: 2026-08-20
area: expense-management
type: feature
priority_signal: table-stakes
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Digital-first receipt attachment, plus phone capture at the point of spend

**Read the signal carefully before ranking this.** Nobody at this account asked for receipt attachment as a capability — it is assumed table stakes, and they already do it by stapling files to an Excel form. What this record carries is the **shape** of a receipt at a 75-person office, and that shape contradicts the framing the expense work has been carrying.

Receipts here are overwhelmingly digital: PDFs and forwarded confirmation emails. Of one month's claims, roughly three were photographs of a paper receipt; everything else arrived already digital. The reason is the spend mix — conference registrations, client dinners where the restaurant emails the receipt, and software subscriptions charged to a personal card. The PM named the assumption this breaks on the call: she had been spending time with a customer whose whole problem is photographing paper in a truck, and had started assuming that was the problem generally.

The one explicit capture ask *is* mobile, and it is narrow: capture a taxi receipt at a conference and be finished with it, rather than carrying the claim home. That overlaps `2026-08-20-acme-corp-mobile-access.md`; the distinction is that this record is about what a receipt is and how it attaches and matches, and that one is about which actions belong on a phone.

**Who asked:** Their Payroll Administrator supplied the shape and the mobile-capture ask; she owns every claim end to end.

**Today instead:** Claimants attach PDFs and forwarded confirmation emails to a shared-drive Excel template and email the whole bundle to the administrator — or to their manager first, inconsistently.

**Signal:** Moderate as a demand, high as a design correction. It converts "receipt capture = photograph paper" from a working assumption into a segment-specific pattern, and gives the opposing case first-hand.

*"Hardly ever paper. I'd say — of the ones I got last month, maybe three were photos of a paper receipt. Everything else was a PDF or somebody forwarding me the confirmation email." — Their Payroll Administrator*

*"Our people buy things online. It's a conference registration, or it's a client dinner where the restaurant emails you the receipt, or it's somebody's put a software subscription on their personal Visa." — Their Payroll Administrator*

*"Submitting. Not the whole thing. I don't need to run a payroll on a phone, God forbid. But snapping the taxi receipt and being done with it, yes." — Their Payroll Administrator*

## Draft ticket

**Objective:** Make attaching a digital receipt — a PDF or a forwarded confirmation email — the primary, first-class path on a claim line, with photo capture supported as the travelling case rather than as the default.

**Acceptance criteria seed:**
- A claimant can attach a PDF to a claim line from a desktop without converting it to an image.
- A claimant can forward a confirmation email into a claim, or attach the email itself, without re-keying the amount and merchant by hand.
- A claimant can photograph a receipt from a phone and attach it to a new or existing claim.
- Multiple receipts attach to one claim (their $4,000 conference trip is flights, hotel and booth costs in a single claim).
- The receipt stays retrievable against the paid claim afterwards — it is what both the administrator and the employee go looking for weeks later.
- Do not design the capture flow around photographing paper as the primary case; validate the default path against this account before committing.
