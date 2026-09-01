# Micro job — Set a goal and keep it current

**Author:** Claire
**Date:** 2026-08-06
**Area:** Goals, part of Performance Management
**Status:** Draft

---

## 1. Words used in this document

Read this first. These words are used in an exact way here.

| Word | What it means here |
|---|---|
| **Micro job** | One small piece of a bigger product idea, cut so it can be built and tested on its own. It says *what a person must be able to do* and *what must be true*. It does not say what the screens look like. |
| **Slice** | The thin path this micro job covers — start to finish, with the least possible at every step. Same thing as the micro job itself. |
| **Goal** | A written record of something a person is trying to achieve, plus a record of how it is going. |
| **Owner** | The employee the goal belongs to. |
| **Lifecycle phase** | Where a goal sits in its life: **Draft** (written down, not in play yet), **Active** (in play), **Closed** (finished, no more changes). |
| **Working status** | While a goal is Active, a short read on whether it will land: **On Track** or **At Risk**. |
| **Overdue** | Worked out by the system, not chosen by a person. True when the due date has passed and the goal is not Closed. A goal can be At Risk *and* Overdue, or On Track *and* Overdue. |
| **Progress log** | The running list of updates on a goal. Each entry is a short note, the working status at that moment, who wrote it, and when. |
| **Reports-To** | The field on an employee record that names that employee's manager. |
| **Direct manager** | The person named in that employee's Reports-To field. |
| **Access scope** | The set of employees a person is already allowed to see in Payworks. It comes from the permissions they have been given: which module and screen they can open, at Read or Write; their security level; and their department and pay group. Goals does not build its own version of this — it uses the one that already exists. |
| **Given / When / Then** | A way of writing a test: *Given* a starting situation, *When* someone does something, *Then* here is what must be true afterwards. It describes results, never buttons or screens. |
| **en-CA / fr-CA** | Canadian English and Canadian French. |

**Confidence labels** used through this document:

- **[Settled]** — good evidence behind it. Build against it.
- **[Assumed]** — a real decision, but ours, not confirmed by clients. Build against it, but with less
  confidence.
- **[Open]** — not decided. Needs an answer before this can be built.

---

## 2. The job story

**When** I am trying to make progress on something over months, and the only record of it is a
spreadsheet, a notebook, or a conversation nobody wrote down,
**I want to** keep one shared, current record of what I am trying to achieve and how it is going,
**so I can** stop relying on memory when it is time to talk about how the year went.

This is one job held by two people at once — the employee and their manager both need the same record
to be true.

**In this slice, only the manager writes.** The manager creates the goal and records how it is going.
The employee can see everything about their own goals and cannot change anything. Employees creating
and updating their own goals is a later slice.

---

## 3. What this slice covers

### The riskiest assumption this slice tests

**That managers will actually keep goals current inside Payworks instead of in a spreadsheet.**

Everything else in Goals rests on this. Cascading, team roll-ups, and goals inside a review are all
worth nothing if the underlying record goes stale. There is a second, sharper edge to the same
question: most of the evidence for structured goal tracking came from larger companies. Smaller
companies said they want the same thing but do it informally. This slice is the cheapest way to find
out whether smaller companies will use a structured goal record at all.

Because only managers write in this slice, the whole recording load sits on one person per team. A
manager with eight reports keeps eight sets of goals current on their own. That is a harder test than
one where both people can update, and it is worth watching for.

### The full flow, for context

Set a goal → keep it current while it runs → talk about it → close it out → use it in a review.

### Where this slice starts and ends

It starts when a manager writes a goal down for one of their people. It ends when that goal is closed
out.

It closes the loop: a goal is created, both the manager and the employee can see it, the manager can
update it, and it can be finished. There is nothing left dangling at the end.

It deliberately does **not** reach the last step of the full flow (using a goal in a review). See
*Section 14 — what comes next*.

---

## 4. The goal, and what it holds in this slice

