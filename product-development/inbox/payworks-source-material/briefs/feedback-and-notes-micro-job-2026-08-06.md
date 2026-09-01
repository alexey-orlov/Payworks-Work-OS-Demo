# Feedback & Performance Notes — Micro Job — 2026-08-06

**Status:** Draft

---

## How to read this document

**Terms used in this document, explained the first time they appear:**

- **Reports To** — the field on an employee record that links them to their manager's employee record.
- **Site Admin** — an admin who can see every employee and every part of the system.
- **Non-Site Admin (NSA)** — an admin whose access is limited to certain people or certain screens. This is
  the normal setup for a "manager" in Payworks today. There is no separate "manager" account type — a
  manager is just an NSA who has been given access to their reports.
- **1:1** — a recurring one-on-one conversation between two specific people, tracked as a series in the
  Check-ins area of Payworks. A 1:1 series can be labelled direct report, indirect report, or peer.
- **Given / When / Then** — a way of writing a rule as a test: **Given** a starting situation, **When**
  someone does something, **Then** state what must happen.

**Tags used throughout — where a rule comes from, or what to watch for:**

| Tag | Meaning |
|---|---|
| `[client]` | At least one real client said this, or was observed doing it. Carries a strength rating — **Strong** (3 or more companies, independently), **Suggestive** (2 companies), **Early** (1 company). More companies means more confidence this is a common need, not one company's habit. |
| `[market]` | At least one competitor product works this way already. Doesn't mean a client asked for it — means it's a known, tested pattern elsewhere. |
| `[direction]` | A deliberate PM or team decision, not based on client or market evidence. Stated as a fact so everyone builds against the same thing — not proof it's the right call. |
| `[assumption]` | Nobody outside the team has confirmed this. It's a working guess, more likely to change than a `[client]`- or `[market]`-backed rule. |
| `[expert]` | Do not build this from what's written here alone. Get a named specialist (security, privacy/legal, etc.) to confirm it first. |
| `[$]` | Getting this wrong is expensive to fix, or can't be fixed at all — a privacy or legal problem, or a decision that locks in once real data or clients depend on it. Needs a confirmed answer before build. |
| `[team]` | A naming or definitions question the team needs to agree on. Doesn't change what gets built — only what it's called. |

**Status labels used on individual rules:**

- **DECISION** — settled, backed by real evidence or a clear team call. Build against this as-is.
- **ASSUMPTION** — a working answer, resting on thin evidence. Build against it for now, but expect it may
  change.
- **UNRESOLVED** — nobody has decided this yet. Do not invent a default — if a builder hits one of these,
  stop and ask.

---

## Outcome

People can capture what they notice about someone's work as it happens — privately for themselves, or
shared with the people who need to see it — so a performance review is written from a real record instead
of memory, and people can ask a colleague for their perspective when they want one.

## Job story

When I notice something about how a direct report, indirect report, or peer is doing — good, or worth
raising — I want to write it down right away, either just for myself or in a way the right people can see,
so a later review is based on a real record instead of memory, and I can ask a colleague for their
perspective when I want one.

## Two objects, one area

