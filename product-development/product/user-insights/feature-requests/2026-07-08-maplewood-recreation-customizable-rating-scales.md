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

# [Performance Management] Customizable, word-based competency rating scales

**Who asked:** their HR Business Partner, reacting to the numeric competency scale on the
prototype's self-assessment screen (2026-07-08 discovery interview + prototype review).

**Underlying need.** They rate on defined *words*, not numbers, and the reason is rating
consistency across a leader population whose technology comfort and judgement vary widely.
A number invites each leader to apply their own scale; a defined word does not. Their
existing PDF form already spells the word ratings out, so this is backed by an artifact,
not a preference.

*"The number ratings, funny that you put number ratings in there. We don't use number ratings, we use words, and you can see my form that we do define out, those, those ratings. I don't know if you have the ability to customize the ratings as well, based on what we want." — Their HR Business Partner*

*"We went with… The words, again, for consistency. I think numbers can maybe become a little bit more subjective to the lead, depending on the leader." — Their HR Business Partner*

*"Numbers we find a bit inconsistent." — Their HR Business Partner*

**What they do today instead.** A PDF fillable form, one per employee, carrying their own
word-based scale with each rating defined in text on the form.

**Signal strength.** Strong and unambiguous. Stated twice in the same exchange, grounded in
their live form, and framed as the reason they chose words in the first place. A numeric-only
scale would be a blocker for this account. Related: they also declined an overall rating
outright — see the session report.

## Draft ticket

**Objective:** Let an administrator define the rating scale used on a review form — the number
of points, the label for each point, and a definition per label — with words as a
first-class scale type rather than a display skin over numbers.

**Acceptance criteria seed:**
- An admin can create a scale with N named points and a definition string per point.
- A form template references a scale; changing the scale does not alter reviews already submitted.
- No numeric value is shown to the employee or manager when a word scale is selected.
- The definition of each rating point is visible to the rater at the moment of rating.
- More than one scale can exist in a company, so different form types can use different scales.
