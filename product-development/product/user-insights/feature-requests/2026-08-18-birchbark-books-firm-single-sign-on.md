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

# [Payroll] One firm login across every client account — replacing forty sign-ins and client-held two-factor codes

**Who asked:** Their Firm Principal at Birchbark Books & Accounting (Persona 6, "The Accountant" — the practice owner). He joined the call partly for this, prefaced it with an acknowledgement that it was not our agenda, and raised it anyway as the change that would most affect his week.

**The underlying need — the firm has forty client identities and no firm identity.** Signing in to a client account takes roughly nine clicks and a two-factor code, and on older accounts that code routes to whoever originally set the account up — which is sometimes the client. The consequence is both operational and a security posture the Firm Principal named himself: to run a client's payroll he has phoned the client to have an authentication code read aloud, which trains clients to read out authentication codes on request. The firm also adds four to six new clients a year at about a day of setup each, so per-account identity is a recurring cost, not a one-time one.

*"The logins. I know it's not what you're working on, and I know you've heard it, but it's the thing that would change my week the most." — Their Firm Principal*

*"We have forty client accounts and I sign into them one at a time. And it's — what is it, nine clicks? And a two-factor code, and the code goes to whoever set the account up, which sometimes is the client." — Their Firm Principal*

*"on Tuesday I texted a plumber to ask him to read me a number so I could run his payroll. That's the state of the art." — Their Firm Principal*

*"It's not good and it's also, um, it's a security thing, right? Like I'm training a client to read authentication codes out loud to whoever asks." — Their Firm Principal*

*"And what I want is one login. One. I sign in as the firm, I see my forty clients, I go where I need to. And when I hire someone, I give them nine clients and not the other thirty-one." — Their Firm Principal*

**What they do today instead:** forty separate sign-ins, one at a time, with out-of-band code retrieval from clients where the two-factor destination is wrong. There is no workaround the firm has found; it absorbs the cost.

**Signal strength — must-have, volunteered, and raised against the meeting's agenda.** He spent the last of his limited time on it rather than the expense topic he was invited for. This is the account's stated top operational pain, and it carries a security dimension the firm articulated without prompting.

**Where it lands:** the catalogued `firm-management` feature (Payroll area, `status: planned`, described as "Firm admin portal where an accounting or bookkeeping firm connects to client accounts and manages its team's access"). **No initiative in this repo currently covers it.** It is also a dependency for the [cross-client expense view](2026-08-18-birchbark-books-cross-client-expense-dashboard.md) that [expense-management-vp2](../../initiatives/expense-management-vp2.md) has in scope — a channel view that still requires forty sign-ins does not deliver the outcome asked for.

## Draft ticket

**Objective:** Give an accounting or bookkeeping firm a single firm-level identity that signs in once and reaches every client account the firm administers, removing per-client sign-in and eliminating two-factor codes that route to the client.

**Acceptance criteria seed:**
- A firm user signs in once with firm credentials and sees a list of the client accounts they are assigned to.
- Moving from the client list into a client account requires no second sign-in and no second two-factor challenge.
- Two-factor for a firm user is delivered to the firm user, never to a contact at the client.
- Adding a new client account to the firm does not require creating a new per-account login for each firm staff member.
- A firm user's client list reflects their assignment, not the firm's full book (see the firm-roles record).
- Existing per-account client logins continue to work for client-side users; the firm route is additive, not a migration the client must perform.
