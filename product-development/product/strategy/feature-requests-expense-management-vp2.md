# Feature Requests — Expense Management VP2

Inbound demand joined to `expense-management-vp2` (initiative, matched in initiatives
registry), clustered by the job behind the ask, with a verdict per theme. The whole-pile
board is [feature-requests.md](feature-requests.md); this file never re-rates it.

**Read this when:** You are planning `expense-management-vp2` and want only the demand
attached to it.

**Last triaged:** 2026-08-31 · **Scope:** `expense-management-vp2` (initiative, matched in
`product-development/product/initiatives/expense-management-vp2.md`) · **Sources:** 14
records + 0 additional via summaries across 2 accounts · **Admitted:** 14 by own
`initiatives:` link · 0 via source summary · 0 by area-only · **Excluded (no join):**
2 records · **Window:** 2026-08-18 – 2026-08-20

**Excluded records — filing gap (carry no `initiatives:` link to `expense-management-vp2`):**
- [`2026-08-18-birchbark-books-firm-role-based-access.md`](../user-insights/feature-requests/2026-08-18-birchbark-books-firm-role-based-access.md) — area: payroll, initiatives: [] — a named dependency of the cross-client dashboard theme (Theme 6) but not linked to this initiative; add `initiatives: [expense-management-vp2]` to bring it in on re-triage
- [`2026-08-18-birchbark-books-firm-single-sign-on.md`](../user-insights/feature-requests/2026-08-18-birchbark-books-firm-single-sign-on.md) — area: payroll, initiatives: [] — same dependency; same fix

**Account normalization:** `birchbark-books` and `acme-corp` both match their frontmatter slugs exactly — no normalization required.

---

## Themes

| # | Theme — the job behind it | Requests folded in | Requests | Accounts | Fit | Evidence | Verdict |
|---|---|---|---:|---:|---|---|---|
| 1 | Match claim submission and approval to the device each role actually uses | *"Massive. For the clients." / "Irrelevant. For us."* — Firm Principal + Senior Bookkeeper (birchbark-books); *"Blocked. Because 'discouraged' means a grey box that says 'are you sure' and everyone taps yes."* — HR Manager (acme-corp) +2 more | 2 | 2 | High — VP2 scope; VP1 baseline | Strong — 2 accounts | **Act now** |
| 2 | Define expense approval routing without becoming a rulesets maintenance burden | *"A firm template. I set it once and push that to every client."* — Senior Bookkeeper (birchbark-books); *"Under two-fifty, it just goes. No approval."* — Payroll Admin (acme-corp) | 2 | 2 | High — VP2 scope (approval chain) + KR 1.4 | Strong — 2 accounts | **Act now** |
| 3 | Attach receipts in the form they actually arrive, retaining them for audit | *"I need to see that it guessed and I need to be able to see the picture. Seven years. CRA."* — Senior Bookkeeper (birchbark-books); *"Maybe three were photos. Everything else was a PDF or somebody forwarding me the confirmation email."* — Payroll Admin (acme-corp) | 2 | 2 | High — VP2 scope (receipt capture, now backed) | Strong — 2 accounts | **Act now** |
| 4 | Give managers visibility into team spending without per-claim email noise | *"A 'for your information' email is a deleted email. I'd want it as a list."* — HR Manager (acme-corp) | 1 | 1 | High — approval-chain design (VP2 scope); condition on Theme 2 | Weak — 1 account | **Collect signal** |
| 5 | Stop the administrator manually chasing claimants to submit before the deadline | *"If the system nudged them at day fifteen — not me, the system — ninety percent of it goes away."* — Payroll Admin (acme-corp) | 1 | 1 | High — VP2 claim submission scope | Weak — 1 account | **Collect signal** |
| 6 | See all client accounts' expense health without logging in to each separately | *"One screen. Forty rows. Here's who hasn't submitted since June. Sorted worst first. That's the thing I want more than anything else."* — Senior Bookkeeper (birchbark-books) | 1 | 1 | High — named explicitly in VP2 initiative scope | Weak — 1 account | **Collect signal** |
| 7 | Let employees track and reconcile their own reimbursement without asking payroll | *"The pay statement just says a number. … Two or three times a pay."* — Payroll Admin (acme-corp); *"Employees seeing their own history."* — HR Manager (acme-corp) | 2 | 1 | High — payroll/A/P boundary in VP2 scope | Weak — 1 account | **Parked** — above cut |
| 8 | Tell the firm about upcoming product changes early enough to brief its clients | *"Tell us first. Two weeks out, I can warn the ten clients it affects."* — Firm Principal (birchbark-books) | 1 | 1 | Low — cross-module; outside VP2 scope | Weak — 1 account | **Park** |

