---
initiatives: [expense-management-vp2]
areas: [expense-management]
---

MICRO JOBS BREAKDOWN  |  Payworks  |  Expense Management VP2

# Expense Management VP2 — Micro Jobs Breakdown

Expense claims that start on a phone at the point of purchase and end as money on a pay run. Cut riskiest-assumption-first: the claim record and its site coding come before anything that reads them, because every later job fails differently if the object is wrong.

| Field | Detail |
|-------|--------|
| **Product / module** | Expense Management |
| **Initiative** | [Expense Management VP2](../../initiatives/expense-management-vp2.md) |
| **Release** | VP2 · M1 (capture → approval → pay run). A/P as a money destination is M2. |
| **VP Product Brief** | [expense-management-vp2-product-brief.md](expense-management-vp2-product-brief.md) |
| **Micro Jobs** | MJ-01, MJ-02, MJ-03, MJ-04 |
| **Author** | Michelle Tremblay, Product Lead |
| **Date** | 2026-08-28 |
| **Status** | Draft |

**Evidence key:** `[Evidenced]` source named · `[Partial]` signal, not proof · `[Hypothesis — needs validation]`

---

## 1. THE BACKBONE

**Actors:** the claimant (field crew, site supervisor, office staff) · the approver (a *position*, not a person — regional manager, controller, owner) · the Payroll Administrator who locks the run · the Accounts Payable clerk (out of scope in M1, see §7) · the Administrator who configures tiers

**Core objects:** the **claim** (image or mileage line, amount, site/job code, claimant, state) · the **approval tier** (dollar band × location → position) · the **pay-run reimbursement line**

**Flow:** buy → capture at source with the site code → claim enters a readable state → routes by employer policy → approved or escalated → posts to the pay run as a non-taxable reimbursement → appears on the register before lock → claimant sees the pay date

---

## 2. PROBLEM STATEMENTS THIS VALUE PACKAGE ADDRESSES

### MJ-01 — Claim record and site coding

**Root cause — why this job exists**

Coding is the failure nobody can repair later. The buyer is the only person who knows which site or job a purchase belongs to, and today that knowledge is gone by the time paper reaches the office. Northwind's A/P clerk spends 2.5 days and ~400 lines at month end reconstructing it, and $3–4k a year is written off to receipts that faded or never arrived `[Evidenced]` — 2026-08-27 northwind expense call.

**Claimant (field crew / site supervisor)**

When I buy something for a job, I want to record what it was for while I am still standing there, so I can stop being asked about it three weeks later.

- **Functional:** attach an amount, an image or a mileage line, and a site/job code to one record `[Evidenced]`
- **Emotional:** the shoebox is a standing accusation; people describe month-end as chasing `[Evidenced]`
- **Top pain:** being asked to recall a purchase they cannot remember `[Evidenced]`

**The business**

Unrecoverable coding means labour costs land on the wrong contract, which is the number Northwind bills municipalities against. Success condition: the site code is captured at the moment of purchase, not inferred afterwards.

**Note on scope / direction**

This job builds the object and its states — not a screen. The claimant-facing surface is MJ-02. The employee identity it hangs off already exists in the shared database; this job must not re-implement it, and the internal sync of 2026-08-26 committed it to carry a **pre-hire state** so employee-onboarding can reuse the same foundation.

### MJ-02 — Capture at source

**Root cause — why this job exists**

Half of Northwind's ~200 field crew have no company email and no desk `[Evidenced]`. Capture that requires a desktop session is capture that does not happen.

**Claimant**

When I am at a counter with no signal, I want the claim held on my phone and to see that it is held, so I never lose one to a failed upload.

- **Functional:** offline-tolerant capture; mileage as its own shape, not a receipt with no image `[Evidenced]`
- **Top pain:** "try again" that silently drops the claim `[Partial]`

**Note on scope / direction**

