---
date: 2026-06-23
customers: [northwind-landscaping]
areas: [performance-management, human-resources, payroll]
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# Customer Interview Insights — 2026-06-23

Source: [transcripts/2026-06-23-northwind-landscaping-interview.md](transcripts/2026-06-23-northwind-landscaping-interview.md) — discovery interview + prototype review, Northwind Landscaping, run by Claire Sutton and Vanessa Lee.

## Executive Summary

- **The merit arithmetic is done in the manager's head, and he wants the product to do it.** Their Operations Director already converts a review score into a recommended increase by hand every cycle: score-as-a-percentage × the company-approved increase percentage. He asked for exactly that to be automatic, with an override for exceptions inside the group budget. This is the clearest statement of the merit-calculation mechanics in the Northwind corpus, and it is the front half of the chain that ends in a payroll upload.
- **He is unambiguously for weighted category scoring** — weights set by category tier (turnover, budgets, compliance), a score by area averaged over the total, out of 5. He describes QuickBase as already doing this. This is the buyer-side of the contradiction the initiative page carries: the site supervisor wants a flat average, this director does not.
- **The approval chain he sits in is three-deep and entirely manual at the top:** the pool is capped at the C-suite and cascaded down; his reports recommend to him; he recommends upward on a spreadsheet reviewed at C-level. Separately he named a gap in the *review* chain — no one-up review of a completed review before it is processed — and asked for one.
- **The prototype landed well on substance and failed on one panel.** He navigated it unaided, called the review form *"very comparable to what we're doing"*, and would use check-ins as his note-taker in place of a Word document. The season-at-a-glance panel above the review was the single clear miss — he could not tell where its numbers came from and asked for a drill-down dashboard instead.

## Interviews Conducted

- Number: 1 · Date range: 2026-06-23 · Segments: multi-site grounds maintenance, director-level people leader with site-leader direct reports (Ontario), Payworks payroll/HR customer running performance management in QuickBase.
- Format: ~44 minutes — roughly 15 minutes of discovery, then a hands-on prototype review with the participant driving the mouse.

## Existing Research Context

**No prior research is filed in this repo yet.** `product-development/product/user-insights/` holds no syntheses and no earlier interview reports; the only other artifact in the transcript archive is the 2026-08-05 Northwind reverse-demo transcript, which has no summary layer. The rest of the design-partner corpus is still staged in `product-development/inbox/payworks-source-material/`.

Consequence for this report: **every theme below is labelled NEW.** Nothing here can be marked VALIDATED or CHALLENGED against filed research, because there is none to compare against. Two themes are labelled NEW with an internal-corroboration note — where this single interview corroborates or contradicts itself across its discovery and prototype halves — and those are the only cross-checks available today. Once the remaining records are filed, this report is a candidate for re-labelling by `/user-research-synthesis`.

## Top Pain Points (ranked)

1. **The merit increase is calculated by hand and lives apart from the score that drives it** — 1 of 1 interviews — *"And then I take the 5% times it by 70%, and that's my recommended percentage for their increase."* — Their Operations Director — impact: every reviewing manager repeats the same arithmetic every cycle, and the resulting number is unverifiable against the score because the two never sit together — *"the performance score is recorded in QuickBase as part of the performance evaluation. The overall increase is done manually outside of the QuickBase application."* — workaround: he computes it himself before touching the spreadsheet and enters only the final percentage.
2. **The review system holds no data, so preparation is memory work** — 1 of 1 — *"It doesn't really collect data."* — Their Operations Director — impact: reviewers either keep private records or reconstruct a year from recall; the attendance and documented performance history already sitting in Payworks is not reachable from the review — workaround: he keeps a running Word document of milestones, kudos and issues on each direct report, written *"as needed"*, so *"I don't have to go looking for it."*
3. **Three systems, one review** — 1 of 1 — *"you're pulling information from Payworks, we're pulling information from QuickBase, we're pulling information from Excel, like, yeah, it's not the most efficient method that we're currently using."* — Their Operations Director — impact: context-switching across Payworks, QuickBase and Excel for a single evaluation — workaround: none; he absorbs it.
4. **All manual entry, with cookie-cutter content re-typed per manager** — 1 of 1 — *"Our current application does not do it. It is all manual entry."* — Their Operations Director — impact: site leaders share substantially the same KPIs (no injuries, no environmental compliance issues, meets budget), so the same material is re-entered per person — *"it's something that is kind of copy and paste, but not quite."* — workaround: retyping; he explicitly denied copy-pasting as a clean shortcut.
5. **No one-up review of a completed review before it is processed** — 1 of 1 — *"there should be a two-stage process as well. It should be, if I'm doing it, then my boss should review it before it gets processed, type of scenario, right? Like a one-up review."* — Their Operations Director — impact: a review reaches processing on one manager's judgment alone — workaround: none described. (Note: the transcript line immediately after this ask is garbled — *"There's none of them."* — so read this as a stated requirement, not a confirmed statement of today's state.)
6. **Time, not clicks, is the binding constraint** — 1 of 1 — *"It really just comes down to having time, right?"* — Their Operations Director — impact: he pushed back on the "what's cumbersome" framing; the cost is the hours the cycle consumes, which is why he cares about pre-filled data more than about UI polish — workaround: allocating time deliberately.
7. **No channel to gather colleague or HR input on a direct report** — 1 of 1 — *"Unless you're doing some kind of group Teams chat thing? No, typically it's not."* — Their Operations Director — impact: input he considers legitimate is gathered informally or not at all — workaround: he asks people directly, and is comfortable doing so — *"I am more than comfortable and happy to get that information where I feel it's appropriate."*