---

## Act Now

**1. Match claim submission and approval to the device each role actually uses**
- **The ask, verbatim:**
  - *"Massive. For the clients."* / *"Irrelevant. For us."* — Firm Principal + Senior Bookkeeper, Birchbark Books ([2026-08-18 summary](../customers/accounts/birchbark-books/calls/summaries/2026-08-18.md))
  - *"My clients are in vans. If the approval isn't on his phone it doesn't happen."* — Firm Principal
  - *"Blocked. Because 'discouraged' means a grey box that says 'are you sure' and everyone taps yes on those too."* — HR Manager, Acme Corp ([2026-08-20 summary](../customers/accounts/acme-corp/calls/summaries/2026-08-20.md))
  - *"I watched this happen with time off. We put time-off approvals on the phone and the approval rate went to basically a hundred percent overnight."* — HR Manager, Acme Corp
- **The job behind it:** The approver in a small trades business has no desk — a desktop approval is a non-approval, and mobile approval (any claim, any amount) invites the muscle-memory tap that Acme documented in their time-off rollout. The firm-side reviewer needs two monitors and would never use a phone surface. Both accounts point at the same design: mobile for submission and for claims below the approval threshold; desktop-only above the threshold.
- **Why now:** VP1 shipped mobile-first submission and a first approval step. VP2 must define the device boundaries before the approval-threshold work lands — they are the same design decision. Directly in VP2 scope. KR 1.4 (multi-module adoption).
- **Effort:** M — builds on VP1's mobile infrastructure; new work is device-based approval blocking above the threshold, and firm/client surface split
- **Design together with:** Theme 2 (approval rules) — the threshold value and the device restriction are one configuration
- **Next:** `/impact-sizing` to size combined mobile demand. Destination: `roadmaps/` → NOW or NEXT (paste manually)

---

**2. Define expense approval routing without becoming a rulesets maintenance burden**
- **The ask, verbatim:**
  - *"A firm template. So I set it once — under a hundred goes, over a hundred goes to the owner, over a thousand flags to me — and I push that to every client I want it on. … If a client changes it, I want to know. Not a report I have to go find. Tell me."* — Senior Bookkeeper, Birchbark Books
  - *"I need defaults. Defaults are influence. Nobody changes a default. That's the only power I've ever had in this job."* — Senior Bookkeeper
  - *"Under two hundred and fifty dollars — and under that, it just goes. No approval. … right now a manager is clicking yes on a nineteen dollar parking receipt, and they're not reading it."* — Payroll Admin, Acme Corp
- **The job behind it:** Two distinct segments, same underlying pain — approval routing that is technically in place but functionally meaningless because the cost of maintaining it outstrips the control value. Birchbark needs firm-level templates pushed across clients with change notifications; Acme needs a floor below which claims auto-approve and managers are informed (not asked). **One solution does not satisfy both** — the firm-template shape and the auto-floor shape are compatible but distinct, and implementing only one leaves the other segment unsatisfied. **Critical from the records:** the per-client-configurable design was specifically rejected by Birchbark as a net negative — *"you'd be giving me forty rulesets to maintain."*
- **Why now:** Directly in VP2 scope. First first-hand customer signal for both the firm-template and the auto-floor hypotheses. The prior decision [2026-08-06-expense-approval-threshold.md](../decisions/2026-08-06-expense-approval-threshold.md) covers the upper tier ($5k executive approval) — this fills in the lower-tier design, which it does not settle. KR 1.4.
- **Effort:** L — two shapes (firm template for channel, auto-floor for direct clients), both require a shared underlying approval-chain model; firm template requires multi-client infrastructure
- **Design together with:** Theme 1 (device) and Theme 4 (manager visibility) — these three form one integrated approval experience
- **Next:** `/impact-sizing`. Destination: `roadmaps/` → NOW or NEXT (paste manually)

---

**3. Attach receipts in the form they actually arrive, retaining them for audit**
- **The ask, verbatim:**
  - *"It has to reach me in a form I can question. If the app reads the receipt and guesses the category, fine, great, but I need to see that it guessed and I need to be able to see the picture."* — Senior Bookkeeper, Birchbark Books
  - *"Seven years. CRA. And I would want to be able to get all seven years out if a client leaves us."* — Senior Bookkeeper
  - *"Hardly ever paper. … maybe three were photos of a paper receipt. Everything else was a PDF or somebody forwarding me the confirmation email."* — Payroll Admin, Acme Corp
  - *"Submitting. Not the whole thing. … snapping the taxi receipt and being done with it, yes."* — Payroll Admin, Acme Corp