Acme is the honest counter-case: their receipts are already PDFs in email and their problem is people not submitting for four months, so capture lands flat for them `[Evidenced]` — 2026-08-20 acme call. This job is not sold as universal.

### MJ-03 — Approval routing

**Root cause — why this job exists**

Approval authority today is a person, so replacing the person rebuilds the chain. Northwind's bands are <$500 regional manager · $500–$2,500 controller · >$2,500 two signatures · >$5,000 the Owner, and the top band can sit eleven days `[Evidenced]`.

**Approver (a position)**

When a claim needs my decision, I want it to reach me by position and escalate if I sit on it, so nothing stalls because someone changed roles.

- **Functional:** employer-configured bands scoped by location, routing to a position; escalation on inaction, never silent `[Evidenced]`
- **Social:** the Acme HR Manager reads the approval email as *information* about her team, not a rubber stamp — she opposed the $250 auto-approve her own admin proposed `[Evidenced]`

**Note on scope / direction**

Northwind's Controller asked for a **desktop fence above $2,500** — enforced, not suggested — because he would otherwise tap yes in a parking lot `[Evidenced]`. That is a constraint on this job, not a preference.

### MJ-04 — Reimbursement on the pay run

**Root cause — why this job exists**

An approved claim is not money. Reimbursements must reach the employee without ever behaving like income — never on a T4, never in pensionable or insurable earnings — and must not be able to enter a register after it is locked.

**Payroll Administrator**

When I approve the register, I want the expense total visible before I lock it and impossible to change after, so the run I transmit is the run I approved.

- **Functional:** register visibility before lock, one-step drill-through, lock integrity, automatic roll to the next run `[Evidenced]`

**Note on scope / direction**

Northwind pays expenses out of accounts payable today, so on day one this job does not win for them — the A/P destination is M2 `[Evidenced]`.

---

## 3. THE MICRO JOBS

| ID | Micro Job | Type | Riskiest assumption it tests | Depends on | Priority — why | Effort | Status |
|----|-----------|------|------------------------------|------------|----------------|--------|--------|
| MJ-01 | Claim record and site coding | Net new | That a site/job code captured at purchase survives into payroll coding without a reconciliation step | — | Must ship first — MJ-02, MJ-03 and MJ-04 all read this object; and the pre-hire state committed on 2026-08-26 makes it employee-onboarding's foundation too | [Eng to confirm] | drafted |
| MJ-02 | Capture at source | Net new | That crews with no company email will capture at the counter rather than at month end | MJ-01 | Next — it is the only job that tests whether the behaviour change happens at all; runs parallel to MJ-04 | [Eng to confirm] | not-drafted |
| MJ-03 | Approval routing | Net new | That position-based tiers express a real employer policy without per-person configuration | MJ-02 | After MJ-02 — routing needs real submitted claims to route; the desktop-fence constraint is money-adjacent, so QA time is planned not discovered | [Eng to confirm] | not-drafted |
| MJ-04 | Reimbursement on the pay run | Integration | That an expense total can enter the register before lock and be provably unable to enter after | MJ-01 | Parallel to MJ-02 — touches the existing register, so feasibility verification is the critical path | [Eng to confirm] | not-drafted |

> **Effort** is Engineering's number, not the PM's — the column carries `[Eng to confirm]` until they fill it. MJ-03 and MJ-04 both touch money and are flagged accordingly.

---

## 4. SEQUENCING RATIONALE

**Riskiest assumption first.** MJ-01 leads because every other job fails differently if the claim object or its site coding is wrong, and because a wrong object is the most expensive thing to discover late — the 2026-08-26 internal sync put 22 engineer-weeks already spent on MJ-01 against 11–12 to duplicate it elsewhere.

MJ-02 comes second, ahead of the money path, because it carries the only assumption that cannot be reasoned about: whether people without desks actually capture at the counter. If that fails, MJ-03 and MJ-04 are routing and paying a volume of claims that does not exist.

MJ-04 runs parallel to MJ-02 rather than after it. It is Integration against a register that already works, so its risk is feasibility, not behaviour, and it can be verified with seeded claims.

