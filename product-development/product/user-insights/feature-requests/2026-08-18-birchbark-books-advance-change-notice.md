---
account: birchbark-books
requested: 2026-08-18
area: expense-management
type: improvement
priority_signal: nice-to-have
tracker_ref: "-"
source: ../../customers/accounts/birchbark-books/calls/summaries/2026-08-18.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Advance notice of client-visible changes, in a form the firm can forward

**Who asked:** Their Firm Principal, seconded by Their Senior Bookkeeper, at Birchbark Books & Accounting — the firm that administers ~40 client accounts and fields the calls when those clients are confused.

**The underlying need — the administering firm is the unpaid first line of support for every change we ship.** When a client-visible change lands, the client phones the firm, not Payworks. The firm accepts this as part of why clients stay with it, but it currently absorbs each change blind: without notice, a rollout costs a morning and some credibility. With roughly two weeks' warning the firm can brief only the clients a change actually affects, which converts an unplanned support incident into a short planned one. The ask is deliberately cheap — notice, and content the firm can paste into an email rather than a page a client would have to log in to read.

*"You ship something, my client phones me, not you. So whatever you build, I'm the support desk for it, and I don't get paid by you." — Their Senior Bookkeeper*

*"We're the front line for a product we don't own. And I'm not complaining exactly, it's part of why clients stay with us. But when you're planning a rollout, we're the people who absorb it." — Their Firm Principal*

*"Tell us first. Genuinely, that's most of it. If I know a change is coming two weeks out I can warn the ten clients it affects. If I find out because a client phones me confused, I've lost the morning and some credibility." — Their Firm Principal*

*"And ideally in a form I can forward. Not a login-required page. Something I can paste in an email." — Their Firm Principal*

**What they do today instead:** they find out from a confused client and reconstruct the change themselves. Michelle Tremblay accepted the point on the call: *"Noted, and that's a fair criticism of how we do it today."*

**Signal strength — real but prompted, and coping-level rather than blocking.** It came in response to Margaret Foster asking what would make absorbing rollouts easier, not volunteered like the cross-client view or the logins, and the firm manages today without it. Rated `nice-to-have` on that basis — but note the language was strong ("that's most of it") and the cost of satisfying it is low relative to the goodwill it buys in a channel the FY27 strategy depends on. It also has direct bearing on the [expense-management-vp2](../../initiatives/expense-management-vp2.md) rollout plan specifically: the firms administering the client accounts are the population that will absorb a VP2 launch.

**Scope note:** raised in the context of an expense rollout, but the need is cross-module — every client-visible change in any module reaches the firm the same way.

## Draft ticket

**Objective:** Give firms administering client accounts advance, forwardable notice of client-visible product changes, so they can brief affected clients before the change lands instead of discovering it through a support call.

**Acceptance criteria seed:**
- Firms administering client accounts receive notice of client-visible changes ahead of release; target lead time approximately two weeks.
- The notice identifies which of the firm's client accounts are affected, not just that a change exists.
- The notice content is self-contained and forwardable — readable without signing in, suitable for pasting into an email to a client.
- Notice reaches the firm contact(s) the firm nominates, not only the account owner at each client.
- A firm can see the recent-changes history for its clients in one place rather than reconstructing it from individual notices.
