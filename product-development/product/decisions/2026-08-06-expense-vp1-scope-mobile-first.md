---
date: 2026-08-06
status: Active
initiatives: [expense-management-vp1, expense-management-vp2]
areas: [expense-management]
docs: [product-development/product/initiatives/expense-management-vp1.md]
---

# Expense VP1 Scope — Mobile-First Over Desktop Parity

**Decided by:** Michelle Tremblay (product lead), with Claire Sutton and the Expense Management discovery team

**Decision:** Expense Management VP1 ships mobile-first — claim submission and the first
approval step delivered as a mobile experience — rather than as a desktop-parity release
or a responsive-web build. General availability, the accountant-and-bookkeeper channel
view, and the accounts-payable / payroll boundary work are all deferred to VP2.

**Why:** The core submission moment — an employee capturing a receipt and submitting a
claim — happens away from a desk. A desktop-first build would be technically complete but
behaviourally wrong: it would reproduce the same friction (manual re-entry after the fact)
that makes current expense processes painful. Mobile-first forces the team to solve the
hard problem — lightweight submission, fast approval — before adding surface area, and it
gives VP1 a signal clean enough to act on: if mobile submission doesn't land well with a
limited group, desktop parity won't fix it. The decision also keeps VP1's scope small
enough to ship and learn from before VP2 commits to a broader rollout.

**Options considered:**

1. **Desktop-parity first** (rejected) — matches the form factor of today's Payworks
   sessions, but misses the submission moment entirely; employees who expense on the road
   would still photograph receipts and re-enter them at a desk.

2. **Responsive web (single build, both surfaces)** (rejected) — reduces the VP1 scope
   discipline; a responsive build sized for desktop tends to ship as desktop-plus-pinch-
   zoom, not a true mobile experience. Deferred to VP2 consideration.

3. **Mobile-first VP1, desktop in VP2** ← **chosen** — clear scope boundary, real signal
   from the hardest use case, and VP2 inherits a tested mobile foundation rather than
   retrofitting one.

**Tradeoff accepted:** Administrators who primarily work at a desk get no Expense
Management interface in VP1. The limited-group launch deliberately targets mobile-primary
users; desk-centric workflows wait for VP2. Any feedback that the VP1 surface is
*insufficient for approvers* is expected and is a VP2 scope input, not a VP1 patch.

**Revisit conditions:** If VP2 research consistently shows that mobile-first created
adoption barriers for the accountant-and-bookkeeper channel (their primary surface is
desktop), the VP2 build should treat desktop as the primary surface and mobile as the
companion — reversing the VP1 priority for that persona.

**Related:** [expense-management-vp1](../initiatives/expense-management-vp1.md) ·
[expense-management-vp2](../initiatives/expense-management-vp2.md)
