---
initiatives: [expense-management-vp2]
areas: [expense-management]
---

MICRO JOB  |  Payworks  |  Expense Management VP2  |  MJ-01

# MJ-01 — Claim record and site coding

| Field | Detail |
|-------|--------|
| **Product / module** | Expense Management |
| **Initiative** | [Expense Management VP2](../../initiatives/expense-management-vp2.md) |
| **Release** | VP2 · M1 |
| **Breakdown** | [expense-management-vp2-micro-jobs-breakdown.md](expense-management-vp2-micro-jobs-breakdown.md) |
| **VP Product Brief** | [expense-management-vp2-product-brief.md](expense-management-vp2-product-brief.md) |
| **Type** | Net new |
| **Author** | Claire Sutton, PM |
| **Date** | 2026-08-29 |
| **Status** | Draft |

**Evidence key:** `[Evidenced]` source named · `[Partial]` signal, not proof · `[Hypothesis — needs validation]`

---

## 1. DESCRIPTION

The claim object and its lifecycle: what a claim *is*, what states it moves through, and how a site or job code binds to it at creation and survives into payroll coding without a reconciliation step.

**The outcome:** a purchase made in the field arrives at finance already coded to the job it belongs to, so nobody reconstructs it later.

## 2. USER STORY

When I buy something for a job, I want the record to carry the site it was for from the moment it is created, so I am not asked to recall it three weeks later.

## 3. THE SLICE

Creating, storing and transitioning a claim — including its site/job code, its amount, its optional image reference, and its pre-hire-capable claimant link. **Not** the capture screen (MJ-02), the routing engine (MJ-03), or the pay-run posting (MJ-04). This job is the object those three read.

**Preconditions:** the shared employee record exists (it does — same database as payroll). This job must not re-implement it.

## 4. VARIATIONS — WHO DOES THIS DIFFERENTLY

**Variation verdict:** two variations found; neither becomes its own Micro Job.

