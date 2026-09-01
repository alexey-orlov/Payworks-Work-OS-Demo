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

# [Performance Management] Manager sees the employee's self-ratings beside their own

**Who asked:** their HR Business Partner, driving the prototype's manager review screen
(2026-07-08).

**Underlying need.** The review meeting is a comparison of two perceptions, and the manager
cannot run it without seeing what the employee said. On the prototype she expected the
employee's competency self-ratings to be visible while she rated, could not find them, and
called it out as confusing. She wants the same side-by-side treatment on competencies that the
goal-achievement screen appeared to offer.

*"It's interesting, because… Didn't the employ… because the employee rated themselves as well, and I can't see how… What they rated themselves." — Their HR Business Partner*

*"So again, I would probably like to see the same thing, where I saw how they rated themselves, and then I'd like to rate them, but I'd like to comment why I'm rating them so high, or so low." — Their HR Business Partner*

**What they do today instead.** On the PDF form both sets of marks sit on the same sheet, so
the comparison is free — the digital prototype is a regression against paper here.

**Signal strength.** Strong. Raised unprompted, twice, and paired with the per-competency
comment ask: seeing the gap and explaining the gap are one requirement in her framing.

## Draft ticket

**Objective:** Show the employee's submitted self-rating next to the manager's rating field
for every competency, matching how goal achievement already presents the two.

**Acceptance criteria seed:**
- Each competency row shows the employee's self-rating and the manager's rating input together.
- The employee's rating is clearly labelled as theirs and is read-only to the manager.
- Employee comments on that competency are visible to the manager in the same row.
- Self-ratings become visible to the manager only after the employee submits.
