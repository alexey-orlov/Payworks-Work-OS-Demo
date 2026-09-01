---
initiatives: [performance-management-discovery]
areas: [performance-management]
date: 2026-08-31
owner: Margaret Foster
---

# Assumption Map — Performance Management Discovery

**Basis:** Cross-interview synthesis (`performance-management-2026-08-31.md`), 13 records, 4 accounts.
**Method:** Each hypothesis is rated across the four DVFU lenses (Desirability, Viability, Feasibility, Usability) for confidence and assigned a validation route. The **Test First** rows (confidence Medium or Low, or where one observation could falsify the belief) populate §4 of the Product Brief.

---

## Hypotheses

### H1 — Anchored scales + mandatory justification eliminates the scale argument

**Claim:** If the rating scale's anchor definitions are shown at the point of entry and a written justification is required before submission, managers and employees will align on the number's meaning and the review conversation will stop being an argument about the digit.

| Lens | Rating | Evidence | Notes |
|---|---|---|---|
| Desirability | **High** | 4/4 accounts confirm self-rating inflation and undefined scale as the highest-count pain. Northwind regional ops manager named the prototype's anchor display as the fix, unprompted. | The workaround — post-meeting negotiation — is actively harmful; users want the fix. |
| Viability | High | No commercial risk to this feature; no pricing sensitivity indicated. | — |
| Feasibility | Medium | No code-grounding yet — depends on HR module's current rating-field structure. [GAP: `/code-qa` once code-repos.yaml has a reachable HR repo] | — |
| Usability | High | Prototype was preferred over QuickBase at Northwind on first contact; anchors-at-point-of-rating was the specific element named. | — |

**Verdict:** Test First — Feasibility is the open leg. Validate the prototype with the Northwind 6-person pilot before locking the anchor UI as a requirement.

**Kill criterion:** If fewer than 50% of pilot managers say the anchor changed what they wrote, this feature is nice-to-have, not must-have.

---

### H2 — In-system notes will displace paper and email journals

**Claim:** If managers can log a note on an employee in Payworks at the moment the observation happens — accessible on mobile — they will stop keeping paper notebooks and personal email chains, because the system note will be findable at review time and the notebook won't.

| Lens | Rating | Evidence | Notes |
|---|---|---|---|
| Desirability | **Medium** | 4/4 accounts have the paper/email workaround. Explicit request for in-system notes at 2/4 accounts; implicit at the other two (workaround present, feature not directly probed). | Single-account must-have (Northwind regional ops manager: mobile-native notes is his only adoption condition). |
| Viability | High | No commercial risk. | — |
| Feasibility | Medium | Mobile note capture introduces a new surface; depends on mobile infrastructure state. [GAP] | — |
| Usability | Medium | Notes UI must cost less than writing on paper (speed, discoverability). No usability test of the notes surface yet. | — |

**Verdict:** Test First — probe at two more accounts before treating as universal must-have. Run the notes-capture surface in prototype at Harbourview and Maplewood.

**Kill criterion:** If fewer than 3 accounts confirm the note-capture surface replaces their external system in a prototype test, scope mobile to the next release and ship desktop notes only.

---

### H3 — Automated reminders will close the cycle-slippage gap

**Claim:** If Payworks sends system reminders at each phase gate (self-rating due, manager rating due, HR quality check due), the annual cycle will complete on schedule without the HR Manager emailing managers and managers chasing supervisors.

| Lens | Rating | Evidence | Notes |
|---|---|---|---|
| Desirability | **High** | 3/4 accounts confirm no automated reminders exist today. The manual enforcement mechanism (HR Manager emails → managers chase supervisors) was described unprompted at multiple accounts. | *"On the surface, yes. In reality, no"* — Northwind on whether cycles complete on time. |
| Viability | High | No commercial risk. | — |
| Feasibility | High | Notification infrastructure is likely shared with other Payworks modules. [GAP: confirm with Engineering] | — |
| Usability | High | Users named the email-chase as a pain; the fix is the same trigger done by the system. Low UX risk. | — |

**Verdict:** Monitor — high confidence across all lenses. Validate the cadence setting (how many reminders, how spaced) with the Harbourview HR Manager, who sets up ~1,000 reviews/year and has the most to lose from over-notification.

---

### H4 — Mobile capture is the adoption gate for deskless managers

**Claim:** If managers who work away from a desk cannot capture notes and complete check-ins on a phone, they will not use the Performance Management module — even if they want to.

| Lens | Rating | Evidence | Notes |
|---|---|---|---|
| Desirability | **Medium** | Single-account must-have (Cascadia: *"a lot of our managers are constantly on the go"*). Corroborated at Northwind (one participant, not the account as a whole). Not probed at Harbourview or Maplewood. | Desk-based HR Administrators at several accounts expressed no mobile preference. |
| Viability | High | No commercial risk. | — |
| Feasibility | Low | Mobile HR surface does not exist today. Infrastructure state unknown. [GAP: `/code-qa`] | — |
| Usability | Medium | Cascadia gave a clear rule (capture on mobile, formal actions on desktop). Other accounts not yet asked. | — |

**Verdict:** Test First — probe Harbourview and Northwind site supervisors on their work location before treating mobile as a universal gate. If fewer than 3 accounts confirm deskless managers are in scope, de-risk by scoping desktop-first and adding mobile in v2.

**Kill criterion:** If Feasibility gap reveals mobile HR infrastructure is 6+ months away, scope desktop-first and re-evaluate mobile for v2.

---

### H5 — A separate compensation approval step is required to reflect actual workflow

**Claim:** If the product separates review submission, HR quality-check approval, and compensation-change approval into three distinct gates, HR Managers and approvers will not mistake a shared review for an approved raise.

| Lens | Rating | Evidence | Notes |
|---|---|---|---|
| Desirability | **Low** | Single-account finding (Cascadia HR Lead — she runs compensation). *"If I, as HR, click approve and share, it doesn't mean that this is approved."* Not probed at Northwind, Harbourview, or Maplewood. | Single-account data point; Cascadia's HR Lead is uniquely the compensation owner. |
| Viability | High | No commercial risk. | — |
| Feasibility | Medium | Three-step workflow is implementable but structural — reversing it post-ship is costly. | — |
| Usability | Low | Other accounts have not confirmed this distinction applies to them. Defaulting it on for all accounts risks adding gates where none are wanted. | — |

**Verdict:** Test First — probe the compensation approver model at Northwind, Harbourview, and Maplewood before making the three-gate structure the default. Ship as configurable (default off) until validated.

**Kill criterion:** If only 1 of 4 accounts confirms the three-gate model fits their workflow, keep it configurable and do not make it the default.

---

## Summary Table — Test First Rows (→ §4 of the Product Brief)

| Hypothesis | Risk lens | Confidence | Validation route | Priority |
|---|---|---|---|---|
| Anchored scales + mandatory justification reduces scale argument | Desirability | High | Northwind 6-person pilot; measure rating-conversation outcome | 1 |
| In-system notes displaces paper / email journals | Desirability | Medium | 2 design-partner sessions with note-capture prototype | 2 |
| Automated reminders close cycle-slippage gap | Desirability | High | Probe cadence with Harbourview HR Manager | 3 |
| Mobile capture is the adoption gate for deskless managers | Usability | Medium | Probe Harbourview + Northwind site supervisors on work location | 4 |
| Separate comp approval step reflects actual workflow | Usability | Low | Probe comp approver model at Northwind, Harbourview, Maplewood | 5 |

---

Payworks Confidential | Updated 2026-08-31
