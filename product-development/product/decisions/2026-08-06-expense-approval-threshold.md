---
date: 2026-08-06
status: Active
initiatives: [expense-management-vp2]
areas: [expense-management, payroll]
docs: [product-development/product/initiatives/expense-management-vp2.md]
---

# Expense Approval Threshold — $5,000 / 150-Employee Cross-Module Rule

**Decided by:** Michelle Tremblay (product lead), Claire Sutton, with input from the
Controller contact at a design-partner account

**Decision:** The expense approval threshold that triggers an additional approver step is
set at **$5,000 per claim**, and that threshold is treated as a **cross-module boundary
with Payroll** — not a standalone Expense Management configuration. Accounts with 150 or
more employees apply this threshold automatically; accounts below 150 may configure it
voluntarily. The $5,000 figure is the baseline; account-level overrides are supported.

**Why — the $5,000 figure:** The threshold emerged from the Controller conversation as the
practical boundary between routine employee expenses (reimbursed with the next pay run,
no executive review) and material outlays that a Controller or CFO needs to see before
approval. Below $5k, managers approve; at or above $5k, the claim routes to a finance
approver. The figure matches Canadian mid-market controller practice: small enough to
catch travel and equipment purchases, large enough that it does not generate noise on meal
and fuel claims.

**Why — the 150-employee boundary:** Below 150 employees, an owner or GM typically
approves all non-trivial purchases directly, and a hard threshold adds process without
reducing workload — the owner sees everything anyway. At 150+, a delegated approval chain
is both necessary and already expected, and the threshold becomes a genuine control.
The 150-employee line aligns with our segmentation break between "small business" and
"mid-market" and avoids enabling complexity for accounts where it would not be used.

**Why — cross-module into Payroll:** An expense claim above the threshold, once approved,
must post into the correct payroll period and appear correctly on the pay statement.
That boundary cannot be managed in Expense Management alone — the threshold decision
affects when the payment posts, how it is labelled on the stub, and whether it triggers a
remittance adjustment. Keeping the threshold in a shared cross-module configuration
(rather than a per-module setting) prevents the scenario where an administrator sets
different thresholds in Expense Management and Payroll and the two surfaces disagree.

**Options considered:**

1. **No threshold — manager approves everything** (rejected) — viable for small accounts
   but removes a control the Controller audience specifically asked for; any account above
   ~50 employees will expect a second-approver option for large claims.

2. **Threshold in Expense Management only, no Payroll join** (rejected) — simpler to ship,
   but creates the divergence risk described above; any Payroll-side report that reads
   expense amounts would not know to flag large claims differently.

3. **Fully configurable threshold, no default** (rejected) — maximally flexible but
   requires every administrator to configure it on setup; most will not, and the control
   is silently absent. A sensible default that accounts can override is better.

4. **$5,000 cross-module default, 150-employee auto-on, per-account override** ← **chosen**

**Tradeoff accepted:** Accounts under 150 employees who want the threshold must configure
it manually — it is not on by default for them. This means a 120-person company with an
active Controller may not discover the feature without onboarding guidance. Acceptable:
the feature-discovery problem is a VP2 onboarding concern, not a reason to impose
approval complexity on 80% of our accounts by default.

**Revisit conditions:** If VP2 research surfaces consistent demand for the threshold at
accounts below 150 employees (particularly in the accountant-and-bookkeeper channel,
where the bookkeeper may be managing expense approval for clients at any size), lower the
auto-on boundary or remove it.

**Related:** [expense-management-vp2](../initiatives/expense-management-vp2.md) ·
[expense-management-vp1](../initiatives/expense-management-vp1.md) ·
[2026-08-06-expense-vp1-scope-mobile-first](2026-08-06-expense-vp1-scope-mobile-first.md)