- **Mileage claims** carry no image and compute amount from kilometres × rate — a different *shape* of the same object, handled as a claim type, not a branch `[Evidenced]`.
- **Pre-hire claimants** (employee-onboarding's case) have no employee number yet. Handled as a value on the existing claimant-state axis, not a second record — the 2026-08-26 decision turned on exactly this: MJ-01 already carries an "unposted" state built after a real VP1 support case where a new hire expensed a hotel before their first pay run `[Evidenced]`.

## 5. HAPPY PATH

1. A claimant creates a claim with an amount, a site/job code, and either an image reference or mileage inputs.
2. The claim is stored in `submitted` state, bound to the claimant and to the site code.
3. The site code is validated against the employer's active site/job list.
4. The claim becomes readable by the routing engine (MJ-03) and by the claimant's status view (MJ-02).

**Capabilities this job does not answer — flagged, not invented:** how the claimant enters any of this (MJ-02), who approves it (MJ-03), how it becomes money (MJ-04).

## 6. ALTERNATE FLOWS

- **Mileage instead of a receipt** — no image, amount computed from kilometres × the applicable rate.
- **Held offline** — a claim created without connectivity exists on device and enters `submitted` on sync; it must not be creatable twice by a retry.

## 7. ROLES & PERMISSIONS

| Role | Can |
|------|-----|
| Claimant | Create a claim; read their own claims |
| Approver (position) | Read claims routed to their position |
| Payroll Administrator | Read claims attached to a run they own |
| Administrator | Configure the site/job list |

## 8. RULES & ACCEPTANCE CRITERIA

- **R1.** A claim cannot exist without a site/job code. *AC:* Given a claim creation request with no site code, when it is submitted, then it is rejected with the missing field named.
- **R2.** A site code must be on the employer's active list at creation time. *AC:* Given a code not on the active list, when a claim is created, then creation fails and the claimant is told which field is wrong.
- **R3.** A claim's site code is immutable after approval. *AC:* Given an approved claim, when a site-code change is attempted, then it is refused and the attempt is recorded.
- **R4.** A claimant without an employee number can hold a claim in `unposted`. *AC:* Given a pre-hire claimant, when a claim is created, then it is stored in `unposted` and is not eligible for a pay run until an employee number exists.
- **R5.** Offline sync is idempotent. *AC:* Given the same device-created claim synced twice, when the second sync arrives, then exactly one claim exists.

## 9. CONSTRAINTS

`[GAP: platform model unfilled — constraints unverified]`
`[GAP: tech constraints unfilled — feasibility unverified]`

## 10. CROSS-CUTTING CONCERNS

- **Localization:** site/job names are employer-entered, not translated. Currency is CAD only in VP2.
- **Audit:** every state transition is recorded with actor and timestamp — required because R3 refusals must be provable.
- **Privacy:** a claim image may contain incidental personal information; retention follows the employer's existing document policy `[GAP: retention period unconfirmed — Legal to confirm]`.

## 11. NAMED EXCEPTIONS

**PM-initiated list, expected to be incomplete — the BA extends it during the deep dive with implementation-level exceptions:**

| # | Exception | Expected handling |
|---|-----------|-------------------|
| E1 | Site code valid at creation, deactivated before approval | Claim stays valid; the code is retained as recorded |
| E2 | Image reference resolves to nothing | Claim remains, flagged for the claimant to re-attach |
| E3 | Two claims, same amount, same site, same minute | Both stored; deduplication is a human judgment, not a system one |

## 12. EDGE CASES

- A claim created in one payroll period and approved in another (named; MJ-04 owns the roll-forward).
- An employer with exactly one site — the code is not meaningfully a choice.

## 13. SCOPE PRIORITIES & GROUNDING

| Priority | Item | Grounding |
|----------|------|-----------|
| Must | Site/job code bound at creation | 2.5 days and ~400 lines of month-end reconstruction; $3–4k/yr written off `[Evidenced]` |
| Must | Immutability after approval | Money-adjacent — auto-Must |
| Must | Pre-hire `unposted` state | Decided 2026-08-26; employee-onboarding depends on it `[Evidenced]` |
| Should | Idempotent offline sync | Field crews with intermittent signal `[Partial]` |

## 14. OPEN QUESTIONS & RESEARCH NEEDED

| # | Question | Owner |
|---|----------|-------|
| 1 | Mileage rate — CRA table per year, or employer-set? | Claire Sutton |
| 2 | Does an auto-approve floor need its own audit record? | Sonia Marsh |
| 3 | Image retention period | Legal |

## 15. ENGINEERING CONFIRMATIONS NEEDED

- Can the existing employee record carry an `unposted` claimant without a schema migration on payroll? A read-only job answers "not applicable: this job writes nothing" — this one writes, so an answer is required.
- Is the site/job list an existing entity anywhere in the platform, or net new?
- Idempotency key strategy for offline sync.

## 16. TELEMETRY PLAN — HOW WE'LL KNOW IT WORKED

> **A threshold with no baseline is an invented number.**

| Measure | Target |
|---------|--------|
| Claims created with a valid site code on first attempt | `[GAP: threshold unset — no baseline; Sonia Marsh sets it from first-cohort data before dev-ready]` |
| Duplicate claims surviving offline sync | 0 — hard requirement, not a target |
| Month-end reconstruction time at a pilot account | Baseline 2.5 days (Northwind, 2026-08-27) `[Evidenced]`; target set after cohort 1 |

## 17. DEPENDENCIES & NOTES

- **Depends on:** nothing. MJ-01 is the foundation job.
- **Depended on by:** MJ-02, MJ-03, MJ-04 — and, per the 2026-08-26 decision, employee-onboarding's employee-profile foundation. A named extension seam lets onboarding add fields without an expense release.

## 18. EXCEPTION LIST — WHAT'S OUT OF SCOPE

**Exclusion verdict:** three items were considered and excluded.

- Corporate-card feed reconciliation — no design partner asked for it.
- Multi-currency claims — CAD only in VP2.
- Receipt OCR / amount extraction — capture accuracy is MJ-02's problem, and birchbark's bookkeeper was explicit that she needs to see and question any machine guess `[Evidenced]`.
