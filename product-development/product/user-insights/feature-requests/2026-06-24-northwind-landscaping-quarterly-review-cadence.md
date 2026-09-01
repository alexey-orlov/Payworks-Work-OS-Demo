---
account: northwind-landscaping
requested: 2026-06-24
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-06-24-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Quarterly review cycle, same format as the annual one

**Who asked:** their Site Operations Manager at `northwind-landscaping` — a front-line
people-manager running a multi-site grounds-maintenance operation, four review subjects this
cycle (two last cycle). Design-partner discovery interview, 2026-06-24.

**The underlying need.** He is not asking for more reviews; he is asking for a shorter gap
between something happening and it being on the record. Today his account runs two cycles —
mid-year and annual — and everything he notices in between lives only in a private
spreadsheet on his own computer. A quarterly beat is his proposal for closing that gap so
that anything glaring gets *"documented, brought to attention on their performance"* near the
event rather than at year end. He explicitly does **not** want a different, lighter artefact:
asked whether quarterly reviews would follow a different format, he said *"Uh, no, similar
format."* — self-review, manager review, then the discussion.

**Signal strength.** Moderate, but the cleanest signal in the session. This was his own,
unprompted answer to the direct question "what pain points do you have with the current
system" — the only thing he named. He proposed it tentatively (*"maybe just…"*) and did not
press it. He is also a first-cycle reviewer, so he has one round of experience behind the
opinion, not several. Weight it as a real, manager-originated cadence ask from one manager at
one account, not as a validated requirement.

**What he does today instead.** Two cycles a year, plus constant informal contact — twice-daily
verbal check-ins that produce no record — plus his own spreadsheet.

**Why it matters beyond cadence.** He connected cadence to review effort himself: with a
quarterly beat, the accumulated material he has to work through each time gets smaller — *"if
it is a quarterly review, the check-ins won't be — it won't be as long of a list."* Cadence
and per-review workload are the same problem for him, and his workload is doubling.

*"a quarterly review instead of the yearly one, because it'd be a lot easier… I know we do the six-month, but it might be easier if it's every quarter, just to kind of keep up with the performance." — Their Site Operations Manager*

*"documented, brought to attention on their performance." — Their Site Operations Manager*

## Draft ticket

**Objective:** Let an administrator configure the review cycle frequency — annual, semi-annual
or quarterly — so a company can run a shorter beat without changing the review artefact or the
workflow around it. Cadence at this account is currently set by HR, not by managers, so the
setting belongs to the admin surface while the demand comes from the manager tier.

**Acceptance criteria seed:**
- An administrator can create review cycles at annual, semi-annual and quarterly frequency,
  and the same review template, rating scale and workflow apply at every frequency.
- A quarterly cycle produces the same three steps as today's cycle — employee self-review,
  manager review, and the manager/employee discussion — with no reduced or alternate form.
- Changing the configured cadence does not alter, invalidate or orphan review records
  completed under a previous cadence; year-over-year comparison of goals still resolves across
  cycles of differing length.
- Managers see the cycles they owe reviews for, and their due dates, without being asked to
  choose or configure a cadence themselves.
- Open for definition — carry to the Product Brief, do not decide here: whether cadence is set
  per company, per division or per employee population; and whether every cycle in a year
  carries equal weight into any downstream compensation step.
