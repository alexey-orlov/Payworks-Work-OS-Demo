# Performance Management Role Based Security --- titles and permissions

**Author:** Sonia Marsh

**Date:** 2026-07-24

**What this is:** a **conceptual model** of the **permission packages** for **Performance Management** **("Performance" for short below)** --- a proposed set of ready-made packages and exactly **what each can do** across every Performance area (reviews, goals, competencies, feedback and notes, pay increase, calibration, configuration). A permission package works **like security works today --- but HR hands out a bundle of permissions instead of one at a time.** HR **assigns a package to a person manually** (independent of their position), and a person can hold **more than one**. It's a **starting point for the separate role-based-security review**, to be mapped into design later. Names are **placeholders/TBD**.

**Companion** to RBS Intersection Map-2026-07-24 and RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24

**Scope note (important):** this is a **conceptual model for Performance Management only**, with **placeholder names**. It works the **same way security works today** (a person is granted access), except a **package** of permissions is assigned instead of one permission at a time. A package is **assigned to a person manually --- at the point HR chooses that person's role** --- and is **independent of position**; connecting packages to positions automatically is a **maybe-later**, not required. Because the **role is free-form** (HR-defined), this maps cleanly: HR just picks the role and assigns a package.

**Terminology (first use):** **Permission package** (also called a *title* here) = a named bundle of Performance permissions --- what **the holder** can do.

**Scope** = which employees **the holder** can act on.

**Recall** = pull back a submitted item.

**Audit trail** = a recorded history of who did what.

**ESS** = employee self-service.

**Calibration** = a session where ratings are compared and adjusted for fairness.

**Comp-ratio** = an employee's pay compared to the midpoint of a pay range.

## How assignment works --- read first

Read top to bottom: HR picks the person's free-form role and, in the same step, assigns one or more permission packages. The Reviewer access is **derived from the reporting line**; the more **elevated** packages are **hand-assigned**. A person can hold several, and the permissions **add up** --- held in check by three guards (self-access, mutually-exclusive pairs, pay-explicit). What a person ends up able to do is the **package** ("what") combined with **scope** ("whose"). The **Site-Admin ceiling** sits over the whole model, and how it and a package resolve when they disagree is the open question.

*Elevated packages are **HR, Approver, Calibration Facilitator, and Legal** --- the docs' "more powerful packages," hand-assigned because they carry configuration, pay-approval, calibration, or sensitive-record access. **Exclusive packages** is an *optional* control --- HR can mark two packages one person can’t hold at once (e.g., the Culture Amp HRBP vs Performance Administrator pair); it is **not** how pay separation of duties works (packages are additive, so a manager who shouldn’t approve pay is simply not given the Approver package, and pay routes to a second-level approver). The Reviewer, by contrast, is derived from the reporting line.*

### The high-level requirements

