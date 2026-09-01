---
account: acme-corp
requested: 2026-08-20
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/acme-corp/calls/summaries/2026-08-20.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Auto-approval floor — claims under a set amount pay without an approval step

At 75 employees every expense claim, down to a $19 parking receipt, waits on a manager click that nobody reads. Their Payroll Administrator wants a configurable floor — she named $250 — under which a claim pays straight onto the pay run with no approval, so that the approvals a manager *does* see are few enough to be read. Her framing is that the current step is not a control at all: it costs three days of waiting and produces no scrutiny. A $5,000 owner tier already exists in their written policy and has fired exactly twice, ever (a conference and a trade-show booth), so functionally they run one approval level today.

**Who asked:** Their Payroll Administrator, on a discovery call requested by client services after expenses came up twice on quarterly check-ins. Their HR Manager contested it and then accepted it, conditional on the manager still being *informed* — see the paired record `2026-08-20-acme-corp-manager-spend-digest.md`.

**Today instead:** One manager approval on every claim regardless of amount; ~25 claims a month; the administrator spends a day and a half a month on the cycle, half of it chasing.

**Signal:** Strong and specific — a named number, an articulated rationale, and an on-call resolution between the two people who own the process. This is the first time approval thresholds appear as stated customer signal anywhere in the corpus; `expense-management-vp2` previously classed them as a hypothesis.

*"Okay. So what I would want is a number — say two hundred and fifty dollars — and under that, it just goes. No approval. Straight to me, straight onto the pay." — Their Payroll Administrator*

*"Auto-approved. Because right now a manager is clicking yes on a nineteen dollar parking receipt, and they're not reading it. Nobody reads a nineteen dollar parking receipt." — Their Payroll Administrator*

*"So it's a fake control that costs me three days of waiting. And then over two-fifty, the manager actually has to look at it, and maybe they would, because there'd be four of them a month instead of twenty." — Their Payroll Administrator*

*"Over five thousand it goes to the owner but that has happened, what, twice? Ever?" — Their HR Manager*

## Draft ticket

**Objective:** Let a client configure an amount below which an approved-by-policy expense claim skips the manager approval step and flows straight to reimbursement, while claims at or above the amount follow the existing approval chain.

**Acceptance criteria seed:**
- An administrator can set a per-client auto-approval amount, and can set it to zero (every claim approved) so today's behaviour remains available.
- A claim whose total is below the amount reaches reimbursement without an approver action and is marked as auto-approved, not as manager-approved, in its audit trail.
- A claim at or above the amount routes to the manager exactly as today; an existing higher tier (their $5,000 owner level) still routes above it.
- The threshold is a single number a non-specialist can set — their HR Manager's stated objection is that *"Adding a tier doesn't add oversight, it adds a thing to configure."*
- Auto-approved claims still appear in the manager's team-spend view (paired record) — the threshold must not remove the manager's awareness of the spend.
- Claim total, not line total, is what the threshold tests (their $4,000 conference trip arrives as one multi-line claim).