| Field | What it is | Required? |
|---|---|---|
| Title | Short text naming the goal. | Yes |
| Description | Longer text. | No |
| Owner | The employee the goal belongs to. Chosen when the goal is created. Never blank. **[Assumed]** | Yes |
| Created by | The owner's direct manager. In this slice, nobody creates a goal for themself. | Yes, set by the system |
| Due date | The date the goal is meant to be finished by. | Yes |
| Lifecycle phase | Draft, Active, or Closed. | Yes |
| Working status | On Track or At Risk. Only exists while the goal is Active. | While Active |
| Closure outcome | Completed or Cancelled. Only exists once the goal is Closed. | When Closed |
| Overdue | Worked out from the due date, not stored and not chosen. | System-derived |
| Progress log | Every update on the goal: note, working status at that moment, who, and when. | Grows over time |
| Change reason | A short note explaining why the title, description, or due date was changed. Required for every such change after the goal is Active. | On edit |
| Last updated | The date of the most recent change to status, or the most recent progress note. A plain factual date. Nothing in Goals reads it or acts on it in this slice — it exists so that later work can. | System-derived |

**Not in this slice:** any way to attach a number to a goal (a dollar amount, a percentage, a count, a
milestone) or to show progress toward that number. See *Section 14*.

---

## 5. Capabilities — what a person must be able to do

No screens, no layout, no wording. Design decides all of that.

### Places a person can be

- Looking at a single goal, including its whole progress log and its change history.
- Looking at the list of goals for one person — either their own, or one employee they have access to.

### Things a person can act on

- **Create a goal** — with a title, an owner, and a due date at minimum.
- **Move a goal from Draft to Active** — put it in play.
- **See a goal** — the goal itself, its progress log, and its change history.
- **Add a progress update** — a short note, and the working status at that moment.
- **Change the working status** — between On Track and At Risk.
- **Edit a goal** — its title, description, or due date. After the goal is Active, this requires a
  reason, which is kept.
- **Carry a goal forward** — give it a later due date so it keeps running rather than closing.
- **Close a goal** — as Completed or as Cancelled.
- **Delete a goal** — only while it is still a Draft.

### Where each action leads

- Creating a goal produces a Draft. A Draft is not in play until someone activates it.
- Activating a goal makes it visible and updatable by both the owner and the people whose access scope
  covers the owner.
- Every progress update is added to the progress log. Nothing in the log is overwritten.
- Every edit after Active is recorded with its reason, who made it, and when.
- Closing a goal ends it. A Closed goal keeps its full history.

### Capabilities this slice does not answer — flagged, not invented

These are real actions that a goal probably needs, and there is no decision behind any of them yet.
They are listed here so nobody builds an answer by reflex.

- **Reopen a Closed goal.** No decision exists on whether this is possible at all.
- **Edit or delete an entry already in the progress log.** No decision exists.
- **Change a goal's owner after it is created.** No decision exists on whether a goal can be moved to a
  different person.
- **Delete an Active or Closed goal.** Deletion is restricted to Draft, so the answer today is no —
  but nothing says what a company does when an Active goal was created in error and must be removed.

---

## 6. Who can do what

Two different bounds are at work, and they are not the same:

- **To see a goal**, the owner must be inside your access scope.
- **To create, edit, update, or close a goal**, the owner must be inside your access scope **and** you
  must be their direct manager. Being able to see someone is not enough to act on their goals.

In this slice, **only a direct manager writes**. Nobody creates or edits a goal for themself — not an
employee, not a manager, not an HR administrator. The employee can see everything about their own goals
and change nothing.

| Action | HR Admin | Manager | Employee |
|---|---|---|---|
| Create a goal for someone else | No | Yes — for employees who report directly to them and are inside their access scope | No |
| Create a goal for themself | No | No | No |
| See a goal | Employees inside their access scope | Employees inside their access scope | Their own |
| Edit a goal | **[Open]** — see Open questions | Employees who report directly to them and are inside their access scope | No |
| Add a progress update | No | Employees who report directly to them and are inside their access scope | No |
| Change the working status | No | Employees who report directly to them and are inside their access scope | No |
| Close a goal | **[Open]** — see Open questions | Employees who report directly to them and are inside their access scope | No |
| Delete a goal (Draft only) | **[Open]** — see Open questions | Employees who report directly to them and are inside their access scope | No |

**A manager's own goals.** A manager is somebody's employee too. Their goals are created and updated by
*their* manager, under exactly the same rule. There is no separate path for it.

**Assumption — a person with no Reports-To cannot have a goal at all in this slice.** Only a person's
direct manager can create or edit a goal for them, and the direct manager comes from the Reports-To
field. If that field is empty, nobody is permitted to create a goal for them, and they cannot create one
for themself either. This affects the people at the very top of the chain of command — an owner, a CEO,
a president. In this slice they cannot have a goal. **[Assumed]** Whether this is a reasonable approach
is an open question, as is whether an HR administrator or site administrator should be able to create a
goal for anyone — see Section 13.

