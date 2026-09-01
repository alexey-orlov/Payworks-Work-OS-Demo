---
account: birchbark-books
requested: 2026-08-18
area: payroll
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/birchbark-books/calls/summaries/2026-08-18.md
features: [firm-management]
initiatives: []
updated: 2026-08-31
---

# [Payroll] Firm-level roles applied across client accounts — code expenses without being able to transmit a payroll

**Who asked:** Their Firm Principal raised it; Their Senior Bookkeeper escalated it unprompted as her single biggest worry. Birchbark Books & Accounting — six staff, ~40 client books, payroll for 33 of them.

**The underlying need — access is all-or-nothing per client account, so the firm's only control over a junior is a verbal instruction.** A firm staff member either has full access to a client's payroll or none at all. There is no grain that separates the low-risk work a junior actually does (coding expenses) from the irreversible act the firm cannot afford them to touch (transmitting a payroll). The firm's compensating control is social, and both participants named it as inadequate. The cost compounds twice over: permissions are set per account, so each of the two or three people the firm hires each year has to be permissioned across forty accounts, and each of the four to six new clients per year has to be permissioned for every existing staff member.

*"Access. Right now it's all or nothing per account. My junior can either get into a client's payroll completely or not at all. There's no 'she can code expenses but she can't transmit a payroll.'" — Their Firm Principal*

*"That's the one that keeps me up, honestly." — Their Senior Bookkeeper*

*"Because a junior with full access to a client's payroll is one wrong click from a real problem, and it wouldn't be malicious, it'd be a Tuesday afternoon and a mis-click." — Their Senior Bookkeeper*

*"I can't limit them, so I do it socially. I tell her not to. Which works because she's good. It is not a control, it's a relationship, and that's not a system." — Their Senior Bookkeeper*

*"Roles at the firm level that apply across clients. Because otherwise I'm setting up permissions forty times per employee, and we hire two or three people a year." — Their Senior Bookkeeper*

**What they do today instead:** grant full access and instruct staff verbally not to use it. The firm is explicit that this is not a control.

**Signal strength — must-have, and the only item on the call that a participant volunteered as costing them sleep.** It was raised by the Firm Principal as an access-scoping convenience and immediately re-framed by the Senior Bookkeeper as a risk-control gap, which is a stronger reading of the same requirement. It is also the item most likely to matter across the channel segment rather than to this account alone: any firm with more than a handful of client databases and any junior staff has the same exposure.

**Where it lands:** the catalogued `firm-management` feature (Payroll area, `status: planned` — "manages its team's access"). **No initiative in this repo currently covers it.** Pairs with the [single firm login record](2026-08-18-birchbark-books-firm-single-sign-on.md); together they are the access substrate the [cross-client expense view](2026-08-18-birchbark-books-cross-client-expense-dashboard.md) depends on.

## Draft ticket

**Objective:** Let a firm define roles once at the firm level, assign staff to specific client accounts, and have the role's permissions apply across those accounts — including a role that can perform expense coding but cannot transmit a payroll.

**Acceptance criteria seed:**
- A firm defines named roles at the firm level; a role is created once and applies wherever it is assigned.
- Role permissions are task-level, not account-level — at minimum, expense coding, payroll preparation and payroll transmission are separately grantable.
- A firm staff member is assigned to a named subset of client accounts; unassigned client accounts are neither visible nor reachable to them.
- Adding a new staff member requires assigning a role and a client list, not configuring permissions once per client account.
- Adding a new client account applies existing firm roles to the staff assigned to it, without per-staff reconfiguration.
- Permission changes are auditable: who changed a firm role or an assignment, and when.
