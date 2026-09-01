---
account: northwind-landscaping
requested: 2026-06-23
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-06-23-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Weighted category scoring with weights set by category

**Who asked:** Their Operations Director at Northwind Landscaping, in a discovery interview + prototype review on 2026-06-23, answering a direct question about whether a calculated overall score with per-category weights would be useful while filling in a review.

**The underlying need.** Not every measured category carries the same consequence for a given role — turnover, budget and compliance do not weigh alike for a site leader. A flat average across categories produces a number he would not stand behind, and the overall score matters here more than usual because it is the input to the merit calculation. He wants the weighting to follow the category tiering the business already applies.

**What they do today.** QuickBase already computes a weighted average for them: scored by area, averaged over the total, landing out of 5. So this is not a new capability request — it is a floor the replacement has to clear to be adoptable.

*"Yes, there should be, and it should be based on what that tiering looks like, whether it's turnover, budgets, compliance, whatever that category should be. It's a weighted average currently in QuickBase."* — Their Operations Director

*"In nature and then I would have a score at the end of it all. And it would be by area and then it would average it out over the total. So and then the score would be out of 5 as well."* — Their Operations Director

**Signal strength: strong, and contested across the account.** He is unambiguous. The initiative already carries the opposing position — the site supervisor at the same account prefers a flat average — so this record is the weighted-side evidence in a live contradiction, not a settled requirement. Note also that he recognised the prototype as doing weighted scoring by reading its on-screen breakdown aloud; those weightings are Payworks mock values, not Northwind's.

## Draft ticket

**Objective:** Support per-category weights in a review template, with an overall score computed as the weighted average across categories and the weighting visible to the reviewer.

**Acceptance criteria seed:**
- A review template can assign a weight to each category; weights are configurable per template so different roles can be measured differently.
- The overall score is computed as the weighted average across categories and updates live as ratings are entered.
- The reviewer can see each category's own score alongside the weighted overall, and can see the weight applied.
- The scoring maximum is configurable (out of 5 and out of 10 both supported).
- A template can be configured for an unweighted flat average, since not every manager at the same account wants weighting.
- The overall score is exposed to the merit-increase calculation as its input.