**Where this sits in the app.** Goals runs inside Payworks' existing access model — a module gives
access to a screen, the screen is set to None, Read, or Write, and the employees a person can act on
are set by their security level, department, and pay group. Goals does not add a new kind of
permission and does not invent its own idea of who a manager is.

**Flag for the security expert:** which screen or screens Goals lives on, and how Goals permissions are
granted to a limited-access administrator, has not been confirmed. Do not assume it copies any other
area's setup.

---

## 7. Rules

These are the things that must be true. They are not suggestions and they are not about how anything
looks.

1. A goal always has an owner. It can never be saved without one. **[Assumed]**
2. A goal always has a title and a due date. **[Settled]**
3. A goal is in exactly one lifecycle phase at a time: Draft, Active, or Closed. **[Settled]**
4. A working status exists only while a goal is Active. A Draft has no working status, and a Closed
   goal has a closure outcome instead. **[Settled]**
5. The working status is set by a person, not worked out by the system. **[Assumed — and this is
   currently an open question, see Open questions]**
6. Overdue is worked out from the due date. It is never chosen by a person and never stored. It sits
   alongside the working status rather than replacing it. **[Assumed]**
7. A goal past its due date is flagged Overdue. It is not closed automatically and its due date is not
   moved automatically. Nothing happens to a goal unless a person does it. **[Assumed]**
8. Changing a goal's title, description, or due date after it is Active requires a reason, and that
   reason is kept. **[Assumed]**
9. Nothing on a goal is ever silently overwritten. Every change to a goal — an edit, a status change, a
   progress note — is kept with who made it and when. **[Assumed]**
10. A goal is deleted only while it is a Draft. Once Active, it can be closed but not deleted.
    **[Assumed]**
11. Only the owner's direct manager writes to a goal — creating it, editing it, adding a progress
    update, changing its working status, closing it, or deleting a Draft. Being able to see an employee
    does not let you do any of these. The owner cannot do them either. **[Assumed]**
12. You cannot act on a goal you cannot see. Every write is bounded by the same access scope as the
    read. **[Assumed]**
13. If two people change the same goal at the same time, the last save is the one that is kept. The
    other person's change is lost, and nobody is told. This is a knowingly accepted trade-off, not an
    oversight. **[Assumed]**
14. There is no limit on how many open goals one person can have. The product never blocks someone from
    creating another goal. **[Assumed]**

---

## 8. Acceptance criteria

Written as *Given / When / Then*. Each one describes a result, never a screen or a control.

**Creating and activating**

1. *Given* a manager is creating a goal for an employee who reports directly to them and is inside their
   access scope, *When* they save it with a title, an owner, and a due date, *Then* the goal exists as a
   Draft with that owner, and no working status.
2. *Given* a manager is creating a goal for an employee who is inside their access scope but does **not**
   report directly to them, *When* they try to save it, *Then* the goal is not created.
3. *Given* a goal is missing a title, an owner, or a due date, *When* someone tries to save it, *Then*
   the goal is not saved and the missing information is made clear.
4. *Given* a goal is a Draft, *When* it is activated, *Then* it becomes Active and visible to its owner.

**Keeping it current**

5. *Given* a goal is Active, *When* the owner's direct manager adds a progress note, *Then* the note is
   added to the progress log with their name and the date, the existing log is unchanged, and the goal's
   last-updated date becomes today.
6. *Given* a goal is Active and On Track, *When* the owner's direct manager changes the status to At
   Risk, *Then* the goal reads At Risk, the change is recorded in the progress log with who and when,
   and the previous status is still visible in the history.
7. *Given* a goal is Active, *When* its direct manager edits the title, description, or due date without
   giving a reason, *Then* the change is not saved.
8. *Given* a goal is Active, *When* its direct manager edits the due date with a reason, *Then* the new
   due date applies, and the old due date, the reason, who changed it, and when are all kept and
   visible.
9. *Given* a goal is Active, *When* its owner tries to edit it, add a progress note, change its working
   status, or close it, *Then* no change is made to the goal.

**Overdue**

10. *Given* a goal is Active and its due date has passed, *When* anyone with access looks at it, *Then*
    it reads as Overdue, its working status is unchanged, and its lifecycle phase is still Active.
