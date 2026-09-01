---
date: 2026-08-26
initiatives: [employee-onboarding, expense-management-vp2]
areas: [onboarding, expense-management, employee-self-service]
---

# Meeting Notes: Internal Product Sync — Onboarding Profile Foundation & Pilot Scope

**Date:** 2026-08-26  
**Attendees:** Michelle Tremblay, Claire Sutton, Margaret Foster, Vanessa Lee  
**Meeting Type:** Internal cross-team product sync (other)  
**Transcript:** [product/meetings/other/transcripts/2026-08-26-internal-product-sync.md](../transcripts/2026-08-26-internal-product-sync.md)

## Summary

Two consequential decisions were made and ratified on the record. First, employee onboarding will reuse the expense VP2 employee profile foundation (MJ-01) rather than build its own HR-module record — with MJ-01 gaining a pre-hire state and a named extension point for onboarding-owned fields as the terms of the deal. Second, the onboarding pilot scope is limited to Employee Self Service only (new hire self-serve), deferring the admin orchestration side until the prerequisite document store and task engine are available. Both decisions are filed separately as decision records and linked from both initiative pages.

## Decisions Made

1. **Onboarding reuses expense VP2 employee profile foundation (MJ-01)** — see [decisions/2026-08-26-onboarding-profile-foundation.md](../../decisions/2026-08-26-onboarding-profile-foundation.md)
2. **Onboarding pilot scoped to Employee Self Service only** — see [decisions/2026-08-26-onboarding-pilot-ess-scope.md](../../decisions/2026-08-26-onboarding-pilot-ess-scope.md)

## Action Items

| Task | Owner | Due Date | Priority | Status |
|------|-------|----------|----------|--------|
| Add pre-hire state to MJ-01 draft; re-run translation checkpoint (invite Claire Sutton) | Michelle Tremblay | ~week of 2026-09-01 | High | 🔴 Not Started |
| Profile layout design for the named extension point seam | Vanessa Lee | Mid-September (before MJ-02 dev-ready bundle) | High | 🔴 Not Started |
| Write both decision records; ensure they appear on both initiative pages | Claire Sutton | This week | High | ✅ Done (filed by this run) |
| Read Maplewood's onboarding spreadsheet properly and send a response | Claire Sutton | This week | High | 🔴 Not Started |
| Add "who owns the org chart?" to Open Questions & Risks on the onboarding brief | Claire Sutton | This week | Medium | 🔴 Not Started |
| Attend Northwind controller call (2026-08-27 9am) | Vanessa Lee | 2026-08-27 | Medium | 🔴 Not Started |

## Key Insights

**Acme visit signal (expense VP2):** 75 employees, one payroll admin. Receipts are already digital PDFs in email — the physical-capture story lands flat. Their HR manager wants mobile approvals *blocked*, not discouraged. This is the second signal in this direction; the Northwind controller has said something similar. Expense VP2 mobile-approval assumptions need to be revisited in light of this pattern.

**MJ-02 schedule impact:** Adding the pre-hire state to MJ-01 costs 3–4 weeks and pushes MJ-02 (receipt capture) right by that amount. Michelle Tremblay accepted this as the correct trade.

**November pilot timing is strategic:** Northwind and Maplewood both hire seasonally — spring is their intake wave. A November pilot gets the team set up and instrumented before spring. A January or February pilot means debugging during the spring wave and losing a year of observation.

**Design drift precedent:** Time and Absence today have two places to see a person's schedule that don't match — described by Vanessa Lee as a live usability problem ("wait, is this the same person?"). Two records = two screens that diverge over time, worst experienced in week one by someone who has never seen Payworks.

**Partner evidence confirms the single-record argument:** Maplewood and Northwind independently described the same cross-system gap (Northwind: review system needs a company email on the Payworks file before it pulls an employee; half their field staff don't have one → manager phones HR → HR types the email → 24-hour wait). Both root back to an incomplete onboarding step, not the downstream system. A second record would widen, not close, this gap.

**Research blind spot flagged:** All 13 interviews Margaret Foster conducted this summer involved HR managers or payroll managers — zero new hires. The admin-side pain is real, but the new hire's experience is unresearched. The ESS pilot is partly motivated by generating that data.

## Open Questions

- [ ] **Who owns the org chart?** Both decisions assume the org relationship lives on the payroll record and everything else copies it. Payroll didn't confirm this — the team asserted it. Needs a real answer before these decisions are fully load-bearing. **Owner:** Claire Sutton to add to onboarding brief Open Questions & Risks.

## Timeline Risks

- **MJ-02 (receipt capture) pushed right 3–4 weeks** due to pre-hire state addition to MJ-01. Accepted trade-off — noted here for downstream scheduling.

## Next Steps

**Immediate (this week):** Maplewood spreadsheet response (Claire Sutton); org chart question in brief (Claire Sutton); MJ-01 pre-hire state scoped (Michelle Tremblay).  
**Short-term (2 weeks):** Translation checkpoint re-run on MJ-01 with Claire Sutton in the room (Sonia to send invite); Vanessa Lee books profile layout session with Curtis.  
**Follow-up:** Northwind controller call 2026-08-27 9am — Michelle Tremblay + Vanessa Lee attending; Maplewood Payroll Manager response re: her spreadsheet.
