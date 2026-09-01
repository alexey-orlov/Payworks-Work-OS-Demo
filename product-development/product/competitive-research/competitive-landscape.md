# Competitive Landscape

_updated: 2026-08-31 · owner: Michelle Tremblay_

The whole-portfolio competitive picture: who we compete with, how the field is positioned, and the differentiation thesis we act on. When a task needs "where do we win, where do we lose, and why us" — this file is the answer; no other file carries the positioning thesis.

**What belongs here:** the tiered competitor list with one line each, the positioning map, the differentiation thesis, and the win/lose patterns with evidence.

**What does not:** who we compete with is *registered* in [business-info.md](../strategy/business-context/business-info.md)'s Competitive Landscape section (confirm tier — names change there first, this page follows in the same session). Capability-by-capability comparison lives in [competitive-matrix.md](competitive-matrix.md). Per-competitor depth lives in `competitors/{slug}/teardown.md`. Account-level loss detail lives in the account's call summaries.

> **State of this page (2026-08-31).** Payworks has never run a portfolio competitive pass. The "Competition landscape" deck is image-only, the strategy decks name no rival, and `business-info.md` records this as the single largest open gap in the business context. One scoped teardown exists (Dayforce, approval workflows). Everything below is either sourced or explicitly marked open — nothing here is inferred to fill a shape.

## Competitors at a glance

Canonical names and tiers, in business-info order. One line per competitor — why they matter, not the full story.

### Direct

- **Wagepoint** — Canadian SMB payroll; described in the Payroll Hub VP2 Product Brief as *"the most frequently cited competitor in win/loss conversations."* The only competitor named in Payworks' strategy material. [GAP: no teardown, no matrix column detail, no capability read — the most-cited rival in win/loss is the one we know least about. Highest-value next analysis.]

### Indirect

- **Dayforce (formerly Ceridian)** — global full-suite HCM; Payworks' own area brief places it as the *"enterprise reference"* rather than a Canadian-SMB rival. Its Canadian statutory depth is real (ROE, T4, RL-1, QPP/QPIP documented), and its approval-workflow engine is the benchmark buyers may have seen. → [teardown](competitors/dayforce/teardown.md) *(scoped to approval workflows; tier proposed by that run, not yet registered in business-info.md)*

### Status quo

- [GAP: not named anywhere in Payworks' material. The nearest stated evidence is the problem statement — disconnected systems and manual bridging. For the adjacent Check-ins area, the internal brief names the real incumbent plainly: *"Word docs and notebooks are the competition, not the absence of a habit."* Whether that generalises to payroll and expense is untested.]

### Named in internal material, not yet registered

Surfaced by the Check-ins & 1:1s area brief (Michelle, 2026-07-23), whose scan was **scoped to check-ins and reviews** — not a portfolio assessment. Listed here so they are not lost; each needs registering in `business-info.md` before it becomes canon.

| Name | Band the brief assigns | Registered? |
|---|---|---|
| Lattice · 15Five · Leapsome | mid-market | No |
| Rise · Humi · Collage · Knit | Canadian SMB | No |

Source: [area-brief-checkins-2026-07-23](../../inbox/payworks-source-material/briefs/area-brief-checkins-2026-07-23.md). [GAP: the brief cites a full scan artifact, `area-brief-checkins-competitive-2026-07-17`, which is **not in this repo.** Recovering it is the cheapest path to a real roster.]

## Positioning map

[GAP: **not drawn.** A 2x2 needs two axes buyers actually decide on, with every player placed from evidence. We hold one axis with a source and nothing credible for the second, so drawing a square here would be invention. What exists today is the one evidenced axis:]

```
  segment size (the only axis we can source)

  20 ────────── 150 ────────── 500 ──────────────► enterprise
   │             │              │                      │
   │◄──── Payworks target ─────►│                      │
   │      (area brief, 20–500 EE)                   Dayforce
   │                            │                 ("enterprise
   Wagepoint, Rise, Humi,       │                  reference")
   Collage, Knit — SMB band     └── expense VP2's proposed
   per the same brief               >150 EE threshold cuts
                                    the target band in half
```

Second axis candidates a future run should test: *breadth of suite* vs *depth of Canadian compliance*, or *self-serve configurability* vs *implementation-led*. Neither is evidenced yet — run `/competitor-analysis` path (d) to place them.

## Differentiation thesis

The sentences the team reuses in PRDs, launches, and battlecards. Every claim evidence-linked.

- **We win when:** [GAP: no won-deal evidence names a competitor. The only competitive signal we hold is the FY27 win-loss read — a **37% Time Management gap** and a **39% HR gap** — and neither is attributed to a named rival.]
- **We lose when:** [GAP: same. Attributing losses needs the win/loss path (e) run against real call summaries.]
- **Unlike** *"platforms that treat Canada as an afterthought"*, **we** are natively Canadian across 13 jurisdictions, correct by construction, and backed by service. [Source: [business-info.md](../strategy/business-context/business-info.md) Our Positioning]
  - ⚠️ **This line does not hold against Dayforce.** Their own admin documentation covers ROE reason codes, T4/RL-1, Canadian federal and provincial tax setup, and Québec QPP/QPIP. Against Dayforce the differentiator has to be segment fit, service model, and price — not Canadian correctness. Using the "afterthought" line in a Dayforce comparison would be a claim a buyer can disprove from public docs. [Source: [Dayforce teardown](competitors/dayforce/teardown.md)]

## Where we win / where we lose

Patterns, not anecdotes — add a row when ≥2 pieces of evidence agree; retire it when the pattern breaks.

| Pattern | Vs | Evidence |
|---------|----|----------|
| _No rows yet._ Zero call summaries in this repo name a competitor, so no pattern clears the ≥2-evidence bar. | — | — |

## Maintenance

- **Auto tier** — living page, edit in place, bump `_updated:` on every change; ≤120 lines.
- **Roster canon:** [business-info.md](../strategy/business-context/business-info.md) Competitive Landscape (confirm tier). Add or remove competitors there first; this page and the root `CLAUDE.md` fundamentals line follow in the same session. **Outstanding:** Dayforce and the seven names above are not yet registered there.
- **Refresh:** `/competitor-analysis` (deep analysis and monthly monitoring both fold through here); `/context-update` and `/process-meeting` update win/lose patterns and at-a-glance lines when call-borne intel warrants.
- **Sources:** `competitors/{slug}/teardown.md` · [intel/](intel/) monthly records · account call summaries.
- **Read by:** `/product-brief-draft`, `/write-prod-strategy`, `/strategy-sprint`, `/launch-checklist`, `/slack-message`, `/decision-doc`, `/expansion-strategy`, `/prototype`, `/red-team`, `/assumption-map`, and the executive reviewer in `/product-brief-challenge`.
