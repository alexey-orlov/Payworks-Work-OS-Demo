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

# [Performance Management] Two review form types — permanent (with goals) and seasonal (without)

**Who asked:** their HR Business Partner, exploring the prototype's HR admin surface
(2026-07-08).

**Underlying need.** They run two workforces on one payroll. The permanent review is mandatory
and includes goals; the seasonal mid-season review is strongly recommended, not mandatory, and
deliberately drops the goals section because a seasonal term is too short to set a sustainable
goal against. The forms are otherwise the same document — this is one template family with a
section toggle, not two products.

*"is there capabilities to have two different types of forms? Because we do permanent reviews, which are mandatory, but then when we do have some managers that do mid-season reviews for our seasonal employees, and the form is just… we… it just doesn't have the goals, because we don't have a long enough time to set sustainable goals. So, essentially, they're the same thing, just one… one section is included and one section is not. So I would see that this… I would set up the two forms." — Their HR Business Partner*

*"We have permanent employees, where our annual performance review is mandatory, and then we have seasonal employees, where it's It's strongly recommended, but it's not mandatory. We utilize a paper form for both. I've created two separate forms." — Their HR Business Partner*

**What they do today instead.** Two separate PDF fillable forms, both authored by their HR
Business Partner.

**Signal strength.** Strong, and structural. This is the first thing she said she would set up
if starting fresh in the admin surface, and it is inseparable from the permanent/seasonal split
that shapes everything else about this account. Depends on the sibling record on making employee
type visible to managers — a manager who cannot tell who is seasonal cannot pick the right form.

## Draft ticket

**Objective:** Support more than one review form template per company, where templates share
structure but can include or exclude whole sections (goals in particular).

**Acceptance criteria seed:**
- An admin can create multiple form templates and name them.
- A template can include or exclude the goals section without losing the rest of the form.
- A review cycle can target a population with the correct template.
- Each template carries its own mandatory-field and rating-scale configuration.