MJ-03 is last of the four because approval routing needs genuine submitted claims to route, and because its hardest requirement — the enforced desktop fence — is only testable once claims arrive from a phone.

**Known cost, on the record:** MJ-01 grows a pre-hire state before dev-ready (3–4 weeks), which pushes MJ-02 right by the same amount. That was accepted on 2026-08-26 with the price stated.

---

## 5. PRESSURE TEST RESULTS

| Micro Job | Before/After | Standalone | Vertical/Horizontal | Scope sanity | False thin slice | INVEST | Verdict |
|-----------|--------------|------------|---------------------|--------------|------------------|--------|---------|
| MJ-01 | Pass | Pass | Pass | Pass | Pass | Pass | Cut stands — spec drafted, not yet agreed |
| MJ-02 | Pass | Pass | Pass | Pass | Pass | Pass | Cut stands |
| MJ-03 | Pass | Pass | Pass | Pass | Pass | Pass | Cut stands |
| MJ-04 | Pass | Pass | Pass | Pass | Pass | Pass | Cut stands |

> **Verdict vocabulary:** `Cut stands` — the gates pass and the cut holds, but the spec is not yet drafted or agreed (the normal state at first cut). `Locked` — all gates passed AND the PM agreed the spec. `Re-cut` — a gate failed; say which and why.

Standalone note: MJ-02, MJ-03 and MJ-04 each declare a prior-job dependency in §17 of their own specs. A declared dependency is not a Standalone failure.

---

## 6. CROSS-JOB DECISIONS & OPEN QUESTIONS

| # | Decision / question | Affects | Owner | Needed by | Status |
|---|---------------------|---------|-------|-----------|--------|
| 1 | Employee-onboarding reuses this foundation rather than building its own record | MJ-01 | Michelle Tremblay | Settled 2026-08-26 | Decided |
| 2 | Is the desktop fence a hard block or a warning above the threshold? | MJ-03 | Claire Sutton | Before MJ-03 spec | Open |
| 3 | Does an auto-approve floor (band routing to nobody) need an audit record of its own? | MJ-01, MJ-03 | Sonia Marsh | Before MJ-03 spec | Open |
| 4 | Mileage rate source — CRA table per year, or employer-set? | MJ-01, MJ-02 | Claire Sutton | Before MJ-02 spec | Open |

> Also lands here as owned rows: Step 1 context gaps (platform model, tech constraints) and end-to-end variations considered but not cut, plus any §7 coverage item recorded as unresolved.

**Variations considered, not cut into their own job:** A/P as a money destination — a genuinely different backbone (no pay run, no register lock), deferred to M2 rather than hidden inside MJ-04. Per-client approval templates for bookkeeping firms — birchbark's ask, real but a Firm Management concern, not this Value Package.

---

## 7. COVERAGE CHECK

- **Covered:** capture at source, offline tolerance, mileage, claimant-readable status → MJ-02
- **Covered:** employer-configured tiers, position routing, escalation, approval-surface policy → MJ-03
- **Covered:** reimbursement on the pay run, register visibility before lock, lock integrity → MJ-04
- **Covered:** the claim object, its states, site/job coding, the pre-hire state → MJ-01
- **Covered, split:** notifying approvers without company email → MJ-03 (routing decides who) + MJ-02 (in-app badge surface) — the two halves have different actors and different failure modes
- **Explicitly out:** accounts-payable as a money destination — why: a different backbone with no pay-run interaction — M2
- **Explicitly out:** corporate-card feed reconciliation — why: no design partner asked for it — deliberately never in VP2
- **Unresolved — no home yet:** per-client approval templates for firms managing many client books — no Micro Job covers it and no destination is decided — owner: Michelle Tremblay, see §6 (variations)

**Exception List status:** one entry per locked Micro Job. None locked yet; MJ-01's spec carries its named exceptions and the BA extends them at the deep dive.