- **The job behind it:** Both accounts need receipts to arrive in whatever form the spend produced (photo, PDF, forwarded confirmation email), attached permanently to the entry, and auditable. The shapes differ materially: Birchbark needs visible derivation (machine-guessed vs human-entered), seven-year statutory retention, and full export on client departure; Acme's primary path is PDF/email attachment at a desk, with photo capture as the travelling case. **Design correction:** do not default the receipt-capture experience to photographing paper — Acme's portfolio is overwhelmingly digital, and building paper-photo-first misses the primary path. Validate the default path against this segment before committing.
- **Note on boundaries:** The Senior Bookkeeper explicitly excluded automated business-vs-personal classification from scope: *"that's a judgment call and it's mine and it always will be. I'm not asking you to solve it."* Do not scope it from this record.
- **Why now:** Receipt capture was an unbacked VP2 hypothesis ("no design-partner record states them" — initiative page). This run provides first first-hand confirmation from both the channel (Birchbark) and the direct-client (Acme) sides. KR 1.4.
- **Effort:** L — two primary attachment paths (photo capture; PDF/email); OCR/auto-coding with visible derivation indicators; seven-year retention architecture; export on client departure
- **Next:** `/impact-sizing`. Destination: `roadmaps/` → NOW or NEXT (paste manually)

---

## Collect Signal

**4. Give managers visibility into team spending without per-claim email noise**
- **What we don't know:** Whether the preference for an in-product spend list (rather than email) is specific to this HR Manager, or whether managers at comparable accounts (SMB, 50–150 employees) would visit it. Their own Payroll Administrator predicted no one would use a self-service expense history — the same adoption risk applies here.
- **Alternative solutions worth considering:** (a) A weekly push notification (app or SMS) with a team-spend summary — lower friction than an in-product destination managers must navigate to; (b) a digest tab embedded within the approval screen the manager already visits, showing auto-approved claims they did not act on; (c) surfacing the spend digest on the manager's most-visited existing screen (e.g., payroll summary) rather than creating a new destination
- **Highest-risk assumption:** That managers at this segment will proactively visit an in-product list, given the Payroll Administrator's counter-evidence that employees ignore self-service even when they know it exists
- **Cheapest test:** On the next Acme follow-up, screenshot where the HR Manager goes first each week in the product. Design the digest into that path in a prototype and show it — does she say "I'd look there" or "I'd still miss it"?
- **Note — this is a condition, not a standalone:** The HR Manager accepted the auto-approval floor (Theme 2) on the understanding that managers would still be informed. Shipping Theme 2 without Theme 4 may violate the account's understanding of what they agreed to.
- **Next:** `/assumption-map` to surface the adoption assumption. Destination: `roadmaps/` → LATER → Under Consideration (paste manually)

---

**5. Stop the administrator manually chasing claimants to submit before the deadline**
- **What we don't know:** Whether the "I'm the nag" pattern is common across the 14-employee-median account base, or specific to a 75-person company where the administrator knows every claimant by name. Smaller accounts may have the same policy-but-no-enforcement dynamic but not describe it as a chasing problem.
- **Alternative solutions worth considering:** (a) An automated system-attributed nudge at a configurable day within the submission window; (b) a per-claimant submission-age indicator visible only to the administrator (shows the problem without solving it, but supports follow-up); (c) a submission deadline that auto-closes the claim and routes it to a late-claim exception queue (harder — but their current pattern is effectively no-deadline)
- **Highest-risk assumption:** That automated nudges reduce chasing at smaller accounts. At accounts under ~30 employees, informal relationships may replace rules in the other direction — the owner may prefer to handle it verbally.
- **Cheapest test:** Ask on one additional discovery call whether the administrator personally feels like the chaser. If two or more accounts independently name the "it comes from me, so I'm the nag" framing, the social frame is load-bearing and the demand is real.
- **Next:** One additional discovery call; `/interview-guide` scoped to claim-submission friction. Destination: `roadmaps/` → LATER → Under Consideration (paste manually)

---

