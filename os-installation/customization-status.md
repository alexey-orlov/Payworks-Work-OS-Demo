# Customization Status — Payworks

---
updated: 2026-09-01
mode: "instance"
naming: "house — PRD→Product Brief, job spec→Micro Job, jobs breakdown→Micro Jobs Breakdown, area→module (mapped 2026-08-30)"
auto-sync: "undecided"
command-aliases: "product-brief-draft→prd-draft · product-brief-challenge→prd-challenge · micro-jobs-breakdown→jobs-breakdown · micro-job-draft→job-spec-draft · micro-job-challenge→job-spec-challenge · pm-ba-handoff→pm-handoff (installed 2026-09-01 as .claude/commands/ aliases; skill folders keep their OS names so master updates still apply)"
---

## Sequence

| # | Target | Phase | One line |
|---|--------|-------|----------|
| 1 | `context-core` | **validated** | Business info, stakeholders, segmentation, FY27 period page and the root fundamentals block populated from Payworks' own documents — 31 filled · 1 resolved · 14 GAP of 46 manifest items |
| 2 | `initiatives` | not started | Owned by a separate run. VP2 Product Briefs, JTBD and Micro Jobs are parked in Deferred sources below |
| 3 | `design-system` | not started | — |
| 4 | `research-source` | not started | — |
| 5 | `demo-readiness` | not started | — |
| 6 | `naming-conventions` | **installed** | Corrected 2026-09-01: the row said `not started`, but the sweep had in fact run — house terms are in repo prose and six skill folders had been renamed by hand. The hand rename was a fork; it is replaced by `.claude/commands/` aliases (header above), so `/product-brief-draft` and the other five resolve while the skill folders keep their OS names |
| 7 | `prd-template` · `micro-jobs-breakdown-template` · `job-spec-template` | not started | Owned by a separate run. Real Payworks examples exist — see Deferred sources |
| 8 | `metric-conventions` | **complete** | KPI Framework (three tiers + required fields) installed into business-info's Metric Reporting Conventions block from the workflow SOP |
| 9 | `instance-handoff` | **passed 2026-09-01** | Mechanical lint clean (0 errors); `.claude/` + `.github/` restored and tracked after a web-upload delivery dropped all 116 dotfiles; every slash command named in repo prose resolves; state file reconciled against the tree |
| — | auto-sync close | not started | Deliberately not run this session — the dispatcher handles it |

## Deferred sources

Parked, not dropped. Each will be consumed by the target named.

- `.../sources-text/ProductBrief_Companies_VP2.txt` → `initiatives` (also a prd-template example) (noted 2026-08-30)
- `.../sources-text/ProductBrief_FirmManagement_VP2.txt` → `initiatives` / `prd-template` (noted 2026-08-30)
- `.../sources-text/ProductBrief_PayrollHub_VP2 (3).txt` → `initiatives` / `prd-template` (noted 2026-08-30)
- `.../sources-text/JTBD- Companies VP2.txt` → `initiatives` (noted 2026-08-30)
- `.../sources-text/Companies-VP2-BA-Handoff.txt` → `initiatives` (noted 2026-08-30)
- `.../sources-text/MJ-01…MJ-04_Companies_VP2.txt` → `initiatives`, and the natural example set for `job-spec-template` (noted 2026-08-30)
- `.../sources-text/Payworks_AIPM_Session2.txt`, `AI PM Jumpstart Session 3 deck`, `Work OS admins deck` → **no target.** SoftServe's own decks: context, never a source of client fact (noted 2026-08-30)

## context-core

- **Phase:** validated (installed and verified against the live files)
- **Artifacts:**
  - Business info → `product-development/product/strategy/business-context/business-info.md`
  - Stakeholder profiles (role-level) → `product-development/product/strategy/business-context/stakeholders.md`
  - Segmentation matrix → `product-development/product/strategy/business-context/segmentation-matrix.md`
  - FY27 period page → `product-development/product/strategy/current-quarter.md`
  - Fundamentals block, H1 title, Team table, Slack table → `CLAUDE.md`
  - Facts annex → `os-installation/customization-facts.yaml`
