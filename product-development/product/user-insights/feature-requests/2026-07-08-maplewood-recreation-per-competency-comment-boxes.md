---
account: maplewood-recreation
requested: 2026-07-08
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-08-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] A comment box against every competency and every goal

**Who asked:** their HR Business Partner, on both the goal-achievement and competency-rating
screens of the prototype (2026-07-08).

**Underlying need.** A rating gap is only useful if the rater has to explain it. They want a
comment field attached to each individual competency and each goal — not one summary box at
the end — and they want those comments capable of being mandatory. This is not speculative:
their own leaders already forced exactly this change on their PDF form.

*"we did get that feedback from our leaders, to change our form, to have, instead of one summary comment box, they wanted a box each… next to each competency rating, so they could make a comment specifically about that, that area." — Their HR Business Partner*

*"I'd love to note make some comments based on why I'm reading them low. I'd actually… like to see their comments. If they've rated themselves high, I'd like to see them comment. Why do you think… right? Especially if you're noting someone rated quite high or quite low. I'd… I encourage commentary to support those." — Their HR Business Partner*

*"It's all about perception and sharing each other's perception to learn more." — Their HR Business Partner*

**What they do today instead.** Their current PDF form already carries a comment box per
competency — a change their leaders requested and they made.

**Signal strength.** Strong. Backed by a change they have already shipped on their own form,
and asked for on both the employee and manager sides. Asked to make the comments mandatory
when prompted — see the sibling record on per-field mandatory control.

## Draft ticket

**Objective:** Attach an optional-or-mandatory free-text comment field to each competency row
and each goal row, on both the self-assessment and the manager review, replacing the
single summary comment box as the only commentary surface.

**Acceptance criteria seed:**
- Every competency and every goal row carries its own comment field, employee side and manager side.
- Each comment field can be configured optional or mandatory per form template.
- A summary comment box remains available but is no longer the only place to comment.
- Comments are visible alongside the rating they belong to, not in a separate list.