**6. See all client accounts' expense health without logging in to each separately**
- **What we don't know:** Whether this pattern — one firm managing 30–40 client accounts and needing a cross-client operational worklist — is representative of the bookkeeper channel segment, or specific to Birchbark's scale. The need is minimal for a 5-client firm and acute for a 40-client firm.
- **Alternative solutions worth considering:** (a) An email digest the firm can forward (Birchbark explicitly stated this format); (b) a Payroll-Hub-style multi-client view (the existing pattern) extended to include expense state — lower build cost if the hub infrastructure already handles multi-tenancy; (c) a firm-level API or data export letting the firm build its own worklist
- **Highest-risk assumption:** That firm-level SSO and firm-level roles ship before (or alongside) this feature. A cross-client expense view that still requires 40 sign-ins delivers the information but not the outcome — the job is intervention, not information. This is a dependency risk, not a demand risk.
- **Cheapest test:** Check whether existing Payroll Hub multi-client firm users also run expenses for those clients. That population is the ready demand pool — if confirmed, the cross-client expense state is additive to something they already use.
- **Strategic note:** This theme is the only one directly named in the VP2 initiative page scope ("the channel view for a firm administering expenses across client databases"). The evidence base is one account, but the strategic alignment is the strongest of the three Collect Signal themes. Promote to Act Now when a second firm confirms the pattern.
- **Next:** `/assumption-map` on the firm-identity dependency. Fix the two filing-gap records (see header) before the next triage. Destination: `roadmaps/` → LATER → Under Consideration (paste manually)

---

## Declined

_None this run._

---

## Parked

- **Let employees track and reconcile their own reimbursement without asking payroll** — first seen 2026-08-31 — above the cut this cycle (Collect Signal cap reached). Covers two asks from one account (acme-corp): (1) itemise expense claims on the pay statement so employees can self-reconcile; (2) employee-visible claim history in ESS. Both are High fit — the pay statement piece maps to the A/P boundary in VP2 scope, the ESS piece is a natural extension. Both are Weak evidence (1 account). There is active disagreement within the account about whether anyone would use the ESS history. Revisit when a second account names either pattern, or when the pay-statement piece can be decoupled and built as a small payroll-module improvement — it is likely the cheaper of the two to ship.

- **Tell the firm about upcoming product changes early enough to brief its clients** — first seen 2026-08-31 — outside VP2 scope. The underlying need is real — the bookkeeper firm is the unpaid first-line support for every module rollout, and advance notice with forwardable content converts support incidents into planned ones. But the scope note on the record is explicit: this applies to every module equally. It is a release-operations and channel-communications concern, not an expense feature. Low fit for VP2. Revisit when the bookkeeper-channel team owns a communications plan for rollouts, or when a cross-module communications initiative is scoped.

---

## Conflicts

- **Themes 1 and 2 must be designed as one experience.** The mobile-approval block (Theme 1) is literally "block above the threshold" — the threshold value (Theme 2) is a shared input. Implementing one without the other leaves a gap: either the device block has no threshold to reference, or the threshold has no device enforcement. Design together.
- **Themes 2 and 4 are a package at Acme Corp.** The HR Manager accepted the auto-approval floor on the condition that managers are still informed of auto-approved spend. Shipping Theme 2 without Theme 4's visibility mechanism may violate the account's understanding of what they agreed to. Mark Theme 4's status visibly when committing Theme 2.
- **Theme 6 depends on firm-level identity infrastructure that is currently out of scope.** The two excluded records (`firm-single-sign-on`, `firm-role-based-access`) are the access substrate the cross-client dashboard requires. A view that still requires 40 sign-ins delivers information but not the operational outcome. Resolve the firm-identity dependency before committing Theme 6.

---

## Defects, Not Demand

_None in this pile._

---

## Already Ships

_Unable to check — `feature-index.yaml` carries no expense-management feature entries yet (open loop on the initiative page: "The Expense Management module carries no feature entries in the catalog"). Re-check on next triage once the VP2 brief proposes the `planned` catalog entries._

---

## Revision History

- 2026-08-31 — First triage — scope: expense-management-vp2. 14 records admitted (by own `initiatives:` link) across 2 accounts (birchbark-books, acme-corp). 2 records excluded — filing gap (see header). 0 defect reports. New: all 8 themes. Act Now: 3 (device-based submission/approval, approval routing, receipt capture). Collect Signal: 3 (manager spend visibility, submission reminders, cross-client dashboard). Parked: 2 (claimant self-service — above cut; advance change notice — outside scope). Declined: 0.
