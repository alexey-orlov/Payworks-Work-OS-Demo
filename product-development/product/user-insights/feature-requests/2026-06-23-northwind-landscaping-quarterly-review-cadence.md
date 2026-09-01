---
account: northwind-landscaping
requested: 2026-06-23
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-06-23-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Optional quarterly review cadence

**Who asked:** Their Operations Director at Northwind Landscaping, in a discovery interview + prototype review on 2026-06-23. Offered as his own argument, not as current practice.

**The underlying need.** A semi-annual rating rests on what the manager can recall, and their system stores nothing to help. More frequent, deliberately light touchpoints would give the annual outcome more evidence behind it — which matters directly here, because that outcome drives the merit increase. His condition is strict: the extra frequency must not cost more effort per touch, or managers will abandon it.

**What they do today.** Mid-year and year-end reviews — semi-annual. Between them he keeps private notes in a Word document as things occur.

*"I would argue that quarterly might be beneficial, though."* — Their Operations Director

*"More data."* — Their Operations Director

*"It gives us a little bit more"* / *"accuracy to the performance review and a little more validity to it."* — Their Operations Director

*"Doesn't have to be anything. It doesn't have to be strenuous. It should be simple."* — Their Operations Director

**Signal strength: moderate.** A considered opinion from a senior manager rather than an unmet operational need — they are not attempting quarterly reviews today and nothing is failing for want of them. Weigh it as cadence-flexibility evidence, not as a blocked workflow. Note the same session also asks for a heavier one-up approval stage; a quarterly cadence carrying that stage would violate his own simplicity condition.

## Draft ticket

**Objective:** Let an administrator configure review cycle frequency including quarterly, with a lighter review form for high-frequency cycles.

**Acceptance criteria seed:**
- Review cycle frequency is configurable per template (at minimum annual, semi-annual, quarterly).
- A quarterly cycle can use a reduced form — a small set of categories plus a comment — rather than the full annual form.
- Results from interim cycles are visible in the employee's review history and available as evidence when the annual review is written.
- Interim cycles can be configured to skip the approval stage that the annual cycle uses.
- An account can run different cadences for different employee groups.
