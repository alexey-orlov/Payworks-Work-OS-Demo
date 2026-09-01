---
account: northwind-landscaping
requested: 2026-06-23
area: performance-management
type: improvement
priority_signal: nice-to-have
tracker_ref: "-"
source: ../2026-06-23-interview-insights.md
features: []
initiatives: [performance-management-discovery]
updated: 2026-08-31
---

# [Performance Management] Make the review summary panel a dashboard with drill-down

**Who asked:** Their Operations Director at Northwind Landscaping, during the hands-on prototype review on 2026-06-23. He was driving the prototype himself and reached the panel unaided.

**The underlying need.** Traceability. He will not rely on a summarised figure he cannot trace to its source — this is the same instinct he showed on goals, where he asked for key components carried into the review with *"the traceability to it."* The season-at-a-glance panel above the review form was the one surface in the whole prototype he could not interpret: he could not tell what it was for or where its numbers came from. His proposed fix was a dashboard he can click into.

**What they do today.** Nothing equivalent exists in QuickBase; this is a reaction to a Payworks prototype rather than a gap in their current tooling.

*"This top box feels a little confusing, to be very honest."* — Their Operations Director

*"I can't figure out where it's coming from and what it's supposed to be doing."* / *"Right? It doesn't — it doesn't — I just don't understand what the purpose of that is."* — Their Operations Director

*"Or maybe more like a dashboard."* — Their Operations Director

*"If I could drill into it, yeah."* / *"Yeah. Yeah. If I can click on it and see where the information's coming from, absolutely."* — Their Operations Director

**Signal strength: moderate, with a caveat he raised himself.** He volunteered that he was seeing the prototype cold — *"Yeah, I'm shooting blind here right now, right? So I'm coming into this pretty cold, right?"* — so this may be an execution problem rather than a wrong concept. Retest before concluding the panel should be cut. Every value on the panel is Payworks mock data.

## Draft ticket

**Objective:** Rework the summary panel above the review form so every figure it shows is traceable to its source, presented as a dashboard the reviewer can drill into.

**Acceptance criteria seed:**
- Each figure on the panel states what it measures and the period it covers.
- Clicking a figure opens its underlying source — the goal, the check-in, the record it was derived from.
- The panel makes clear which values are the employee's self-reported input and which are system-derived.
- The panel's contents are testable against a warm participant before the concept is judged; retest with a manager who has used the product.
- If a figure cannot be made traceable, it is removed from the panel rather than shown unexplained.
