---
week: "2026-W35"
week_start: "2026-08-24"
week_end: "2026-08-30"
quarter: FY27
reviewed: "2026-08-31"
reviewer: "vladyslav.butenko@payworks.ca"
---

# Weekly Review — Week of Aug 24–30, 2026

> No git history in this repo — movement read from files and the ingestion ledger only.

---

## 📋 Part A — Team Digest

### Initiatives

**Onboarding**

- **[employee-onboarding](../initiatives/employee-onboarding.md)** (active) — Two decisions landed at the Aug 26 sync: onboarding reuses expense VP2's MJ-01 profile foundation (gains pre-hire state + named extension point), and the pilot is scoped to ESS only targeting November — before Northwind and Maplewood's spring hiring wave.
  - ⚠️ Maplewood spreadsheet response — Claire Sutton — 1 day overdue (committed "this week" of Aug 26; not yet filed)
  - ⚠️ "Who owns the org chart?" to onboarding brief Open Questions — Claire Sutton — 1 day overdue (same commitment)

**Expense Management**

- **[expense-management-vp2](../initiatives/expense-management-vp2.md)** (active) — MJ-01 now shared with onboarding; MJ-02 (receipt capture) pushed right 3–4 weeks. Second signal against mobile-approval assumptions: Acme Corp (75 employees) has digital receipts already and wants mobile approvals blocked, not discouraged. Northwind controller call was scheduled for Aug 27 — outcome not yet recorded.
  - ⚠️ MJ-02 milestone date update — Michelle Tremblay — pending

**Performance Management**

- **[performance-management-discovery](../initiatives/performance-management-discovery.md)** (active) — Cross-interview synthesis filed (13 records, 4 accounts: Northwind, Harbourview, Maplewood, Cascadia; sessions Jun 22–Aug 12). Synthesis is the input for the Product Brief. All 13 transcripts moved to the central archive.

Quiet this week: Time Management, Absence Management, Workforce Analytics (no active initiative)

---

### Also this week (no initiative)

- **Decisions:** [Link Architecture v2](../decisions/2026-08-30-link-architecture-v2.md) — the repo's information model is now an explicit graph; `feature-index.yaml` is a pure catalog, initiatives own all artifacts, frontmatter links are required on every record. This is the OS infrastructure decision, not a product one — it resolves ~40 inconsistencies found in an independent review.
- **Research:** [Performance Management synthesis](../user-insights/performance-management-2026-08-31.md) — 13 records, 4 accounts; synthesis covers contradictions in peer feedback, scoring models, and three incompatible compensation paths. Ready to feed the Product Brief.
- **Feature requests:** 14 requests awaiting tracker push
  - Birchbark Books (Aug 18, 7 requests): advance-change-notice, approval-thresholds, cross-client-expense-dashboard, firm-role-based-access, firm-single-sign-on, mobile-access, receipt-capture — all expense-mgmt/channel-view signal
  - Acme Corp (Aug 20, 7 requests): approval-thresholds, claim-submission-reminders, expense-history-self-service, manager-spend-digest, mobile-access, pay-statement-expense-detail, receipt-capture
  - ⏳ 14 requests awaiting tracker push — `/create-tickets push`

---

### Next week

- Product Brief draft — Margaret Foster — due **2026-09-07** — performance-management-discovery
- Three probe questions (mobile boundary, compensation approver model, data migration) — Margaret Foster — due **2026-09-12** — performance-management-discovery
- MJ-01 pre-hire state scoped; re-run translation checkpoint (invite Claire Sutton) — Michelle Tremblay — due ~week of 2026-09-01 — expense-management-vp2
- Northwind controller call outcome recorded — Michelle Tremblay — no date agreed — expense-management-vp2
- Maplewood spreadsheet response sent — Claire Sutton — **overdue** — employee-onboarding
- Review pending gated proposal: [expense-management features catalog addition](../../../governance/proposals/2026-08-31-add-expense-management-features-to-catalog.md) — requires in-session yes to apply to `feature-index.yaml`
- **Quarter checkpoint:** This week's movement directly served KR 1.4 (multi-module 32→35% — onboarding + expense VP2 expansion work) and the HR-gap bet behind KR 2 (performance management synthesis ready for briefing). KR 1.5 (Aurora live) and KR 1.6 (AI attributed to revenue) had no visible movement.

---

### ⚡ Top 3 Things to Know

1. **Onboarding pilot is November — but two commitments are overdue.** The ESS-only scope and shared MJ-01 foundation are decided. Claire Sutton still owes the Maplewood spreadsheet response (committed this week) and the org-chart confirmation in the brief — both are now 1 day past.
2. **Performance management synthesis is done — the Product Brief clock is ticking.** 13 records synthesised, contradictions named, brief due Sep 7. The most loaded open question: three incompatible compensation models (automatic at Harbourview, CEO-approved at Cascadia, board-budget at Maplewood). The brief has to carry that divergence without smoothing it.
3. **Mobile-approval assumptions for expense VP2 are weakening.** Two signals now point the same direction: Northwind's controller and Acme Corp's HR manager both push back on the mobile-approval story. Whether the Northwind controller call happened on Aug 27 and what it produced needs to be recorded before the VP2 brief is written.

