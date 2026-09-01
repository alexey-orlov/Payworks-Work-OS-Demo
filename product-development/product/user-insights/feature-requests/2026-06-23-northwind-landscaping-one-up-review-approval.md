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

# [Performance Management] One-up review of a completed review before it is processed

**Who asked:** Their Operations Director at Northwind Landscaping, in a discovery interview + prototype review on 2026-06-23. He raised it unprompted while describing what the review should pull in.

**The underlying need.** A completed review reaches processing on the judgment of one manager. He wants the same escalation the compensation recommendation already gets — his boss sees the review before it is final — and he wants the approver to see the evidence the reviewer saw, not just the verdict. This matters more once the review drives the merit increase, because an unreviewed rating then becomes an unreviewed pay decision.

**What they do today.** Compensation recommendations do escalate: his reports recommend to him, he recommends upward, and the spreadsheet is reviewed at C-level. The review itself has no equivalent second stage described. (The transcript line immediately after his ask is garbled, so treat this as a stated requirement rather than a confirmed statement of today's state.)

*"and there should be a two-stage process as well. It should be, if I'm doing it, then my boss should review it before it gets processed, type of scenario, right? Like a one-up review."* — Their Operations Director

*"And then if somebody has to review it."* / *"before it's processed, then they have the visibility to that information as well"* — Their Operations Director

**Signal strength: strong.** Volunteered, specific, named with its own term ("one-up review"), and consistent with the escalation pattern the account already runs for compensation.

## Draft ticket

**Objective:** Add an approval stage between a manager completing a review and the review being processed, routed to the reviewer's own manager.

**Acceptance criteria seed:**
- A completed review can be routed to the reviewer's manager for approval before it is finalised or shared with the employee.
- The approver sees the ratings, the comments and the supporting evidence the reviewer saw.
- The approver can approve or return the review with a comment; a returned review goes back to the reviewer, not to the employee.
- The approval stage is configurable per review cycle or review level — not every review needs it.
- The approval state and approver are recorded on the review.
- Where the review carries a compensation recommendation, the recommendation is visible at the same approval step rather than escalating on a separate path.
