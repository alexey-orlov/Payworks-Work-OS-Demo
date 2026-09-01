---
date: 2026-07-08
updated: 2026-08-31
owner: "Margaret Foster"
customers: [maplewood-recreation]
areas: [performance-management, payroll, employee-self-service, workforce-analytics, onboarding]
features: []
initiatives: [performance-management-discovery, employee-onboarding]
---

# Customer Interview Insights — 2026-07-08

Session report for one discovery interview + prototype review with Maplewood Recreation.
Source: [transcripts/2026-07-08-maplewood-recreation-interview.md](transcripts/2026-07-08-maplewood-recreation-interview.md) ·
Account: [maplewood-recreation](../customers/accounts/maplewood-recreation/account-context.md)

> **Prototype data warning.** This session walked a Payworks prototype. Every employee
> name, competency, goal and figure visible on those screens — the employee "Jordan", the
> manager "Sarah", the sample goals — is **our mock data**, not a Maplewood fact. Reactions
> to mock values are recorded below; the values themselves are not customer truth.

## Existing Research Context

- **Prior syntheses found: none.** No filed research existed in this repo when this record
  was processed — `product/user-insights/` held no synthesis and no session report, and
  `performance-management-discovery` lists its cross-interview synthesis as an open loop.
- **Validated themes carried in: none.** Every theme below is therefore labelled **NEW**
  unless it is corroborated a second time *inside this same interview* (both participants
  independently, or the same participant against a concrete artifact).
- **Related work:** [performance-management-discovery](../initiatives/performance-management-discovery.md)
  (thirteen design-partner records, four accounts, none previously filed) and
  [employee-onboarding](../initiatives/employee-onboarding.md) (whose origin is the closing
  exchange of this very call). No Product Brief exists for either yet.
- Cross-account patterns are explicitly **out of scope here** — that is
  `/user-research-synthesis`'s job once 4+ interviews are filed.

## Executive Summary

- **They tried the existing Payworks review capability and walked away from it, and the
  reason is a compensation-model mismatch, not a UX one.** Submitting a review in the
  current module grants the raise: *"once it's submitted, it just says, yes, they get their
  raise."* Their increase is set by executive off a board-approved budget, so a review that
  decides pay is structurally wrong for them. This is a displacement story about our own
  product, not a greenfield one.
- **Confidentiality is the gate on any replacement — and simultaneously the reason Payworks
  is attractive.** A prior digital rollout on their company intranet left review forms
  readable by system administrators; they rolled back to PDF **two weeks before this call**.
  The same concern is what makes a Payworks-native home appealing: *"we know that it is,
  built for… with the confidentiality piece around it"*.
- **HR does not track review completion, by design.** Their operating model hands
  accountability to directors and executives; HR builds and trains, then steps back. Any
  admin surface built for "HR chases stragglers" is aimed at a persona that does not exist
  here — but an **executive** view rolled up by hierarchy branch would land.
- **Adoption is the headline risk, stated in the first ninety seconds of the prototype**
  (*"I'm just a smidgen overwhelmed"*) and confirmed as a design philosophy: they build
  every process around their two least technical leaders. A staged rollout is a
  precondition, not a preference.
- **The onboarding thread in this call is ~45 seconds long and contains no requirement.**
  It is recorded at that weight in its own section below. Do not read it as demand.

## Interviews Conducted

- **Number:** 1 (one session, two customer-side participants: their HR Business Partner,
  who drove the prototype, and their Payroll Manager)
- **Date range:** 2026-07-08 – 2026-07-08 · **Length:** ~63 minutes recorded
- **Format:** discovery interview (~4 min current state) + facilitated prototype walkthrough
  across the employee, manager and HR surfaces, closing with a 45-second onboarding exchange
- **Segment:** recreation employer running **two workforces on one payroll** — permanent
  (annual review mandatory) and seasonal (strongly recommended, not mandatory); Payworks
  carries payroll and employee self-service today; performance runs entirely outside
  Payworks on PDF forms and a company intranet. Headcount, site count, province and union
  status are **not stated on the record**.

## Top Pain Points (ranked)

Counts read `1 of 1` throughout — this is a single-session report and the numbers carry no
cross-account weight yet. Ranking is by severity and by how hard the pain constrains a
future design.

