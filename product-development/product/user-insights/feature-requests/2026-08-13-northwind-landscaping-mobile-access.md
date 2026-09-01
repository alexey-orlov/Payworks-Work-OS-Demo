---
account: northwind-landscaping
requested: 2026-08-13
area: employee-self-service
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-13.md
features: [mobile-self-service]
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Employee Self Service] Manager role in the mobile app — recognise a supervisor's direct reports, not just their own employee record

Northwind's first reviewed level of management is the **route supervisor**, and route
supervisors do not have computers. The mobile app resolves them as employees only: a
supervisor can punch in and book a vacation day, and nothing on the manager side of the
product is reachable. This is a role-modelling gap, not a screen-size gap — the app has no
notion that the person holding the phone has people reporting to them.

*"the app you've got now only knows those guys as employees… Not as managers. So a supervisor
can punch in and book a vacation day, and that's it. He's got nine people reporting to him and
the app doesn't know." — Their HR Manager*

**What they do today instead:** paper. This year one of their site supervisors ran his entire
crew's reviews off his own initiative — for hourly staff who are not even in scope for
reviews at this company. He printed the forms, had the crew fill them in during a Sunday
lunchroom session, then interviewed each person an hour at a time over two days. The work
happened; the data did not survive it.

*"If that man had had it on his phone, he'd have done it in half the time and I'd have the
data. Instead there's a stack of paper in a yard office somewhere and it's worth nothing to
us." — Their HR Manager*

**Signal strength:** strong and repeated. The HR Manager tracked the repetition herself on
this call — *"I've said this to Margaret about five times and I'll keep saying it until
somebody writes it down." — Their HR Manager* — and pre-empted the question before it was
asked. It is a gating dependency rather than an enhancement: the review cycle's stalled 27%
sits with exactly these field-based managers, so escalation reminders (see
[2026-08-13-northwind-landscaping-review-reminders.md](2026-08-13-northwind-landscaping-review-reminders.md))
land on people who currently cannot act on them.

**Cross-module note, recorded as stated and not extrapolated:** she said she had made the same
point to the expense-side product contact — *"I said this to the product person on the expense
side too, by the way."* That is a statement about where the point was raised. **No expense
requirement was given on this call**, and this record is deliberately not linked to
`expense-management-vp2`, whose evidence base is unchanged until the Controller conversation.

## Draft ticket

**Objective:** Let a manager act as a manager from the mobile app — starting with performance
reviews for their direct reports — so field-based supervisors without computers can complete
manager-side work at the site instead of on paper or not at all.

**Acceptance criteria seed:**
- The mobile app resolves the signed-in user's **manager** context from the reporting
  structure, in addition to their employee context
- A supervisor with direct reports sees a manager surface listing those reports; a supervisor
  with none sees no change
- Manager-side review work — open a report's review, complete the manager section, record the
  closing conversation — is completable end to end on a phone
- Manager notifications (including escalation reminders) are deliverable to and actionable
  from the mobile app
- Works for a supervisor whose only device is a phone: no step in the flow requires a desktop
  handoff
- Reporting-structure changes (seasonal hire promoted to route supervisor) take effect without
  a manual role assignment per person
