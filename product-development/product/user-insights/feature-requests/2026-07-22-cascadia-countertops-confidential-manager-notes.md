---
account: cascadia-countertops
requested: 2026-07-22
area: human-resources
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-22-interview-insights.md
features: [performance-and-talent-tracking]
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Human Resources] Confidential manager notes on the employee record, with per-item employee visibility

There is a class of record between nothing-happened and a formal disciplinary action: the
manager noticing a pattern and wanting it documented before it becomes anything. Today that
either goes nowhere or lands on the Discipline tab, which managers avoid because of what
the tab is called and what it implies.

Her requirement is that visibility is decided **per item, not per surface**. A manager's
private early note stays private; anything the employee took part in — a documented
conversation, a warning letter they signed — they must be able to see. She volunteered the
exact Payworks pattern she wants copied: the confidential comment on a time-off request,
where manager and HR can record a concern the employee does not see.

*"So there are just maybe some notes or information from the manager, that the manager wants to record it for themselves or for future things. But if there are any conversations where employee was present." — Their HR Lead*

*"Or, like, the formal disciplinary action, like, warning letter, because there's signature, on there, or they are a part of this process. They should be able to see it." — Their HR Lead*

*"When somebody submits time off requests, that managers or HR has this confidential comments section." — Their HR Lead*

*"So, the same about discipline. There is information that we would like to keep structured under this employee, but it's not…" / "action yet. It's just…" / "Recording and documenting some events, or just not to forget that potentially can lead to something." — Their HR Lead*

**Today instead:** manager emails HR, HR PDFs the email into the employee file and mirrors
it as a Discipline-tab record; some managers avoid the tab entirely —
*"they just don't dare to use the paperwork, because there is a, discipline"*.
**Signal strength:** clear ask with a named in-product precedent and a real workaround cost;
filed nice-to-have because she never made it a condition of adoption.

## Draft ticket

**Objective:** Support dated notes on the employee record whose visibility to the employee
is set per note, following the confidential-comment pattern already used on time-off
requests.

**Acceptance criteria seed:**
- A manager can add a dated note against a direct report without it being a disciplinary action.
- Each note carries an explicit employee-visible flag, set at creation.
- Notes the employee participated in (documented conversations, signed letters) are employee-visible.
- HR sees all notes regardless of the flag.
- Notes are surfaced to the manager while writing that employee's review.
- The surface is not labelled "discipline".