## Top Feature Requests

1. **Automatic merit-increase calculation from the review score** — priority: high — requested by 1 (their Operations Director, a recommending manager in the chain) — underlying need: stop re-deriving by hand a number that is already deterministic from the score and the approved pool, while keeping room for the exceptions that real cases demand — record: [feature-requests/2026-06-23-northwind-landscaping-merit-increase-calculation.md](feature-requests/2026-06-23-northwind-landscaping-merit-increase-calculation.md)
2. **Weighted category scoring** — priority: high — requested by 1 — underlying need: an overall score that reflects what actually matters per role rather than treating every category alike — record: [feature-requests/2026-06-23-northwind-landscaping-weighted-category-scoring.md](feature-requests/2026-06-23-northwind-landscaping-weighted-category-scoring.md)
3. **Pre-fill the review from data already in Payworks** — priority: high — requested by 1 — underlying need: end memory-based preparation by surfacing attendance and documented performance history at review time, for the reviewer and the approver above them — record: [feature-requests/2026-06-23-northwind-landscaping-employee-data-prefill-in-review.md](feature-requests/2026-06-23-northwind-landscaping-employee-data-prefill-in-review.md)
4. **One-up review approval before a review is processed** — priority: high — requested by 1 — underlying need: a second set of eyes on a completed review, matching how compensation recommendations already escalate — record: [feature-requests/2026-06-23-northwind-landscaping-one-up-review-approval.md](feature-requests/2026-06-23-northwind-landscaping-one-up-review-approval.md)
5. **Quarterly review cadence option** — priority: medium — requested by 1 — underlying need: more frequent, lighter evidence points so the annual rating rests on data rather than the last quarter's memory — record: [feature-requests/2026-06-23-northwind-landscaping-quarterly-review-cadence.md](feature-requests/2026-06-23-northwind-landscaping-quarterly-review-cadence.md)
6. **Solicited peer and HR feedback into a review** — priority: medium — requested by 1 — underlying need: pull in the perspective of colleagues who work with the employee regularly, without exposing anyone else's evaluation — record: [feature-requests/2026-06-23-northwind-landscaping-peer-feedback.md](feature-requests/2026-06-23-northwind-landscaping-peer-feedback.md)
7. **Drill-down on the review summary panel** — priority: medium — requested by 1 — underlying need: know where a summary number came from before trusting it in a review conversation — record: [feature-requests/2026-06-23-northwind-landscaping-review-summary-drill-down.md](feature-requests/2026-06-23-northwind-landscaping-review-summary-drill-down.md)

## Theme Labels vs Prior Research

- VALIDATED: none — no prior research is filed in this repo to validate against (see Existing Research Context).
- CHALLENGED: none — same reason.
- NEW: merit calculation performed manually by the recommending manager · weighted category scoring preferred over a flat average · review data pre-fill from the payroll/HR record · one-up review approval · quarterly cadence for evidence density · solicited peer/HR feedback bounded by a confidentiality line · traceability and drill-down on computed summary figures · simplicity and reversibility as the adoption gate · AI accepted where it earns its place.