11. *Given* a goal is Overdue, *When* its direct manager carries it forward with a later due date,
    *Then* it is no longer Overdue, it is still Active, and the whole earlier progress log is still
    there.

**Closing**

12. *Given* a goal is Active, *When* its direct manager closes it as Completed, *Then* it is Closed with
    an outcome of Completed, it no longer carries a working status, and its full history is still
    readable.
13. *Given* a goal is Closed, *When* someone tries to add a progress note or change its details, *Then*
    the change is not made.
14. *Given* a goal is Active, *When* someone tries to delete it, *Then* it is not deleted.

**Access**

15. *Given* an employee, *When* they look at their goals, *Then* they see every goal they own,
    including Drafts created by their manager if Draft goals are visible to owners **[Open — see Open
    questions]**.
16. *Given* an administrator whose access scope does not cover an employee, *When* they try to see or
    act on that employee's goal, *Then* nothing about the goal is shown to them.

---

## 9. Constraints — the things a build cannot guess and must not break

Each one is a rule plus the reason it exists.

- **Goal titles and descriptions must accept both an English (en-CA) and a French (fr-CA) value.**
  *Why:* Quebec language law. Any content one person types that another person will read has to support
  both languages. One language is enough to save; the second is optional. This is a legal obligation,
  not a wording preference. **[Compliance]**
- **Every label, message, empty state, and error this feature produces must exist in en-CA and fr-CA.**
  *Why:* same obligation, but about the product's own words rather than what users type. This is
  separate from the point above and does not come for free with it. **[Compliance]**
- **Every change to a goal must record who made it and when, and must not overwrite what was there
  before. Every edit to the title, description, or due date after activation must also record a
  reason.** *Why:* a goal can end up shaping a performance review, and in some companies a pay or bonus
  decision. If a goal's history can be quietly rewritten, nobody can defend the decision later, and an
  employee has no way to challenge it.
- **Goals must use Payworks' existing access model, not a new one.** *Why:* a second, separate idea of
  who can see whom is how data gets exposed to the wrong person. It also puts Goals out of step with the
  rest of Performance Management.
- **When an employee's Reports-To field is missing, wrong, or out of date, the access check must grant
  nothing rather than guess.** *Why:* this is the platform's existing rule and it must not be
  re-invented here. A broken manager link must never silently widen who can see a goal.

**Not applicable to this slice:** there is no tax content, no money movement, no pay-period rule, and no
statutory employee data here. Nothing in this slice can post to or affect a pay run.

---

## 10. Cross-cutting concerns

The work every slice carries that a happy-path demo hides. Each one is either *in this slice* or
*deferred with the risk named*. Where no decision exists, that is stated rather than filled in.

| Concern | State | Notes |
|---|---|---|
| **Accessibility** — keyboard-only use, screen readers, nothing carried by colour alone | **No decision exists** | Goals introduces at least two things that are likely to need custom work: the On Track / At Risk indicator and the Overdue flag. Both are the kind of signal that gets built as colour alone. This needs a call before build — for an HR product it is an accessibility-law exposure, not a nice-to-have. **Your decision needed.** |
| **The product's own English and French words** | **In this slice** | Named as a constraint above. Not optional. |
| **Bilingual input on goal titles and descriptions** | **In this slice** | Named as a constraint above. Not optional. |
| **Notifications and reminders** — telling someone a goal is Overdue, or that it has not been updated | **No decision exists** | Nobody has decided whether Goals sends anything at all, by email or otherwise. This matters more here than usual: the whole slice rests on people keeping goals current, and nothing currently prompts them to. **Your decision needed.** |
| **Audit** — who changed what, when, and why | **In this slice** | The change reason, the progress log, and the who-and-when stamp are all in scope. |
| **Day-one data** | **In this slice** | No goals exist before this ships, so there is nothing to migrate. Every company starts empty. What a person sees when they have no goals yet is a real state design has to handle. |
| **Permission denied** — what someone sees when a goal is outside their access scope | **No decision exists** | The rule is that they see nothing about the goal. Whether they are told the goal exists but is not theirs to see, or told nothing at all, is not decided. **Your decision needed.** |

---

## 11. Exceptions — a starting floor, not a full list

Design and testing will find more. This is a floor.