- **Inputs received:** nine Payworks documents plus the August 2026 customer base workbook; house vocabulary confirmed in chat; domain `payworks.ca` confirmed in chat
- **Coverage:**

  | Group | Tier | filled | GAP | N/A | resolved |
  |---|---|---|---|---|---|
  | Company & product identity | core | 4 | 0 | 0 | 1 (`fi-areas` → installs with `initiatives`) |
  | Customers — segments, ICP, personas | core | 3 | 0 | 0 | — |
  | Problem & value proposition | core | 3 | 0 | 0 | — |
  | Mission, strategy & current OKRs | core | 6 | 0 | 0 | — |
  | Business model, pricing & key metrics | core | 1 | 1 | 0 | — |
  | Team roster & channels | core | 1 | 2 | 0 | — |
  | Stakeholder map | core | 5 | 0 | 0 | — |
  | Segmentation matrix | core | 4 | 0 | 0 | — |
  | Market & competitive landscape | later | 0 | 7 | 0 | — |
  | Go-to-market motion | later | 1 | 1 | 0 | — |
  | Product development process | later | 2 | 0 | 0 | — |
  | Culture, values & product principles | later | 1 | 1 | 0 | — |
  | Platform model | later | 0 | 1 | 0 | — |
  | Tech constraints | later | 0 | 1 | 0 | — |
  | **Total (46 items)** | | **31** | **14** | **0** | **1** |

  Core tier alone: 27 filled · 3 GAP · 1 resolved of 31.

- **Open — Critical:**
  1. **There is no competitor list.** The "Competition landscape" deck contains a title slide reading *"List Claude can leverage for research"* and five blank slides; no strategy or competitive document names a rival. Exactly one competitor surfaces anywhere — **Wagepoint**, named in the deferred Payroll Hub VP2 Product Brief as "the most frequently cited competitor in win/loss conversations" — and it is now installed with its source. Seven manifest items still depend on the missing list, and `business-info.md`'s "why customers choose us" section cannot be completed. → Provide the intended competitor list, or approve a web-research pass.
  2. **No pricing or revenue data anywhere.** No price book, no tiers, no ARR/MRR, and the customer base export has **no revenue field of any kind**. Every ARR cell in the segmentation matrix is a GAP, and revenue-weighted prioritization cannot run. → Provide a price book and a billing export keyed on `CustID`.
  3. **No roster.** Role titles and approval authority are recorded, but no person is named against any role — the Team table, every stakeholder profile, and all OKR owners are `[GAP]`. → Provide the product-org roster (name, role, GitHub, Slack ID, escalation).
  4. **FY27 targets have no baselines and no owners.** Ontario/Québec share, retention and NRR are stated as targets with no current reading. A target without a baseline cannot be scored. → Provide current values and name an owner per objective.