## Recommended Actions

1. File the remaining twelve staged records so these themes can be labelled against real corroboration rather than assumed novel — Owner: Margaret Foster — Due: 2026-09-07
2. Run `/user-research-synthesis` once 4+ interviews are filed, and re-label this report's NEW themes against the cross-account picture — Owner: Margaret Foster — Due: 2026-09-14
3. Carry the weighted-vs-flat scoring split into the Product Brief as a named contradiction with this interview as the weighted-side evidence; do not average the two positions — Owner: Claire Sutton — Due: 2026-09-18
4. Specify the merit-increase calculation as a first-class question for definition — the inputs (score, approved pool), the override path, and where the computed increase is stored relative to the score — Owner: Claire Sutton — Due: 2026-09-18
5. Redesign or remove the season-at-a-glance panel above the review form; test the dashboard-with-drill-down alternative in the next prototype round — Owner: Claire Sutton — Due: 2026-09-11

## Interviews

## Interview — Operations Director, multi-site grounds maintenance (director-level people leader) (2026-06-23)

**Research goal:** Learn how a manager who actually completes reviews in the current system works — what is manual, what data he reaches for, how a review becomes a compensation recommendation — and test an early proof of concept against that reality.

**Hypotheses tested:**
- Managers want employee data carried into the review rather than re-entered.
- An overall calculated score with category weights is useful during review writing.
- Check-ins and continuous feedback fit how managers already work.
- Managers want visibility into how their own reports rate their teams.

**Jobs-to-be-Done:**
When it is review season for my six site-leader direct reports, I want the evidence I have already logged during the year and the data Payworks already holds to be waiting for me in the review, so I can produce a defensible rating and a compensation recommendation without rebuilding the year from memory and a spreadsheet.

### How the merit calculation actually works (verified against the transcript)

He walked the arithmetic three times, consistently. The chain, in his words:

1. The company sets an approved annual increase percentage, **capped at the C-suite and cascaded down** — *"The amount is capped out, decided at the C-level or the C-suite, if you will, and then it's cascaded down."*
2. He converts the employee's review outcome into a **percentage of the maximum** — *"I'm taking what their performance review gives me. Again, so if it's 7 out of 10, it's 70%."*
3. He multiplies the two: **approved percentage × score percentage = his recommended increase percentage** — *"And then I take the 5% times it by 70%, and that's my recommended percentage for their increase."* On his own worked example that is 5% × 70% = 3.5%.
4. He overrides where warranted — *"Unless there's an exceptional circumstance, then I'll modify it accordingly."* — and any override has to fit the group's budget.
5. Only the final percentage is entered. *"it's typically laid out. We just enter in what we think is the appropriate percentage. But for me, I've already done the calculation."*

**Two cautions on the numbers.** The **5% is his own hypothetical** — *"Let's say the annual approved increases for this year is 5%"* — not a stated Northwind pool figure; the account page carries a company merit pool of *"2.5% or 3%"* from a separate record. And he articulates the conversion on a **/10 basis** while describing the QuickBase weighted average as landing **out of 5** — *"the score would be out of 5 as well."* What is consistent across both is the method: the review outcome becomes a percentage of the maximum, whatever the scale.

The account page's recorded quote — *"I take the 5% times it by 70%, and that's my recommended percentage for their increase"* — is **verbatim and correct** as filed.

### The approval chain he sits in

- **Compensation:** pool capped at C-suite → cascaded down → his reports send him their recommendations for their own teams → he sends his recommendations upward → *"It's a spreadsheet. We fill it out, we put in our recommendation, and then it's reviewed at the sea level, if you will."* ("sea level" is the transcription of *C-level*.) He confirmed the handoff target is HR when asked where the number goes.
- **The review itself:** no equivalent second stage exists, and he wants one — *"if I'm doing it, then my boss should review it before it gets processed."* He extended the same logic to the evidence: whoever reviews it *"before it's processed, then they have the visibility to that information as well."*
- **Score vs increase storage:** *"the performance score is recorded in QuickBase as part of the performance evaluation. The overall increase is done manually outside of the QuickBase application."* — *"Correct. And the last part is very manual."*

### Weighted scoring vs a flat average — his position

