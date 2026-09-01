---
updated: 2026-08-31
areas: [payroll, human-resources, employee-self-service]
features: []
initiatives: []
---

# Acme Corp (acme-corp) — Account Context

> **Synthetic account, now with one real record.** Acme Corp began as the worked example
> Payworks uses in its own proposal material: a 75-employee Canadian business with one HR
> Manager and one Payroll Administrator. It exists here so the **Administrator** and
> **Manager** personas have a small, uncomplicated customer voice to speak through,
> against a design-partner set that skews large and multi-site. **The firmographics below
> are still illustrative** — treat them as the shape of the account, not as findings. The
> 2026-08-20 expense discovery call in History IS a filed research record, and anything
> sourced to it is evidence like any other.

## Who they are

- **75 employees** across a head office and one satellite location in Ontario; semi-monthly payroll. The whole company sits inside one Payworks account with one pay group.
- **Two people run everything people-related:** an **HR Manager** who owns records, onboarding, benefits and the review cycle, and a **Payroll Administrator** who owns the run, remittances and year-end. There is no HR business partner layer, no compensation committee and no analytics function — the pair are the whole back office.
- Managers are working managers: they approve time off and sign reviews between doing their own jobs. Nobody has a second screen open on an HR system all day.
- Vertical, size band and ARR in [portfolio.yaml](../portfolio.yaml) are illustrative — see the conventions block at the top of that file.

## Current truth

- **Modules in use:** Payroll, Human Resources and Employee Self Service. No Time Management, no Absence Management, no Workforce Analytics — the multi-module expansion path the FY27 test measures (32% → 35%) is entirely open here.
- **The value they buy is "one system, no rekeying."** At 75 employees a second system is not a tooling decision, it is a second job for someone who already has one. Every requirement this account generates should be read through that: if a capability needs configuration before it produces value, the HR Manager will not reach it.
- **How they represent the base:** the segmentation matrix puts 59.7% of active accounts under 20 employees and 32.8% between 20 and 99 — Acme sits in the second band, and the *shape* of that band (one generalist administrator, no specialist functions) is what most of the customer base actually looks like. Design-partner input from Northwind, Harbourview, Maplewood and Cascadia is louder but not more typical.
- **Use it as a check, not as evidence.** Where a Product Brief or a demand ranking needs a small-customer view, this page supplies the shape of the account; it does not supply findings. Anything stated as customer signal has to come from a filed research record.

## History

- 2026-08-20 — Expense discovery call, account-initiated after expenses came up twice on the quarterly check-in — a listening call, nothing demoed. Receipt formats, approval thresholds, reminders and pay-statement detail, from the HR Manager and Payroll Administrator → [summary](calls/summaries/2026-08-20.md) · [transcript](../../../user-insights/transcripts/2026-08-20-acme-corp-call.md)
