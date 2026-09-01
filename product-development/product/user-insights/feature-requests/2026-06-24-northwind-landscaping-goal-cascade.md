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

# [Performance Management] Assign goals and observations to the team in-system, and track them, instead of by email

**Who asked:** their Site Operations Manager at `northwind-landscaping` — front-line
people-manager, four review subjects this cycle, works on-site with his supervisors.
Design-partner discovery interview, 2026-06-24.

**The underlying need.** Two different things are called "goals" in his world and only one of
them is in a system. Employees set their own goals during the self-review, and those are
compared year over year. But the work *he* assigns — his example was having a supervisor
complete observations on drivers — goes out as an email and then has no trail at all. He
cannot see whether it was done, and it cannot carry into the review, because nothing recorded
that it was ever asked for. What he wants is not a goal-setting ceremony; it is a durable,
checkable record of "I asked for this, here is whether it happened."

**Signal strength.** Moderate and credible. Volunteered rather than elicited — it came out
while he was looking at the prototype's Goals tab, but the behaviour and its shortcoming are
his, not the screen's, and he named the current workaround unprompted. One manager, one
account. He described the benefit in tracking terms (*"track it a little better"*), not in
alignment or cascade terms, so do not read this as a demand for org-wide goal cascading.

**What he does today instead.** *"it'll be quick email"* — nothing tracks completion.

**Adjacent evidence at the same account (do not merge without checking):** the account page
(`customers/accounts/northwind-landscaping/account-context.md`) notes that the 2026-06-22
district-manager record covers goal-cascade duplication and the typing burden it creates.
That record is a separate, still-unfiled conversation, and its wording is not reproduced
here — treat this as a second independent instance of the same theme only once both are
filed and read side by side.

*"we compare them year over year. Um, currently, I kind of just… I'll set, like, if we need, uh, certain observations done on drivers, I'll just kind of… it'll be quick email, but it'd be nice with some system like this that I can track it a little better than just sending emails" — Their Site Operations Manager*

*"It would be a lot handier." — Their Site Operations Manager*

## Draft ticket

**Objective:** Let a manager assign a goal or a specific piece of work to a direct report from
inside the module, and see its status later, so manager-set expectations have a record that
survives to the next review instead of living in someone's sent mail.

**Acceptance criteria seed:**
- A manager can create a goal or assigned item on a direct report's record, with a due date,
  without the employee having to create it first.
- Manager-assigned items and employee-set (self-review) goals are both visible on the
  employee's goal list, and it is clear which is which.
- The manager can see current status of every item he assigned across his whole team from one
  place, without opening each employee in turn.
- Items assigned during a period appear in the goals panel alongside the review when that
  period's review is written, so the assignment carries into the review automatically.
- Completed and closed items remain readable after the cycle ends — the trail is the point.
- Open for definition — carry to the Product Brief: whether an assigned item is the same
  object as a goal or a lighter-weight task; and whether the employee can update its status
  or only the manager can.
