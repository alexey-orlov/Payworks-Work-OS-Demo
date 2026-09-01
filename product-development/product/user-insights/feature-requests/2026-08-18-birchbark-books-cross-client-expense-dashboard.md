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

# [Expense Management] Cross-client expense status view — one screen, forty rows, worst first

**Who asked:** Their Senior Bookkeeper at Birchbark Books & Accounting — a six-person bookkeeping practice doing full-cycle bookkeeping for ~40 small businesses and payroll for 33 of them, ~1,100 employees across the book. She is the hands-on processor for the whole book (Persona 7, "The Bookkeeper").

**The underlying need — seeing a problem in October instead of discovering it in February.** The firm loses two weeks of whole-firm capacity every February to catch-up work on clients who did nothing all year. It is the same eight or nine clients annually, and she can name them by September — but she has no way to watch the backlog accumulate, because the data lives per-client behind forty separate logins. The ask is not analytics or insight; it is an operational worklist that makes an already-known problem visible early enough to act on. The intervention it unlocks is a single phone call per at-risk client in October, which is also the firm's economic argument for the feature: a billable advisory hour in October replaces two unbillable days of firefighting in February.

*"One screen. Forty rows. Here's how many receipts are unprocessed, here's how many approvals are sitting, here's who hasn't submitted since June. Sorted worst first." — Their Senior Bookkeeper*

*"I can tell you today which clients are going to hand me a bag in February. I just can't do anything about it, because I've got no way to see it building." — Their Senior Bookkeeper*

*"That's a billable hour in October instead of two unbillable days in February. So it's better for them and better for us, and I can't do it, because I can't see it." — Their Senior Bookkeeper*

**What they do today instead:** nothing — and that is the point. The information exists per client, but assembling it means signing into forty client accounts one at a time. *"right now to get that I'd log in forty times."* / *"Nobody does that. So instead I find out in February. The information exists, it's just in forty places and I'm one person." — Their Senior Bookkeeper*

**Signal strength — the strongest single ask on the call, and volunteered, not prompted.** It surfaced only in the last three minutes, after the Firm Principal left, in response to an open "anything you want to say" question — not to a feature question. She ranked it herself against everything else we had asked about, and asked to be shown it at any fidelity: *"That's the thing I want more than anything else you've asked me about today. Not because it's clever — because right now to get that I'd log in forty times." — Their Senior Bookkeeper* / *"bring me the forty-row screen, even if it's a drawing on a napkin. That's the one I want to argue about." — Their Senior Bookkeeper*

**Why this one matters beyond one account:** it is the concrete form of what [expense-management-vp2](../../initiatives/expense-management-vp2.md) already has in scope as "the channel view for a firm administering expenses across client databases," and it is the same shape as the live Payroll Hub feature (one dashboard of every client's upcoming payroll obligations) applied to expense obligations — a pattern this account already runs for payroll.

**Dependency:** firm-level identity and cross-client access. See [single firm login](2026-08-18-birchbark-books-firm-single-sign-on.md) and [firm-level roles](2026-08-18-birchbark-books-firm-role-based-access.md) — a cross-client view that still requires forty sign-ins does not deliver the outcome asked for.

## Draft ticket

**Objective:** Give a firm administering expenses across multiple client databases one screen listing every client it administers, with the expense-state counts that predict a year-end backlog, ordered worst-first, so the firm can intervene during the year rather than at year end.

**Acceptance criteria seed:**
- One row per client account the signed-in firm user is assigned to; the full book is visible in one view without switching accounts.
- Per-row metrics, at minimum: count of unprocessed/uncoded receipts, count of approvals outstanding, and time since the client's last submission.
- Default sort is worst-first on backlog severity; the firm can re-sort and filter.
- A row drills through to that client's expense queue without a separate sign-in.
- Counts are current as of the last data refresh, and the view states its freshness.
- Scoped to the client accounts the firm user has been assigned (see the firm-roles record) — never the firm's whole client list regardless of assignment.
