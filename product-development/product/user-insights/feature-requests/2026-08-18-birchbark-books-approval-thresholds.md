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

# [Expense Management] Approval thresholds as a firm template — set once, push to clients, override per client, notify on change

**Who asked:** Their Senior Bookkeeper at Birchbark Books & Accounting (Persona 7, "The Bookkeeper"), with Their Firm Principal on the call.

**The underlying need — the firm needs the policy to be its default, because it has responsibility without authority.** In her clients' businesses the owner approves everything, which works at eight employees and silently stops working around thirty: the owner is in a van clearing forty-one notifications, so approval still happens and means nothing — and the firm relies on that hollow approval at year end when an auditor asks who signed off. Only nine of forty clients have any written policy, and those nine use two numbers, $100 and $500, both of which she supplied. She needs the rule to be hers by default and to find out immediately when a client changes it, because she is the one who has to explain the rule later.

*"It looks like everything's approved, because he approves everything, because he's in a van and he's got forty-one notifications and he just clears them." — Their Senior Bookkeeper*

*"The approval is a formality that we then rely on at year end. And when the auditor asks who approved this, I say the owner did, and technically that's true." — Their Senior Bookkeeper*

*"I'm the person who's responsible for forty companies and accountable for none of them." — Their Senior Bookkeeper*

*"I need defaults. Defaults are influence. Nobody changes a default. That's the only power I've ever had in this job." — Their Senior Bookkeeper*

**Critical: the obvious version of this feature is a net negative for the firm.** Asked directly whether configurable per-client approval thresholds would be good for her, she said *"Honestly? Partly bad." — Their Senior Bookkeeper* — because *"you'd be giving me forty rulesets to maintain"* and *"If it's in the system it's forty things the client can change without telling me. And I'll find out in November when something didn't route, or worse, at year end when the auditor asks and the rule isn't what I said it was."* Her precedent for this failure mode is an existing Payworks decision: *"It's the same as the chart of accounts. You gave clients the ability to add accounts and now I've got a client with three accounts called Materials. Three. All slightly different." — Their Senior Bookkeeper*

**The shape that makes it good:**

*"A firm template. So I set it once — under a hundred goes, over a hundred goes to the owner, over a thousand flags to me — and I push that to every client I want it on." — Their Senior Bookkeeper*

*"Override where I need to, yes. But the default is mine, not theirs. And if a client changes it, I want to know. Not a report I have to go find. Tell me." — Their Senior Bookkeeper*

*"Notified, and ideally with a 'was, now' so I can see what it used to be. Because half the time the client will swear they didn't change it and they did, and I'd like to not have that conversation." — Their Senior Bookkeeper*

**What they do today instead:** the policy lives in one person's head and in nine emails. *"Right now the policy lives in my head and in nine emails. That's bad, I'm not defending it. But it's forty things I know."*

**Signal strength — strong need, and a direct correction to how we framed the feature.** Prompted (Michelle asked the design question outright) but answered with a rejection of the proposed design and a substitute design, which is stronger evidence than agreement would have been. This is the **first record in the corpus that states approval thresholds as a customer requirement** — [expense-management-vp2](../../initiatives/expense-management-vp2.md) has held it as an unbacked hypothesis. It arrives with its shape changed: per-client configuration alone should not be built for this segment.

## Draft ticket

**Objective:** Let an administering firm define expense approval routing once at the firm level and apply it across its client accounts, overriding per client where needed and being notified — with the prior and new values — whenever a client changes a rule the firm depends on.

**Acceptance criteria seed:**
- A firm can define a named approval-threshold template: amount bands with a routing target per band (auto-approve / client owner / firm reviewer).
- A template can be applied to a firm-selected subset of client accounts, not only all-or-nothing.
- A client account's rules can be overridden individually; the override is visible at the firm level as a deviation from the template.
- When a client-side user changes a threshold or routing rule, the firm is notified proactively — a push notification, not a report the firm must go looking for.
- The notification states the previous value and the new value, with who changed it and when.
- Applying a template to a client never silently discards a client-side rule without surfacing the change to the firm.
