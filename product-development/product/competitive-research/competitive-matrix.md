# Competitive Matrix

_updated: 2026-08-31 · owner: Michelle Tremblay_

Capability-level comparison against the tracked competitors — whole-product first, then one table per product area. When a task needs "do they have X / how do we compare on X", this file is the answer; no other file carries the comparison grid.

**What belongs here:** the General (whole-product) table, the per-area capability tables, and the legend that keeps cells honest.

**What does not:** the positioning narrative and win/lose patterns live in [competitive-landscape.md](competitive-landscape.md). SWOT, pricing detail, and recent moves live in `competitors/{slug}/teardown.md`. Who we track is registered in [business-info.md](../strategy/business-context/business-info.md)'s Competitive Landscape.

## Legend & rules

- ✅ full · ⚠️ partial/beta · ❌ absent. Every ⚠️/❌ cell carries a ≤6-word note.
- **— = not established.** An open question, *not* a ❌. Use it whenever no source settles the cell; never infer a ❌ from silence.
- Columns: Us first, then competitors in business-info roster order — same names everywhere.
- Rows are capabilities buyers compare on, not your feature list verbatim.
- Dated facts (prices, launch dates) live in teardowns; cells hold status only.
- Every cell flip cites its source — an intel record or teardown line — in the change that flips it.

## General

Whole-product view — the rows every deal touches.

| | Us | Wagepoint | Dayforce |
|---|-----|-----------|----------|
| Target segment | Canadian SMB, 20–500 EE | — not analysed | Enterprise — our internal label |
| Pricing shape | — no price book in repo | — not analysed | — none published |
| GTM motion | — not established | — not analysed | — inferred implementation-led |
| Standout strength | Canadian correctness + service | — not analysed | Configurable approval graphs |
| Standout weakness | Expense module not in market | — not analysed | No documented first-party T&E |

**Row sources.** Us / target segment + expense: [area-brief-checkins-2026-07-23](../../inbox/payworks-source-material/briefs/area-brief-checkins-2026-07-23.md) (20–500 EE) and `feature-index.yaml` (`expense-management` has no features, "not yet in market"). Us / strength: [business-info.md](../strategy/business-context/business-info.md) Our Positioning; its pricing section is itself a recorded GAP. Dayforce: [teardown](competitors/dayforce/teardown.md), 2026-08-31. Wagepoint has no teardown — every cell is open, not negative.

## Approval workflows — `expense-management` · `payroll`

One table, two areas, on purpose. The 2026-08-31 Dayforce run was scoped to approval workflows *across* expense and payroll, and the findings are the same findings from either side; splitting them into two identical area tables would duplicate the very thing the shared competitors home exists to prevent. Split into `competitive-matrix-{area}.md` files when each area accumulates depth of its own.

| Capability | Us | Wagepoint | Dayforce |
|-----------|-----|-----------|----------|
| Multi-level approval chain by manager level | — not in catalog | — not analysed | ✅ |
| Delegated approver, date-bounded | — not in catalog | — not analysed | ✅ |
| Mobile approval of pending requests | ✅ | — not analysed | ✅ |
| Time-off request approval | ✅ | — not analysed | ✅ |
| Manager approval gate on the payroll run | ✅ per company | — not analysed | ✅ per location |
| First-party expense claim capture + approval | ❌ module not in market | — not analysed | ⚠️ forms, payroll earning, partners |

**Row sources.** Us: `feature-index.yaml` — `mobile-self-service` ("pending approvals handled from a mobile device"), `time-off-requests` ("managers are notified and approve, edit or reject"), `pay-groups` ("run schedule and approval workflow for each company"), `expense-management` (`features: {}`). Dayforce: [teardown](competitors/dayforce/teardown.md) — Routing Nodes, Configure an Approval Delegate for Workflows, Dayforce Mobile HR App, Approve Payroll, all verified 2026-08-31.

**Deliberately not a row: amount-threshold routing.** It is the capability the expense VP2 `$5k` decision turns on, and *neither* side is established — Dayforce's routing documentation describes hierarchy and role recipients with no amount condition, and our own rule is still a proposal. An all-open row would read as a comparison where none exists; the open question is written up instead in the [teardown](competitors/dayforce/teardown.md)'s implications section.

## Maintenance

- **Auto tier** — living page, edit in place, bump `_updated:` on every change; ≤120 lines. If an area outgrows the budget, copy [competitive-area-matrix-template.md](../handbook/templates/competitive-area-matrix-template.md) to `competitive-matrix-{area}.md` beside this file and link it from the area's section — the prefix keeps splits discoverable by the `competitive-*.md` pattern skills read.
- **Refresh:** `/competitor-analysis` (deep analysis fills columns; monthly monitoring flips cells); `/context-update` and `/process-meeting` refresh rows when call-borne intel warrants.
- **Sources:** `competitors/{slug}/teardown.md` · [intel/](intel/) monthly records.
- **Read by:** the same roster as [competitive-landscape.md](competitive-landscape.md) — PRD, strategy, launch, review, and battlecard skills.
