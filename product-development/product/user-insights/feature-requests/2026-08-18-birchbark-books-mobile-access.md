---
account: birchbark-books
requested: 2026-08-18
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/birchbark-books/calls/summaries/2026-08-18.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Mobile approval for the client-side approver — and explicitly not for the firm

**Who asked:** Their Firm Principal (mobile-for-clients) and Their Senior Bookkeeper (not-for-the-firm) at Birchbark Books & Accounting — a six-person bookkeeping practice administering ~40 client books, 33 of them on payroll.

**The underlying need — the approver in a small trades business has no desk, so a desktop approval is a non-approval.** The firm's clients are trades businesses: plumbing, electrical, HVAC. The person who approves expenses is the owner, and the owner is driving to jobs. The Firm Principal accepted the quality tradeoff knowingly — a phone approval cleared quickly is worth more to him than a considered approval that arrives in March, because the realistic alternative to a phone approval is no approval at all. The firm side is the exact inverse: reviewing forty clients' coding is two-screen comparison work, and a firm-side phone surface would go unused.

*"Massive. For the clients." — Their Firm Principal* / *"Irrelevant. For us." — Their Senior Bookkeeper*

*"My clients are in vans. That's the honest picture. The approver is a guy who owns a plumbing company and drives to jobs, and if the approval isn't on his phone it doesn't happen, it just doesn't happen." — Their Firm Principal*

*"I'd rather he cleared them badly on time than well in March. That's the trade, and I know that's an unpopular thing to say to a product person." — Their Firm Principal*

*"Because the alternative isn't careful approval, it's no approval. There is no world where he sits down at a desk. There is no desk. He does not have a desk." — Their Firm Principal*

*"Nothing. I have two monitors and I need both. Every single thing I do is comparing one screen to another screen. There is no phone version of my job and I would never use one." — Their Senior Bookkeeper*

*"I don't approve. I review. Those are different words. If I'm reviewing forty clients' expense coding I'm doing it at eight in the morning with coffee and two monitors, and I like it that way." — Their Senior Bookkeeper*

**What they do today instead:** client owners clear notifications in bulk from a phone, which is the mechanism behind the hollow-approval problem the [approval-thresholds record](2026-08-18-birchbark-books-approval-thresholds.md) documents — *"he's in a van and he's got forty-one notifications and he just clears them."* The firm does its review on desktop and would not change that.

**Signal strength — strong and directional; prompted by our question, answered with a split we did not anticipate.** This is the **first record in the corpus that states mobile access as a customer requirement.** [expense-management-vp2](../../initiatives/expense-management-vp2.md) has held mobile as an unbacked hypothesis; it is now backed for one population and explicitly rejected for the other. The negative half is the more useful half for scoping: **any VP2 mobile scope that includes a firm-side mobile surface is building something this firm says it would never use.** Note the adjacency — [expense-management-vp1](../../initiatives/expense-management-vp1.md) shipped mobile-first claim submission and a first approval step to a limited group on 2026-08-21, three days after this call; neither participant referenced having seen or used it, so this record is a statement of need, not feedback on what shipped.

**Also relevant to the role model:** the review-is-not-approval distinction. The firm is not a node in the approval chain; it inspects afterwards. Modelling the firm as an approver would put it in a workflow position it does not occupy.

## Draft ticket

**Objective:** Make the client-side expense approval step complete on a phone, end to end, for an approver who never sits at a desk — while keeping the firm-side review experience a desktop, multi-pane surface.

**Acceptance criteria seed:**
- A client-side approver can see a pending claim, view its receipt image, and approve or reject it entirely on a phone, with no desktop step required to finish.
- Approval works from the notification without requiring the approver to locate the claim separately.
- Bulk clearing is possible but distinguishable in the audit trail from item-by-item approval, so the firm can see how an approval was given.
- The firm-side review surface is designed for desktop and multi-pane comparison; no firm-side workflow requires a mobile device to complete.
- No firm-only capability is delivered exclusively on mobile.
