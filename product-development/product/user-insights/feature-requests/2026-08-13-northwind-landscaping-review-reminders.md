---
account: northwind-landscaping
requested: 2026-08-13
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-13.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Escalation-tiered review reminders — notify the manager's manager, not just the manager

Northwind's review cycle does not fail at the form, it fails at the last step. They launch in
November, target completion by end of January, and have never hit it — **173 of roughly 230
in-scope reviews complete by February, 73%**. In every stalled case the employee's
self-review is done and the manager's review is done; what has not happened is the manager
sitting down with the employee to close it off. The blocker is calendar logistics with
field-based people: booking half an hour with someone who is on a site, then having it moved.

Their HR Manager was asked directly whether a reminder would help or would just be noise, and
drew a sharp line — a reminder to the assigned manager is worth "maybe"; a reminder to that
manager's manager is the version she will vouch for, on an explicit incentive argument.

*"A nudge to the manager? Maybe. A nudge to the manager's manager, yes. Definitely. Because
the manager ignoring an email is free, and their boss asking them about it is not free." —
Their HR Manager*

**What they do today instead:** she performs the escalation herself, by hand, across the whole
cycle — chasing managers, watching bookings get moved, and re-chasing. She named the role and
asked to be released from it.

*"It's the only thing that works. And I say that as someone who is currently the escalation.
I'm a human notification system and I'd like to retire from that role." — Their HR Manager*

**Signal strength:** strong, and unusually well-specified. The ask is quantified against a
known completion gap (27% of ~230 reviews), the customer has already tested the cheaper
version informally and rated it lower, and the requester is the buyer for this module at this
account. Caveat worth carrying: the plain manager reminder is rated "maybe" by the customer —
building only that tier would not address what she asked for.

## Draft ticket

**Objective:** When a review sits unresolved at the closing-conversation step past its due
date, escalate the notification up the reporting line rather than repeating it to the same
manager — so HR stops being the escalation mechanism and cycle completion stops depending on
one person's chasing.

**Acceptance criteria seed:**
- A review that has both self-review and manager review complete, but no closing conversation
  recorded, is identifiable as a distinct state — not lumped with "in progress"
- After a configurable interval past the due date, a reminder goes to the assigned manager
- After a second configurable interval with no change, the reminder escalates to that
  manager's manager, resolved from the reporting structure, and names the specific stalled
  review(s)
- Escalation intervals and the number of tiers are configurable by HR per review cycle
- HR can see, in one view, every review sitting at the closing-conversation step and which
  escalation tier it has reached
- Escalation stops immediately when the closing conversation is recorded
- Field-based managers can receive and act on the notification without a computer — see the
  companion request [2026-08-13-northwind-landscaping-mobile-access.md](2026-08-13-northwind-landscaping-mobile-access.md)
