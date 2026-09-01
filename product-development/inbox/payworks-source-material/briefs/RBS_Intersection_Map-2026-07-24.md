# Role-based security --- intersection map with Role Profiles and Reports-To

**Author:** Sonia Marsh

**Date:** 2026-07-24

**What this is:** a **mapping**, not a design. It identifies every place the new **role-based security** idea touches the **Role Profiles** work and the **Reports-To** work, so developers aren't blindsided. The full role-based-security design gets its **own comprehensive review** --- this doc just makes the connections (and the conflicts) explicit up front.

**Companion** to the Role Profiles and Reports-To definitions/briefs, RBS Titles and Permissions-2026-07-24 and RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24

**Terminology (first use):**

-   **Role-based security (RBS)** --- the new idea: named bundles of access (permissions) that a client can add to the roles they set up, plus some ready-made bundles (e.g., a "reviewer" bundle, name TBD) they can reuse --- like the way a site admin already gets access to everything.

-   **Permission bundle** --- a named set of "what you can do / see," which is what RBS attaches to a role. (Other tools call this a "permission role," "security group," or "access level.")

-   **Role Profile** --- the *performance* job role (competencies, leader/IC, level). Describes **what a job is**. It is **one criterion** a cycle's template rules match on --- it does **not** own a template.

-   **Reports-To (RT)** --- the field linking an employee to their manager. Describes **who manages whom**.

-   **ESS** --- employee self-service.