1. **No confidential home for a completed review form** — 1 of 1 — *"personal and
   confidential forms were living in the back end, where system administrators that aren't
   privy to that confidential information could actually access, for example, my performance
   review, and that's where I was like, I don't like this."* — Their HR Business Partner —
   impact: forced a full rollback from digital to PDF two weeks before this call — workaround:
   PDF fillable forms stored on leaders' own computers, then uploaded to payroll.
2. **The current Payworks review module auto-grants the raise on submit** — 1 of 1 —
   *"we actually tested out how the module's set up right now in PayWorks with our annual
   reviews a few years ago, but once it's submitted, it just says, yes, they get their
   raise."* — Their Payroll Manager — impact: incompatible with a board-approved budget and
   an executive-set increase list; they abandoned the module — workaround: reviews run
   entirely outside Payworks.
3. **Digital forms came back blank and nothing could be made mandatory** — 1 of 1 —
   *"There's leaders that would submit the digital form, and it would be blank."* — Their HR
   Business Partner — impact: rework loops between payroll, HR and the leader; a direct cause
   of the PDF rollback — workaround: PDF form plus the Payroll Manager visually scanning every
   submission (*"As long as there's words and nothing, like, extreme this way or that way, or
   blanks, that's when I would just flag it to HR."*).
4. **The signature round-trip has no digital path** — 1 of 1 — *"you have to email the sign
   to get a digital signature, or you have to print it. physically give it to them, sign it,
   scan it, because we, also do not allow paper copies to go back to payroll. We need them all
   digital"* — Their HR Business Partner — impact: the clunkiest step in the whole cycle —
   workaround: email or print-sign-scan, per leader.
5. **A manager cannot see the employee's self-ratings while writing their own** — 1 of 1 —
   *"because the employee rated themselves as well, and I can't see how… What they rated
   themselves."* — Their HR Business Partner (reacting to the prototype) — impact: removes the
   perception gap that the review conversation is supposed to be about — workaround: none in
   the prototype; on the PDF form both sets of marks sit on one page.
6. **Goals are set and never closed** — 1 of 1 — *"there's no… there's no loop, closing the
   loop with goals, with our goals right now."* — Their HR Business Partner — impact: SMART
   goals are agreed in the review and never measured against — workaround: whatever the
   individual leader remembers a year later.
7. **Retrieving a filed review from the ESS document library** — 1 of 1 — *"we have to go
   into the documents library, and we have to kind of click and click and click and click
   until we actually find it."* — Their HR Business Partner — impact: prior-year reviews and
   development plans are effectively invisible to a new leader — workaround: ask the Payroll
   Manager, who labels the uploads carefully.
8. **Managers cannot tell which of their own people are seasonal** — 1 of 1 — *"some managers
   don't even know if their employee that they're talking about is a seasonal employee versus
   a permanent employee."* — Their Payroll Manager — impact: the permanent/seasonal split
   decides which form and which obligation applies — workaround: *"I have to give some of them
   a list of their permanent employees, because they just…"*
9. **Prototype density on first sight** — 1 of 1 — *"I'm just a smidgen overwhelmed"* /
   *"Yeah, it's, it's busy,"* / *"I don't really know where to start."* — Their HR Business
   Partner — impact: the adoption risk for a manager population that includes leaders who
   *"won't touch computers with a 10 feet foot pole"* — workaround: n/a, this is our design to
   fix (see the manager-roster finding in the card).

## Top Feature Requests

Each links its dated record in [feature-requests/](feature-requests/).

1. **Customizable word-based rating scales** — priority: must-have — requested by their HR
   Business Partner — underlying need: rating consistency across a leader population they do
   not trust to interpret numbers the same way → [record](feature-requests/2026-07-08-maplewood-recreation-customizable-rating-scales.md)
2. **A comment box against every competency and goal** — priority: must-have — requested by
   their HR Business Partner — underlying need: make the perception gap explainable, not just
   visible; their own leaders already demanded this of the PDF form → [record](feature-requests/2026-07-08-maplewood-recreation-per-competency-comment-boxes.md)
3. **Per-field mandatory control** — priority: must-have — requested by their HR Business
   Partner — underlying need: stop blank submissions at the source, which is what killed their
   last digital rollout → [record](feature-requests/2026-07-08-maplewood-recreation-configurable-mandatory-fields.md)
4. **Manager sees the employee's self-ratings side by side** — priority: must-have —
   requested by their HR Business Partner — underlying need: the review conversation is about
   comparing two perceptions → [record](feature-requests/2026-07-08-maplewood-recreation-side-by-side-self-ratings.md)
5. **Two review form types — permanent (with goals) and seasonal (without)** — priority:
   must-have — requested by their HR Business Partner — underlying need: a seasonal term is
   too short to set sustainable goals against → [record](feature-requests/2026-07-08-maplewood-recreation-multiple-review-form-types.md)
6. **Goal-achievement tracking** — priority: must-have — requested by their HR Business
   Partner — underlying need: close the loop they have never been able to close → [record](feature-requests/2026-07-08-maplewood-recreation-goal-achievement-tracking.md)
7. **Prior reviews, development plans and letters of expectation visible from the review** —
   priority: must-have — requested by their HR Business Partner and their Payroll Manager
   (both, independently) — underlying need: high leader turnover means the person writing the
   review often does not know the employee's history → [record](feature-requests/2026-07-08-maplewood-recreation-review-history-in-employee-record.md)
8. **Outlook calendar integration for recurring one-on-ones** — priority: must-have (stated
   as a requirement when asked directly) — requested by their HR Business Partner —
   underlying need: a check-in tool that does not live in Outlook will not be used by a
   Microsoft-native organisation → [record](feature-requests/2026-07-08-maplewood-recreation-outlook-calendar-integration.md)
9. **Executive access to the review-status view, rolled up by hierarchy branch** — priority:
   nice-to-have for HR, potentially must-have for the executive buyer — requested by their HR
   Business Partner — underlying need: accountability sits with executives, not HR → [record](feature-requests/2026-07-08-maplewood-recreation-executive-hierarchy-dashboard.md)
10. **Process-status analytics with CSV export** — priority: must-have for payroll —
    requested by their Payroll Manager — underlying need: a checklist-driven payroll team
    needs to know what is submitted, paid and owed — explicitly *not* people analytics →
    [record](feature-requests/2026-07-08-maplewood-recreation-analytics-and-reporting.md)
11. **Organisational → director → employee goal cascade** — priority: nice-to-have today,
    named as executive appetite — requested by their HR Business Partner — underlying need:
    they already believe goals should cascade and are inconsistent at doing it →
    [record](feature-requests/2026-07-08-maplewood-recreation-goal-cascade.md)
12. **Employee type (seasonal vs permanent) visible to the manager** — priority:
    nice-to-have — surfaced by their Payroll Manager — underlying need: the manager must pick
    the right form and know which obligation applies → [record](feature-requests/2026-07-08-maplewood-recreation-employee-type-visible-to-managers.md)

**Explicitly not wanted:** an overall rating — *"Overall rating… we probably wouldn't use an
overall rating. I think overall ratings can become a bit subjective."* And numeric competency
scales — *"We don't use number ratings, we use words"* / *"Numbers we find a bit inconsistent."*

## The onboarding thread — recorded at its true weight

This is the exchange that [employee-onboarding](../initiatives/employee-onboarding.md) exists
because of. It is a **~45-second closing exchange** (01:02:35 → 01:03:18 on the recording —
43 seconds), raised by Margaret Foster after the session had already run five minutes over on
performance management, and **there is no requirement in it.**

What it establishes, in full:

- Payworks is looking at onboarding and offboarding with a stated goal — *"this is what we're looking at in
  terms of onboarding, offboarding, kind of looking at, you know, how can we simplify the
  experience?"* — Margaret Foster
- Their Payroll Manager had **already emailed an onboarding process map** before the call, and
  Payworks has read and queued it — *"So I've taken a look at your email that you sent me. Thank
  you so much, with your massive Excel spreadsheet. So, looking at that, already shared it
  with a colleague of mine, so that's next on our bucket. I just wanted to say I'm not
  ignoring you. We have taken a look at it, but that's kind of the process we're going
  through, just so you know, so we will ping you as well when we get to that."* — Margaret Foster
- The **offboarding equivalent is promised but unfinished**, blocked behind seasonal volume —
  *"Yeah, and I'll put together the same thing for the offboarding, we're just still working
  through it. We just did 300 plus on the SPR side, so we're just trying to do ROEs and get
  everything all dialed up for that."* — Their Payroll Manager

What it does **not** establish: no pain point, no current-state process detail beyond the
existence of a spreadsheet, no system inventory, no requirement, no priority signal. **No
feature-request record has been created from this exchange**, and none should be. The
onboarding process map itself is not in this repo — it is an email attachment.

## Theme Labels vs Prior Research

No prior filed research existed, so nothing can be VALIDATED or CHALLENGED against an earlier
report. Themes corroborated twice *within this session* are marked as such.

- **NEW — Compensation decoupled from the review.** The annual increase is a list; the review
  feeds only the bonus, and only as a precondition. First surfaced here. Probe in every
  future interview: the three accounts on this initiative may each have a different model.
- **NEW — Raise-on-submit as a churn cause for the current module.** They tested it and left.
  Probe whether other accounts hit the same wall.
- **NEW — Confidentiality as the buying gate.** Corroborated twice inside this interview: it
  caused the PDF rollback, and it is the stated reason a Payworks-native home appeals.
- **NEW — HR deliberately outside the tracking loop.** Corroborated by both participants (the
  HR Business Partner's model description and the Payroll Manager's *"would you and the HR
  Coordinator ever be involved in the process of approving reviews?"* → *"No."*).
- **NEW — Design for the least technical leader.** Stated as an explicit method, not a
  complaint.
- **NEW — Word-based, customizable rating scales; no overall rating.** Backed by an artifact
  (their own PDF form defines the word ratings), so this is stronger than a preference.
- **NEW — Two-population form design (permanent / seasonal).** Probe: does any other design
  partner run a two-population review?
- **NEW — Payroll status reporting as the "analytics" ask.** Their analytics request is
  process status and CSV, explicitly not people analytics. Probe carefully elsewhere — the
  word "analytics" is being used for two different things across this corpus.
- **NEW — Onboarding/offboarding interest.** One artifact, one 45-second exchange, zero
  requirements. Not a theme yet; a placeholder for one.

## Recommended Actions

1. **Design the compensation handoff as "review completes → bonus nomination → executive
   approves", with the annual increase entirely outside the review.** Raise-on-submit must not
   survive into the Performance Management module — it is the documented reason this account
   abandoned the current capability. Owner: Claire Sutton — Due: 2026-09-15
2. **Cut the manager roster to 3–4 columns and re-test it with this account.** They named the
   number themselves and named which columns matter (*"where they are, what's due, when it's
   due"*), and flagged `Check-in`, `Feedback`, `My Step` and `Risk` as unclear or redundant.
   Owner: Vanessa Lee — Due: 2026-09-19
3. **Confirm their Employee Experience Director for the next session.** She was volunteered
   on the call as the technology-adoption lens this account is missing. Owner: Margaret Foster
   — Due: 2026-09-12
4. **Chase the offboarding process map, and fold the onboarding map already received into the
   repo.** Both are open loops on `employee-onboarding`; the offboarding one was blocked
   behind a 300+ seasonal ROE batch as of 2026-07-08 and that batch is long finished. Owner:
   Claire Sutton — Due: 2026-09-15
5. **Carry the confidentiality requirement into the Product Brief as a hard constraint, not a
   feature.** A system-administrator role that can read a review form is a disqualifier for
   this account. Owner: Claire Sutton — Due: 2026-09-15
6. **Run `/user-research-synthesis` once 4+ interviews are filed** — the contradictions across
   compensation models are the thing the Product Brief needs named, not averaged. Owner:
   Margaret Foster — Due: 2026-09-26

## Interviews

### Interview — HR Business Partner + Payroll Manager, seasonal/permanent recreation employer (2026-07-08)

**Research goal:** whether a Payworks-native review process could displace what this account
runs today, and what the employee / manager / HR surfaces of a prototype would have to do to
be adopted by a manager population with a very wide technology-comfort spread.

**Hypotheses tested:**
- H1 — the employee → manager → HR flow matches how they actually work
- H2 — a numeric competency scale is acceptable
- H3 — an overall rating usefully summarises a review
- H4 — HR wants to track review completion
- H5 — a company-goal cascade is out of scope for an employer this size
- H6 — the prototype's information density is workable for their managers
- H7 — the review should drive the compensation decision

**Jobs-to-be-Done:**
When our fiscal-year review window opens in May and I have to push a mandatory review through
a leader population that ranges from fluent to computer-averse, I want a process so simple
that my two most-struggling leaders can complete it without help — and a place to keep the
finished form where only the people entitled to read it can, so I can satisfy the payroll
dependency and the bonus deadline without the review itself becoming the thing that fails.

**Pain points:** (severity + current workaround for each)
- **No confidential storage for completed reviews** — severity: high — workaround: rolled back
  to PDF fillable forms two weeks before this call<br>
  *"personal and confidential forms were living in the back end, where system administrators that aren't privy to that confidential information could actually access, for example, my performance review, and that's where I was like, I don't like this." — Their HR Business Partner*
- **The current Payworks review module grants the raise on submit** — severity: high —
  workaround: abandoned it; performance runs outside Payworks entirely<br>
  *"we actually tested out how the module's set up right now in PayWorks with our annual reviews a few years ago, but once it's submitted, it just says, yes, they get their raise." — Their Payroll Manager*
- **Blank digital submissions, no mandatory fields** — severity: high — workaround: PDF plus
  manual scanning of every submission by payroll<br>
  *"There's leaders that would submit the digital form, and it would be blank." — Their HR Business Partner*
- **Signature collection has no digital path** — severity: high — workaround: email for
  e-signature, or print / sign / scan<br>
  *"you have to email the sign to get a digital signature, or you have to print it. physically give it to them, sign it, scan it, because we, also do not allow paper copies to go back to payroll. We need them all digital" — Their HR Business Partner*
- **Manager cannot see the employee's self-ratings** — severity: medium — workaround: none in
  the prototype; on their PDF both sets sit on one sheet<br>
  *"because the employee rated themselves as well, and I can't see how… What they rated themselves." — Their HR Business Partner*
- **Goals are set, never measured** — severity: medium — workaround: none<br>
  *"there's no… there's no loop, closing the loop with goals, with our goals right now." — Their HR Business Partner*
- **Filed reviews are buried in the ESS document library** — severity: medium — workaround:
  careful labelling by the Payroll Manager<br>
  *"we have to go into the documents library, and we have to kind of click and click and click and click until we actually find it." — Their HR Business Partner*
- **Managers do not know who on their team is seasonal** — severity: medium — workaround: the
  Payroll Manager hands them a list<br>
  *"I have to give some of them a list of their permanent employees, because they just… And sometimes it's just because there's new, because of turnover." — Their Payroll Manager*
- **First-sight density of the prototype** — severity: medium, rising to high on adoption —
  workaround: n/a — ours to fix<br>
  *"Yeah, it's, it's busy, So that's… that's my initial thought. I'm just a bit overwhelmed. I don't really know where to start." — Their HR Business Partner*

**Feature requests:** (underlying need, not just the ask)
- **Customizable word-based rating scales** — underlying need: consistency across leaders they
  do not trust to read a number the same way; their existing PDF already defines the words —
  priority signal: must-have.
  *"We don't use number ratings, we use words, and you can see my form that we do define out, those, those ratings. I don't know if you have the ability to customize the ratings as well, based on what we want." — Their HR Business Partner*
- **A comment box per competency and per goal** — underlying need: a rating gap is only useful
  if the rater has to explain it; their own leaders already demanded this change of the PDF —
  priority signal: must-have, and the comments should be mandatory.
  *"we did get that feedback from our leaders, to change our form, to have, instead of one summary comment box, they wanted a box each… next to each competency rating, so they could make a comment specifically about that, that area." — Their HR Business Partner*
- **Per-field mandatory control** — underlying need: prevent the blank submission that killed
  the last digital rollout, while keeping flexibility over which fields are compulsory —
  priority signal: must-have.
  *"you could pick and choose which ones were mandatory, that one would be best." — Their HR Business Partner*
- **Manager sees the employee's self-ratings beside their own** — underlying need: the review
  meeting is a perception comparison — priority signal: must-have.
  *"It's all about perception and sharing each other's perception to learn more." — Their HR Business Partner*
- **Two review form types** — underlying need: a seasonal term is too short to set sustainable
  goals, so the seasonal form is the permanent one minus the goals section — priority signal:
  must-have.
  *"is there capabilities to have two different types of forms?" — Their HR Business Partner*
- **Goal-achievement tracking** — underlying need: close the loop they have never closed;
  also the input the executive already uses to calculate director bonuses — priority signal:
  must-have.
  *"This might be… really helpful for us to measure goal achievement. Right now, we don't… we don't measure goal achievement." — Their HR Business Partner*
- **Prior reviews, development plans and letters of expectation surfaced on the review** —
  underlying need: high leader turnover means the reviewer often does not know the employee's
  performance-management history — priority signal: must-have; asked by both participants.
  *"we have lots of leader turnover, and sometimes they don't do their own research. into an employee file before they do a performance review, so they might not even know that the person has a development plan, or they have a letter of expectation on file." — Their HR Business Partner*
  *"I had a lot of managers recently ask for copies of the previous year's performance review so that they can start preparing for the next one." — Their Payroll Manager*
- **Recurring one-on-ones written into the Outlook calendar** — underlying need: an
  Outlook/Teams-native organisation will not adopt a scheduling surface that sits outside
  Outlook — priority signal: must-have (confirmed as a requirement when asked directly).
  *"Can you set up a recurring? Because all my one-on-ones are recurring. I just set up an outlet recurring for the whole entire year." — Their HR Business Partner*
- **Executive access to the review-status view, branch by branch** — underlying need:
  accountability for completion sits with directors and executives; HR will not police it —
  priority signal: nice-to-have for HR, likely higher for the executive buyer.
  *"It'd be really nice for executive to be able to check in as well, especially with their kind of leaders that branch off in the hierarchy, not necessarily every single employee, because that'd be overwhelming, but if we could branch them off." — Their HR Business Partner*
- **Process-status analytics with CSV export** — underlying need: a checklist-driven payroll
  function needs submitted / paid / owed state, not competency distributions — priority
  signal: must-have for payroll.
  *"we need to know, like, who's been submitted, when we've done their increase, have they been paid, do they… are they owed retro pay, or anything like that?" — Their Payroll Manager*
  *"oh, there's export to CSV, then that's perfect, because then we can see exactly where people are." — Their Payroll Manager*
- **Goal cascade from organisational to director to employee** — underlying need: they already
  believe goals should cascade and are inconsistent at making it happen — priority signal:
  nice-to-have today, named as executive appetite.
  *"I think our executive would quite like that kind of cascade down ability, for the… to see that in the goals section." — Their HR Business Partner*
- **Employee type visible to the manager** — underlying need: the manager has to pick the
  right form and know whether the review is mandatory — priority signal: nice-to-have.
  *"my thought is, some managers don't even know if their employee that they're talking about is a seasonal employee versus a permanent employee." — Their Payroll Manager*

**Prototype reactions worth keeping** (mock screen data excluded, per the warning above):
- **Liked, unprompted:** the "Action required" block (*"they need the action actually called
  out, or else it never gets done"*), the per-task Start / Prepare / Review buttons, the days
  -remaining counter, "Prepare for your one-on-one", Save draft, the journey bar (*"Because I
  can still see that there's steps needed to be completed"*), and colour-coded status
  (*"Our, our demographic is all about the visuals"*).
- **Confusing or unwanted:** the `Check-in`, `Feedback` and `My Step` columns on the manager
  roster (*"I don't quite understand what the check-in column is"*), the `Risk` column
  (*"the risk column is kinda covered off in the goals column"*), the word "at risk" itself,
  and the overall-rating field.
- **The number they gave us:** cut the manager roster from seven columns to three or four —
  *"where they are, what's due, when it's due."* — Their Payroll Manager
- **On configuring a cycle**, their HR Business Partner declined to guess and said she would
  need hands-on time first — an honest signal that the admin surface was not evaluated in this
  session.

**Pain Points Validated:**
- ✅ H1 — the employee → manager → HR sequence matches their reality, including the payroll
  handoff at the end (*"there is a payroll dependency on these reviews"*).
- ❌ H2 — numeric competency scales are rejected outright: *"Numbers we find a bit
  inconsistent."*
- ❌ H3 — an overall rating is unwanted: *"I think overall ratings can become a bit
  subjective."*
- ❌ H4 — HR does **not** want to track completion: *"We don't track it as an HR business
  partner."* It is a nice-to-know, not a job. The tracking persona is the executive.
- ❌ H5 — the goal cascade was assumed out of scope and turned out to be the most
  forward-looking interest of the call.
- ❌ H6 — density is not workable as drawn; the first reaction to the employee home was
  overwhelm, and the manager roster was called out at seven columns.
- ❌/✅ H7 — split. The review does **not** drive the annual increase (*"the performance
  review doesn't come into play at all with the merit increase"* — confirmed by their Payroll
  Manager as *"No, not for… not for the annual increase."*). It **is** a precondition for the
  pay-for-performance bonus: *"they don't look at any bonuses until the review is done"* /
  *"there's a dependency, for sure."*
- ❓ Unclear — whether directors' goal achievement is tracked anywhere today. Both participants
  said they are outside that process: *"I get the list, and I process."*

**Theme labels:** {NEW: compensation decoupled from the review} {NEW: raise-on-submit as a
churn cause} {NEW: confidentiality as the buying gate} {NEW: HR deliberately outside the
tracking loop} {NEW: design for the least technical leader} {NEW: word-based customizable
scales, no overall rating} {NEW: two-population form design} {NEW: "analytics" meaning payroll
process status} {NEW: onboarding/offboarding interest — placeholder only}
No VALIDATED or CHALLENGED labels are available — nothing was filed before this record.

**Quotes to remember:**
- *"we actually tested out how the module's set up right now in PayWorks with our annual reviews a few years ago, but once it's submitted, it just says, yes, they get their raise." — Their Payroll Manager* → use in: Product Brief (compensation handoff), stakeholder update
- *"I get the list of every single permanent employee, and that's what they get. So the leader doesn't get to choose or recommend or say yes or no to an increase." — Their Payroll Manager* → use in: Product Brief (compensation models are not universal)
- *"personal and confidential forms were living in the back end, where system administrators that aren't privy to that confidential information could actually access" — Their HR Business Partner* → use in: Product Brief (confidentiality as a hard constraint)
- *"our structure, our HR model, is we're actually quite disconnected. Our role isn't to keep track of these types of initiatives or processes. We create them, and then we…" — Their HR Business Partner* → use in: Product Brief (persona map), presentation
- *"I always think of my one or two leaders that we struggle with the most, and, build the process based on their thought process." — Their HR Business Partner* → use in: design principles, presentation
- *"I'm just a smidgen overwhelmed" — Their HR Business Partner* → use in: prototype feedback, stakeholder update
- *"I like the idea of keeping it within, our pay work system, because we know that it is, built for… with the confidentiality piece around it, where it has the ability to link to that employee's profile." — Their HR Business Partner* → use in: stakeholder update (the expansion case)

**Surprises:**
- **HR opting out of tracking.** The assumption that HR is the admin persona chasing
  completion is wrong here — HR builds and trains, then hands accountability to directors and
  executives, and considers a completion dashboard a nice-to-know they would not log in for.
  That inverts who the admin surface is for.
- **We are the incumbent being displaced.** This is not a greenfield account for performance —
  they used the existing Payworks capability and left, for a specific and fixable reason.
- **The goal cascade landed backwards.** Margaret introduced it as probably not relevant to
  them; it drew the most forward-looking response in the call.
- **The confidentiality failure cuts both ways.** The same concern that pushed them back to
  paper is the strongest reason they want this inside Payworks.
- **Their reviews sit on the fiscal year, not the calendar** — a May execution window, which
  makes goal periods genuinely ambiguous for staff who think in calendar years: *"Some managers
  will go write the goals as of May 1st through to April 30th, where I'm thinking I need to
  write my goals from January 1st"*.

## Sensitive-content note

Nothing on the Privacy Contract's never-commit list appears in this record. Customer-side
participants are recorded by role only. The transcript preserves the raw record per the
transcript rules; this report does not.
