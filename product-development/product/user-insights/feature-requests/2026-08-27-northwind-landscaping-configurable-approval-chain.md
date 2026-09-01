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

# [Expense Management] Configurable, position-based approval chain with auto-escalation and desktop enforcement

**Who asked:** Their Controller at Northwind Landscaping, with supporting pushback from their HR Manager on the escalation piece.

**The underlying need — approval rules that survive people changes and respect geographic structure.** Northwind runs two approval jurisdictions that cannot share a chain: Ontario has regional managers in the hierarchy; BC reports straight to the Ops Director. The current "Approval Authority.doc" was last updated in 2022–2023, names people rather than positions, and has to be manually rebuilt every time a regional manager turns over (three times in four years in one Ontario role). The Controller wants to configure the chain once, have it derive approvers from whoever holds each role in HR, and never rebuild it by hand again.

*"What I would want from a system — and I've thought about this — is I want the tiers to be mine. Not, here's three levels, pick one. I want to say, this yard, this dollar figure, this person." — Their Controller*

*"Approvals should hang off 'regional manager, Ontario west,' and if you put a new person in that chair in the HR side, the approvals should just follow. Nobody should have to remember." — Their Controller*

*"The system already knows who reports to who. Payroll knows. It's just, expense doesn't ask payroll." — Their Controller*

**Current approval tiers (as stated):**
- Under $500 → Regional manager (supervisor's manager)
- $500–$2,500 → Controller
- $2,500+ → Controller + Ops Director (two signatures)
- $5,000+ → Owner (can sit 11 days; happens 6–8 times/year)
- Applied to the whole report total, not per-receipt — and the Controller acknowledged this likely drives gaming (splitting reports to stay under the next tier)

**Threshold scope — per-report today, possibly wrong.** The Controller stated that today the threshold applies to the total report. When asked if that's right: *"Probably not, actually. Because that's how you get someone submitting twice in a month to stay under. Which — I know that happens."* This is an open design question the product team must resolve.

**Auto-escalation with audit trail.** The HR Manager raised the "person in Portugal for two weeks" failure mode from the merit spreadsheet (four-approval chain, stalls every year, she becomes the human escalation system). The Controller agreed: auto-escalate after five business days, but always notify and always record who it went to and why — for audit defensibility.

*"I'd take an auto-escalate after, I don't know, five business days. As long as it tells me it did it. I don't want things approving themselves quietly." — Their Controller*

*"Notify. And it should still say who it went to and why. If I get audited I need to point at the trail." — Their Controller*

*"The thing I would beg for is: what happens when the person in tier three is in Portugal for two weeks." — Their HR Manager*

**Desktop-enforcement above a threshold (Controller-requested, opt-in setting).** For approvals at the Controller's tier ($2,500+), the Controller wants the system to require a desktop browser — not as a security measure but as an attention mechanism. He will "tap yes in a parking lot" on mobile and knows it. The setting should be admin-configurable ("approvals over X require desktop"), opt-in, and sticky once set. This is the second account to request this pattern (Acme Corp also raised it in August).

*"Enforce it. If it's optional I'll do it in the parking lot. No — genuinely, make it a setting I turn on, and then make it stick. 'Approvals over X require desktop.' I'd turn that on day one." — Their Controller*

*"Everybody asks you for more mobile. I'm asking you for a fence. It's the same reason my five thousand goes to the Owner. Some decisions should be slightly annoying." — Their Controller*

**Notification channels — email for office, push badge for field.** Regional managers can receive email (sometimes at a computer). Yard-level supervisors need a push notification badge on the mobile app. The Controller flagged that many field employees have no company email address in the system (the same root as the performance-management QuickBase gap); an email-only notification story does not reach the people who most need it.

*"For the yard-level guys it has to be the phone, and it has to be a badge, not an email." — Their Controller*

*"Half of them don't have a company email. That's the other thing… If your notification story is email, it doesn't reach the people who most need it." — Their Controller*

**What they do today instead:** A Word document called "Approval Authority.doc" last updated 2022–2023. Manual routing. When a regional manager leaves, the Controller rebuilds the routing by hand. Eleven-day approvals for $5,000+ items because the Owner is on-site and unreachable.

**Signal strength — strong, detailed, first-hand.** This is the first record in the corpus that states approval-chain configuration requirements (number of tiers, per-yard geography, position-vs-person binding, auto-escalation, desktop enforcement) from a client-side Controller. The pattern is consistent with the Birchbark Books `approval-thresholds` record and the Acme Corp `approval-thresholds` record but goes substantially deeper in operational detail.

## Draft ticket

**Objective:** Let an admin define expense approval chains that are configurable by site/yard and dollar threshold, bound to positions rather than named individuals, automatically escalate when an approver is unavailable, enforce desktop review above a configured threshold, and deliver notifications through the right channel for each approver tier.

**Acceptance criteria seed:**
- An admin can define approval tiers per site/yard: threshold range → position (e.g., "Regional Manager, Ontario West").
- Approver resolution looks up who currently holds that position from the HR/Payroll org hierarchy — no manual name binding.
- When the approver in a tier has not acted within a configurable number of business days (default: 5), the item auto-escalates to the next tier; both the escalation and the reason are recorded in the approval log.
- Auto-escalation generates an audit-legible trail: timestamp, what escalated, from whom, to whom, and why.
- An admin can set a threshold above which approvals require a desktop browser; mobile approval attempts above that threshold are blocked, not merely warned.
- Approvers at office tiers receive email notifications; approvers without a company email in the Payworks profile receive push notifications on the mobile app.
- The admin approval-chain configuration is editable without a support ticket; changes take effect on the next submission cycle.
- BC yards can run a different chain from Ontario yards within the same account.
