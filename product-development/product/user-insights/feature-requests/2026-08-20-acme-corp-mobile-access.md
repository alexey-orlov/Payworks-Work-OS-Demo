---
account: acme-corp
requested: 2026-08-20
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: [manager-otg-approval]
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Mobile: submission yes, approval blocked above the threshold

Asked whether they need expenses on a phone, the two attendees answered in the same breath — "Yes" and "No" — and the split is the useful part.

**Submission, yes.** Their Payroll Administrator wants to capture and submit at the moment of spend while travelling, and scoped the ask deliberately narrow: capture the receipt and be done, nothing else. She is explicit that she does not want the rest of the product on a phone.

**Approval, no — and blocked rather than discouraged.** Their HR Manager opposes approving expense claims on a phone, on first-hand evidence from their own time-off rollout: putting time-off approvals on mobile took the approval rate to effectively 100% overnight, and not because the requests improved. She describes the failure mode as muscle memory, which is why she does not believe a confirmation dialog helps: everyone taps yes on those too. She wants the system to prevent a large claim from being approved on a phone.

Crucially, she does **not** object below the auto-approval floor — under $250 she agrees it should not need approving at all. That makes this and the threshold record the same design decision: the block applies above whatever number the threshold sets.

Michelle noted on the call that the account team had relayed the same instinct from a finance person at a much larger client, which suggests this is not a small-employer preference.

**Who asked:** Their Payroll Administrator (mobile submission); Their HR Manager (mobile approval blocked above the threshold).

**Today instead:** Claims are filled on an Excel template and emailed, so nothing happens at the point of spend; a traveller carries the claim home. Manager approval happens wherever the email is read, including on a phone.

**Signal:** Strong on both sides, and evidence-backed on the approval side by an outcome they observed in their own absence process. This bears directly on `expense-management-vp1`, which shipped mobile-first including the first approval step.

*"I mean — submitting, yes. If I'm at a conference and I've just paid for a taxi, I want to deal with it there, not carry it home in my head for a week." — Their Payroll Administrator*

*"Submitting. Not the whole thing. I don't need to run a payroll on a phone, God forbid. But snapping the taxi receipt and being done with it, yes." — Their Payroll Administrator*

*"I watched this happen with time off. We put time-off approvals on the phone and the approval rate went to basically a hundred percent overnight, and it wasn't because everybody's requests got better." — Their HR Manager*

*"It's a tap. It's the same tap as clearing a notification. Your thumb does it before your brain arrives. And with time off that's mostly fine, honestly, but with money I don't love it." — Their HR Manager*

*"But the four-thousand-dollar conference claim? No. I want that person at a desk with the receipts open. And I'd rather the system just didn't let them do it on a phone at all." — Their HR Manager*

*"Blocked. Because 'discouraged' means a grey box that says 'are you sure' and everyone taps yes on those too." — Their HR Manager*

## Draft ticket

**Objective:** Support full claim capture and submission on a mobile device, and let a client prevent expense approvals above the auto-approval threshold from being completed on a mobile device.

**Acceptance criteria seed:**
- A claimant can create, attach a receipt photo to, and submit a complete claim from a phone, without needing a desktop step to finish it.
- Approving a claim at or above the client's auto-approval threshold on a mobile device is prevented, not warned — no "are you sure" dialog path to completion.
- Below the threshold no approval exists at all, so the restriction is inert there by construction.
- The blocked state tells the approver what to do next (open it on a desktop) rather than failing silently.
- The restriction is a client setting, defaulting to the behaviour the launch group already has, so VP1's shipped mobile-first approval is not removed from anyone without a decision.
- Verify against VP1's shipped scope before building — VP1 delivered mobile-first submission *and* the first approval step to a limited group.