| # | When this happens... | ...what must be true |
|---|---|---|
| E1 | The goal's owner has no manager set, or their manager has left | The access check grants nothing rather than guessing. **What happens to the goal itself in the meantime — whether anyone can act on it, or whether it sits untouched until HR fixes the reporting link — is not decided. [Open]** |
| E2 | The goal's owner changes managers while the goal is running | The new manager can see and act on the goal going forward. The old manager's access ends. The goal itself is not changed. **[Assumed]** |
| E3 | The goal's owner is terminated with goals still open | The goal record is kept and stays readable by their former manager and by HR. **[Assumed]** |
| E4 | Two people edit the same goal at the same moment | The last save wins. The other change is lost with no warning. Accepted on purpose. **[Assumed]** |
| E5 | A goal reaches its due date with nothing done to it | It is flagged Overdue. It is not closed and its date is not moved. **[Assumed]** |
| E6 | A goal has read On Track for months and nobody has touched it | Nothing in this slice catches this. The last-updated date exists so that later work can surface it. **This is a known, unsolved weakness of this slice.** |
| E7 | Someone tries to save a goal with a due date in the past | **No decision exists.** Whether this is allowed, blocked, or allowed-and-immediately-Overdue is not specified. **[Open]** |
| E8 | An employee disagrees with a goal their manager set, or with a progress note written about them | Nothing in this slice gives them a way to respond. They can see it and cannot answer it. **This is a known gap created by making the slice manager-only, not an oversight.** |
| E9 | A person holds both an employee account and an administrator account | The existing platform guard should stop them acting on their own record as an administrator. **Whether that guard covers Goals, and whether it should, has not been confirmed.** Flag for the security expert. |
| E10 | A person has no Reports-To — for example an owner, a CEO, or a president | They cannot have a goal at all in this slice. Nobody can create one for them, because there is no direct manager, and they cannot create one for themself. **[Assumed]** — and see the open question on whether this is a reasonable approach. |

---

## 12. How we will know it worked

- **The behaviour we expect to change:** managers stop keeping their people's goals in a spreadsheet, a
  notebook, or nowhere, and keep them in Payworks instead — and keep them current, not just entered
  once.
- **Fast signal:** the share of Active goals that get at least one progress update in the first 90 days
  after they are created. Entering a goal is easy; coming back to it is the real test.
- **Real-value signal:** the share of goals that reach a deliberate end — Closed as Completed or
  Cancelled, or carried forward with a new due date — rather than sitting Active and Overdue with
  nobody touching them.
- **Guardrail — must not get worse:** the share of Active goals that go untouched past their due date.
  If most goals end up stale and Overdue, the product is collecting goals rather than tracking them,
  and every later slice is built on sand.
- **Second guardrail:** the share of managers who create goals for some of their reports but not all of
  them. Because one person carries the whole recording load, partial coverage is a likely failure — a
  manager sets goals for two people out of eight and stops.
- **How this settles the risky assumption:** if goals get created and never updated, or if smaller
  companies barely create them at all, the assumption is dead and the fuller build should stop and be
  rethought — before cascading, dashboards, or review integration are built on top of it.

**Worth splitting these numbers by company size.** The doubt about whether smaller companies want a
structured goal record is the single most expensive thing to have wrong here, and an overall average
will hide it.

**A limit on what this slice can tell us.** It measures whether *managers* maintain goals. It cannot
tell us whether employees would maintain their own, because employees cannot write here. If the numbers
come back weak, that result does not by itself rule out the version where employees can update their
own goals — it may be evidence for it.

---

## 13. Open questions

Every one of these is genuinely undecided. None has been filled in with a guess.

**About the goal itself**

1. **Is the working status set by a person, or worked out by the system?** This slice assumes a person
   sets it. Working it out automatically would fix the stale-status weakness — a computed status cannot
   go quietly out of date. But it needs a start date on the goal, which this slice does not have, and it
   only works when the goal carries a number to measure against, which is not in this slice. Until this
   is answered, the assumption stays "set by a person."
2. **What working status does a goal have the moment it becomes Active?** Not specified. Whether it
   starts as On Track, or has no status until someone sets one, is undecided.
3. **Who moves a goal from Draft to Active?** Not specified — creator only, owner only, or either.
4. **Can the owner see a Draft goal their manager created about them?** Not specified. This decides
   whether Draft is a private workspace or just an early phase.
5. **Can a Closed goal be reopened?** Not specified.
6. **Can a progress log entry be edited or deleted after it is written?** Not specified.
7. **Can a goal's owner be changed after creation?** Not specified.
8. **Can a goal be given a due date in the past?** Not specified.