This area covers two different kinds of record. They share one home (an employee's record) but behave very
differently. Confusing the two is the single easiest way to get this area wrong.

| | **Note** | **Feedback** |
|---|---|---|
| Who can see it | Only the author — or, if the author shares it, the other person in that same 1:1 and no one else | Someone besides the creator, always — that's what makes it Feedback and not a Note |
| Can it be edited later? | Yes, any time, by the author | No — never, by anyone, once it exists |
| Can it be deleted? | Yes, any time, by the author | No |
| Who can create it | Anyone with a 1:1 series set up with the subject, or the subject's manager via Reports To | Any admin, about any employee — unprompted, or when someone (usually a manager) has specifically asked them for it. Anyone can be asked, not just managers or the employee's own manager. |
| Does the subject (the employee) see it? | No — never | Not automatically. Only if it is explicitly shared with them at the moment it's created. |

---

## The slice

- **Riskiest assumption this micro job tests:** whether Payworks' access model can actually enforce a
  record that only one specific person (or two named people) can see — finer-grained than anything the
  platform does today. If this isn't buildable as specified, the entire privacy premise of the Note object
  needs a different design.
- **The backbone (full flow, for context):** someone captures a Note or gives Feedback about an employee →
  the record lands on that employee's record → the visibility chosen at creation controls who can read it,
  permanently → a review workspace later reads Feedback (and any Notes the reader is entitled to see) as
  reference material.
- **What this slice covers:** the full backbone above, start to finish — capturing a Note or Feedback item,
  it appearing on the right employee's record, the visibility rule holding, and it becoming visible
  (read-only) in a review workspace to whoever is entitled to see it. It closes the loop: content is
  captured, it lands on the record, and it gets used.

---

## Capabilities

No layout, no components, no copy — just what the user must be able to do.

### Where this shows up
- An employee's own record — where Notes about them and Feedback about them live.
- A 1:1 conversation — a second entry point into the same Note object as the employee record (not a
  separate store).
- A standalone give-feedback / request-feedback surface, usable any time, independent of any review cycle.
- A review workspace — reads Notes and Feedback as reference. It does not create or store content of its
  own; it displays the real record, live, following the same visibility rules as everywhere else.

### What people can do
- **Write a Note** about someone if *either* of these is true: a 1:1 series already exists between the
  author and that person (labelled direct report, indirect report, or peer), *or* the author is that
  person's manager according to Reports To. Either one is enough on its own — neither is required in
  addition to the other. There is no way to write a Note about someone if neither condition is met.
- **Choose a Note's visibility at the moment of creation:** author-only, or pair-visible (shared with the
  one other person in that 1:1, when the Note was created through a 1:1 series). This choice cannot change
  later.
- **Edit or delete** an author-only Note, at any time, only by its author.
- **View** a pair-visible Note as the other named participant in that 1:1 — but not edit it. Each
  participant keeps their own separate Note.
- **Search** your own Notes on a person by text, and narrow results by date range.
- **Write Feedback** about any employee. Any admin can do this — it is not limited to that employee's
  manager, and it does not require the target's manager to have asked for it first.
- **Choose Feedback's visibility at the moment of creation:** manager-only (only the target's manager can
  read it — the employee cannot), or shared with the employee (the employee and the manager both see it).
  This choice cannot change later, and Feedback itself can never be edited or deleted once created,
  regardless of which visibility was chosen.
- **Request feedback** from anyone about a specific employee, at any time — the person being asked doesn't
  need to be a manager, or that employee's manager specifically; this is not tied to, or dependent on, a
  review cycle being open.
- **Respond to a feedback request** — the response becomes a normal Feedback item, following the same
  visibility rule as any other Feedback.
- **View Notes and Feedback inside a review workspace**, read-only, as reference while writing a review.

### How the pieces connect
- A Note or Feedback item always shows up on the subject's employee record — that's where someone goes to
  find it. But what that means for *who can read it* is different for each object. Feedback's visibility
  is genuinely tied to that record: if the employee gets a new manager, manager-only Feedback moves with
  them, and the new manager can read it (R17). A Note is different — it only *appears* on the employee
  record as a display location. Who can actually read a Note is locked to its author (and, for a
  pair-visible Note, the other person in that 1:1) — permanently, and a manager change does not extend
  that to a new manager (R17).
- A Note written from inside a 1:1 and a Note written directly on the employee record are the same
  underlying record — opening either place shows the same thing, not two different copies.
- A feedback request, once answered, becomes an ordinary Feedback item and follows the same visibility
  rule as any other Feedback item.
- The review workspace pulls Notes and Feedback live from where they're stored. It never copies or stores
  its own version of the content.

---

## Rules & acceptance criteria

### Rules

