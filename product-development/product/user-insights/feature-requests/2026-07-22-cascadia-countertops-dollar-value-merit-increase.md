---
account: cascadia-countertops
requested: 2026-07-22
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-22-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Dollar-value option on the merit-increase recommendation, not percentage-only

Their workforce is hourly and every compensation conversation in the company happens in
dollars per hour. The prototype's merit-increase field on the manager's recommendation
offered a percentage only, and she could not map it onto anything she does. This is not a
display preference — a percentage field is the wrong unit for the decision their CEO
actually makes.

She pointed out that core Payworks already does this correctly today, and asked for the
same behaviour here: entering an amount shows the current wage and the resulting new wage.

*"I'm not sure what you mean, it's very hard to deal with percentages." — Their HR Lead*

*"Our company, we use dollar value, like, 100%, so it would be nice to have an option for dollar value." — Their HR Lead*

*"Dollar one! It's actually working very, very good right now, because as soon as I enter dollar amount or percentage, the paperwork shows me what is the current wage, what will be the new wage." — Their HR Lead*

**Today instead:** the recommendation is written as a dollar amount on a Word form or in the
body of an email to the CEO. **Signal strength:** high — stated twice, with the existing
Payworks behaviour named as the model. Corroborates the same pattern already recorded on
this account's page.

## Draft ticket

**Objective:** Let a manager express a merit recommendation as a dollar amount or a
percentage, and show the resulting new wage either way.

**Acceptance criteria seed:**
- The recommendation field accepts dollar amount or percentage; the unit is a per-company setting with a per-recommendation override.
- Hourly employees default to a per-hour dollar amount.
- Entering either form displays current wage → new wage before submission.
- The stored value keeps the unit the manager entered, so nothing is round-tripped through a percentage.
