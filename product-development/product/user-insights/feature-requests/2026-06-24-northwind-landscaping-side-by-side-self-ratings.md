---
account: northwind-landscaping
requested: 2026-06-24
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-06-24-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Show the employee's self-review beside the manager's while the manager writes

**Who asked:** their Site Operations Manager at `northwind-landscaping` — front-line
people-manager, four review subjects this cycle. Design-partner discovery interview +
prototype review, 2026-06-24.

**Read this qualifier first.** This is **prototype-elicited, not volunteered.** He did not
arrive with this ask; he was shown a review-writing screen that displayed the employee's
self-review beside his own, and reacted positively to it. Do not rank it as customer-initiated
demand. Its value as evidence is that the reaction cut against the sequencing his own account
runs today.

**The underlying need.** He wants to know the size of the disagreement before he commits to a
rating — not to be talked out of his own view, but to see the gap. In their current system he
cannot: his review is submitted **first**, and only then is the employee notified to complete
the self-review. He corrected the interviewer on this when she assumed the reverse order. He
also said plainly that the self-review does not change his ratings once written — so the value
he is describing is *awareness of the gap going into the discussion*, not revision.

**Signal strength.** Low to medium. One manager, one account, elicited by the screen. Note the
tension worth carrying rather than resolving: he liked seeing the self-review first, and he
also believes *"They… they aren't seeing some of their faults"* — a manager who wants the
employee's view visible but is not going to be moved by it. Whether seeing the self-review
first anchors a manager's ratings is a real design risk this record does not answer.

**What he does today instead.** Writes and submits his review with no visibility of the
employee's self-assessment; sees it only afterwards, and did not revise anything this cycle.

*"I do like the fact it shows the self-review, um, but it's quite handy just to kind of see what they're…" — Their Site Operations Manager*

*"How they thought they did and how I thought they did is on there." — Their Site Operations Manager*

*"Uh, no, I got it after I had done it. Once I had put the review in, it sent the notification through for them to do their own self-review." — Their Site Operations Manager*

## Draft ticket

**Objective:** Give the manager the employee's submitted self-review in context while writing
the manager review, so the rating gap is visible before the discussion — with the anchoring
risk explicitly considered rather than assumed away.

**Acceptance criteria seed:**
- When an employee's self-review is submitted, its ratings and comments are visible to the
  manager on the same screen as the manager's own review, per question, without navigating
  away.
- Where a self-rating and the manager's rating differ, the difference is apparent at a glance.
- The manager's own entry is never pre-filled from, or defaulted to, the employee's
  self-rating.
- If the employee has not submitted a self-review, the manager can still complete and submit
  the manager review — the panel shows "not yet submitted" and never blocks.
- Open for definition — carry to the Product Brief, do not decide here: whether the order is
  configurable per company (this account runs manager-first today, and its HR function owns
  the cycle); and what mitigation, if any, is needed against manager ratings anchoring to a
  visible self-rating.