Asked directly whether a calculated overall score with different category weights would be beneficial, he answered without hedging: *"Yes, there should be, and it should be based on what that tiering looks like, whether it's turnover, budgets, compliance, whatever that category should be. It's a weighted average currently in QuickBase."* He described the mechanic he already has — *"it would be by area and then it would average it out over the total. So and then the score would be out of 5 as well."* — and recognised the prototype as doing the same thing, reading its weighted breakdown aloud off the screen. **The weightings and the summary figure he read out are Payworks mock values on the prototype, not Northwind's own.**

### Reaching payroll

He never describes what happens after the signed recommendation leaves him — no pay run, no extract, no effective dating, no retro pay, and the word "payroll" does not appear in the transcript. His chain ends at *"reviewed at the sea level"* and the handoff to HR. The increase he computes is a real wage increase, but this record does not narrate it becoming pay.

**Pain points:** (severity + current workaround for each)
- **Merit increase calculated by hand, stored apart from the score** — severity: high — workaround: he does the arithmetic himself and enters only the resulting percentage<br>
  *"And then I take the 5% times it by 70%, and that's my recommended percentage for their increase."* — Their Operations Director
- **The review system collects no data** — severity: high — workaround: a private running Word document of milestones, kudos and issues per direct report<br>
  *"It doesn't really collect data."* — Their Operations Director
- **Everything is manual entry in an "online spreadsheet"** — severity: high — workaround: retyping cookie-cutter KPI content per site leader<br>
  *"our system is archaic. It's painful to use at best"* — Their Operations Director
- **Three systems for one review (Payworks, QuickBase, Excel)** — severity: medium — workaround: none; he absorbs the switching<br>
  *"it's not the most efficient method that we're currently using."* — Their Operations Director
- **No one-up review before processing** — severity: medium — workaround: none described<br>
  *"there should be a two-stage process as well."* — Their Operations Director
- **No route to colleague or HR input** — severity: medium — workaround: informal direct asks<br>
  *"Unless you're doing some kind of group Teams chat thing? No, typically it's not."* — Their Operations Director
- **Time is the real cost** — severity: medium — workaround: deliberate time allocation<br>
  *"It really just comes down to having time, right?"* — Their Operations Director

**Feature requests:** (underlying need, not just the ask)
- **Automatic merit-increase calculation with an exception override** — underlying need: the number is deterministic from the score and the pool, so deriving it by hand every cycle is waste — and the exception path has to survive automation, bounded by the group budget — priority signal: must-have — *"And I think if that was automatic into that, and then being able to make an exception depending upon the rule, right?"*
- **Weighted category scoring, weights by category tier** — underlying need: an overall score whose weighting reflects what the role is actually measured on — priority signal: must-have
- **Pre-fill the review from Payworks data** — underlying need: attendance and documented performance issues already live in Payworks; surfacing them at review time removes the memory work and the searching — priority signal: must-have — *"if they could pull that information in advance, that would be a very beneficial and time-saving approach."*
- **One-up review approval before processing** — underlying need: a completed review should not reach processing on one manager's judgment alone — priority signal: must-have
- **Quarterly review cadence** — underlying need: more evidence points, so the rating is defensible — priority signal: nice-to-have (they run mid-year and year-end today; this is his argument, not their practice) — *"I would argue that quarterly might be beneficial, though."* / *"More data."*
- **Solicited peer and HR feedback on a direct report** — underlying need: colleagues and HR who deal with the person regularly hold context he does not — priority signal: nice-to-have (he can already get it informally and is comfortable doing so) — *"And if you can ask for it from peers, then that would be even better."*
- **Drill-down on computed summary figures** — underlying need: traceability — he will not use a number he cannot trace — priority signal: nice-to-have — *"If I can click on it and see where the information's coming from, absolutely."*

**Pain Points Validated:**
- ✅ Managers want employee data carried into the review rather than re-entered — he opened the interview with it, unprompted, before any prototype was shown.
- ✅ A calculated overall score with category weights is wanted — answered directly and affirmatively, and it matches what QuickBase already does for them.
- ✅ Check-ins fit how he already works — he would use them as his note-taker in place of a Word document and email: *"I would say utilizing this as a note taker."* He also endorsed the prompting: *"And these check-in pieces, those are good. Having them prompt you is good."*
- ❌ Managers want visibility into how their reports rate their own teams — flatly rejected: *"Do I want to see somebody else's evaluation of another employee? I don't think it's appropriate."* What he wants instead is solicited input on his own reports, which is a different feature.
- ❓ Whether the season-at-a-glance panel has a salvageable purpose — he could not tell what it was for, and volunteered the caveat that he was seeing it cold: *"Yeah, I'm shooting blind here right now, right? So I'm coming into this pretty cold, right?"* Needs a second look with a warmer participant before concluding the concept is wrong rather than the execution.

