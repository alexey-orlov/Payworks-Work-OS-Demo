---
updated: 2026-08-31
slug: dayforce
tier: indirect
last-deep-analysis: 2026-08-31
analysis-goal: "how does Dayforce handle approval workflows — expense claims and payroll runs? feeds the expense VP2 approval-workflow scope call and the proposed $5k / >150-employee threshold"
analysis-scope: [expense-management, payroll]
competes-areas: [payroll, human-resources, time-management, absence-management, employee-self-service]
competes-features: [pay-groups, payroll-run, roe-and-year-end, online-timesheets, time-off-requests, mobile-self-service]
initiatives: [expense-management-vp2]
---

# Dayforce (formerly Ceridian) — Teardown

Scoped run: **approval workflows**, across expense claims and the payroll run. Not a company baseline — see *What this run did not cover*.

> **Reuse note.** Approval-workflow findings live here once, for both modules. The mechanics below (chain construction, delegation, mobile, the payroll-run gate) are written to be read from a payroll framing as readily as an expense one; a payroll question does not need a second teardown. Whole-product comparison sits in [competitive-matrix.md](../../competitive-matrix.md), which carries the shared *Approval workflows* table for both areas.

## What we already knew (internal intel, checked first)

Exactly one line, and it is worth more than its length. Payworks' own Check-ins & 1:1s area brief (Michelle, 2026-07-23) lists the vendor set it scanned: *"Lattice, 15Five, Leapsome (mid-market); Rise, Humi, Collage, Knit, Wagepoint (Canadian SMB); **Dayforce (enterprise reference)**."* [High — [area-brief-checkins-2026-07-23](../../../../inbox/payworks-source-material/briefs/area-brief-checkins-2026-07-23.md)]

So Payworks' own product organisation already places Dayforce as an **enterprise reference point**, not a Canadian-SMB rival — which is why `tier:` above reads `indirect`, not `direct`. The same brief states the target segment for that area as **20–500 employees** and consciously defers "enterprise over-build" beyond ~500 EE. Both facts bear directly on the threshold decision below.

