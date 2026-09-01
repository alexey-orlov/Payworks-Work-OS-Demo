---
status: shipped
note: "Shipped 2026-08-21 to a limited group, mobile-first — kept as the historical record VP2 and its decisions refer back to"
updated: 2026-08-31
owner: "Michelle Tremblay"
areas: [expense-management]
features: []
---

# Expense Management VP1 (A/B 2.0)

## Snapshot

- The first Value Package of the Expense Management module, shipped **mobile-first** to a limited group on 2026-08-21 — the same shape A/B 1.0 used, where VP1 was a small soft launch and VP2 carries the package to general availability.
- **Closed page, kept deliberately.** Two canonical decisions and the VP2 brief refer back to this work; deleting the page would break the "why did we choose that?" trail that makes the decision register useful.
- Filed **retrospectively**: this Value Package shipped before this OS instance was populated, so there is no launch-gate verdict to link and no artifact trail from the time. What survives is the scope, the mobile-first call, and the decisions that recorded it.
- The catalog carries **no feature entries for Expense Management yet** (`features: {}` on the area, described as "not yet in market"). That is correct for a limited launch and is not this page's to change — `/feature-launch-gate` is the only writer of catalog status, and it re-reads the catalog immediately before writing.

## Scope & goal

- **Goal:** get a working expense claim into clients' hands on the surface they actually carry — phones — and learn from a small group before committing the module to general availability.
- **In scope (shipped):** mobile-first claim submission and the first approval step, for a limited launch group.
- **Out of scope (deferred to [expense-management-vp2](expense-management-vp2.md)):** general availability, the accountant-and-bookkeeper channel view, and the accounts-payable / payroll boundary work.

## Instructions

- Closed page — historical record. Edit it only to link a decision or artifact that names this Value Package; do not reopen scope here. Current expense work lives on [expense-management-vp2](expense-management-vp2.md).

## Sources

- [expense-management-vp2](expense-management-vp2.md) — where the work continued
- [strategy/current-quarter.md](../strategy/current-quarter.md) — A/B 2.0 (Expense Mgmt) on the 24-month roadmap, and the wallet-share objective it serves

## Artifacts

- VP Product Brief: -
- Assumption map: -
- Challenge report: -
- Micro Jobs Breakdown: -
- Micro Jobs: -
- Impact sizing: -
- User insights: -
- Competitive analysis: -
- Pre-mortem: -
- Eng plan: -
- Metrics: -
- Experiments: -
- Launch checklist / gate verdict: - *(no gate verdict — shipped before this OS instance was populated)*

## Decisions

- 2026-08-06 — [Expense VP1 Scope — Mobile-First](../decisions/2026-08-06-expense-vp1-scope-mobile-first.md)
- 2026-08-06 — [Expense Approval Threshold](../decisions/2026-08-06-expense-approval-threshold.md)

## Open loops

- None — both pending decisions filed 2026-08-31.

## Activity

- 2026-08-31 — Page filed retrospectively so VP2 and the pending decision records have something to point at.
- 2026-08-21 — Shipped mobile-first to a limited launch group; status set to `shipped`.
- 2026-08-06 — Mobile-first chosen over desktop-first parity and responsive web for VP1 scope.