**About who can do what**

9. **What can HR edit, close, or delete?** HR does not create individual goals. Whether HR can edit,
   close, or delete an individual goal inside its access scope — or only goals it created itself — was
   never decided. The table in Section 6 leaves it open rather than guessing.
9a. **Should an HR administrator or a site administrator be able to create a goal for anyone, including
    themselves?** In this slice they cannot. Only a person's direct manager creates a goal for them, and
    nobody creates a goal for themself. Whether that is right has not been decided.
    *What saying yes would buy:* it closes the gap where a person with no Reports-To — an owner, a CEO,
    a president — cannot have a goal at all, without changing how Reports-To works. It also gives a
    company a way to set goals when a manager has left, is on leave, or has no administrator account.
    *What saying yes would cost:* it widens who can write to someone else's goal beyond the person
    accountable for their work, and it means someone can set and grade their own goal with nobody else
    involved. It also cuts across the platform convention that stops an administrator acting on their
    own employee record. This is a real trade-off, not a free fix.
    *If the answer is yes, these follow and are not answered here:* whether it applies to a site
    administrator only or to any administrator with the right permission; whether it covers editing,
    progress updates, and closing as well as creating; and whether a goal created this way is treated
    any differently from one a manager created.
10. **When employees can create and update their own goals in a later slice, is that always on, or
    something a company turns on and off?** Not decided. It does not affect this slice, where nobody
    writes to their own goal.
10a. **Is it a reasonable approach that a person with no Reports-To cannot have a goal at all?**
    In this slice only a direct manager creates or edits a goal, and nobody creates a goal for themself.
    Put together, that means a person with an empty Reports-To field — an owner, a CEO, a president —
    cannot have a goal in Payworks at all. This is a knowing trade-off, not an oversight, but it has not
    been confirmed as acceptable. **It needs an explicit answer before build.** It also rules those
    people out of any pilot, which matters if the pilot is at a small company where the owner expected
    to take part. One way to close this gap is question 9a above; it is not the only way.
11. **Which screen does Goals live on, and how is access to it granted to a limited-access
    administrator?** Not confirmed. Flag for the security expert.
11a. **Does the platform's self-access guard cover Goals?** When one person holds both an employee
    account and an administrator account, the platform is meant to stop them acting on their own record
    as an administrator. Whether that guard reaches Goals has not been confirmed. In this slice nobody
    writes to their own goal anyway, so the guard and the rule point the same way — but that stops being
    true the moment employees can update their own goals, so it needs confirming before that slice.
    Flag for the security expert.

**Bigger questions this slice sits inside**

12. **Is the existing platform access model the right foundation for Performance Management at all?**
    This is a live question shared with the Reviews area, not a Goals-only one. Goals uses the existing
    model today. If Performance moves to a different access model, Goals and Reviews move together, and
    a meaningful part of this slice would need reworking. This is a real rework risk, not a formality.
13. **What happens to a goal while its owner's manager link is broken?** The access side is settled —
    a broken link grants nothing. What is not settled is whether anyone can act on the goal in the
    meantime, or whether it sits untouched until HR fixes the reporting link.
14. **Does anything notify or remind anyone about a goal?** Nobody has decided whether Goals sends
    anything at all. Given that the slice depends on people coming back to update their goals, this is
    closer to a core question than a side one.
15. **Does the accessibility work land in this slice or a later one?** Needs an explicit call.

**A gap in what we know, not a decision anyone made**

16. **Most of what we learned about structured goal tracking came from larger companies.** Smaller
    companies described wanting the same thing but doing it informally — a spreadsheet, a conversation.
    This slice builds the structured version for everyone. We do not actually know whether smaller
    companies want it. This sits underneath everything above, which is exactly why it is the assumption
    this slice is built to test.

---

## 14. Not in this slice — and what comes after

This slice is deliberately narrow. Everything below is real and wanted; it is sequenced, not dropped.

### Why these come later

Each one either needs a working goal record to exist first, or is blocked on a decision nobody has
made yet. Building any of them before the core record is proven means building on an unproven
foundation.

### The order