-   **NSA** --- Non-Site Admin (an admin account that isn't the top Site Admin).

## 1. Why this matters now (and one big caution)

Access control at Payworks is **fixed, engineering-owned, and already mid-migration to "a newer permission model."** Product and design don't decide how access works. So two things are true at once:

-   RBS as described (permission bundles added to roles, reusable generic bundles) **is very likely the same "newer permission model"** the security area is already moving to --- not a fresh invention. **This must be confirmed with the security expert before anyone builds on it.**

-   The map's job is **not** to design RBS. It's to point at every spot where the Role Profiles and Reports-To work would **touch** or **collide** with it, so the separate RBS review starts with the map already drawn.

**The headline:** both the Role Profiles definition and the Reports-To definition make the same promise --- **"a role (or a relationship) never grants access."** Role-based security **keeps** that promise: the role still grants nothing on its own --- it's the **permission bundle tied to the role** that grants access. What actually shifts (and the one thing still open) is in Section 5.

-   **The model.** Security is a **package** of permissions that works **like security works today --- just bundled** (instead of permission-by-permission). HR **assigns a package to a person manually**, at the point of choosing their (free-form) role, and it is **independent of position**; connecting packages to positions is a **maybe-later**, not required. **One person can hold several.**

-   **Reports-To is not impacted.**

-   Separately, the **whole Role Profile object is now Blocked**: not just how a required **primary role** is established, but whether the object is a **new build or a reuse of the existing HR/TM Positions model** --- while everything downstream (template selection with the role as **one criterion**, competencies, goals) still flows and can be prototyped. The **Site-Admin ceiling** still exists (*which overrules which* is the open question). See the RBS Titles and Permissions document for the full model.

## 2. The three things called "role" (read this first)

Most of the blindside risk comes from one word meaning three things. Keep them apart:

| Term                                                 | What it is                                                                                                                                                                 | Does it grant access today?                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| **Role Profile** (performance)                       | A user-defined job role: competencies, leader/IC, level (one criterion for template selection --- no template attached to the role)                                        | **No** --- the Role Profiles doc says a role never grants access |
| **Permission package** (the new role-based security) | A named bundle of permissions, **assigned to a person manually** (like today's security, bundled) --- independent of the job/position                                      | **Yes --- the package grants; the job role still doesn't**       |
| **"Reviewer"**                                       | Two different things: (a) the **person assigned to complete the review** (Reports-To defaults it); (b) a proposed **generic access bundle** ("reviewer" access, renamable) | \(a\) no; (b) yes                                                |

If a document, ticket, or conversation says "role" or "reviewer" without saying **which** of these it means, stop and pin it down. Most of the mappings below are really about lining these three up.

## 3. Competitive read --- how HR platforms do role-based access (market scan, 2026-07-24)

*Scanned three platforms across the size range from vendor docs (SAP, Workday, BambooHR), current at the scan date. Findings paraphrased.*

**The universal pattern --- and it matches the idea exactly:** a **permission bundle** = a named set of "what you can do/see," which clients get as **ready-made bundles** they can reuse or copy-and-tweak, plus **custom** ones they build. Scope ("**whose** data") is kept separate from the bundle ("**what** you can do").

-   **SAP SuccessFactors (enterprise) ---**
    -   **"Role-Based Permissions."** Clients create **permission roles** (bundles of permissions) and assign them to **permission groups** (sets of users, e.g., by department or job code) with a **target population** (whose data).
    -   Ships **standard roles** --- Employee, Manager (defined as "an employee that has direct reports"), Security Admin, Super Admin. Roles are reusable across departments.
    -   Caution from their own docs: too many overlapping roles create inconsistent access that's hard to audit.
-   **Workday (enterprise) --- security groups + policies.**
    -   **Role-based security groups** (e.g., HR Partner, Payroll Partner) are **assigned by position**, so access **transfers automatically** when someone new fills the position.
    -   **Domain / business-process policies** say what each group can view/modify.
    -   A built-in filter is how "a manager sees their direct reports" works --- the relationship sets a data filter *inside* the security model, not access on its own. Clients often **copy a delivered bundle and trim it** (e.g., make "Compensation Partner" from "HR Partner").
-   **BambooHR (small/mid) --- access levels.**
    -   A **hybrid**: four ready-made system roles (Account Owner, Full Admin, Manager, Employee) **plus**
    -   **fully custom Access Levels**. A custom level is field-level "view/edit" per data category, **scoped to a population** (All Employees, **Direct Reports**, Specific Employees). Notably, a **Performance permission can be added to a custom level** so a non-admin can run review cycles --- a real "reviewer-style" bundle.
    -   New levels **default to No Access** (fail-safe).

**What this shows:**

-   The idea (reusable generic bundles + client-built bundles, added to roles) is **the market norm** --- high confidence.

-   "**Has direct reports = Manager**" is a delivered role in this world too (SuccessFactors), and **role-by-position that transfers automatically** (Workday) is directly relevant to Payworks' position/occupation work.

-   A **"reviewer"/Performance access bundle already exists** in the market (BambooHR) --- so the RT "scoped review-only access" fast-follow (Section 7) is well-precedented.

-   **Scope stays separate from the bundle** --- the bundle is "what," a group or population is "whose." Payworks already owns the "whose" part (security level + pay group + department + the reporting relationship). RBS mostly adds the "what bundle" layer.

**Performance-native tools (Lattice, 15Five, Culture Amp, Leapsome, Betterworks)**

These are the closest analog to the proposed model, and they confirm the same two-part split (**what** = roles/permission checklists, **whose** = a scoped group). Three things stand out beyond the HR-platform read:

\(1\) they **derive the reviewer from the reporting line** and manually assign only the **more powerful admin and calibration roles** --- so pure manual per-person assignment is *not* how the market scales;

\(2\) when a person holds several roles the norm is **union / most-access-wins**, but several of them **override it with a self-access guard** --- you can't use an *admin* role as a back door to your own record (explicit in Leapsome and 15Five; Culture Amp bars an admin from calibrating themselves). This does **not** block the normal employee view of one's own record;

\(3\) **separation of duties for pay is not guaranteed by any tool in the scan** (confirm in demos) --- recommend-then-approve just walks up the reporting line and an admin can override. Culture Amp also enforces a **mutually-exclusive role pair** (**Perform HRBP** vs **Performance Administrator**). Full detail and recommendations in RBS Competitive Scan --- Performance Native and Canadian Small Business Tools-2026-07-24

**Confidence & gaps:**

-   High on the pattern (three independent vendors agree).

-   Medium on which exact shape fits Payworks (bundle-only vs bundle+group vs position-tied).

-   **Humi (Canadian small business)** has three fixed default roles (Admin/Manager/Employee) plus custom roles by cloning, weak scope separation (the Manager role's 'direct reports' scope is baked in), a notable over-granting default (Managers can edit their reports' compensation and banking data unless a custom role removes it), and multiple roles that the user **switches between** rather than combining.

-   Other Canadian small-business Platforms:

    -   **Rise People** --- default roles (Owner, Admin, Manager, Member/Employee); **Manager is auto-assigned to anyone with direct reports** (derived, not hand-set), and **add-on roles are customizable by toggling permissions**. Compensation visibility is a separate setting, and generating a compensation report requires an Admin/HR Manager/HR Coordinator role --- a light separation for pay. Same two-part idea as the mid-market performance tools scanned above (what a role can do, plus whose data), and closest to the proposed reporting-line-derived reviewer. --

    -   **Collage HR** --- a fixed **Super Admin** (all access, not editable) plus **custom roles** built from two permission types they name explicitly --- **Feature Permissions ("what you can do")** and **Employee Data Permissions ("whose data")**. That is the clearest real-world example of the exact what/whose split the proposed model uses, at the small-business end.

    -   **Knit** and **Nethris** --- both market role-based access ("access privileges tailored to their role"; admin-controlled feature access) and both have performance-review modules, but **no documentation was found** detailing their permission structure, scope model, or how multiple roles resolve --- do not assume.

-   **Takeaway:** the Canadian small-business segment uses the **same two-part model**, and Rise (reviewer derived from reporting line) and Collage (explicit what/whose split) both reinforce the proposed direction. Knit and Nethris would need trial/demo confirmation (their permission model wasn't documented) if the Canadian small-business market is a priority for benchmarking.

-   These are based on the vendors' own documentation at the time, not hands-on testing --- treat it as a useful but dated read, and confirm the specifics (trial accounts or demos) before betting design decisions on them.

## 4. What Payworks has today vs what RBS adds

**Today (from the security ground-truth):** access is **not** role-based. It's built per admin from four layers

-   **Module** (read/write) → **Screen** (None/Read/Write) → **Security Level 1--10** (see only at/below your level) → **Pay Group + Department** (which employees).

-   **Site Admin** = everything;

-   **NSA** = starts with nothing, granted piece by piece.

-   The reporting relationship drives *who a manager can see* only **through** those layers, never on its own.

**What the Performance model is:** a **standalone** set of permission bundles for Performance --- **not** a layer bolted onto the four-layer model above. It brings its own **"what"** (the permission bundle) and gets its **"whose"** from **reports-to + role assignment**. The four-layer model keeps running everything **outside** Performance; how the two eventually line up is a **later** step.

**The open structural question (for the RBS review):**

-   how does this standalone Performance model eventually line up with the broader admin access model

-   and does the existing security ever overrule it, or the other way round? This is deferred --- for the **security expert** to resolve in the later role-based-security review, not this map.

## 5. The rule --- and the one thing still open

Both docs commit to the same rule, and **it still holds**:

-   **Role Profiles:** a role assigned to someone **grants no access on its own**; access comes from the security system.

-   **Reports-To:** the reporting relationship **grants no access on its own**.

Role-based security fits **inside** that rule --- it doesn't break it: **a job role still grants nothing by itself; it's the permission package assigned to the person that grants access.** A package works **like today's security, just bundled**, and HR **assigns it to a person manually** --- at the point of choosing their (free-form) role, and **independent of position**. **A person can hold several** (permissions add up). *Whose* data follows how security scopes people today (exact scoping is for the role-based-security review). *(Reports-to still decides who a reviewer is assigned to in a cycle --- separate from the package.)*

**The one thing still open**

-   **the Site-Admin ceiling.** Performance security is standalone, but the existing **Site-Admin ceiling doesn't go away**: a Site Admin can technically reach the platform. So the two **touch at that ceiling**, and the real question is **which overrules the other when they disagree** --- likely **only one way** (a package can make access **more restrictive** than the Site Admin's, but may not fully **override** the Site Admin's reach). The sharp test case is a **private note** --- a note visible only to whoever wrote it, which stays private **even from a Site Admin**; it is one place Performance security would sit *above* the ceiling. This map **flags it, rather than solving it** ---the **role-based-security review** settles it.

## 6. Mapping --- Role Profiles ↔ RBS

| Touchpoint in the Role Profiles docs                                             | What it says today                                                                              | How RBS touches it                                                                                     | Decision the RBS review must make                                          | Blindside risk if ignored                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| "A role never grants access" (Role Profiles definition Section 13, access table) | A role on its own grants nothing                                                                | Still true --- the **bundle tied to the role** grants; the role alone doesn't (Section 5)              | State the rule precisely: the bundle grants access, the role alone doesn't | Devs build as if the role itself grants access, breaking the stated rule |
| Who can create/edit/publish a role (HR, Write on the Role Profiles screen)       | Set by the current screen permission                                                            | That very permission ("edit Role Profiles") is a possible **bundle** item                              | Is "manage Role Profiles" one of the packaged permissions?                 | Two systems (screen permission + bundle) both claim to gate role editing |
| Leader/IC flag on the role                                                       | A **grouping/criterion** signal (calibration; **one template criterion**)                       | RBS could use leader/IC to define a **permission group** (whose data / who gets a bundle)              | May leader/IC drive a security group?                                      | Leader/IC quietly becomes an access control, not just a grouping label   |
| Attaching things to a role                                                       | **No template attaches to the role** --- the role is **one criterion** a cycle's rules match on | RBS packages are **assigned to the person;** whether a bundle could instead attach to the role is open | Does a permission bundle attach to the role or the person?                 | If a bundle attaches to the role, it needs its own care                  |
| Occupation / position direction                                                  | Role/position is user-defined                                                                   | Market ties the security **role to the position** (Workday), transferring automatically                | Should a bundle attach to position/occupation?                             | Position work and RBS designed in isolation, then collide                |
| Own-role visibility via ESS toggle                                               | An ESS setting, not a permission bundle                                                         | RBS may express ESS access as a bundle too                                                             | Does the ESS "see your own role" path become a bundle?                     | Two ways to control the same self-view                                   |

## 7. Mapping --- Reports-To ↔ RBS

| Touchpoint in the Reports-To docs                                                                | What it says today                                                                       | How RBS touches it                                                                                                                | Decision the RBS review must make                                           | Blindside risk if ignored                                                                                          |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| "A relationship never grants access" (Reports-To definition Section 12)                          | RT decides *who a manager sees* only through the security model                          | **No change** --- packages are assigned to people manually, not derived from RT; RT still grants nothing on its own               | Confirm RT is genuinely untouched                                           | Someone wires a package to RT and the relationship starts granting access                                          |
| **Scoped just-in-time review-only access** (fast-follow, Reports-To definition Section 12/RT-13) | Grant a reviewer temporary review-only access to one employee                            | This **is a permission bundle** --- a "reviewer" bundle with a target population                                                  | Should the RT fast-follow be *delivered by* RBS's "reviewer" bundle?        | The same capability gets built twice, two different ways                                                           |
| "**Reviewer**" as the person assigned to complete the review (RT default reviewer)               | A per-review assignment                                                                  | RBS proposes "**reviewer**" as a **generic access bundle** (renamable)                                                            | Keep the two "reviewer" meanings clearly named apart                        | Devs mix up the person assigned to complete the review with the access bundle --- wrong access or wrong assignment |
| Admin-as-Reports-To / non-employee manager (Reports-To definition Section 10)                    | A non-employee admin can be a valid manager                                              | Market grants non-employees access via a **custom bundle** (BambooHR benefits-broker pattern)                                     | Does admin-as-RT get a scoped bundle instead of being handled case-by-case? | Non-employee access handled two ways, inconsistently                                                               |
| Reviewer override to "anyone with access" (Reports-To definition Section 8)                      | Eligible set = who already has access under the current model                            | RBS redefines "has access" as "holds the right bundle"                                                                            | Does "eligible reviewer" mean "holds the reviewer bundle"?                  | The override's eligible-set logic breaks when access moves to bundles                                              |
| Leader/IC derived from RT                                                                        | One criterion a cycle's template rules match on (and a grouping signal for calibration) | Packages are assigned by hand, not auto-granted from leader/IC --- so leader/IC stays a **grouping** signal, not an access driver | Keep leader/IC out of access unless explicitly decided later                | Reporting data quietly becomes an access driver                                                                    |

## 8. Naming collisions to settle before build

-   **"Role"** --- Role Profile vs Permission bundle. Recommend never using bare "role" in RBS work; say "Role Profile" or "permission bundle."
-   **"Reviewer"** --- the **person assigned to complete the review** vs the access bundle. Recommend keeping "reviewer" for that person and naming the bundle differently (e.g., "review access"), even though the bundle name is client-changeable.
-   **"Manager"** --- the employee's manager (Reports-To), a manager-level admin, and the market's delivered "Manager" role (has direct reports). Keep the sense explicit.

## 9. Open questions for the separate RBS review

-   Is RBS the in-flight "newer permission model," or a layer on the current four-layer model? Everything depends on this. \[expert\]
-   When role-based security and the existing security setup both apply inside Performance, which one decides --- can one overrule the other, or must both agree? (Section 5) \[expert\] \[team\]
-   Should the reporting relationship or leader/IC decide who belongs to a bundle group (the way "a manager sees their direct reports" works), and if so, is that still fine given the relationship itself never grants access? \[expert\]
-   Is the RT "scoped review-only access" fast-follow the same thing as the RBS "reviewer" bundle --- build once? \[team\]
-   Clearing a held employee with a package: once packages exist, can HR clear a held employee by assigning a reviewer package directly, instead of the scoped-access fast-follow? The hold must still need a deliberate assignment (no auto-pick), but the mechanism to clear it may change. \[team\] \[expert\]
-   Does the permission live *inside* the role, or is it a separate bundle the role *points to* (so one bundle can be reused across many roles)? Could it also attach to the position/occupation? \[expert\] \[team\]
-   What ready-made bundles ship (reviewer, manager, HR, read-only...), and are they client-renamable like the market's standard roles? \[team\]
-   How to avoid the market's known failure --- too many overlapping bundles that can't be audited? \[team\]
-   **Whether the Reports-To / position work is linked to role-based security is not settled.** This mapping assumes a link (a package is assigned when HR picks a role); confirm that link is intended. **\[team\]**

## 10. Break points --- where devs get blindsided if this isn't mapped

-   **A stated rule silently reverses.** The Role Profiles and Reports-To definitions both state that a role/relationship never grants access. If RBS is built as if the role itself grants access (see the rule in Section 5), the rule is quietly broken in production. *Expensive-when-wrong.*
-   **The same capability built twice.** The RT "scoped review-only access" fast-follow and the RBS "reviewer" bundle are the same need; *if the reviewer bundle grants the access* (open in the Reports-To definition) --- built separately, they'll diverge

-   **Attaching to a role:** The role is a **one criterion** for template selection, with no template-link field --- nothing attaches a template to the role. The open question is whether an RBS **permission bundle** attaches to the role or to the **person** --- for the security review.

-   **Reporting data becomes access.** If leader/IC or Reports-To starts driving a permission group, the reporting relationship becomes an access control --- a real change no one may have decided.
-   **Name confusion in code and config.** "Role" and "reviewer" meaning different things across teams leads to wrong wiring.
-   **Building on an unconfirmed model.** If RBS is the in-flight permission migration and the design assumes today's four-layer model (or vice-versa), the work targets the wrong foundation. **→ confirm with the security expert first.**

## 11. Handoff note

This is a **map, not a decision**. The single most important thing before any RBS build:

-   **confirm with the security expert whether RBS is the in-flight "newer permission model,"** and

-   **settle the Site-Admin ceiling question** (which overrules which).

-   The "never grants access" rule stands --- access lives in the **package** assigned to the person, not the job role. Packages work **like today's security, just bundled**, are **assigned manually**, and are **independent of position**;

-   **Reports-To is not impacted**. The **Blocked** item is the **whole Role Profile object** --- how a required **primary role** is established, and whether the object is **new or reuses HR/TM Positions** --- while downstream (template selection via the role as **one criterion**, competencies, goals) still flows. Until then, keep the three "roles" (Section 2) and the two "reviewers" (Section 8) strictly named apart, and treat the RT "scoped review-only access" fast-follow and the RBS "reviewer" bundle as **one** capability to design together.

-   Everything here points at the existing access model and the Role Profiles and Reports-To definitions rather than inventing new access behaviour --- new access needs go to the security expert, not into these requirements.
