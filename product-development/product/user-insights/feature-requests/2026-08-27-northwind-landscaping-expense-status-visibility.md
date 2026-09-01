---
account: northwind-landscaping
requested: 2026-08-27
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Claimant status visibility — "approved, paying on the 11th"

**Who asked:** Their Controller and Their HR Manager at Northwind Landscaping.

**The underlying need — the number-one phone call is "did it go through," not "where's my money."** The Controller states that expense-related phone calls are the single most common support call he fields — not payroll questions, expenses. The frustration is not primarily about the wait; it is about not knowing whether the receipt arrived at all. The HR Manager generalised this to every HR process they run: reviews, time off requests, expenses — the question is always the same.

*"That's the single thing I get phoned about. Not 'where's my paycheque,' they never phone about that, payroll's fine. It's 'where's my ninety bucks from the Home Hardware.'" — Their Controller*

*"He doesn't need it faster, necessarily. He needs to know. Half the frustration is not the wait, it's not knowing if the envelope even arrived." — Their Controller*

*"Just — reviews, time off, expenses. The number one question I get is 'did it go through.' Not 'can you approve it,' just, did the thing I did land somewhere. It's the same question every time." — Their HR Manager*

**What "visible" means here.** The Controller's specific resolution: the claimant should be able to see in the mobile app the status of each submitted expense item, including the target pay date once approved. The phrase he used — "approved, paying on the eleventh" — is the complete user story. No additional detail is required beyond the status and the date.

*"It should roll to the next one. Quietly, automatically, and the guy should be able to see, in whatever app he's got, 'approved, paying on the eleventh.' That's it. That's ninety percent of my phone calls gone." — Their Controller*

**Why this is filed as a separate record from the payroll-register request.** The payroll-register record covers the Controller's view (what appears on the register, lock behaviour, drill-down). This record covers the submitter's view (what the crew member or supervisor sees in the mobile app after submitting). They are different surfaces with different audiences, and either could be built without the other.

**Cross-module signal.** The HR Manager's generalisation is the most important sentence: "did it go through" is the number-one question across reviews, time off requests, and expenses. This is not an expense-specific request — it is evidence that status visibility is a platform-level gap. Filed here against expense management because that is the context in which it was stated. The performance-management and onboarding initiatives may benefit from the same pattern.

**What they do today instead:** No status. The receipt goes into an envelope or, if lost, nowhere. The submitter has no way to know whether the envelope arrived until they receive a reimbursement or make a phone call.

**Signal strength — strong, dual-voice, first-hand.** Both the Controller and the HR Manager raised this independently and consistently. The Controller quantified it ("ninety percent of my phone calls"). The HR Manager generalised it across every HR process.

## Draft ticket

**Objective:** Let a claimant see the real-time status of each expense submission in the mobile app — including whether it was received, whether it is approved, and which pay date it is targeting — so "did it go through" is never a phone call.

**Acceptance criteria seed:**
- After submitting an expense, the submitter sees a status in the mobile app: submitted / under review / approved / rejected / paid.
- When an approved expense is assigned to a pay run, the status updates to show the target pay date (e.g., "Approved — paying Thu, Sep 11").
- When an expense rolls to the next pay run (missed cutoff), the status reflects the new target date automatically, without the submitter needing to re-submit or inquire.
- A rejected expense shows the reason in the same status view.
- Status updates are pushed to the mobile app without requiring a manual refresh.
- The status view is accessible to crew members and supervisors who submit claims, not only to admins.
