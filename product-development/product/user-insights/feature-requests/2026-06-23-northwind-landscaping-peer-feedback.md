---
account: northwind-landscaping
requested: 2026-06-23
area: performance-management
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-06-23-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Request peer and HR feedback on a direct report

**Who asked:** Their Operations Director at Northwind Landscaping, in a discovery interview + prototype review on 2026-06-23.

**The underlying need.** Colleagues and HR who deal with an employee regularly hold context a single manager does not. He wants to solicit that input into a review at the click of a button rather than by chasing it. Critically, this is **manager-solicited input on his own reports** — not employee-to-employee 360 feedback, and not visibility into other managers' evaluations, a line he drew himself and firmly.

**What they do today.** Nothing systematic — *"Unless you're doing some kind of group Teams chat thing? No, typically it's not."* He gathers it informally when he wants it and is entirely comfortable doing so, which is exactly why the signal is convenience rather than blockage.

*"And if you can ask for it from peers, then that would be even better."* — Their Operations Director

*"So if I've got… let's say I've got a plant manager that works for me, and I want to get information from… but I also want to get some feedback from our HR department. Being able to get that would be very value-added."* — Their Operations Director

*"No, not at all, not at all. I am more than comfortable and happy to get that information where I feel it's appropriate. Um, having it at the click of a button."* / *"It's convenient."* — Their Operations Director

*"Do I want to see somebody else's evaluation of another employee? I don't think it's appropriate."* — Their Operations Director

**Signal strength: moderate, and contested at the account.** He wants it and can already get it informally, so the gain is convenience. More importantly, the initiative already records that Northwind's HR Manager — the buyer — declines peer and 360 feedback. This record is the manager-side evidence in that split; the confidentiality boundary he drew is a requirement in its own right and should travel with any build.

## Draft ticket

**Objective:** Let a reviewing manager request feedback on a direct report from named colleagues or HR, with responses attached to the review and bounded by explicit visibility rules.

**Acceptance criteria seed:**
- A reviewing manager can request feedback on a direct report from one or more named colleagues or HR contacts.
- The request is a simple prompt with a free-text response; the responder is not asked to rate the employee.
- Responses are attached to the review and visible to the reviewer and the review's approver.
- Requesting feedback never exposes another manager's evaluation of any employee to the requester.
- Whether a responder's identity is visible to the reviewer is configurable by the account.
- Peer feedback can be switched off entirely at account level, since the HR buyer at this account does not want it.
- The employee under review does not see raw responses unless the account explicitly enables it.