---

### 📊 Repo Health

- Files added: initiative pages × 4, synthesis × 1, decisions × 3, meeting summary × 1, transcripts archived × 13 — from file signals (no git history)
- Stale files (wiki-lint): 1 — deliberate demo fixture in `governance/health/wiki-lint-stale-fixture.md` (removable after demo)
- Transcripts: 17 total in the central archive (all in processed.txt — fully folded); 11 inbox artifacts not yet folded → `/context-update`
- Pending gated proposal: 1 (`governance/proposals/2026-08-31-add-expense-management-features-to-catalog.md`)

---

### 🔎 Where to look

- [performance-management-2026-08-31.md](../user-insights/performance-management-2026-08-31.md) — open this before writing the performance management brief; it's the only synthesis of all 13 records and the contradictions are on the page, not averaged away
- [2026-08-26-onboarding-pilot-ess-scope.md](../decisions/2026-08-26-onboarding-pilot-ess-scope.md) — Margaret Foster's on-the-record counter-argument (the pain that was researched is administrative, not new-hire-side) is in § "Counter-argument on record" — worth reading before scoping the next round

---

## 🔍 Part B — Execution Review

### TL;DR

- Week wasn't planned in `planning/` — reviewing what happened only. Suggest `/weekly-plan` at the start of each week.
- Performance management synthesis landed — largest single output of the week; 13 records closed into one document.
- Three initiative pages created and two shipped retrospectively — the OS now has a working artifact layer for current work.
- Link Architecture v2 decided — OS infrastructure stable; the gated catalog proposal is the first test of the new model.
- Two overdue action items from the Aug 26 sync (Maplewood response, org-chart question) — both owed by Claire Sutton; should clear Monday.
- Northwind controller call outcome is a gap: if the call happened Aug 27, its signal belongs in the VP2 brief before it's written.

---

### Priorities — plan vs actual

No planning file found for W35 (`planning/2026-W35-weekly-plan.md` does not exist). The review is against what moved, not against stated intent.

#### What moved

**Performance management synthesis** — 13 records distilled, all four accounts covered, synthesis filed. ✅ Complete (as a deliverable)

**Onboarding decisions** — two decisions written, ratified, and linked from both initiative pages. ✅ Complete

**Initiative infrastructure** — 4 pages created or filed retrospectively; the initiatives layer is now operational. ✅ Complete

**Maplewood spreadsheet response + org-chart question** — committed for the week of Aug 26. ❌ Not started (both still open)

**Northwind controller call (Aug 27)** — scheduled; no outcome recorded. 🟡 Partial (call may have happened; outcome absent from the repo)

---

### Top 3 Learnings

1. **Sequencing decisions need the dependency made explicit.** The onboarding-reuses-MJ-01 decision is solid, but it creates a hard scheduling dependency (onboarding's date is now coupled to MJ-01's date, which has already moved once). The dependency should be a tracked open loop, not just a paragraph in the decision record — or the next surprise is another slip.

2. **Signal against a hypothesis is as valuable as signal for one.** Two accounts independently pushing back on mobile approvals for expense VP2 is a meaningful result. The risk is that this gets treated as noise because it contradicts the assumptions already in the plan. The Northwind controller call outcome (if recorded) is the third data point — capture it before it fades.

3. **Commitments made in syncs need a follow-up owner, not just a record.** The Aug 26 sync produced six action items; two are already overdue 24 hours later. The action items table in the summary is correct — the gap is that nothing flags them as overdue between sessions. A weekly-review prompt or a standing open-loop sweep would catch these while they are still cheap to close.

---

### Next Week Preview

1. **Margaret Foster: Performance Management Product Brief** (carry-forward → new urgent) — due Sep 7; synthesis is ready; the three open probes (mobile boundary, compensation approver, data migration) should be in parallel, not sequential
2. **Michelle Tremblay: MJ-01 pre-hire state scoped + VP2 brief unblocked** (new urgent) — Northwind controller signal needs recording; mobile-approval section of the brief needs revision before VP Product Brief is written
3. **Claire Sutton: Two overdue loops closed** (carry-forward, overdue) — Maplewood spreadsheet response + org-chart ownership question in the onboarding brief

**Items to unblock Monday:**
- Was the Northwind controller call (Aug 27) completed? If so, who holds the notes and when do they land in the repo? — blocked on Michelle Tremblay / Vanessa Lee
- Gated proposal review: apply or reject `governance/proposals/2026-08-31-add-expense-management-features-to-catalog.md` — requires steward's in-session yes; currently blocking the expense-management catalog entries

---

*Offer: durable process learnings above → append to `meetings/retros/lessons-learned.md`? Also: run `/weekly-plan` now to set W36 priorities.*
