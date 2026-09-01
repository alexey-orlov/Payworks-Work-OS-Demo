---
type: gated-change-proposal
date: 2026-08-31
proposed_by: "Michelle Tremblay"
target_file: product-development/feature-index.yaml
status: pending
---

# Proposal: Add Expense Management Features to Catalog

## What

Add two new feature entries to the `expense-management` area in `feature-index.yaml`:

```yaml
expense-management:
  features:
    mobile-claim-submission:
      status: live
      shipped: 2026-08-21
      description: >
        Employee submits an expense claim on a mobile device; first approval step
        available on mobile. Limited launch group only.
    expense-approval-workflow:
      status: planned
      description: >
        Configurable approval chain with threshold routing ($5k default), cross-module
        integration with Payroll for payment posting, and accountant-and-bookkeeper
        channel view. VP2 target.
```

## Why

`expense-management` currently has `features: {}` — the area exists in the catalog but no
features are enumerated. VP1 has shipped; that entry should reflect it. VP2 has a scoped
feature in definition; adding a `planned` entry now makes it findable by
`/prioritize-requests` and the OS Console before the launch gate fires.

## Why this is gated

`feature-index.yaml` is a gated file — only `/feature-launch-gate` writes `status: live`
entries, and structural changes to the catalog require the steward's explicit approval.
This proposal follows the gated-change path: filed here so the steward can review and
apply with an in-session yes.

## How to apply

1. Open `product-development/feature-index.yaml`.
2. Find the `expense-management:` area block.
3. Replace `features: {}` with the YAML above.
4. The launch-gate verdict for `mobile-claim-submission` was not recorded (VP1 shipped
   before the OS was populated) — accept the `shipped: 2026-08-21` date as the record.

## Related

- [expense-management-vp1](../../product-development/product/initiatives/expense-management-vp1.md)
- [expense-management-vp2](../../product-development/product/initiatives/expense-management-vp2.md)
- [2026-08-06-expense-approval-threshold](../../product-development/product/decisions/2026-08-06-expense-approval-threshold.md)