**Theme labels:** {NEW: manual merit calculation by the recommending manager — first surfaced here; recommend probing at every account with a merit chain} {NEW: weighted category scoring preferred, weights by category tier — recommend probing explicitly, since the initiative already expects a split} {NEW: review data pre-fill from the payroll/HR record} {NEW: one-up review approval} {NEW: quarterly cadence for evidence density} {NEW: solicited peer/HR feedback bounded by a confidentiality line — *internally corroborated*: he asked for peer input in the discovery half and independently drew the visibility boundary in the prototype half, so the two halves of this session agree} {NEW: traceability/drill-down on computed figures — *internally corroborated*: raised once about goals, once about the summary panel} {NEW: simplicity and reversibility as the adoption gate} {NEW: AI accepted conditionally, on a value test}

**Quotes to remember:**

*"And then I take the 5% times it by 70%, and that's my recommended percentage for their increase."* — Their Operations Director → use in: Product Brief (the merit-calculation requirement), stakeholder update

*"Yes, there should be, and it should be based on what that tiering looks like, whether it's turnover, budgets, compliance, whatever that category should be. It's a weighted average currently in QuickBase."* — Their Operations Director → use in: Product Brief (the weighted-vs-flat contradiction)

*"there should be a two-stage process as well. It should be, if I'm doing it, then my boss should review it before it gets processed, type of scenario, right? Like a one-up review."* — Their Operations Director → use in: Product Brief (approval workflow)

*"It has to be easy for the person doing it. If it becomes complicated or cumbersome, then it will fall apart."* — Their Operations Director → use in: Product Brief (adoption risk), presentation

*"you're pulling information from Payworks, we're pulling information from QuickBase, we're pulling information from Excel, like, yeah, it's not the most efficient method that we're currently using."* — Their Operations Director → use in: stakeholder update (the consolidation case)

*"Do I want to see somebody else's evaluation of another employee? I don't think it's appropriate."* — Their Operations Director → use in: Product Brief (visibility and confidentiality rules)

**Surprises:**
- **He pushed back on the pain-point framing.** Asked what was cumbersome, he answered *"That's a tricky question to answer. It's just time, really"* — and asked whether he copy-pastes, he said *"Nope."* The waste he cares about is preparation and re-derivation, not clicking. A brief that optimises the form and not the inputs would miss him.
- **He declined to let the self-review move him before the conversation** — *"No, because I think in that scenario, it's important to have that conversation."* — on the principle that *"if you get into a review and there's a shock on either end, I haven't done my job right."* That is an argument against surfacing self-ratings side-by-side as a nudge, and worth setting against other participants who may want exactly that.
- **He drew the peer-feedback boundary himself,** unprompted, immediately after asking for peer feedback — wanting solicited input from colleagues and HR while refusing to see another manager's evaluation of another employee. The feature and its constraint arrived in the same breath.
- **The one panel he could not read was the one summarising the person.** Everything transactional — the form, ratings, comments, goals, check-ins — he understood without help; the synthesised overview was the thing that lost him.
- **He volunteered an AI position with a value bar attached:** *"If I can use AI to help me get something done faster, I'm gonna use it"* — immediately qualified by *"I don't want to do it just because it fits in there. That doesn't make any sense, right? It has to make sense, it has to have value."*
- **He treats guidance copy as a feature, not decoration** — he singled out the prototype's rating guidance approvingly: *"Descriptive, right? Tangible example, right? Required for top or bottom rating."* / *"Those are important things."*
- **His stated accessibility requirement is undo, not training** — *"Oh no, I hit one instead of five. How do I get back to that, right?"* — raised on behalf of colleagues rather than himself: *"Not everybody has the same level of confidence and comfort when using technology."*

> **Prototype mock data notice.** The prototype screens carry Payworks-invented employee names, a mock company, sample goals and sample figures (including the weighting split and summary score he read aloud). None of them are Northwind facts, and none are recorded as such anywhere in this report. Where he reacted to a mock value, the reaction is recorded and the value is not.
