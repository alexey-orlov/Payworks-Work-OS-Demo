---
updated: 2026-08-31
areas: [payroll, human-resources, time-management, absence-management, workforce-analytics]
features: []
initiatives: [performance-management-discovery, expense-management-vp2]
---

# Northwind Landscaping (northwind-landscaping) — Account Context

> Design-partner account. Every claim below traces to one of the research records listed
> under History. Those records were anonymized on import — company, site and person names
> are fictionalized labels, and customer-side people appear as role titles only.

## Who they are

- Multi-site **grounds maintenance and seasonal operations** — *"In the grounds maintenance industry, the sites got serviced, the green waste got picked up."* Their customers are **municipalities** (*"the municipalities, which are our customers"*) and the residents those contracts serve. Snow removal runs as a seasonal line, and there is a separate equipment-yard side — *"the fleet and equipment side of things."*
- Footprint spans **Ontario and British Columbia**; HR is staffed in both — *"our manager in British Columbia, our HR manager and our HR manager in Ontario."* Sites are referred to locally (Shore, East, South yard, North yard, Central); no site count appears on any record.
- Layered field org: crews and drivers → **route supervisor** (the first salaried, reviewed level) → site manager → district/divisional manager → senior leaders → executive team → **the Owner**, who signs off personally on the annual merit round.
- **Reviews cover salaried and administrative staff only** — *"we don't do it for our hourly, labor-type positions."* 173 reviews were completed in the 2025 cycle, **73% of those in scope**.
- No total headcount is stated on any record. The size band and ARR in [portfolio.yaml](../portfolio.yaml) are illustrative — see the conventions block at the top of that file.

## Current truth

- **The most multi-module account in the design-partner group**, and still expanding. Payroll is the system of record (the salaried extract, increases and retros all run through it); HR carries employee documents, disciplinary records and scanned review history; managers approve timesheets and holidays daily; and Workforce Analytics onboarding is live — *"we've got calls going also with the analytics… the 2.0, so we're doing training on that."* Document management is under active evaluation: *"we want to look at the document management part of things."*
- **Performance management runs entirely outside Payworks, in QuickBase**, linked to Payworks by an in-house API that pulls employee master data (a missing company email in the Payworks profile silently breaks the pull). QuickBase cannot export, so every score is re-keyed by hand.
- **The merit chain is the account's defining pain.** Payroll pulls the salaried list out of Payworks; the Head of HR splits it into one tab per manager and is *"the keeper of the spreadsheet"*; each manager re-keys their QuickBase rating plus a recommended percentage; tabs come back one email at a time; she reconciles rating against increase by eye; the executive team reviews and the Owner signs. Then the Payroll Administrator uploads it — *"We got the signed, approved sheet Monday night from the Owner"* with a Wednesday-noon payroll cutoff and a Friday payday. Her own verdict: *"It's gotta be the worst spreadsheet you've ever experienced."*
- **Weighting and pool, for reference:** goals 70% / performance behaviours 30%, a 1–5 scale with mandatory examples at 1 and 5, five behaviours (six for people leaders), a company merit pool of *"2.5% or 3%"*, and a June 1 eligibility cutoff.
- **The headline ask is consolidation, not a new tool:** *"I should be able to go right into PayWorks. Not only can I see your whole file, now I can see your performance file."* Four years of review history are currently unreachable from the employee record — *"for the last 4 years since we don't do paper, yeah, you got nothing."*
- **Expense (Controller call held 2026-08-27):** full workflow now documented. ~60 trucks across Ontario and BC. Fuel cards handle $28k/month cleanly. Everything else (~650 receipts/month in season, $40k/month, $350k/year) flows through a physical shoebox; the A/P clerk spends 2.5 days at every month end sorting and coding. Critical coding problem: 11 municipal contracts where field materials are billable to municipalities — miscoded receipts produce silent revenue leakage. Key requirements: (1) mobile capture + site attribution at the moment of purchase with offline queuing; (2) position-based approval chains per yard (BC has no regional manager); (3) expense reimbursement on the payroll register — visible before lock, non-taxable, clickable to receipts, misses auto-roll to next pay run; (4) claimant status visibility ("approved, paying on the 11th"). Renewal on the horizon; Controller wants to expand, not just renew. A/P clerk to attend the next session. See [expense-management-vp2](../../../initiatives/expense-management-vp2.md).
- **Pilot committed:** a six-person east/west group of managers and employees for prototype testing — *"I've got a number of pilot teams out there that help us create stuff."*
- **Risks:** the whole merit round is a single point of failure on one person's spreadsheet; reconciliation between QuickBase scores and the merit sheet is unverified; mid-year reviews remain optional and under-adopted; adoption depends on managers who do not all work at a desk.
- **Commercial terms are not carried in this repo.** Contract dates, renewal and pricing are CRM-class facts — **Salesforce is the system of record** for the commercial relationship. This page holds product and research context only.

## History

- 2026-08-27 — Controller expense discovery call: first substantive expense conversation with the Controller and HR Manager (first 17 min). Receipt flow, job coding, approval chain (BC vs. Ontario), payroll register requirements, status visibility, standalone-tool evaluation, renewal signal → [summary](calls/summaries/2026-08-27.md) · [transcript](../../../user-insights/transcripts/2026-08-27-northwind-landscaping-call.md)
- 2026-08-13 — Follow-up call over the HR Manager's working lunch: two open loops closed, and the final four minutes opened an unplanned onboarding conversation — ESS named as the half that matters → [summary](calls/summaries/2026-08-13.md) · [transcript](../../../user-insights/transcripts/2026-08-13-northwind-landscaping-call.md)
- 2026-08-05 — Reverse demo: the HR Manager walked the current merit workflow end to end, and the expense/Controller bridge surfaced in the closing minutes → [summary](calls/summaries/2026-08-05.md) · [transcript](../../../user-insights/transcripts/2026-08-05-northwind-landscaping-call.md)
- 2026-07-17 — HR leadership call: the Head of HR and HR Manager on the review process, its history, and what consolidation into Payworks would have to do → [summary](calls/summaries/2026-07-17.md) · [transcript](../../../user-insights/transcripts/2026-07-17-northwind-landscaping-call.md)
- 2026-07-10 — Discovery interview + prototype review, site supervisor: ran his last review round on paper off a template found online → [session report](../../../user-insights/2026-07-10-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-07-10-northwind-landscaping-interview.md)
- 2026-06-24 — Discovery interview + prototype review, site operations manager (joined from his truck) → [session report](../../../user-insights/2026-06-24-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-06-24-northwind-landscaping-interview.md)
- 2026-06-23 — Discovery interview + prototype review, operations director: the merit-calculation detail — *"I take the 5% times it by 70%, and that's my recommended percentage for their increase"* → [session report](../../../user-insights/2026-06-23-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-06-23-northwind-landscaping-interview.md)
- 2026-06-22 — Discovery interview + prototype review, regional operations manager: the 1–5 rating disconnect and the mobile-capture ask → [session report](../../../user-insights/2026-06-22-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-06-22-northwind-landscaping-interview-3.md)
- 2026-06-22 — Discovery interview + prototype review, district manager: goal-cascade duplication, *"it's a lot of typing right now"* → [session report](../../../user-insights/2026-06-22-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-06-22-northwind-landscaping-interview-2.md)
- 2026-06-22 — Discovery interview + prototype review, HR manager and operations manager: the merit spreadsheet and the 30/70 weighting → [session report](../../../user-insights/2026-06-22-interview-insights.md) · [transcript](../../../user-insights/transcripts/2026-06-22-northwind-landscaping-interview-1.md)
