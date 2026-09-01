---
date: 2026-08-26
initiatives: [employee-onboarding, expense-management-vp2]
areas: [onboarding, expense-management, employee-self-service, payroll]
status: decided
decided-by: Michelle Tremblay, Claire Sutton, Margaret Foster, Vanessa Lee
---

# Decision: Onboarding Reuses the Expense VP2 Employee Profile Foundation

**Date:** 2026-08-26  
**Source:** [Internal product sync — transcript](../meetings/other/transcripts/2026-08-26-internal-product-sync.md) · [summary](../meetings/other/summaries/2026-08-26-internal-product-sync.md)

## Decision

Employee onboarding will reuse the employee profile foundation being built in expense VP2 (MJ-01). It will not build its own record in the HR module.

**Terms agreed in exchange:**
1. MJ-01 gains a **pre-hire state** (covering the period after an offer is accepted but before an employee number is assigned in payroll) before it goes dev-ready — scoped tightly to the minimum required to hold a person without an employee number; not the whole candidate/ATS world.
2. A **named extension point** is added to MJ-01, allowing onboarding to add its own fields (e.g., background check status, work permit expiry) to the profile without requiring an expense Value Package release.
3. These additions cost **3–4 weeks** in front of MJ-02 (receipt capture), pushing MJ-02 right by that amount. Michelle Tremblay accepted this as the correct trade.

## Rationale

**Primary reason — one database is the product promise.** Payworks sells "six integrated modules, one shared database." Two person records for the same hire would mean two org charts, connected by a sync. A sync is a failure mode (breaks at 2am; one record is always stale after a reporting line change). Cost was the second reason, not the first.

**Supporting reason — partner evidence.** Two design-partner accounts independently described the same downstream gap caused by incomplete onboarding data: Northwind's review system won't pull an employee without a company email address on the Payworks file — half their field staff don't have one, so a manager can't start a review and HR has to manually patch the record with a 24-hour delay. Maplewood's payroll manager's line: *"the employee record isn't real until payroll says it is."* A second record does not fix this gap; it creates an additional instance of it.

**Supporting reason — design drift.** Two records become two screens, built six months apart by different people. Time and Absence already have this problem — two schedule views that don't match, causing usability confusion ("wait, is this the same person?"). A new hire in week one is the worst possible audience for that confusion.

**Supporting reason — MJ-01 is closer than it looks.** MJ-01 already carries an `unposted` state (person exists in HR, payroll record pending) — built post-VP1 after a support case where a new hire submitted an expense before their first pay run. Onboarding's need is one step further back on the same axis: pre-hire. It's adding a lifecycle value, not a new dimension.

## Rejected alternative

**Build a separate HR-module record (candidate / pre-hire model).** Estimated cost: 11–12 weeks of two engineers — optimistic, because it would be built while the expense team is actively changing the same tables. If onboarding forked the foundation, Time and Absence (next in the queue for MJ-01) would face two competing foundations and would choose whichever was finished, not whichever was correct.

Claire Sutton's original schedule concern (not resolved by this decision): onboarding's date remains coupled to MJ-01's date, which has already moved once (June → September milestone). That dependency is real and is accepted — the onboarding PM will need to track MJ-01's readiness. The schedule risk is preferable to the data fragmentation risk.

## Open question flagged (not resolved)

Both decisions in this sync assume the org chart lives on the payroll record and downstream modules copy it. Payroll did not confirm this — the team stated it. This assumption is load-bearing for the single-record argument and should be confirmed before either decision is treated as fully settled.

**Owner:** Claire Sutton to add to Open Questions & Risks in the onboarding Product Brief.
