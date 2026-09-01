---
account: northwind-landscaping
requested: 2026-06-23
area: performance-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../2026-06-23-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Calculate the recommended merit increase from the review score

**Who asked:** Their Operations Director at Northwind Landscaping — a director-level people leader with roughly six site-leader direct reports across Ontario, who both makes recommendations upward and receives them from his own reports. Raised in a discovery interview + prototype review on 2026-06-23.

**The underlying need.** The recommended increase is already a deterministic function of two numbers the company holds: the employee's review outcome and the company-approved annual increase percentage. He performs that multiplication by hand for every direct report, every cycle, before entering anything — so the calculation is unrecorded, unauditable, and repeated by every recommending manager in the chain. He is not asking for a compensation module; he is asking the review to finish its own arithmetic, and to keep the exception path he relies on for real cases.

**What they do today.** The company-approved percentage is capped at the C-suite and cascaded down. He converts the review outcome into a percentage of the maximum, multiplies it by the approved percentage, overrides where circumstances warrant (within the group budget), and types only the final percentage into a manual spreadsheet that is reviewed at C-level and handed to HR. The score itself stays in QuickBase; the increase is computed and held entirely outside it.

*"Yeah, again, like I said, I'm taking what their performance review gives me. Again, so if it's 7 out of 10, it's 70%."* — Their Operations Director

*"And then I take the 5% times it by 70%, and that's my recommended percentage for their increase."* — Their Operations Director

*"And I think if that was automatic into that, and then being able to make an exception depending upon the rule, right?"* — Their Operations Director

*"Unless there's an exceptional circumstance, then I'll modify it accordingly."* — Their Operations Director

**Signal strength: strong.** Unprompted, stated three times with consistent mechanics, and framed as a preference he already applies rather than a wish — *"Personally, I think if we're gonna use a performance review, it should be tied to it."* The same manual merit chain is the defining pain on the Northwind account page.

**Number caution:** the 5% in his example is his own hypothetical figure, not a stated Northwind pool. He also states the conversion on a /10 basis while the QuickBase weighted average lands out of 5 — the constant is the method (outcome as a percentage of maximum), not the scale.

## Draft ticket

**Objective:** From a completed review, compute and present a recommended increase percentage as (approved increase percentage x review score as a percentage of maximum), with a manager override and the computed and final values stored alongside the score.

**Acceptance criteria seed:**
- An admin can set the company-approved increase percentage for a cycle; it is visible to recommending managers as the basis of the calculation.
- On a completed review, the system derives the score as a percentage of the maximum and shows the computed recommended increase percentage, with the arithmetic visible (inputs, not just the result).
- The manager can override the computed percentage; an override requires a reason and is flagged as an exception.
- Overrides are checked against a group or cascaded budget, and the manager can see the group position while overriding.
- The computed value, any override, and the final recommendation are stored with the review — never in a separate document.
- The scale is configurable: the calculation must hold whether the review scores out of 5 or out of 10.
- Recommendations roll up the reporting chain so an approver sees each report's score, computed value and final recommendation together.
