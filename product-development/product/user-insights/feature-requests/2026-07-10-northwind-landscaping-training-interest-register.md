---
account: northwind-landscaping
requested: 2026-07-10
area: employee-self-service
type: feature
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-07-10-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Employee Self Service] Employee "expression of interest" register for training and committee seats

Shown the Performance Management prototype's **Goals** screen, Northwind Landscaping's
**site supervisor** reframed it rather than filled it in. Output targets do not work for his
crew — depot volume swings with the season and with how busy the yard is on a given day, so
"how many pallets have you wrapped" measures the weather, not the person. What he wants in
that space instead is a standing, **employee-declared statement of interest**: who wants
scale training, first aid, forklift, loader tickets, or a seat on the health-and-safety
committee.

The underlying job is a lookup he currently performs on foot. Today he walks the yard asking
who wants to be a first aider. He wants to open a screen and see who has already said so.
Note the ownership: the employee declares it, the supervisor reads it — which makes this an
**Employee Self Service** capability surfaced to managers, not a goal-setting one, even
though it arrived through the Performance Management prototype.

*"Yeah, I think a goal one would definitely be helpful, especially like, even if they could
just put some sort of training that they may want in the future, right? That kind of lets us
management know who's involved, who wants to be involved, who's interested, right?"* — Their
Site Supervisor

*"Uh, I would almost say, like, uh, expression of interest, almost, would be a better, uh,
thing. Like, what are you interested in? What kind of, like, are you interested in some scale
training? Are you interested in first aid? Forklift? Uh, uh, uh, loaders?"* — Their Site
Supervisor

*"at least for me as a supervisor, if I could just come in and go, hey, who's interested? You
know, instead of walking around going, hey, we need a couple first aider guys, is that
something you'd like? If it was just here, I could click in and go, oh yeah, they've already
said that, like, that would be a lot easier for us, for sure."* — Their Site Supervisor

*"That one might be a bit harder to measure, just because, like, the depot, like, it just
depends on how busy they are, so I wouldn't want to be, like…"* / *"How many pallets have you
wrapped today, when some days are slower, some… winter, summer, it varies so much?"* — Their
Site Supervisor (on why output targets do not work)

**Signal strength.** Enthusiastic, specific, and self-generated — he proposed the concept and
named the exact interest categories — but it is one voice from one account, and it is a
reframe of a screen rather than a request against a shipped surface. Its weight is highest as
evidence that the **Goals surface as designed does not fit seasonal field crews**.

**What they do today:** he asks people in person, walking the yard, as the need arises.

## Draft ticket

**Objective:** Let employees record standing interests — training, equipment tickets,
committee seats — on their own record, and let their manager query that list, so staffing a
first-aid or forklift slot does not require asking the yard one person at a time.

**Acceptance criteria seed:**
- The employee enters and maintains their own interests; the manager reads but does not
  author them.
- A manager can list, for their team, everyone who has declared a given interest.
- Interests are a persistent attribute of the employee record, not tied to one review cycle —
  they survive the cycle that captured them.
- Declaring an interest is not a commitment or an approval request; no workflow fires.
- Decide and record whether this lands in Employee Self Service or inside the Performance
  Management Goals surface before either is specified — this evidence supports the capability,
  not the placement.
