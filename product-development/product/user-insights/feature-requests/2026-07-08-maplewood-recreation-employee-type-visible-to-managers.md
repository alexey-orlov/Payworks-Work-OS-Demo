---
account: maplewood-recreation
requested: 2026-07-08
area: performance-management
type: improvement
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-08-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Employee type (seasonal vs permanent) visible to the manager

**Who asked:** their Payroll Manager, unprompted, while their HR Business Partner was exploring
the review-cycle setup screen (2026-07-08).

**Underlying need.** The permanent/seasonal split decides which review form applies and whether
the review is mandatory at all — and managers routinely cannot tell which of their own people
are which, particularly after turnover. Any cycle that asks a manager to pick a form, or that
holds them to a mandatory review, has to tell them who they are looking at.

*"Because my thought is, some managers don't even know if their employee that they're talking about is a seasonal employee versus a permanent employee." — Their Payroll Manager*

*"I have to give some of them a list of their permanent employees, because they just… And sometimes it's just because there's new, because of turnover." — Their Payroll Manager*

**What they do today instead.** The Payroll Manager manually sends managers a list of their
permanent employees.

**Signal strength.** Moderate — stated as a fact about their managers rather than as a demand,
and Margaret Foster converted it into the requirement on the call (*"that means that that
information needs to be clearly available to those managers"*). It is a dependency of the
two-form-types record rather than a standalone want, but it is real, recurring, and currently
absorbed as manual work by payroll.

## Draft ticket

**Objective:** Show employee type (permanent / seasonal, or the company's own equivalent
classification) wherever a manager sees their team in the review flow.

**Acceptance criteria seed:**
- The manager's team roster shows each employee's type.
- The type drives which form template the review uses, without the manager choosing manually.
- Whether the review is mandatory for that employee is visible to the manager.
- The classification is read from the existing employee record, not re-entered.
