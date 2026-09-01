---
date: 2026-08-26
initiatives: [employee-onboarding]
areas: [onboarding, employee-self-service]
status: decided
decided-by: Michelle Tremblay, Claire Sutton, Margaret Foster, Vanessa Lee
---

# Decision: Onboarding Pilot Scoped to Employee Self Service Only

**Date:** 2026-08-26  
**Source:** [Internal product sync — transcript](../meetings/other/transcripts/2026-08-26-internal-product-sync.md) · [summary](../meetings/other/summaries/2026-08-26-internal-product-sync.md)

## Decision

The onboarding pilot is scoped to **Employee Self Service (ESS) only.** The admin side of onboarding is unchanged in the pilot.

**What is in the pilot:**
- New hire receives a link before day one
- Self-serves: personal details, banking information, tax forms
- Uploads SIN and void cheque (both already stored by ESS today for existing employees — no new document store needed)
- Sees a first-day view

**What is not in the pilot:** admin task assignment, document collection from the admin side, multi-department task orchestration, any admin-side workflow automation.

**Target date:** November (before the seasonal spring hiring wave at Northwind and Maplewood).

## Rationale

**Primary reason — the admin side can't run for real without infrastructure that doesn't exist.** A full admin onboarding pilot requires a document store and a task orchestration engine. Neither is built or scheduled. Document management has been "next year" for two years. No task engine exists anywhere in the product (Absence has a hand-rolled workflow). Building both takes approximately two quarters, which pushes the pilot to January or February.

**Primary reason — a pilot without those pieces is a mock, and you can't learn adoption from a mock.** The team has already done four prototype rounds for admin onboarding. Those tell you "is this the right shape." They cannot tell you "did anyone use it in week three." The pilot's job is the second question. Running the admin side without the infrastructure produces a fifth prototype round under a different label.

**Timing reason — seasonal hiring window.** Northwind and Maplewood both hire seasonally; their intake wave is spring. A November pilot gets the team set up and instrumented before spring. A January or February pilot means debugging during the spring wave — the team gets pushed aside — and the next real observation window is a full year later. The timing cost of delaying the pilot is not two quarters; it is one year of learning.

**Design reason — the new hire user is unresearched.** All 13 design-partner interviews this summer involved HR managers or payroll managers; not one involved a new hire. The ESS pilot is the first chance to observe the experience of someone who has no Payworks training, no context, and may be completing onboarding on a phone in a parking lot before their first shift.

**ESS can run for real against MJ-01.** It needs a person (MJ-01's pre-hire state, agreed above), a form (exists), and a place to put two specific documents — SIN and void cheque — both of which ESS already handles for existing employees. No new document store is needed for this scope.

## Counter-argument on record

Margaret Foster's view, stated explicitly and not conceded: the researched pain is administrative. Onboarding came up unprompted in 4–5 of 13 interviews this summer; every time, the described pain was on the HR side (e.g., Maplewood's tab-per-department spreadsheet, Cascadia's credential tracking in someone's head and a calendar reminder, Northwind's email-field gap). Not one person described a new hire having a bad experience. An ESS-only pilot tests the half nobody complained about.

**This is a sequencing call, not a judgment that the admin problem is smaller.** Margaret Foster's position — that the admin burden may be the larger problem — is on the record and not resolved by this decision.

## Three conditions (agreed as part of the decision)

1. **The pilot instruments admin handoffs even though they are manual.** Count the number of manual interventions per new hire during the pilot — by hand if necessary. This prevents the pilot from being reported as successful based only on the half that was built.

2. **The decision record states explicitly that this is a sequencing call.** Not a ranking of the problems. (This document fulfils that condition.)

3. **Maplewood's Payroll Manager receives a proper response to her spreadsheet.** She sent an onboarding process map; it should be acknowledged as heard, not filed silently. Claire Sutton committed to do this in the week of 2026-08-26.

## Rejected alternative

**Pilot the full HR-module onboarding flow** (admin task assignment, document collection, orchestration across HR, IT, and payroll). Rejected because: (a) requires a document store and task engine — two quarters of prerequisite build; (b) puts the pilot in January or February, missing the spring seasonal window and losing a year of observation; (c) requires recruiting new design partners (current partners were recruited for performance management; a high-volume-hiring cohort takes 6–8 weeks to recruit); (d) a pilot without the document store and task engine would be a prototype, not a pilot.

## Partner recruiting note

If and when the admin-side pilot runs (post-ESS), current design partners were recruited for performance management. A high-volume hiring pilot requires at least two partners with that profile; last recruitment cycle took 6 weeks, realistically 8.