1. **Packages are ready-made and reusable.** The model ships a set (Individual Contributor, Reviewer, Manager, Approver, HR/Performance Admin, Legal, Calibration Facilitator, Performance Viewer). A client can rename them, toggle individual permissions to build a custom package, or clone one as a starting point.
2. **A package is assigned to a *person*, manually, at the moment HR picks that person's free-form role.** Picking the role and assigning the package happen in the same step, but the package is a **separate choice** --- never derived from the role or the position. A job role grants nothing on its own.
3. **A Role Profile can carry a default package** as a convenience --- a suggestion HR can override, not an automatic derivation. Whether a bundle attaches to the role itself, rather than being assigned to the person, is an open question for the security review; connecting packages to positions automatically is a maybe-later.
4. **Derive the Reviewer from the reporting line as clients scale; reserve manual assignment for the elevated packages.** v1 can assign packages manually, but as headcount and turnover grow, hand-set permissions fall behind reality --- so derive the reviewer from the reporting line (matching what Reports-To already does) and keep manual assignment for the elevated packages --- the docs’ "more powerful packages": HR, Approver, Calibration Facilitator, Legal.
5. **A person can hold more than one package; permissions add up** (union --- most access wins).
6. **The self-access guard overrides the union.** No one can act on their *own* record through an admin package (recommend or approve their own pay, change their own review). The normal employee view of one's own record is unaffected.
7. **HR can optionally mark package pairs as mutually exclusive** (the Culture Amp "HRBP vs Performance Administrator" pattern). This is **not** how pay separation of duties is handled: because packages are **additive**, a manager who shouldn’t approve pay simply isn’t given the Approver package, and a pay recommendation routes to a **separate approver** (the second-level approval flow). **Manager + Approver is not a hard exclusive pair.** Note this makes pay separation of duties an **operational** control --- HR must not grant Approver to a line manager, and a pay recommendation must route to a **separate** approver --- **not a hard system guard**: the model does not, by itself, stop someone who holds both packages from approving a pay increase they recommended.
8. **Pay and other sensitive data need their own explicit switch inside a package --- never on by default.** Private notes stay author-only; no package sees another person's private notes.
9. **"What" and "whose" stay separate.** The package sets *what* the holder can do; *which* employees they can act on --- the **home** it applies to --- follows how security scopes people today (**security level, pay group, department, and group**) and is the security review's to confirm. A **group** can be arbitrary: a set of people who are neither a department nor a reporting line (e.g., a project team whose expenses one person approves). A role applies to a group of individuals, whatever that group is. Reports-To still decides who a reviewer is assigned to in a cycle.
10. **The Site-Admin ceiling still exists** above all of this. Which overrules the other when they disagree is open --- likely one-way (a package can *tighten* access below the ceiling but may not fully *override* platform reach). A private note is the test case.

Walking this flow surfaces the open questions listed in Section 7; the Site-Admin ceiling is in Section 5.

## 1. How the model works (the one-paragraph version)

A **permission package** (e.g., Reviewer, Approver) is a named bundle of Performance permissions --- what a person is allowed to do in reviews, goals, competencies, feedback, pay, and calibration. It works **exactly like security works today**, with one change: instead of switching permissions on one at a time, HR hands someone a ready-made **package**. Example: build a "Team Lead" package once, then **assign that package to a person manually**.

**HR assigns the package when it chooses the person's role.** Picking the (free-form) role and giving the person a package happen in the same step, but the package is a **separate, manual choice** --- it is **not** derived from the role or the position. Because the role is free-form, this maps cleanly: no rigid position→role→security lookup is needed. A person can hold **more than one** package, and the permissions add up. They still **can't act on their own record** (the self-access guard) --- so someone who reviews their reports can't change their own review.

Two things stay separate:

-   **The package = what the holder can do** (write a review, set a goal, recall a submitted review).

