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

# [Performance Management] Per-field mandatory control on review forms

**Who asked:** their HR Business Partner, at the point of submitting the prototype's
self-assessment (2026-07-08).

**Underlying need.** Blank submissions are the specific failure that ended their last digital
rollout: leaders submitted empty forms, payroll caught them, and the work had to be redone. She
wants the system to refuse an incomplete submission — but not uniformly, because a blanket
mandatory rule would be too rigid across two form types and a wide leader population. Field-level
control is the ask.

*"I'd probably have those as mandatory before submitting the assessments." — Their HR Business Partner*

*"Yeah, I have the mandatory, because I submitted that blank. Right. […] That would happen a lot." — Their HR Business Partner*

*"if you could flex Michelle, that'd probably be best. Like, you could pick and choose which ones were mandatory, that one would be best." — Their HR Business Partner*

**What they do today instead.** Nothing enforces completion. On the PDF, every field is
optional — she checked her own form live on the call and confirmed it. Their control is the
Payroll Manager visually scanning every submitted form and flagging blanks to HR.

**Signal strength.** Strong, and load-bearing: blank digital submissions are one of the two
documented reasons this account rolled back from a digital form to PDF two weeks before the
interview. A review form that can be submitted empty repeats the failure they just escaped.

## Draft ticket

**Objective:** Let an administrator mark any field on a review form template as mandatory or
optional, and block submission until every mandatory field on that form is complete.

**Acceptance criteria seed:**
- Each field on a form template carries a mandatory / optional setting.
- Submission is blocked with a clear per-field indication of what is missing.
- Save-draft is unaffected — an incomplete form can always be saved and resumed.
- The setting is per form template, so the permanent and seasonal forms can differ.