[GAP: the brief cites a full competitive scan artifact, `area-brief-checkins-competitive-2026-07-17` — **it is not in this repo.** Recovering it would likely close more of this teardown's gaps than more web research would.] Beyond that one line there is no internal Dayforce evidence anywhere: no call summary, no lost deal, no interview mention. `business-info.md` records that the only competitor named in Payworks' strategy material is Wagepoint, and that no competitor list exists at all.

## Who they are

Global full-suite HCM — payroll, HR, time, absence, self-service, recruiting, benefits, compensation on one platform. Renamed from Ceridian; taken private by Thoma Bravo in an all-cash deal at **US$12.3B enterprise value** (announced 2025-08-21, completed February 2026), with a minority investment from an ADIA subsidiary. [High — [Thoma Bravo announcement](https://www.thomabravo.com/press-releases/dayforce-enters-into-us12.3-billion-definitive-agreement-with-thoma-bravo-to-become-a-private-company), [completion release](https://www.thomabravo.com/press-releases/thoma-bravo-completes-acquisition-of-dayforce), verified 2026-08-31]

Canadian payroll is genuinely native for them, not an afterthought: their own admin documentation covers ROE issuance with reason codes, T4 and RL-1, Canadian federal and provincial tax configuration, and Québec-specific QPP/QPIP handling. [High — [Record of Employment](https://help.dayforce.com/r/documents/Payroll-Administrator-Guide/Record-of-Employment-ROE), [Understanding your RL-1](https://help.dayforce.com/r/documents/Dayforce-FAQs/Understanding-your-RL-1), [Define Canadian Provincial Tax Information](https://help.dayforce.com/r/documents/Payroll-Administrator-Guide/Define-Canadian-Provincial-Tax-Information), verified 2026-08-31]

## Positioning & pricing

- **Their pitch:** [GAP: not captured this run — the scope was approval mechanics, not messaging. Run path (d) before using any positioning line externally.]
- **Pricing shape:** [GAP: Dayforce publishes no price list. Do not quote a number from a third-party aggregator.]

## Approval workflows — how they actually work

**Chains are built, not configured from a menu.** Approvals run on a workflow graph. *"Routing nodes direct requests to the users who can review and respond to the submitted forms."* A routing object *"must have only one outgoing link, which must lead to a Decision object"*; the Decision object's outgoing connectors become the buttons on the form. Chain depth is set by a numeric **Relative Level of Affected Employee's Manager** field — enter a whole number to route to that level of management. Recipients can also be a named user, the affected employee, the submitter, a future manager (new hires / transfers), or an **authority type** (Manager, Performance Admin, Approve Pay Rate Change). [High — [Routing Nodes](https://help.dayforce.com/r/documents/Self-Service-Guide/Routing-Nodes), verified 2026-08-31]

**Parallel routing resolves first-responder-wins.** *"The first person to make a decision triggers the next step in the process. Subsequent decisions by other recipients are ignored."* Sequential multi-level approval is explicit and supported — *"you could specify that two different levels of approval (such as from a team lead and a manager) must be reached before the request is considered approved."* [High — [Routing Nodes](https://help.dayforce.com/r/documents/Self-Service-Guide/Routing-Nodes), [Workflow Configuration for Time Away from Work](https://help.dayforce.com/r/documents/Self-Service-Guide/Workflow-Configuration-for-Time-Away-from-Work), verified 2026-08-31]

**Thresholds: not found.** The page that defines routing describes recipients by hierarchy, role and authority type — **no amount-based or value-conditional routing appears in it.** Condition nodes exist elsewhere in the workflow engine (documented against recruiting fields such as candidate status and decline reason), so conditional branching is clearly a primitive of the engine. [GAP: whether a Condition node can branch on a claim *amount* — the thing a $5k rule needs — is not stated in any page read. Absence in the docs is not proof of absence in the product. Closing this needs a demo, a Dayforce SE, or a customer who has built it.] [Med — [Configure Condition Nodes to Check for Decline Reason](https://help.dayforce.com/r/documents/Recruiting-Guide/Configure-Condition-Nodes-to-Check-for-Decline-Reason), verified 2026-08-31]

**Delegation is a date-bounded employee property, not an ad-hoc reassignment.** An admin sets *"Workflow Approval Delegate (Employee Number)"* on the approver's profile with Effective Start / Effective To dates; then *"the approval is routed to the delegated approver instead"* and *"the delegate also gets any relevant workflow notifications."* Eligible delegates: *"a manager who reports to the same manager as the usual approver, or an employee who reports to the usual approver"* — with the caveat that *"for security reasons, access should be delegated from managers to other managers rather than from managers to employees."* Separately, account-level delegation lets a delegate act for an absent manager on timesheets and time-away. [High — [Configure an Approval Delegate for Workflows](https://help.dayforce.com/r/documents/Self-Service-Guide/Configure-an-Approval-Delegate-for-Workflows), verified 2026-08-31]

**Mobile approval is first-class.** Dayforce markets it directly: *"Review, approve, and adjust employee timesheets. Quickly approve vacation and shift-trade requests with full visibility into balances and accruals"* and *"quickly respond to employee requests, authorize timesheets, manage absenteeism, and complete other team-related tasks using the mobile app."* [High — [Dayforce Mobile HR App](https://www.dayforce.com/how-we-help/dayforce/hrm-software/hr-software/mobile-hr-app), verified 2026-08-31] [GAP: no source read states whether a *claim/expense* approval or a receipt photo is available on mobile — the marketed list is timesheets, time away and shift trades.]

**The payroll run has its own approval gate, and it is location-shaped.** *"Users from each location, typically managers, approve the records for each pay period on its due date, using Pay Approve Checklist."* Managers clear problems first (missing punches, adjustments); then payroll administrators *review which locations have approved*, perform the final approval, and transmit. So the payroll gate is a **two-stage, location-by-location checklist against a due date** — structurally separate from the form/workflow engine above, not a step inside it. [High — [Approve Payroll](https://help.dayforce.com/r/manager-guide/Approve-Payroll), verified 2026-08-31]

**Expense claims: no documented first-party T&E module.** Searches of Dayforce's own help portal surface no travel-and-expense guide. What exists instead: *Reimbursement Plans*, which sit under the **Benefits** Administration Guide (plan settings, option settings, contribution settings) — a benefits-account construct, not claim-and-approve T&E; generic **Forms** with a *"Supporting Documents"* upload section (anti-virus scanned) that a customer can wire to any workflow; expense reimbursement as a **generated earning** paid through payroll; and third-party T&E vendors listed on Dayforce's own app exchange (Emburse). [Med — [Reimbursement Plans](https://help.dayforce.com/r/ImplementationGuide/Dayforce-Implementation-Guide/Reimbursement-Plans), [Attach Files to Forms](https://help.dayforce.com/r/documents/Employee-Guide/Attach-Files-to-Forms), [Emburse on Dayforce Exchange](https://exchange.dayforce.com/en-US/apps/430217/emburse-expense-management/support), verified 2026-08-31] [GAP: this is a bounded negative — a *public documentation* absence. A private module, a recent release, or a regional SKU would not show up this way. Verify before repeating it to a customer.]

## SWOT (scoped — approval workflows only)

No full SWOT pass ran; these are the rows the capability comparison actually produced.

### Strengths

- Genuinely configurable approval graphs — arbitrary chain depth by manager level, authority-type recipients, parallel-then-first-wins, sequential multi-level. [High — Routing Nodes, above]
- Delegation that survives an audit: effective-dated, on the employee record, with notification follow-through. [High — Configure an Approval Delegate, above]
- Mobile approvals marketed as a headline manager capability. [High — Dayforce Mobile HR App, above]
- Canadian statutory depth (ROE, T4, RL-1, QPP/QPIP) is documented and real — **this is not where we out-compete them.** [High — sources above]

### Weaknesses

- No documented first-party expense-claim experience; customers appear to reach for Forms, a payroll earning, or a third-party vendor. [Med — above]
- Approval configuration is implementation work — routing nodes, decision objects, connector response types, employee properties. That is a consultant-and-project shape, not a self-serve admin toggle. [Med — inferred from the configuration surface described across the pages above]
- The payroll gate is location-and-due-date shaped, not amount-and-risk shaped. Nothing read suggests "this run is unusually large, escalate it". [Med — Approve Payroll, above]

### Opportunities (for us)

- A claim-to-approval path that a client's own admin can configure in an afternoon is a real wedge against a build-it-in-implementation engine — **if** we can evidence that the configuration burden actually costs Dayforce deals. [GAP: no such evidence exists in this repo. Hypothesis, not a finding.]

### Threats (from them)

- If they wire a Condition node to a claim amount, threshold routing becomes a configuration, not a roadmap item — and any threshold feature we ship stops being a differentiator. [Med — engine primitives exist; the amount binding is the unknown]

## What this run did not cover

Scope was approval mechanics. Deliberately absent: pricing, packaging, segment and ICP overlap with Payworks, win/loss, customer sentiment, recent product releases, and every module outside payroll and expense.

[GAP: apart from the one line quoted at the top, everything here comes from Dayforce's **public documentation**. Nothing in this repo says whether we meet Dayforce in deals, or how often — so this teardown describes their product, not our competitive position against it. The `tier: indirect` above is a proposal derived from one internal line, not a registered fact: Dayforce is absent from `business-info.md`'s Competitive Landscape roster, and adding it there is a gated change this run did not make.]

## Recent moves

- 2026-02 — Thoma Bravo acquisition completed; shares delisted from NYSE and TSX. [High — [completion release](https://www.thomabravo.com/press-releases/thoma-bravo-completes-acquisition-of-dayforce)]
- 2025-08-21 — US$12.3B take-private agreed at $70.00/share, a 32% premium to the 2025-08-15 unaffected close. [High — [announcement](https://www.thomabravo.com/press-releases/dayforce-enters-into-us12.3-billion-definitive-agreement-with-thoma-bravo-to-become-a-private-company)]

## How we sell against them

- **We win when:** [GAP: no won-deal evidence against Dayforce exists in this repo. Do not put a claim here until a call summary supports it.]
- **We lose when:** [GAP: same — the only internal competitive signal we hold is the FY27 win-loss read, a 37% Time Management gap and a 39% HR gap, and neither is attributed to a named competitor.]
- **Trap questions** (safe to ask — each is grounded in a documented Dayforce behaviour, not a guess):
  - "Can an admin route a claim to a second approver above a dollar amount without opening the workflow designer?"
  - "When my approver is on leave, who approves — and did someone have to edit their employee record to make that happen?"
  - "Is expense claim approval in the mobile app, or only timesheets and time off?"

## What this means for our approval-workflow decisions

**Expense VP2 — the proposed $5k / >150-employee threshold.** The decision is not yet filed, and the initiative page is explicit that approval thresholds are still a *hypothesis*: across thirteen design-partner records, expense appears once, and Northwind's claims route **claimant → approver → accounts payable, not through payroll**. Three things this teardown adds:

1. **Amount-based routing is not a category expectation we are behind on.** The buyer-side comparison would be against a workflow engine where, as far as public documentation shows, an approval chain is built from hierarchy and role — not from a dollar figure. If we ship a first-class threshold, it is plausibly a *differentiator*, not table stakes. The confidence limit is real: see the Condition-node gap above.
2. **The 150-employee half of the rule cuts our own target segment in half.** Payworks' area brief puts the target at **20–500 EE**, so a ">150 employees" condition applies to roughly the upper half of that band and excludes the lower half — worth stating out loud, because it means the rule is a *segment* decision, not just a risk-control one. On the competitive side there is nothing to compare against: Dayforce's only scale-shaped gate is the location-by-location payroll checklist, and headcount is not a routing input anywhere we found. [GAP: whether headcount-conditioned approval is a real buyer expectation is unevidenced on both sides.]
3. **Delegation is the part the threshold breaks.** A $5k escalation puts a named senior approver in the path; Dayforce answers that with effective-dated delegation on the employee record. Any threshold we ship needs its out-of-office story decided in the same change, or the rule will stall claims the first time an approver takes vacation.

**For a payroll PM.** Two findings stand alone and need no expense framing. First, Dayforce's payroll approval is a **two-stage location checklist against a due date** (manager per location → admin final approval → transmit), which is a different shape from the per-company run approval our catalog describes on `pay-groups`; if a prospect describes approvals as "each site signs off by Tuesday", that is the model they are used to. Second, **delegation on payroll approvals** is a solved, audited thing on their side — date-bounded, on the employee record, notifications included — and it is worth knowing what our answer is before a deal asks.

## Sources

Every claim above carries its source inline with a confidence level and the date verified (all 2026-08-31). External primary sources: Dayforce's own help portal (`help.dayforce.com`), `dayforce.com`, Dayforce's app exchange, and Thoma Bravo's press releases.

Internal sources read: [area-brief-checkins-2026-07-23](../../../../inbox/payworks-source-material/briefs/area-brief-checkins-2026-07-23.md) (the one Dayforce mention, plus the 20–500 EE segment) · [expense-management-vp2](../../../initiatives/expense-management-vp2.md) (evidence base, A/P routing, threshold hypothesis) · [business-info.md](../../../strategy/business-context/business-info.md) Competitive Landscape (the no-competitor-list gap) · `feature-index.yaml` (our approval-relevant capability). Consulted and empty on Dayforce: `user-insights/`, `customers/`, `meetings/`, `decisions/`, `analytics/`.
