---
account: northwind-landscaping
requested: 2026-08-27
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Expense reimbursement on the payroll register — visible before lock, non-taxable, drill-down to receipt

**Who asked:** Their Controller at Northwind Landscaping.

**The underlying need — the Controller needs to see expenses before he signs the register, not after.** Today expenses route through A/P (EFT run every second Thursday) while payroll runs on the opposite Thursday. The A/P cutoff is Monday noon; receipts that arrive late miss the run and wait a month. The Controller would take expense reimbursement on the payroll register for everyone — but especially for hourly workers who front money on personal Visas and feel the delay acutely. The hard constraint: reimbursements cannot be taxable, cannot appear on a T4, and cannot touch pensionable earnings or EI. The harder constraint: he approves the payroll register and transmits it; expenses that arrive after that lock mean he hasn't actually approved what he signed.

*"For the hourly guys, yes. They're the ones fronting money on a personal card. The salaried people have a company card mostly, so it's not their cash, they don't care as much." — Their Controller*

*"One. It's a reimbursement, it's not income. It cannot be taxable, it cannot show up on a T4, it should not touch anybody's, um, pensionable earnings, EI, none of it. If it does that once we'd have a very bad year." — Their Controller*

*"And two — and this is the one I actually lose sleep over — I approve the payroll register. I look at it, I sign it, we transmit. If expenses can push things into a pay run after I've approved that register, then I haven't approved anything." — Their Controller*

**Register visibility requirements:**
- Expenses appear as a line on the payroll register: employee name → regular pay → overtime → expenses total
- The expenses total must be clickable to drill down to the individual receipts — from the register, not by navigating to a separate module
- The total is visible before the Controller locks the register; once locked, no new expenses can enter that pay run

*"I need to see, on the register, here's your regular pay, here's your overtime, and here's four hundred and twelve dollars of expenses with a link so I can see what they were." — Their Controller*

*"Total on the register, but clickable. I'm not reading six hundred receipts on a register. But when the guy phones and says my expenses are wrong, I need to get to the receipt in one click, not go to another system." — Their Controller*

**Cutoff handling — auto-roll, not rejection.** Payroll cutoff for Northwind is Monday at noon for a Thursday pay date. Expenses submitted after cutoff must roll automatically to the next pay run. The employee must be able to see, in the mobile app, which pay date their approved expenses are targeting ("approved, paying on the eleventh"). This is described as the single change that would eliminate 90% of the Controller's expense-related phone calls.

*"It should roll to the next one. Quietly, automatically, and the guy should be able to see, in whatever app he's got, 'approved, paying on the eleventh.' That's it. That's ninety percent of my phone calls gone." — Their Controller*

**What they do today instead:** A/P runs every second Thursday; payroll runs the opposite Thursday. The gap between an expense event and reimbursement can reach a full month when the receipt arrives late. No visibility into when the claim will pay.

**Signal strength — strong, first-hand, specific.** This is the first record in the corpus stating payroll-register integration requirements from a client-side Controller, and the first to define the lock/visibility constraint as a hard requirement (not a nice-to-have). The non-taxable treatment requirement is a regulatory constraint, not a preference.

## Draft ticket

**Objective:** Let approved expense reimbursements appear on the payroll register as a separate, non-taxable line item — visible before the Controller locks the register, drill-down accessible to individual receipts, and auto-rolled to the next pay date when submitted after cutoff — so the Controller's register approval is meaningful and hourly workers know when their money is coming.

**Acceptance criteria seed:**
- Approved expenses for a pay period appear on each employee's payroll register row as a separate "Expenses" line showing the total for that period.
- The expenses total links to a drill-down view of individual receipts; the drill-down is accessible from the register without navigating to a separate module.
- Expenses are visible on the register before the Controller locks it; once the register is locked, no additional expenses can enter that pay run.
- Expense reimbursements are classified as non-taxable reimbursements: they do not appear on the T4, do not affect CPP pensionable earnings, and do not affect EI insurable earnings.
- Expenses submitted after the payroll cutoff automatically roll to the next eligible pay run; no manual intervention is required.
- The submitting employee can see in the mobile app which pay date their approved expenses are targeting (e.g., "approved, paying on the 11th").
- The cutoff time and the rollover behaviour are configurable by the administrator.
