---
updated: 2026-08-31
areas: [payroll, human-resources, time-management, absence-management, employee-self-service]
features: []
initiatives: [performance-management-discovery]
---

# Cascadia Countertops (cascadia-countertops) — Account Context

> Design-partner account. Every claim below traces to one of the research records listed
> under History. Those records were anonymized on import — company, site and person names
> are fictionalized labels, and customer-side people appear as role titles only. The
> records state *"we are a manufacturing company"* and never name the product line;
> countertop fabrication is the account label assigned at import, not a quoted fact.

## Who they are

- **A manufacturer with multiple branches** — *"we are a manufacturing company"*, and *"I will choose install teams in every branch."* No branch count, headcount or province appears on either record.
- **Three workforces:** customer-facing showroom and sales staff, shop/production people, and **installers** — who are named the most important function in the company twice over: the competency map was built *"for the most important people in the company. For installers."* Roles named include install helper, lead installer, install foreman, laminate installer, polisher, production manager, showroom supervisor and branch manager.
- **Small-company decision-making by design:** *"we don't have, like, compensations banned [bands], because a lot of things depend on a lot of things"* and *"We're not a big corporation."* Departments are still being formalized.
- **Mid-migration onto Payworks from Rippling** — *"we set some goals based on Rippling implementation, but now it's all changed. Now we're implementing new modules."* The Rippling experience shapes their requirements: *"I didn't like their performance management module at all… they are obsessed with cycles."*
- Size band and ARR in [portfolio.yaml](../portfolio.yaml) are illustrative — see the conventions block at the top of that file.

## Current truth

- **In the product today:** payroll (the destination for approved rate changes), the HR employee file with documents and a Discipline tab, time-off requests, time recording, and employee self-service where staff see documents they have signed. **Workforce Analytics and the Report Builder are not licensed** — and that gap is what stops her answering basic questions: *"if, for example, I want to see how many employees have been reviewed or have not been reviewed… I don't have access to this."*
- **Credential tracking is the account's signature problem.** Requirements attach to the position, not the person — first aid, WHMIS, forklift for the roles that need them; office and showroom roles need none. Payworks does fire the expiry alert; everything after it is human: *"we know what the role requires… We kind of manually go in the file and monitor if they have it or not"* and *"after the system gives us… We chase an employee and everything, and then to put it in the system."* Nobody but HR can see or push on a gap — *"they don't have any other means of saying, like, hey. This is still missing."* What she wants is the payroll-warning pattern applied to credentials: *"Your forklift expired, you need to fix it very quickly!"*
- **The CEO approves every raise, one at a time.** A manager initiates, attaches the review and emails the CEO, copying HR — *"the manager should complete the review, and then it's attaching it to the email, and sends email to… to the CEO, and CC me."* HR benchmarks the ask but does not approve — *"I'm a consultant, yeah… Influencer!"* Asked whether the CEO reviews a batch or an individual: *"One at the time… because it's a serious decision about wage increase."* Once approved, HR actions it into payroll; the employee learns officially by an Adobe-signed letter only after the pay period runs.
- **Everything is in dollars per hour, not percentages** — *"we use dollar value, like, 100%"* and *"it's very hard to deal with percentages."* Worked examples from the record: a polisher *"from, I don't know, $25 to $27 an hour"*; an installer at 29 → 30 against a benchmark of *"in between 30 and 32"* for lead laminate installers in other branches; a $2/hr request agreed as $1 now and $1 in a month — staged in what she calls *"my magical spreadsheet"*, an unmanaged system of record for future pay changes.
- **Reviews run on Word forms and paper.** The only stable process is the probationary review; after that managers are expected to evaluate *"at least once a year."* She authored both instruments herself — a general review form and a role-specific **Competency Evaluation Map** with score thresholds (under 500 points is not a fit for the role; over 1,600 is delivering great results). The cost is the point: *"I need to print out this map, they need to fill it in, then I'm taking it, then I'm putting the results, then I'm entering this in [Payworks]… It's so much of, um, admin work that it diminishes the value of this tool."*
- **Mobile is an adoption gate, and it is about managers, not installers.** *"a lot of our managers are constantly on the go"*, but *"Right now, app is strictly for recording times, or time of requests, or whatever, so managers cannot do their stuff."* The one thing she would ship first is note capture after a conversation — *"Take some notes, right away on the phone."* Formal discipline she explicitly wants kept off mobile.
- **Asks beyond the above:** a 1–7 rating scale (*"1, 2, 5 is not enough"*), ad-hoc reviews rather than company-wide cycles, review timing tied to the hire date, composable templates (general questions plus role-specific), conditional workflows to replace the email raise chain, a managed occupation list with job descriptions, wage-increase history shown at the point of recommendation, and comment boxes on every rating.
- **Risks:** manager avoidance is already visible — *"Some managers even… they just don't dare to use the [Payworks]"* — and manager capability is a real constraint: *"majority of managers and supervisors are not good with setting the goals, and it's a huge coaching process."* Any cycle-first design will hit the Rippling scar tissue.
- **Expansion signals:** Analytics and Report Builder are named unprompted as the missing module; performance management has no product footing at all today; and appetite for AI is unreserved — *"I would love… this."*

## History

- 2026-07-22 — Prototype review, employee and manager surfaces: the mobile gate, dollar-value merit increases, and the CEO approval chain in detail → [source record](../../../../inbox/payworks-source-material/2026-07-22-cascadia-countertops-interview-2.vtt) *(staged — summary lands when `/process-meeting` files it)*
- 2026-07-15 — Discovery interview + HR-admin prototype review: credential tracking, the Competency Evaluation Map, and the missing analytics module → [source record](../../../../inbox/payworks-source-material/2026-07-15-cascadia-countertops-interview-1.txt) *(staged)*
