---
account: northwind-landscaping
requested: 2026-07-10
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-07-10-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Site- and manager-level configurable review templates

Northwind Landscaping's **site supervisor** raised template configuration unprompted, twice,
while walking the Performance Management prototype's review screen. His sites differ
operationally — some take soil, some have a depot for brush and green waste, some take
neither — so a single company-wide question set under-fits by construction. He had already
hit this on paper: the template he downloaded was not written for his job, and he had to
explain the gaps out loud in every review conversation.

The second half of the ask matters as much as the first: **he wants managers, not HR, to own
the configuration**, on the grounds that HR is not on site and does not see operational
change as it happens — with supervisors helping, because supervisors are the most hands-on
level.

*"Yeah, like, I was gonna say this one here, like, would I be able to change that and be
like, um…"* / *"uh, I don't know, like, organization of pallets, or, like, things like that,
and then we could go in and… like, would that be something we could change as we're
reviewing, or are these set in stone, and then when we go into our reviews, we just have to
score them down the columns?"* — Their Site Supervisor

*"So, there may be, like, a secondary set of questions or something that they may need to
have, like, site specifically for Central, and going forward to the other sites."* — Their
Site Supervisor

*"I think managers… I think managers would be best at that, because HR is not here every
day, they don't know the changes up to date as much, so I think a manager would definitely
be better if they could, uh…"* / *"Kind of fine-tune it to their site."* — Their Site
Supervisor

*"With, maybe with the help of the supervisor, since we're kind of on hands a little more,
hands-on a little more."* — Their Site Supervisor

**Signal strength.** Strong and unprompted, but note his own hedge on the granularity: *"So,
I don't know, I don't want to say site-specific so much, but it may need to be tailored that
way"*. He is certain the form must vary and certain managers should own it; he is not
certain that "site" is the right axis. Do not read a site-scoped data model into this — read
a requirement that the axis be configurable by someone close to the work.

**Open conflict to carry:** this is a front-line manager arguing for manager-owned
configuration. Northwind's HR side has not been asked the same question, and HR is the buyer
on this account.

**What they do today:** he downloaded a template from the internet and edited it in Microsoft
Word toward his own job descriptions, then explained the remaining mismatches verbally.

## Draft ticket

**Objective:** Let review question sets be varied below the company level and maintained by
managers (with supervisor input), so a review form matches the work actually done at a given
site or department.

**Acceptance criteria seed:**
- A company-level base question set can be extended or overridden by a secondary set scoped
  below the company — the scoping axis (site, department, position) is a design question, not
  settled by this evidence.
- Configuration is permissioned to a manager role, not only to HR/company admin; a supervisor
  can contribute without needing full admin rights.
- Changing a template does not alter reviews already in flight or already completed.
- Per-question rating definitions (filed separately the same day) travel with the question
  into every variant set.
- The employee's review shows only their applicable question set — no empty or
  not-applicable categories from another site's work.
