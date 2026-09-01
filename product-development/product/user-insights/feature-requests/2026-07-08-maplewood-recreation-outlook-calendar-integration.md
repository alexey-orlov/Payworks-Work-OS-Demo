---
account: maplewood-recreation
requested: 2026-07-08
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-08-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Recurring one-on-ones written into the Outlook calendar

**Who asked:** their HR Business Partner, with agreement from their Payroll Manager, on the
prototype's check-in screen (2026-07-08).

**Underlying need.** They are a Microsoft-native organisation and their one-on-one cadence
already lives in Outlook — set up once as a recurring series for the whole year. A check-in
tool that schedules outside Outlook creates a second calendar nobody will maintain. When asked
directly whether recurring scheduling was a requirement, the answer was yes.

*"Does it link directly into your Outlook calendar?" — Their HR Business Partner*

*"Probably be handy." — Their Payroll Manager*

*"It's just our organizational behavior. We're very dependent on our outlook, very Microsoft-driven, Office 365, anything in there. Teams, we're a very Teams-oriented organization." — Their HR Business Partner*

*"Can you set up a recurring? Because all my one-on-ones are recurring. I just set up an outlet recurring for the whole entire year." — Their HR Business Partner*

**What they do today instead.** Outlook recurring invitations, personal notes, and a follow-up
email after each meeting that becomes the agenda for the next one — the whole loop runs on
email and calendar.

**Signal strength.** Strong for this account and explicitly confirmed as a requirement when
Margaret Foster asked. Note the scope boundary: the check-in *notes* are the product value they
liked; Outlook is how the meeting gets on the calendar. Both halves are needed for the check-in
feature to be used at all here.

## Draft ticket

**Objective:** Let a manager schedule a check-in — including a recurring series — from the
review surface, with the meeting landing in the participants' Outlook calendars.

**Acceptance criteria seed:**
- Scheduling a check-in creates a calendar invitation for manager and employee.
- A recurring series can be created with a frequency and an end date.
- Rescheduling or cancelling in the product updates the calendar entry.
- Check-in notes remain in the product and are shared between manager and employee.
