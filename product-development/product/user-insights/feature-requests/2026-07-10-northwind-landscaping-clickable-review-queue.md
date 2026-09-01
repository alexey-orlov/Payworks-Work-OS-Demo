---
account: northwind-landscaping
requested: 2026-07-10
area: performance-management
type: improvement
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-10-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Make the manager home counters click through to the work

The first thing Northwind Landscaping's **site supervisor** tried to do on the Performance
Management prototype's manager home screen was click an overdue counter. He read the tile
correctly, understood what it was telling him, and expected it to be the entry point into the
reviews it was counting.

The underlying need is small and specific: a manager who is not a desk worker wants the fewest
possible steps between "you have work outstanding" and the outstanding work itself. He found the
list further down the page afterwards and accepted it, but the click was his instinct first.

*"So, like, check-ins overdue, so this is, like, a review that I didn't get to, now it's in my
overview, or overdue, sorry."* — Their Site Supervisor

*"Is this something I can click into?"* — Their Site Supervisor

*"I'm just thinking, because if it's, like, reviews to write, and I can click into it, and it
would show me my two people that I need to review, I think that would be easy, and then you
click in, and then you could go right into the review to see them."* — Their Site Supervisor

*"Oh, but I see how you kinda have it down here. It's a little bit lower. Okay."* — Their Site
Supervisor (finding the list below the fold)

**Signal strength.** Weak-to-moderate and small in scope: a first-click expectation on a
prototype, volunteered without prompting, resolved once he found the equivalent list lower on the
page. Filed because it is concrete, cheap, and one of the few navigation observations in the
Northwind field-management set — not because it is a blocker.

**What they do today:** nothing — this is prototype feedback, not a current workflow.

## Draft ticket

**Objective:** Make the manager home screen's status counters actionable, so a count of overdue
or outstanding reviews leads directly to the filtered list and from there into the review.

**Acceptance criteria seed:**
- Each counter tile on the manager home is a link, not a static number.
- Activating a counter opens the matching filtered list — overdue reviews shows exactly the
  overdue reviews, scoped to that manager's team.
- From the filtered list, one further action opens the review itself.
- The same information stays reachable by scrolling for managers who never click the tile — the
  tile is a shortcut, not the only route.