- **Open — Other:**
  1. **Roadmap sequencing lost in extraction.** The roadmap deck's NOW / NEXT / LATER columns survive but the item-to-column mapping does not, so no roadmap item is asserted as in flight. → Re-extract the original `.pptx` with layout preserved, or confirm with the Roadmap Hub owner.
  2. **Size-band thresholds are our recommended default, not Payworks'.** Micro 1–19 / Small 20–99 / Mid 100–499 / Large 500+, chosen because the OS template's SMB/Corp/Ent would file 97% of the base as "SMB" (active-base distribution: median 14, p75 34, p90 77, p95 126, p99 369). → Confirm or replace.
  3. **`EECount` is undefined** in the export — current headcount or employees paid year-to-date? It drives every size band.
  4. **The `GRW` module flag is unmapped** — 12,433 active accounts, its own charge date and run count, defined nowhere. 98% overlap with `AnalyticsV2`, but overlap is not identity. → Ask the data owner.
  5. **"Multi-module" is undefined.** The 32→35% FY27 target has no stated definition; independently computed cuts give 26.6% or 28.9% depending on which modules count. → Confirm the definition so the metric can be tracked.
  6. **18.3% of accounts (7,983) have a blank `Industry` field**, kept as an `Unclassified` row rather than hidden in `Other`. → CRM hygiene before vertical strategy leans on these numbers.
  7. **"VP, Product Management" vs "VP of Product"** — one role or two? Both titles appear across the sources.
  8. **No Sales, Customer Success, Marketing or QA role** appears in any process document — material given the channel-led strategy.
  9. **No company values statement** exists; company priorities and product principles were *not* relabelled as values.
  10. **`platform-model.md` was not written** (outside this run's scope), but its source material is fully resolved and annexed — a short follow-up run can install it without re-extraction.
  11. **Both SOPs are unpublished DRAFTs**, all five artifact templates are `[PLACEHOLDER] — to be built by Product Ops`, and five terminology decisions are open. The recorded process may shift.
  12. **Four child SOPs and the parent "AI-First Product Development Lifecycle — Team Overview (May 2026)"** are referenced by the workflow SOP but were not provided. The SOP calls that parent the single source of truth for the end-to-end flow.
  13. **No design tool is named** — Figma, Jira, Confluence and Azure DevOps appear in no source. `toolchain.yaml` surfaces stay undecided.
  14. **Basic firmographics missing:** stage, founding year, headcount, funding, HQ city. Web-enrichable from payworks.ca.
  15. **No market sizing** (TAM/SAM/SOM) and **no marketing channel mix** stated. Both web-enrichable in part.

- **Log:**
  - 2026-08-30 (alexey-orlov) — First run. Read the playbook and manifest; labelled 10 sources; dispatched three `context-extractor` batches over the strategy/vision/roadmap, architecture/terminology, and SOP documents; aggregated the customer base workbook directly from XLSX after finding the `.txt` extraction column-misaligned. Installed five steering surfaces plus the facts annex. Coverage 31 filled · 1 resolved · 14 GAP of 46. Auto-sync close deliberately skipped (handled by the dispatcher). Nothing committed.
  - 2026-09-01 (alexey-orlov) — Audit repair pass. Restored the runtime layer lost in delivery
    (`.claude/` — 60 skills, agents, hooks, settings — plus `.github/` workflows and scripts; the
    GitHub web upload had dropped every dotfile). Installed six `.claude/commands/` aliases for the
    house command names instead of re-forking skill folders. Repaired the data the write-back
    contract had never been enforced against: 32 byte-order marks stripped (they made frontmatter
    parse as empty), 5 transcripts that filing had COPIED rather than moved removed from the inbox,
    all 10 Northwind conversations relinked from the account page (8 links had been dead), 18
    artifact→initiative joins written including the 2026-08-13 call that touches three initiatives
    and had reached none of them, 2 `[PENDING:]` markers replaced with the files that already
    existed, 7 folder contents lists created and 88 nav lines appended, 7 mis-counted relative paths
    repaired, and 21 links to records that were never filed replaced with honest `[GAP:]` markers
    rather than invented content. `employee-onboarding` now names its 5 target features, so the
    feature→initiative rollup works. Lint: 141 errors → 0. Five warnings remain and are deliberate:
    three competitive pages cite staged source briefs (needs a decision on a durable home for source
    documents), three artifact filenames use house terms rather than the canonical chain suffixes,
    and CODEOWNERS still has a placeholder owner.
  - 2026-08-30 (alexey-orlov) — Verify step (fresh-context agent, independent re-derivation of every computed figure). Manifest coverage and shared-fact agreement passed; five defects found and fixed: (1) EECount percentiles had been computed on the raw export instead of the active base — median 13→14, p75 33→34, p90 76→77, p95 124→126, p99 367→369, corrected in three files; (2) province rollup PE/NF/YT/NU/NT 954→955, and a total row added so the table reconciles to 43,550; (3) distinct franchise brands ~90→35; (4) master-template placeholders (`[github]`, `[slack-id]`, `[phone or page link]`, `[id]`, `#[…]`) still sitting in the root Team and Slack tables, replaced with `[GAP]`; (5) the claim "no competitor is named in any source" was falsifiable — **Wagepoint** appears in a provided (deferred) Product Brief; claim narrowed and Wagepoint installed with its source. Also noted the one repaired source typo in the `Other Services (except Public Administration` label. Every other number re-derived exactly.

## Data handling note

The customer base export was used for **aggregates only**. No customer name, `CustID`, parent company, franchise brand, sales-rep or CSR name entered the repository. The reproducible aggregation recipe is recorded in `segmentation-matrix.md` so the numbers can be re-derived without re-reading raw rows.