**Next — Slice 2: the employee can write to their own goals**
The employee can create a goal for themself, add progress notes to their own goals, and change their own
working status. This is what turns a goal from a record kept *about* someone into a record kept *with*
them.
*Why it comes after:* it is the single biggest change to who can do what, and separating it means the
first slice gives a clean answer to one question — whether a structured goal record gets kept current at
all — before a second variable is added.
*What it needs decided first:* whether employee self-creation is on for everyone or something a company
switches on and off; whether an employee's own update can contradict or override their manager's; and
whether the platform's self-access guard blocks a person from writing to their own goal record. That
last one is a build blocker, not a detail.
*Known cost of leaving it out of Slice 1:* an employee has no way to answer a goal set for them or a
progress note written about them, the whole recording load sits on the manager, and anyone without a
Reports-To cannot have a goal at all.

**Then — Slice 3: a measurable target and progress toward it**
Adds an optional number to a goal — a dollar amount, a percentage, a plain count, a done/not-done, or a
set of milestones — plus a target value and a current value, so progress can be shown as its own thing,
separate from the On Track / At Risk status.
*Why it comes after:* a goal record has to exist and be kept current first. This is also the piece most
tangled up with the open question about whether the status is set by a person or worked out by the
system — answering that question is easier once real goals exist.
*Evidence note:* no client asked for this specifically, but every one of the three products closest to
Payworks has it. It is one of the few places where the closest competitors all build **more** structure,
not less.

**Then — Slice 4: a manager sees goal progress across their team**
One view showing where every person a manager is responsible for stands, instead of opening one record
at a time.
*Why it comes after:* there is nothing to roll up until goals exist and are being kept current. This
slice is also where the last-updated date earns its keep — it is what a "not updated recently" signal
would be built from. How stale counts as stale is a per-company setting, not a fixed number Goals
decides.

**Then — Slice 5: company-level goals**
HR publishes goals for the whole company that individual goals can point at.
*Why it comes after:* it is the simpler half of cascading and it does not depend on the org chart being
correct, so it is the safer of the two to build first.

**Then — Slice 6: cascading between people's goals**
A goal links to a goal one level up, so a bigger goal splits into smaller ones below it, and an
employee can see which larger goal their own work supports.
*Why it comes after:* this is the hardest thing in the whole Goals area to get right, because linking
goals together is how a goal ends up visible to someone who should not see it. It needs real data and
serious testing before launch. It also has two unanswered questions in front of it: how many levels
deep a cascade may go, and what happens to a link when someone changes teams.
*Also open:* the current thinking is that a manager creates the link, not the employee. That is our own
call, not something clients or competitors confirmed.

**Then — Slice 7: goals inside a review**
A review form pulls in an employee's goals as real content, not just something shown off to the side.
*Why it comes after — and what blocks it:* how goals get matched to a review is genuinely undecided.
Two real approaches exist: match goals whose dates fall inside the review's period, or take whatever
exists at the moment the review is created. Both are used in the market. Building either without
deciding on purpose means reviews can silently include or exclude the wrong goals. **This cannot be
estimated until that is decided.**
*Note on direction:* goals feed into a review. A review does not create a new goal on the way out. That
is settled and is not planned to change.

**Later — goals that differ by role**
A goal attached to a person's role rather than to them individually.
*Blocked on:* the platform does not currently mark which of a person's positions is their main one, and
assigning a role-based goal to the right people needs that first.

**Later — goal templates and template versions**
Company-defined structure for what a goal must contain, and keeping old goals tied to the template they
were created under when that template later changes.
*Evidence note:* this came from internal sales conversations. No client interview asked for it, and no
competitor was confirmed to do it.

**Later — reporting on a company's own year**
Grouping and reporting goals by whatever cycle a company runs on, including a fiscal year that does not
match the calendar year. Expected to be a company-level setting and to group by due date, rather than a
new field on every goal.

### Deliberately out, with the reason

- **A full development-plan object** attached to an At-Risk goal, with its own owner, due date, and
  status. Only one company described wanting this. A goal already carries a progress note, which covers
  the lighter version of the same need. This is the most likely item to be promoted later if more
  companies ask for it.
- **A step where the employee formally acknowledges a goal.** No client asked for it in either
  direction, and no competitor checked has it. A goal already shows engagement through its status and
  its progress log.
- **AI-written goal suggestions and progress summaries.** This needs a working goal object holding real
  data first. Sequencing, not a rejection.
- **A link to the training and certification module.** A real ask, but a separate integration project
  rather than part of the goal itself.
- **An employee who reports to more than one manager.** Out of scope everywhere in Performance
  Management, because the platform records only one manager per employee today. If that ever changes,
  Goals, Check-ins, and Reviews all need to revisit it together.