-   **The *whose* --- which employees (the *home* a package applies to)** --- follows how security scopes people today: **security level, pay group, department, and group** (a **group** can be arbitrary --- e.g., a project team that is neither a department nor a reporting line); the exact scoping is for the security review. *(Reports-to still decides who a reviewer is assigned to in a cycle --- that's separate from the package.)*

> **How this squares with everything.** The rule "a role never grants access on its own" **still holds** --- access comes from the **package a person is assigned**, not the job role. A package is **independent of position** (it can be assigned to anyone). It works like today's security, just bundled. The existing **Site-Admin ceiling still exists**, and *which overrules which* is an open question for the Role Based Security review (Section 5). Names are **placeholders/TBD**.

## 2. The ready-made titles (summary)

| Title                       | One-line purpose                                                                                                                                                                                                             | Typical real-world holder                                                                                                                                                                                                          |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Individual Contributor**  | See and act on **the holder's own** performance only                                                                                                                                                                        | Every employee                                                                                                                                                                                                                     |
| **Reviewer**                | **Write** the reviews **the holder is** assigned; nothing wider                                                                                                                                                              | Anyone **formally assigned to write someone's review** --- usually a manager, sometimes a non-manager assigned as a reviewer *(casual peer feedback in a cycle is covered by the Individual Contributor package, not this one)* |
| **Manager**                 | Everything a Reviewer does **+ manage their team's** goals, notes, and review status; **recommend** pay                                                                                                                      | A manager with direct reports                                                                                                                                                                                                      |
| **Approver**                | Approve or send back pay-increase recommendations --- the case the approval step exists for; an org may also route goals for sign-off if it configures that (a completed review itself is shared/acknowledged, not approved) | A director/leader who signs off (pay approval is the sensitive case)                                                                                                                                                               |
| **HR (Performance Admin)**  | **Configure and run** cycles, templates, roles, reporting --- the whole Performance module                                                                                                                                   | HR / the admin who runs Performance                                                                                                                                                                                                |
| **Legal**                   | **Read** reviews, history, and **audit trails** for compliance/disputes (**not private notes** --- those stay author-only); place a **hold** that blocks deletion                                                            | Legal / compliance                                                                                                                                                                                                                 |
| **Calibration Facilitator** | **Compare and adjust ratings** across a group in calibration                                                                                                                                                                 | HR or senior leader running calibration                                                                                                                                                                                            |
| **Performance Viewer**      | **Read-only** across the area within scope                                                                                                                                                                                   | Auditor, observer                                                                                                                                                                                                                  |

Clients can **rename** any of these and **build custom**

## 3. Detailed permissions by title

Each title below is a permission package **(see Section 1)** and lists what it **can do** across the Performance areas. Anything not listed, it **cannot** do. All actions are still limited by **scope** (which employees). Actions use a common set of verbs: **read, write, review, approve, recall** (pull back a submitted item), and **delete with an audit trail**. Two hard rules apply to **every** package, including admins:

-   **Private notes are author-only, forever.** A **private note** is a note visible only to the person who wrote it --- no package lets anyone see someone else's private note (not even an HR/admin role or a Site Admin).

-   Only **shared feedback** is visible more widely --- how widely depends on how it's shared. The **sharing tiers are defined in the Feedback & Performance Notes area brief** (that model is still being settled there).

-   **No one can act on their own record as a reviewer/approver** (the self-access guard) --- no one can review, calibrate, or approve pay for themselves.

### 3.1 Individual Contributor

-   **Goals:** create/edit **own** the goals they **set themselves**; **view and update progress** on all their goals --- including a goal a **manager set for them** --- but **not edit a manager-set goal's definition** (that stays with the manager who set it).
-   **Reviews:** view **own** completed review (only if HR turns on the ESS view); acknowledge / sign own review. (If ESS isn't on, the employee isn't locked out --- the completed review is a stored, printable record the manager or HR can share as a print/PDF outside the app; ESS-off just means no self-service.)
-   **Self-assessment:** write and submit their **own self-assessment** when a cycle includes one (HR sets the cycle to manager-only, self-only, or both). Once submitted, the employee can **view** it but **not edit or recall** it --- reopening is an HR/cycle action, not a self-service one.
-   **Competencies:** view **own** competency results (same ESS toggle).
-   **Feedback & notes:** capture **own private notes**; give shared feedback **only if** a cycle invites it (e.g., peer input); see shared feedback addressed to them per those sharing tiers (see the Feedback & Performance Notes area brief).
-   **Role Profile:** view **own** role, read-only --- only if HR turns on the **role-visibility toggle**, which is a **separate** control from the per-cycle review-share setting (assumed client-wide; an IC sees it via ESS since they have no admin access).
-   **Everything else:** no.

### 3.2 Reviewer

-   **Reviews:** **write and complete** the reviews they are **assigned**; **score competencies** inside those reviews; submit.
-   **Feedback & notes:** capture **private notes** on the people they review; add **shared feedback** where the cycle allows.
-   **Goals:** view the goals of the people they review (read-only), so the review is written against real goals; **no** set/edit/cascade --- those are Manager actions.
-   **Recall:** pull back **their own submitted** review before it's locked, with the change recorded.
-   **Viewing:** see only the reviews they are assigned; **not** the whole team or the org.
-   **Pay / calibration / config / delete:** no.
-   *Maps to* two Reports-To ideas:

(1) the **default reviewer** --- Reports-To makes the manager the reviewer automatically; and
(2) the **"scoped review-only access" fast-follow** --- narrow, temporary access so a reviewer can write a review for someone they don't otherwise have access to.

> The Reports-To definition treats the **Reviewer package (**what the person can do (write the review)) **and that fast-follow as the same capability, to be built once** --- *provided the Reviewer package itself grants the review-only access* (open in that definition; if it instead assumes prior access, scoped access stays a separate build).

### 3.3 Manager

-   Everything **Reviewer** can do, plus, **for their own team (direct reports within scope):**

-   **Goals:** set / edit / **cascade** goals to reports; view reports' goals and progress.

-   **Reviews:** view their reports' reviews (current and past, within scope); track who's done and who's overdue.

-   **Feedback & notes:** capture private notes on reports; give and see shared feedback per those sharing tiers (see the Feedback & Performance Notes area brief).

-   **Pay increase:** **recommend** an increase for a report (recommend only --- not approve).

-   **Dashboards:** see their **team status** (whose reviews/goals are done or overdue, and whether each active goal is On Track, At Risk, or Overdue if past its due date).

-   **Config / calibration / approve-pay:** no.

-   *Maps to* the market's standard **Manager** role --- the team-manager permissions. Typically held by someone who has direct reports (the "leader" idea) but **assigned manually by HR like any package** --- having direct reports does not auto-grant it, and the Reports-To leader/IC signal itself only drives template selection, not this access.

### 3.4 Approver

-   **Approve or send back:** **approve pay-increase recommendations --- the required approval case ---** or **send them back** (a recall) for changes, with the change recorded. An org **may also** route **goals** for sign-off if it configures an approval step. **A review itself does not require approval** --- a completed review is **shared and acknowledged**, not approved (approval exists for the pay recommendation, not the review write up).
-   **Pay (the sensitive case):** **view** ratings alongside **comp-ratio** (pay vs range midpoint) and the manager's recommendation; **approve or deny** pay recommendations --- especially **deviations** from the recommended range; **export** the comp view; where supported, push approved increases to payroll **in a batch** (all at once, rather than one at a time). *(Pay approval is a sensitive subset --- see the hard rule in Section 5 that pay needs its own explicit permission, never on by default)*
-   **Reviews / competencies:** view (read-only) what justifies the decision, within scope.
-   **Write reviews / set goals / configure / delete:** no.
-   *Maps to:* how companies sign off on pay today --- checking increase figures by hand in a spreadsheet, a director working out each person's merit (performance-based) increase, and a **rating-plus-pay-band grid** that suggests an increase while **anything outside it needs extra approval** (a 'decision matrix'). This package is where **pay-increase approval** (M3) and any later **compensation features** land.

### 3.5 HR (Performance Admin)

The broad package for whoever runs the Performance module.

-   **Cycles:** create / configure / **launch** / close / reopen review cycles; manage **templates**.

-   **Reviewer assignment:** set the default reviewer source (Reports-To), **override/reassign**, **exclude**, resolve **held** employees.

-   **Packages:** **assign** packages to people (and set which package a job/Role Profile comes with by default) --- the point where a person gets their Performance permissions.

-   **Goals / competencies:** configure the goal framework and the competency framework; view across the org (within scope).

-   **Reporting:** view org-wide **completion/tracking**; run and **export** reports.

-   **Delete:** HR **cannot** delete completed reviews (a permanent record) or roles (a role is **deactivated**, not deleted). Deleting a completed review is a **Site-Admin** action only, for a **legal/privacy obligation**, always **with an audit trail** --- outside this package.

-   **Feedback:** manage the shared-feedback settings; **cannot** see anyone's **private** notes (hard rule).

-   **Pay:** may **view** comp reports for reporting, but **approving** pay is the **Approver** package unless HR also holds it.

-   *Maps to:* today's HR/admin person who runs Performance module today --- cycle setup, reviewer reassignment, role management, reporting/export).

### 3.6 Legal

-   **Read** reviews, review history, and **audit trails** for a defined population, for compliance or a dispute --- read-only *(Reviews are controlled-visibility records, not author-only content --- HR already sees them --- which is why a compliance read is possible; private notes and 1:1 private content are author-only and stay off-limits to Legal, see below.)*

-   **Hold:** place a **legal hold** on records that **blocks deletion** (even by HR) until the hold is lifted, with the hold recorded.
-   **Write / approve / configure:** no. **No** private notes.
-   *Placeholder --- confirm what Legal actually needs.* Included because Legal is one of the base packages in scope, the exact permissions are a question for the Role Based Security Review.

### 3.7 Calibration Facilitator

-   **Calibration:** run a calibration session for a defined group; **view the rating distribution** **(how ratings are spread across the group)**; **adjust ratings** within the session, with the change recorded.
-   **Reviews:** view the reviews **of the people in the calibration group** --- **view-only**, except that ratings can be **adjusted while a calibration session is running** (per the previous point).
-   **Competencies:** view competency scores for the group (to calibrate).
-   **Everything else:** no --- a facilitator is **not** a general editor; they can't write reviews, set goals, or approve pay unless they also hold those titles.
-   *Maps to:* the calibration need (senior leadership reviewing rating distribution; a calibration / comp-ratio report) and after the market's equivalent **Calibration Facilitator** role.

### 3.8 Performance Viewer (read-only)

-   **View-only** across reviews, goals, competencies, dashboards, and reports **within scope**. No writing, no config, no pay approval. **No** private notes.
-   *Maps to:* auditors, or senior leaders who observe but don't act ("manager-facing, not employee-facing" reporting; oversight roles).

## 4. Condensed capability grid

*Columns are the main Performance capabilities; rows are the packages. **✓** = yes (within scope); **own** = own record only; **rec** = recommend only;* ***self** = own self-assessment only; **---** = no. Private notes are author-only for everyone, so they aren't a grantable column. **Delete:** completed review history is a permanent record --- the only deletion is a Site-Admin action for a legal/privacy obligation (audit-trailed, outside these Performance packages); a role is **deactivated**, not deleted. **Later-milestone (VP3):** competency scoring and calibration are VP3 capabilities --- in the MVP competencies are descriptive text and there is no calibration, so those columns show the eventual package model, not MVP scope. **Recall (open):** whether Reviewer/Manager can **self-recall** a submitted item, or pulling one back is always an **HR reopen**, is unsettled --- see Section 7.*

| Package                 | Config cycles / templates | Assign reviewer / packages | Write review (**assigned / self** | View team reviews | View all reviews | Set/edit/cascade goals                | Score competencies | Recommend pay | Approve pay | Recall submitted | Delete (with audit) | Calibrate | Reports / export |
|-------------------------|---------------------------|----------------------------|-----------------------------------|-------------------|------------------|---------------------------------------|--------------------|---------------|-------------|------------------|---------------------|-----------|------------------|
| Individual Contributor  | ---                       | ---                        | self                              | ---               | ---              | own                                   | ---                | ---           | ---         | ---              | ---                 | ---       | ---              |
| Reviewer                | ---                       | ---                        | ✓                                 | ---               | ---              | view                                  | ✓                  | ---           | ---         | own              | ---                 | ---       | ---              |
| Manager                 | ---                       | ---                        | ✓                                 | ✓                 | ---              | ✓ (team)                              | ✓                  | rec           | ---         | team             | ---                 | ---       | team             |
| Approver                | ---                       | ---                        | ---                               | view              | ---              | sign-off (if configured) | view               | ---           | ✓           | send back        | ---                 | ---       | comp             |
| HR (Performance Admin)  | ✓                         | ✓                          | ---                               | ✓                 | ✓                | configure                             | configure          | ---           | ---         | ✓                | ---                 | ---       | ✓ / export       |
| Legal                   | ---                       | ---                        | ---                               | read              | read             | ---                                   | read               | ---           | ---         | ---              | hold (blocks)       | ---       | read             |
| Calibration Facilitator | ---                       | ---                        | ---                               | group             | ---              | ---                                   | view               | ---           | ---         | ---              | ---                 | ✓         | group            |
| Performance Viewer      | ---                       | ---                        | ---                               | ✓                 | ✓                | view                                  | view               | ---           | ---         | ---              | ---                 | ---       | view             |

*(A client can rename these and turn individual cells on/off to build custom packages. One person can hold more than one --- the permissions add up.)*

## 5. How this relates to the existing security access

This works **the same way security works today** --- a person is granted access --- except a **package** of permissions is assigned instead of one permission at a time. So it isn't a **separate, new access system added alongside the current one**: it's the same mechanism, bundled.

What that means here:

-   **A package is assigned to a person manually**, at the point HR chooses their (free-form) role, and is **independent of position**. Connecting packages to positions automatically is a **maybe-later**, not required.

-   **The *whose* --- which employees a person can act on (the *home* a package applies to) --- follows how security scopes people today**: security level, pay group, department, and **group** (a group can be arbitrary --- e.g., a project team that is neither a department nor a reporting line). The exact scoping is for the security review to confirm. *(Reports-to still decides who a reviewer is assigned to in a cycle; that is separate from the package.)*

-   **Two rules to keep:**

    -   A **private note stays author-only** (no package sees another person's private notes), and

    -   **pay and other sensitive data need their own explicit permission** inside a package --- never on by default.

**The open question**

-   **The Site-Admin ceiling.** Because this works like today's security, the **Site-Admin ceiling still exists**: a Site Admin can technically reach the platform. **Which overrules the other when they disagree** is the open question --- likely **not symmetric** (a package can *tighten* below the ceiling but may not fully *override* platform access).

    -   A **private note** (visible only to whoever wrote it) is the test case --- not even a Site Admin can read one. Flag it; the Role Based Security review settles it.

-   **Could this extend beyond Performance? (parked --- unvalidated.)** Today this is scoped to **Performance Management only** (see the scope note). An option the team raised is to build the permission model **on top of the existing platform security** so it reaches **beyond Performance** --- avoiding a rewrite of access for each area. This is **not validated** and is a **technical question to vet with the dev/security team**; nothing is decided. Noted so the model can be designed with the possibility in mind. **[expert/dev]**

-   **Groups as a home --- open questions.** Adding *group* as a home raises decisions the security review must settle: **who creates and maintains a group** (an arbitrary group is not a department, so someone owns its membership); whether a group's scope **combines with or restricts** a holder's other scope (**union vs intersection**); and whether a package can be scoped to a **group the holder is not a member of** (the expense-approver case implies yes); what applies when a **person is in more than one group** (union of their scopes?); and whether the **existing platform even supports arbitrary groups** today, or whether that is new build. **[team/expert]**

## 6. Coverage check --- areas addressed (with known gaps)

-   **Review cycles & writing:** HR configures/launches; Reviewer/Manager write; Individual Contributor views/acknowledges. ✓
-   **Reviewer assignment (reports-to):** HR overrides/reassigns; the **Reviewer package = the "scoped review access" build** --- do it once. ✓
-   **Goals:** Individual Contributor sets own; Manager sets/edits/cascades for reports; HR publishes company-level goals and configures. ✓
-   **Competencies:** HR configures the framework; Reviewer scores in a review; Calibration Facilitator adjusts; Individual Contributor views own. ✓
-   **Feedback & notes:** private notes author-only for all; shared feedback **per those sharing tiers** (see the Feedback & Performance Notes area brief).; Reviewer/Manager capture. ✓
-   **Pay increase / comp:** Manager recommends; Approver approves deviations and pushes to payroll; Viewer/HR can see comp reports where cleared. ✓
-   **Calibration:** Calibration Facilitator runs sessions and adjusts; senior leaders view distribution. ✓
-   **Compliance:** Legal reads records/audit trails and can place a hold that blocks deletion. ✓
-   **Dashboards / reporting:** Manager sees team; HR sees org-wide and exports. ✓
-   **Reports-to is separate:** reports-to decides who a *reviewer* is assigned to in a cycle; the **security package is assigned to the person independently** (manually, when HR picks the role). The package *assignment* is independent of reports-to --- but the Reviewer package's *scope* leans on it (the shared scoped-review-access build). ✓

**Known gaps (conceptual coverage is not the same as fully specified). The** RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24 surfaced gaps this model does not yet close --- carried into the open questions and break points below:

-   **Separation of duties for pay** --- a person holding **Manager + Approver** could recommend a report's pay *and* approve it (the self-access guard only blocks their *own* record).

-   **Package lifecycle** --- no rule yet for **termination, role change, or leave** (manual assignment implies manual removal → stale access).

-   **Delegation** --- the *reviewer* handoff for a manager on leave is handled by Reports-To's temporary leave override (a dated stand-in see Reports-To definition Section 11), but whether the manager's **permission package** can be temporarily **delegated** the same way isn't settled (see the open question below).

-   **Self-review vs the self-access guard** --- a self-assessment *is* acting on their own record; the two need reconciling.

-   **New hire with no package** --- if the default is "nothing," a new hire can't acknowledge their own review; whether Individual Contributor is auto-granted to everyone is unresolved.

## 7. Open questions for the role-based-security review

-   **When a person holds several packages, how do they combine?**
    -   The market norm is **union --- most access wins** (matches "add up"); keep that, but **hard-code a self-access guard that overrides the union** (no one can use an admin package as a back door to their *own* record --- the normal employee view of one's own record is unaffected), and let HR mark **role pairs as mutually exclusive** (as Culture Amp does with **Perform HRBP** vs **Performance Administrator**). **\[team\]**
-   **Separation of duties for pay** --- should the same person be blocked from both **recommending and approving** a given employee's pay increase?
    -   No performance-native tool in the RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24 appears to guarantee this (confirm in demos); as a payroll company it's a differentiator worth building (optional, client-configurable, with an audit-logged override). **\[team\] \[expert\]**
-   **Package lifecycle** --- what happens to a person's packages on **termination, role change, or leave**?
    -   Define removal/transfer so access doesn't go stale. **\[team\]**
-   **Delegation ---** the *reviewer* handoff for leave is already covered by the Reports-To temporary leave override; **can a manager on leave also temporarily delegate their Reviewer/Manager package?** (Ties to the Reports-To 'reassign to someone without access' fast-follow.) **\[team\]**
-   **Self-review vs the self-access guard** --- a self-assessment is acting on their own record; confirm how a self-review is allowed while the guard still blocks reviewing/approving oneself. **\[team\]**
-   **Default with no package** --- is **Individual Contributor** auto-granted to every employee (so they can acknowledge their own review), or must it be assigned? "Nothing by default" would block a new hire from their own review. **\[team\]**
-   **Run a cycle without reading results** --- add a cycle-admin permission separate from result visibility (Lattice / Culture Amp pattern), so **whoever runs a cycle** can do so without seeing sensitive content. **\[team\]**
-   **Where does a person's scope** (the *whose* --- which employees they can act on) **come from?** It follows how security scopes people today; confirm the exact scoping with the security expert. **\[expert\]**
-   **Connecting packages to positions (maybe-later):** should a package ever be suggested or derived from an employee's position/role, or always assigned by hand? Not required now. **\[team\]**
-   **What is the default** for a person with no package yet --- nothing until one is assigned? **\[team\]**
-   **What can Legal actually do** (read + hold is a placeholder) --- and does placing/lifting a hold need its own approval? **\[expert\]**
-   **How to prevent package sprawl** --- too many overlapping custom packages that can't be audited (the market's known failure)? **\[team\]**
-   **Recall window** --- how far back can a submitted item be recalled/reopened? *(Deletion is **not** open --- completed reviews are a permanent record; the only exception is a Site-Admin legal/privacy deletion, TBC with legal --- see Section 3.6 and the grid.)* **\[team\]**
-   **Recall vs. reopen (grounding).** The grid uses 'recall' (pull back a submitted item) for Reviewer/Manager/Approver, but the project has no 'recall' concept --- it defines an HR/cycle-triggered **reopen** and an **edit-after-submit** path. Confirm: can a reviewer/manager **self-recall** their own submitted review, or is pulling one back always an **HR reopen**? If HR-only, the Reviewer 'own' and Manager 'team' recall cells should change. **\[team\]**
-   **The Site-Admin ceiling (flag, don't solve):** this works like today's security, so a Site Admin can technically reach the platform. Which overrules the other when they disagree --- and does it work **only one way** (a package can make access **more restrictive** than the Site Admin's, but **can't fully override** the Site Admin's reach)? A **private note** (visible only to whoever wrote it) is the test case --- not even a Site Admin can read one. **\[expert\]**

## 8. Break points --- where devs get blindsided

-   **The "role never grants access" rule.** It still holds --- access comes from the **package**, not the job role. If a build wires access to the job role directly, that rule is silently broken. *Expensive-when-wrong.*
-   **Private notes leaking.** If a broad package (HR, or a custom "super" role) is built to "see everything," it must **still** be blocked from private notes. *Expensive-when-wrong (trust).*
-   **Scope confused with the package.** A package that accidentally widens *whose* (not just *what*) is a leak. Keep "what" (the package) and "whose" (reports-to + assignment) separate.
-   **Pay data over-exposed.** A custom package with comp permissions handed out too widely exposes salary/SIN --- pay needs its own explicit permission, never on by default.
-   **"Reviewer" built twice.** The Reviewer package and the Reports-To 'scoped review access' fast-follow are intended as the **same capability --- build once** --- *provided the Reviewer package itself grants the review-only access* (open in the Reports-To definition: if it instead assumes prior access, scoped access stays a separate build).
-   **Reaching into the existing model too early.** This is standalone for Performance; wiring it to the existing site-admin model now (for scope or for a Site-Admin override) pre-empts a decision that is deliberately deferred. Keep it separate until the later alignment.
-   **Manager + Approver self-approving pay.** If one person holds both, nothing stops them approving their own pay recommendation for a report --- **a gap in separation of duties** (the recommender of a pay increase shouldn't also be its approver). *Expensive-when-wrong (pay/compliance).*
-   **Calibration adjusting a rating after the employee has seen it.** Employee visibility ships (VP1-M4); if calibration adjusts a rating post-acknowledgement, the employee acknowledged a number that later changed. Sequence calibration before visibility.
-   **Legal hold vs. Site-Admin ceiling vs. privacy erasure.** A Legal hold blocks deletion "even by HR," a Site Admin may override the ceiling, and a privacy/erasure request may require deletion --- three rules that can collide. *Expensive-when-wrong (compliance).*
-   **Reopen after a downstream step (later milestones).** Pay approval is **M3** and calibration is **VP3**, so once those exist: if a completed review is **reopened** after its pay was approved or its rating was calibrated, does reopening **invalidate** those steps? Define the limit. *(Depends on the recall-vs-reopen question in Section 7.)*
-   **Manual assignment gets hard to keep accurate as a client grows.** As headcount and turnover rise, hand-set permissions fall behind reality (people change roles, are promoted, or leave, but nobody updates their access by hand); derive the reviewer from the reporting line and reserve manual assignment for the more powerful packages (HR, Approver, Calibration, Legal) (see the RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24). *(No specific headcount threshold is assumed --- that's a team call on real client data.)*

## 9. Handoff note

This is a **conceptual model to start the role-based-security review** --- Performance-only, with **placeholder names**. A permission package works **like today's security, just bundled**:

-   HR **assigns a package to a person manually**, at the point of choosing their (free-form) role, and it is **independent of position**. **One person can hold several** (permissions add up). The "a role never grants access on its own" rule holds --- access comes from the **package**.

-   **Connecting packages to positions** is a maybe-later; how the package model sits under the **Site-Admin ceiling** (*which overrules which*) is the flagged open question.

-   Keep three rules non-negotiable:

    -   **private notes are author-only**,

    -   **the package sets "what" while reports-to + assignment set "whose,"** and

    -   **pay/SIN data needs its own explicit permission --- never on by default**.

-   Treat the **Reviewer package** and the Reports-To **scoped-review-access** fast-follow as one build, and expect **reports-to logic to have to evolve** since scope leans on it. How this lines up with the broader admin access model (including anything like Site Admin) is a **later** step --- deliberately not solved in this document.