| # | Rule | Status |
|---|---|---|
| R1 | A Note is visible to its author only — forever. No other admin, no Site Admin, and not the employee it's about can ever see it. | **DECISION** |
| R2 | A Feedback item must be seen by at least one person besides its creator. That is the definition that separates Feedback from a Note. | **DECISION (definition)** — see the open naming question below |
| R3 | The author can edit or delete their own author-only Note at any time. | **DECISION** |
| R4 | Deleting a Note is permanent. There is no recovery, by anyone, including the author. | **ASSUMPTION** |
| R5 | A person can search their own Notes on someone by text, and narrow results by a date range. | **DECISION** on the underlying need to search · **ASSUMPTION** on text-search-plus-date-filter being the right way to do it |
| R6 | A Note is a separate object from a Disciplinary Action. Creating or editing a Note never creates, changes, or otherwise touches a Disciplinary Action record. | **ASSUMPTION** |
| R7 | Feedback's visibility is chosen once, at the moment of creation, and never changes afterward. Nothing turns a Note into Feedback. Nothing un-shares Feedback once it's shared. To share a private Note's content later, someone has to write brand-new Feedback from scratch. | **ASSUMPTION** |
| R8 | Once Feedback is shared, it is permanent — no edit, no delete, no undo, and no admin override, by anyone, ever. | **DECISION** |
| R8a | A Note can be created about someone if *either* of these is true: a 1:1 series exists between the author and that person, *or* the author is that person's manager according to Reports To. Either is sufficient on its own. | **ASSUMPTION** — added because some managers may not have formal 1:1s set up with their direct reports yet, but still need to write Notes about them. No client or market evidence confirms this specific gap; it's a reasonable working answer, not a proven one. |
| R9 | A Note created through a 1:1 series has a visibility chosen at creation: **author-only**, or **pair-visible**. Pair-visible means a single-author Note, shared on a 1:1, visible only to the author and the one other named person in that 1:1 — nobody else, not a manager chain, not HR, not Site Admin. The other participant can see it but cannot edit it; each person keeps their own separate Note. A Note created only through the Reports-To path (R8a), with no 1:1 series behind it, has no second person to share it with — it can only be author-only. | **DECISION (direction)** on the model · **UNRESOLVED** on whether it's technically buildable — see Constraints |
| R10 | A pair-visible Note can be edited by its author after it's written. Edits are attributed through the normal audit trail. A pair-visible Note never converts to or from an author-only Note. | **DECISION (direction)** |
| R11 | Any admin can write Feedback about any employee. This does not require that employee's manager to have requested it first, and it is not limited to the manager. | **DECISION** |
| R12 | As a direct result of R11, a colleague can give Feedback about another colleague unprompted, with no request or approval step. | **DECISION (by consequence)** — allowed because nothing blocks it, not because demand for it was confirmed |
| R13 | A colleague who is not the subject's manager can give Feedback about that person unprompted. It can reach that person's manager. Whether it can reach the employee directly is still open — see R16. | **DECISION (by consequence)** on reaching the manager · open on reaching the employee |
| R14 | Feedback has two visibility choices: **manager-only** (only the target's manager can read it; the employee cannot) and **shared-with-employee** (the manager and the employee both see it). | **DECISION** on these two choices existing · **ASSUMPTION** on how often each will be used, and on there being exactly two |
| R15 | Requesting feedback is a stand-alone capability. It works any time and does not depend on a review cycle being open. A review reads from existing feedback as reference; it does not create feedback. | **DECISION** |
| R16 | Who is allowed to **read** a piece of Feedback once it exists is not fully decided. This is the single biggest open question in this whole area. It covers four separate parts: (a) is reading limited to the employee's current manager; (b) does read access move to a new manager if the employee gets one — **decided, see R17**; (c) can HR or other admins read it — open; (d) who is allowed to choose to share a piece of Feedback with the employee (any author, or only the direct manager) — open. | **UNRESOLVED** — parts (a), (c), (d) still open; part (b) resolved via R17 |
| R17 | When an employee gets a new manager, or their manager leaves the company, **manager-only Feedback about that employee transfers to the new manager** — the new manager can read it; the previous manager cannot, once the transfer happens. This applies to Feedback only. Existing Notes are not affected by a manager change — a Note's visibility, once set, does not move to a new manager, regardless of whether it was created through a 1:1 series or through Reports To (R8a, R9). A manager change only affects whether the *new* manager can create *new* Notes going forward, via the Reports-To path in R8a. | **DECISION** — see basis below |
| R18 | Whether HR or other higher-level admins can read Feedback at all — including getting any kind of log or list of who wrote what, to whom, when — is not decided. | **UNRESOLVED** — no call made |

**Basis for R8a:** the Reports-To path was added because some managers may not have a formal 1:1 series
set up with their direct reports yet, but still need to be able to write a Note about them — waiting for a
1:1 to exist first would block a real, everyday need. This reason has not been confirmed by any client or
competitor research; it's marked as an assumption because it's a reasonable working answer, not a proven
one.

Reports To is documented elsewhere in this feature as a "weak signal that fails safe" (see Constraints) —
a missing or wrong Reports-To link should never be trusted as a hard access gate on its own. R8a means
Reports To is now doing gating work for Notes, which is unproven at this fine-grained a level for any
object. That reliability question is separate from the reasoning above — the reasoning is why this path
exists; the reliability question is whether the platform can support it safely. Flag the reliability
question to a platform expert; the reasoning itself doesn't need expert review, since it's a deliberate PM
scoping call.

**Basis for R17 (2026-08-05 competitive check):** a focused check of five competitors with clear public
documentation on this exact question found that **transfer-to-new-manager is the market default**, not an
even split:

- **Lattice** — transfers. The new manager gains visibility into past manager-only feedback; the previous
  manager loses it.
- **15Five** — transfers by default when a manager change happens. The previous manager can be manually
  kept on as a "review viewer," but that is a deliberate override, not the default behaviour.
- **PerformYard** — transfers. Their own documentation states it directly: if the employee gets a new
  manager, the new manager sees the feedback and the previous manager no longer does.
- **Betterworks** — transfers, provided the org's reporting structure is updated to reflect the change.
  Once it is, the new manager gains access and the old manager loses it.
- **Culture Amp** — splits by feedback type, which is the one real nuance in an otherwise consistent
  picture. Manager-Requested Feedback (structured, initiated by a manager) transfers automatically to a new
  manager. Anytime Feedback (informal, given without a request) does **not** transfer automatically — it
  stays with the original manager unless the employee manually re-shares it.

Four of the five transfer by default; the fifth transfers for structured/requested feedback and does not
for informal/unprompted feedback. None of the five treat "stays with the original author, new manager
never sees it" as their default behaviour. Transfer is the stronger, more common pattern, with Culture
Amp's request-vs-unprompted distinction as the one open nuance worth watching, given this area's own mix of
requested and unprompted Feedback (R11–R13).

**Open naming question (does not affect what gets built):** R2 defines Feedback as anything visible to
someone besides the creator. A pair-visible Note (R9) is also visible to someone besides its author — by
R2's own wording, that would make it Feedback, not a Note. The team has decided to treat it as a Note
anyway. The rules for who can do what with each object are clear and don't conflict — this is only a
labelling question the team should agree on, not something that changes behaviour. `[team]`

### Acceptance criteria (Given / When / Then)

Written only for rules marked **DECISION** above. Writing one of these for an ASSUMPTION or UNRESOLVED
rule would state an answer that doesn't actually exist yet.

- Given a Note written by its author, When anyone else — including Site Admin — views that employee's
  record, Then the Note does not appear. *(R1 — the rule itself is decided; whether it can be built this
  precisely is a separate open question — see Constraints.)*
- Given a pair-visible Note, When the other named participant in that 1:1 views their shared history, Then
  they see it. When anyone else views it, Then they do not. *(R9 — the model is decided; whether it can be
  enforced is open — see Constraints.)*
- Given a Note, When its author edits or deletes it, Then the change applies immediately, with no approval
  step from anyone else. *(R3.)*
- Given Feedback that has been created, When anyone — including an admin — tries to edit or delete it,
  Then no such action exists for them. *(R8.)*
- Given Feedback marked manager-only, When the employee it's about views their own record, Then it does
  not appear, because employee-visibility is a choice made at creation, not something that happens by
  default.
- Given a Note captured from inside a 1:1 conversation, When it is later viewed from the employee's record
  directly, Then it is the exact same record — not a copy.
- Given manager-only Feedback about an employee, When that employee is assigned a new manager, Then the
  new manager can read it and the previous manager can no longer read it. *(R17.)*

**Not written as acceptance criteria, because nothing has settled them yet:** anything depending on R16
(who can read Feedback), R7 (ASSUMPTION), R8a (ASSUMPTION), or R9's buildability (UNRESOLVED). Writing a
Given/When/Then for these would assert an answer that doesn't exist.

---

## Constraints

The non-negotiables the build cannot guess at, and must not break.

- **Bilingual (English-Canada / French-Canada).** Payworks operates under Quebec's language law. All of
  this feature's own screen text, labels, buttons, and system messages must work in both languages. This
  applies to the feature's chrome only — not to what a person actually writes in a Note or Feedback item.
  What a person writes is free text and is never translated. *(compliance)*
- **Notes and Feedback are personal information about an employee, held on the employer's system.**
  Retention, audit trail requirements, and whether these records must be produced on request (an access
  request, or a legal hold) are governed by privacy and records law, not by product preference. This must
  be confirmed before build, not assumed. *(compliance)*
- **The permanence built into this design removes the usual fallback of "just look at the history."** A
  deleted Note is gone — nobody can pull it back up if a dispute comes up later. Feedback is never editable
  in the first place. Anyone building support processes around this area needs to plan for that; there is
  no "check what was actually written" option after the fact.
- **Reports To, used as a way to control who can see what, is documented elsewhere in Payworks as a "weak
  signal that fails safe."** That means: if the Reports To link is missing or wrong, it grants nobody
  access — it is never allowed to be a hard, all-or-nothing access gate on its own. This now directly
  affects this area: R8a lets a Note be created through the Reports To relationship, not only through a
  1:1 series. Two things about this are still open: (1) this pattern has not yet been proven at the very
  fine-grained, single-person level a Note needs; (2) whether Reports To can even be looked up efficiently
  enough, at the moment someone tries to create or read a record, is itself an unresolved question
  elsewhere in the platform. If the answer there is no, this area needs a fallback too. If Reports To is
  missing or wrong for someone, R8a's Reports-To path simply doesn't apply for that person — it fails
  safe, consistent with the platform-wide rule — but that means a manager with no working Reports To link
  loses this route to creating a Note, with the 1:1-series path as the only way in.

---

## Roles & permissions

*(There is no separate "manager" account type in Payworks. Differences below come from permissions and the
Reports To link, not from a different kind of account.)*

**Notes**
- **The author** — any admin who has *either* a 1:1 series set up with the person (labelled direct report,
  indirect report, or peer) *or* is that person's manager according to Reports To: can create, view, edit,
  search, and permanently delete **their own** author-only Notes. Cannot see anyone else's author-only
  Notes about anyone. If the author reached this person only through Reports To, with no 1:1 series, their
  Notes about that person can only ever be author-only (R9) — there's no second person to share with.
- **The other participant on a pair-visible Note:** can view it. Cannot edit it. Only exists for Notes
  created through a 1:1 series.
- **Any other admin, including Site Admin:** cannot see an author-only Note, ever. Cannot see a
  pair-visible Note unless they are one of the two named people on it.
- **The employee a Note is about:** never sees Notes about them — not the author-only kind, and not the
  pair-visible kind, unless they themselves are one of the two named people on that specific pair-visible
  Note.

**Feedback**
- **Creation:** any admin can create Feedback about any employee.
- **The employee the Feedback is about:** does not see it by default. Sees it only if it was explicitly
  shared with them at creation (the shared-with-employee choice). Who is allowed to make that
  share-with-employee choice is not decided — see R16.
- **The employee's manager, when the employee gets a new manager:** the new manager gains read access to
  existing manager-only Feedback about that employee; the previous manager loses it (R17).
- **Who can read it otherwise:** not decided at all — see R16.

---

## Cross-cutting concerns (in this slice, or deferred)

| Dimension | In this slice? | If deferred — risk + what picks it up |
|---|---|---|
| Accessibility (keyboard, screen reader, colour) | Not addressed in this brief. | Deferred. Standard build-time requirement; no area-specific risk identified. |
| Localization (this feature's own screen text, en-CA / fr-CA) | In this slice — see Constraints. | — |
| Notifications (in-app + email, both languages) | Not addressed. Whether giving or requesting Feedback sends any notification is an open question (see Open Questions) — nothing here specifies one exists. | Open, not deferred — a real gap, not a decided-and-postponed item. |
| Audit & history (who / what / when) | Partially addressed: Feedback's permanence and Notes' hard-delete are specified (R4, R8). What minimum audit or retention applies to a deleted Note, or to Feedback generally, as personal information, is not decided. | Open — see Open Questions and Constraints. |
| Existing data & day-one state | Not addressed anywhere in this brief. | Open — not yet considered. |
| Permission-denied & out-of-scope personas | Partially addressed through the roles table above (who can and can't see what). What a person sees when they try to reach content they're not entitled to is not specified. | Open — not yet considered. |

---

## Out of scope

- A public, company-wide visibility tier for Feedback (like a "give recognition publicly" feature). No
  client has asked for this, and it matches how Payworks already keeps recognition-style features separate
  from private/constructive feedback.
- Unprompted upward feedback — an employee proactively reviewing their own manager without being asked. If
  a manager's manager wants input on that manager, they can use the standalone feedback-request capability
  instead; that already covers this case. Only the *unprompted* version is excluded.
- A three-way visibility model (something like separate Recognition / Development / Concern types). No
  client evidence supports this shape; the simpler model in this brief matches what clients actually
  described.
- An employee's own private journal — self-authored notes about themselves, separate from a manager's
  Notes about them. No client has asked for this.
- Any reporting or nudges built on top of Feedback data (for example, "this person hasn't received
  feedback in 60 days"). Not explored in this pass.

---

## Open questions

- **Can Payworks technically enforce a record visible to only one specific person, or two specific named
  people — not even Site Admin?** This is finer-grained than anything the access model does today. This is
  the single biggest open question under the whole Notes side of this area. `[expert]`
- **Is Reports To reliable enough to gate Note creation on (R8a)?** R8a lets a manager create a Note just
  because Reports To says they manage that person — no 1:1 series required. Whether Reports To can be
  looked up efficiently enough at the moment someone tries to create a Note, and whether it's accurate
  enough to trust for this, are both open elsewhere in the platform. If Reports To is missing or wrong for
  a given manager, they lose this creation path entirely and are left with the 1:1-series path only — this
  hasn't been tested against real data. `[expert]`
- **Does R17's transfer rule need Culture Amp's request-vs-unprompted distinction?** R17 decides that
  manager-only Feedback transfers to a new manager. The one open competitor nuance behind that decision is
  that some products transfer *requested* Feedback automatically but leave *unprompted* Feedback with the
  original manager unless the employee re-shares it. Since this area allows both requested and unprompted
  Feedback (R11–R13), whether the same transfer rule should really apply to both, or only to requested
  Feedback, hasn't been decided separately. `[assumption]`
- **Is request-gating the right long-term answer for manager-only feedback, or was it only ever meant to
  be a safer starting point?** Only one company's evidence speaks to this either way. `[assumption]`
- **Where does Feedback live on the employee's record** — a new tab next to the existing Reviews and
  Disciplinary Actions tabs, or folded into one of those? This has a real cost impact: a new tab means a
  new screen and a new permission to manage. This is also not a decision this area alone can make — other
  parts of Payworks' performance-management work are adding tabs to the same part of the employee record,
  and how many tabs that record ends up with is a shared decision, not a per-feature one. `[assumption]`
- **Does a Note or Feedback item need any structure** — a length limit, a title, tags? No client has asked
  for this. Not urgent. `[assumption]`
- **What minimum audit trail or retention applies to these records**, given they are personal information
  about an employee (covering things like access requests and legal holds)? `[expert]`
- **Does giving or requesting Feedback send a notification** to the person it's about, their manager, or
  the person being asked to give input? A private Note never needed this — there's no second person to
  tell. Feedback always has at least one other party, so this is a genuinely new question. Whether this
  should use a notification system that already exists elsewhere for performance-related features, or need
  its own, is also unresolved. `[assumption]`
- **Does the person who gives manager-only feedback keep their own view of what they submitted afterward?**
  Not decided either way. `[assumption]`
- **Who is allowed to read Feedback once it exists — the read-scope question.** This is R16 above, restated
  as a question because it is the most important open item in this entire area: is reading limited to the
  current manager, can HR read it, and who can choose to share it with the employee? (Whether it moves with
  a manager change is now decided — see R17 — but the other three parts are not.) `[$] [expert]`
- **Is there a privacy problem with the current design as a whole?** Any admin can write Feedback about any
  employee. It lands on that employee's record. That employee may never see it. Under Canadian privacy law
  (federal, and Quebec's own law), a person can request the personal information an organization holds
  about them. A growing pool of Feedback an employee can never see may create real exposure if that request
  is ever made. This needs an answer before build, not after. `[$] [expert]`

---

## Exceptions (this is a starting list — expect more to turn up later)

| # | When this happens... | ...the outcome must be | Status |
|---|---|---|---|
| E1 | An employee's manager changes, or their manager leaves the company | Manager-only Feedback about that employee transfers to the new manager; the previous manager loses read access once the transfer happens. Notes are unaffected — see R17. | **Decided** |
| E2 | An employee is terminated | Not enough information to say. This connects to an existing terminated-employee access setting elsewhere in Payworks, but how it applies here hasn't been worked out. | **Open** |
| E3 | An employee has two managers, or their Reports To link is broken or missing | Not enough information to say. Out of scope until Payworks' current single-manager assumption changes elsewhere in the platform. | **Open** |
| E4 | Someone picks the wrong object (Note vs. Feedback), or the wrong visibility, and only notices after saving | There is no way to fix this after the fact — both the object choice and the visibility choice are permanent by design (R7, R4, R8). One direction worth design exploring: making the type/visibility choice its own step before someone starts writing, to reduce — not eliminate — how often this happens. Left to design to solve, not specified here. | **Open** |
| E5 | A manager requested feedback from a colleague, and later wants to see exactly what that colleague submitted | Not enough information to say. Undecided either way. | **Open** |

Known unknowns not yet worked through: this is only a starting list. Design and testing will surface more
exceptions once real screens and real data exist.

---

## Risks / break points

- **The core privacy promise of Notes may not be legally enforceable.** A Note is designed to be invisible
  to the employee it's about, forever (R1). But under Canadian privacy law, a person can request the
  personal information an organization holds about them. A manager's private Note very likely counts as
  personal information about that employee — it names them and records observations about their work. If
  it does, "invisible to the employee, forever" may not hold up against a legal access request or in
  litigation. This is different from the technical question above (*can* the system hide it) — this is
  *is it legal to promise it stays hidden.* Get a legal answer before this promise is built into the
  product or told to any client. `[$] [expert]`
- **The entire Notes design depends on an access capability that may not exist yet.** If Payworks cannot
  enforce visibility down to one specific person, the whole "speak freely, nobody will ever see this"
  premise for Notes fails and needs a different design. This is expensive to discover late — there's no
  cheap fix once clients are already relying on the promise.
- **Reports To is only ever a "weak signal" elsewhere in Payworks — R8a now makes this area the first
  place that could change.** Letting a manager create a Note through Reports To alone (no 1:1 required) is
  new platform work, not something already proven at this fine-grained a level. Getting it wrong could
  silently give the wrong person the ability to create a Note, or silently block a real manager who should
  be able to.
- **A wrong visibility default can never be corrected.** Because visibility locks in at creation with no
  edit and no undo, a bug or a bad default that shows something to the wrong person cannot be fixed after
  the fact — the content has already been seen. Test this very carefully before anything launches; there
  is no cleanup possible once real data exists.
- **Someone can pick the wrong object or the wrong visibility and have no way back.** If it isn't
  unmistakably clear in the moment which one someone is creating, a person who meant to write a private
  Note but accidentally made it shared (or the other way around) has no way to undo it.
- **The manager-change transfer rule (R17) may be too blunt for unprompted Feedback.** R17 decides that
  manager-only Feedback transfers to a new manager. Some competitors only auto-transfer *requested*
  Feedback, and leave *unprompted* Feedback with the original manager unless the employee re-shares it.
  Since this area allows unprompted Feedback (R11–R13) as well as requested Feedback, applying one
  transfer rule to both hasn't been separately tested — worth a second look once real usage exists.
- **What happens when an employee is terminated is completely undefined.** Whether a former manager keeps
  or loses access to Notes and Feedback about someone no longer employed isn't decided.
- **An employee with two managers, or a broken Reports To link, isn't handled by this design at all.** This
  is inherited from an assumption made elsewhere in Payworks that every employee has exactly one manager.
- **Manager-only feedback being open to anyone, unprompted, assumes people will actually use the request
  option when they want structured input.** If they don't, the "capture what's really happening" value
  this area is meant to provide quietly weakens, with nothing forcing anyone to notice. Not a hard failure —
  worth watching after launch.
- **This whole area's value depends on a review workspace actually using it.** If reviews aren't built to
  pull in Notes and Feedback as reference material, the core reason for building this — "write a review
  from a real record, not memory" — doesn't land. That workspace is a separate piece of work this area
  depends on, not something this area controls on its own.
- **Unprompted peer-to-peer feedback is allowed by default, not because demand for it was confirmed.** If
  usage patterns show real demand, that's a good sign. If it goes unused, or causes problems, the current
  evidence isn't strong enough to justify leaving it as-is without a second look.
- **How this area's records are logged and audited may not tell a consistent story next to related
  features.** Other performance-related records elsewhere in Payworks are fully exportable. Feedback here
  may have no HR-facing log at all, depending on how R18 is resolved. Notes are permanently deleted with no
  recovery. Whether these three different postures make sense side by side, to a client asking about them,
  hasn't been checked.
- **Where the employee sees shared Feedback is a shared surface, not something this area owns alone.** The
  shared-with-employee tier means the employee needs somewhere to see it — and that "somewhere" is a
  broader employee self-service space that other performance-management work is building, not a
  Feedback-only screen. Who decides what the employee sees across different kinds of content in that shared
  space is not yet assigned to anyone.

---

## Competitive notes

A scan covered 16 competitor products: Lattice, 15Five, BambooHR, Humi, Rise People, Culture Amp, Leapsome,
Rippling, HiBob, PerformYard, Betterworks, Zoho People, UKG Pro, ADP Workforce Now, Paylocity, and Workday.
What follows is what mattered from that scan, not the full detail.

- The market splits cleanly into "Recognition" (public praise, its own separate feature) and "Feedback"
  (private or constructive, closed by default). Keeping a public tier out of Feedback matches this split.
- Private, author-only notes are a common, standalone pattern — confirmed in at least 4 of the 16
  products checked. Two of them (Lattice, 15Five) are author-only and invisible even to admins — the same
  shape used here. One (UKG Pro) goes further, with several distinct note types, never visible to the
  employee, freely editable by the author.
- Merging Notes and Feedback into one object, with sharing chosen once at creation, is a proven pattern —
  confirmed in at least 2 of the 16 products checked.
- Whether feedback can be edited after it's shared is a genuine split in the market — not a settled
  standard. Three products lock it forever once submitted (matching the choice here). One allows full
  edit/delete, any time, by the author. The rest either had no clear documentation, or used a
  middle-ground, approval-based process.
- Manager-only visibility (the recipient's manager sees it, the recipient doesn't) is common and
  well-established — confirmed in at least 3 of the 16 checked.
- A stand-alone request-feedback capability, not tied to a review cycle, is the norm — confirmed in at
  least 3 of the 16 checked.
- Whether HR or admins can see the actual content of feedback is far from universal, and even where it
  exists, it's usually a setting the organization controls, not a fixed requirement. But whether HR gets a
  *log* of feedback activity (who gave what, to whom, when) is a different story — at least one major
  competitor gives admins a full log and export of this, with no way to turn it off. A "no log at all"
  position, if that's where this area lands, would be the stricter, less common choice in the market.
- Most competitors with clear documentation default to open, unprompted manager-only feedback — confirmed
  in at least 5 of the 16 checked. None of the 16 checked had a request-only model as their *only* option.
- When an employee gets a new manager, manager-only feedback transferring to the new manager (rather than
  staying with the original manager) is the clear market default — confirmed in 4 of the 16 checked
  (Lattice, 15Five, PerformYard, Betterworks). A fifth (Culture Amp) splits by feedback type: structured,
  manager-requested feedback transfers automatically; informal, unprompted feedback does not transfer
  unless the employee manually re-shares it. See R17.

---

## Handoff note

The core object model — a Note (author-only, editable any time) and Feedback (seen by someone besides the
creator, locked forever once shared, visibility chosen once at creation with no way to change it later) —
is well-reasoned and ready to be sized for build.

**The one thing not to guess on:** whether Payworks' access model can actually enforce a record visible to
literally nobody but its author — not even Site Admin (R1). This is finer-grained than anything the
platform does today, and it is the load-bearing assumption under this entire area. Get a confirmed answer
from a security or platform expert before committing further build time here.

**The second thing to flag loudly:** who is allowed to read Feedback at all (R16) is genuinely undecided,
and it is the single biggest open question in this area — manager-change (R17) is settled, but R16's other
three parts (limiting reads to the current manager, HR/admin access, and who may share with the employee)
are not. Don't let a default get picked implicitly during build — this needs a deliberate decision first.

**The third thing to flag loudly:** R8a lets a manager create a Note through Reports To alone, with no 1:1
series required. This directly raises the reliability concern already noted elsewhere in this document
about Reports To ("weak signal that fails safe" — see Constraints). Get this checked against Reports-To's
known reliability limits before build, not after.

**One certain cost to plan for from the start, not an open question:** this feature's own screen text and
system messages must work in both English and French, per Quebec's language law. That applies no matter
how the open questions above get resolved.
