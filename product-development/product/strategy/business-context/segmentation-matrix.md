# Segmentation Matrix

_updated: 2026-08-30 · snapshot: 2026-08-31 (August 2026 Customer Base report) · owner: [GAP: assign an owner]

The quantitative mix of the paying customer base: how many accounts sit in each segment — vertical × size band — overall and per module. When a task needs "how many accounts are in segment X", this file is the answer; no other file in the repo carries these numbers.

**What belongs here:** the canonical segment axes (size bands, verticals, module categories), the counting rules, and the filled matrices.

**What does not:** who we *target* and why — ICP, personas, budgets, TAM/SAM/SOM — lives in [business-info.md](business-info.md). Per-account facts live in [portfolio.yaml](../../customers/accounts/portfolio.yaml). What counts as ARR is defined in `analytics/metrics/`. This file only aggregates.

> ### ⚠ ARR is unavailable — every revenue column below is a GAP
>
> The August 2026 Customer Base report **contains no revenue, price, contract-value, or billing-amount field of any kind.** Its 59 columns cover identity, firmographics, module flags, per-module charge dates and run counts — but no money. Account counts below are solid and reproducible; **ARR cannot be derived from this source at all** and has not been estimated, modelled, or inferred.
>
> **To close this:** provide a billing or finance export carrying account-level ARR/MRR keyed on `CustID`, and re-run the recipe at the bottom of this file. Until then, any task that needs revenue weighting by segment must say so rather than substituting account counts for ARR.

## Segment Axes

Canonical labels — every other doc, skill, and `portfolio.yaml` entry uses these exact names.

**Size bands** (by the export's `EECount` field):

| Band | Meaning | Threshold | Active accounts | Share |
|------|---------|-----------|-----------------|-------|
| Micro | Owner-operator and very small teams | 1–19 employees | 26,020 | 59.7% |
| Small | Established small business | 20–99 employees | 14,284 | 32.8% |
| Mid | Mid-market | 100–499 employees | 2,771 | 6.4% |
| Large | Largest accounts | 500+ employees | 260 | 0.6% |
| Unknown | `EECount` zero or absent | — | 215 | 0.5% |

> **⚠ These thresholds are a recommended default, not a Payworks decision.** No source states Payworks' own size bands. The OS template ships SMB / Corp / Ent at under-200 / 200–2,000 / over-2,000 — on this base that would file **97% of accounts as "SMB"** and discriminate nothing. The four bands above were chosen to split the actual distribution of the active base (43,335 accounts with `EECount` > 0, nearest-rank: **median 14 employees; p75 = 34, p90 = 77, p95 = 126, p99 = 369**, max 36,442). **Confirm or replace them**, then keep them stable so matrices stay comparable quarter over quarter. Also note `EECount` is not defined in the export — confirm whether it is current headcount or employees paid year-to-date.

**Verticals** — the export's `Industry` field (NAICS sector names). Every account maps to exactly one. The ten largest are named; the remaining eleven sectors roll into `Other`.

Other Services (except Public Administration) · Health Care and Social Assistance · Retail Trade · Accommodation and Food Services · Professional, Scientific and Technical Services · Construction · Manufacturing · Arts, Entertainment and Recreation · Wholesale Trade · Finance and Insurance · Other · Unclassified

> **`Unclassified` is 18.3% of the base (7,983 accounts) — a real data-quality gap, not a tail.** These accounts have a blank `Industry` field. It is kept as its own row rather than folded into `Other` so no analysis silently treats it as a sector. Closing it is a CRM hygiene task worth doing before vertical strategy leans on these numbers.

**Use-case categories** — for Payworks these are the **modules**. An account is counted in a module when its adoption flag is set in the export.

Payroll (all accounts) · Employee Self Service · Human Resources · Time Management · Absence Management · Workforce Analytics

> One billed module flag in the export, `GRW` (12,433 active accounts, with its own charge date and run count), is **not defined anywhere in the source data** and has deliberately not been mapped to a module name. It overlaps 98% with `AnalyticsV2` — but overlap is not identity. Ask the data owner what `GRW` is before using it.

## Counting Rules

- **Account** = one `CustID` — one payroll account. Not one parent company: a multi-location franchise operator with eight locations counts as eight accounts if it holds eight payroll accounts. 34 duplicate `CustID` rows in the export were de-duplicated (first occurrence kept).
- **Active / paying** = ran a regular payroll within **12 months** of the snapshot date, per `LastRegularRun`. This is the working definition of "paying" in the absence of a billing field. **43,550 of 44,832 unique accounts qualify.** Excluded: 1,086 last ran over 24 months ago, 163 in the 12–24 month window, 15 future-dated, 18 never-run or unparseable.
- **ARR** — unavailable. See the banner above. **Mirror rule:** the General matrix account total (43,550) must equal the active-account figure in the root `CLAUDE.md` fundamentals block and in business-info's Key Metrics; whoever changes one reconciles all three in the same change.
- **General matrix:** each account sits in exactly one cell — one vertical, one size band. Cells sum to the totals; the totals are the truth.
- **Module matrices:** an account appears in **every** module it has enabled, so module totals overlap and exceed the General total — they are lenses, not partitions.

## General Matrix — all paying accounts

Source: `Customer Base report_August_2026 (1).xlsx`, aggregated per the recipe below. ARR columns omitted entirely rather than shown empty — the source has no revenue field.

| Vertical | Micro (1–19) | Small (20–99) | Mid (100–499) | Large (500+) | Unknown | Total # | ARR |
|---|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 4,298 | 1,522 | 238 | 33 | 34 | **6,125** | [GAP] |
| Health Care and Social Assistance | 2,895 | 1,459 | 332 | 42 | 15 | **4,743** | [GAP] |
| Retail Trade | 2,423 | 1,732 | 311 | 18 | 16 | **4,500** | [GAP] |
| Accommodation and Food Services | 1,477 | 2,278 | 546 | 44 | 13 | **4,358** | [GAP] |
| Professional, Scientific and Technical Services | 2,463 | 888 | 131 | 12 | 19 | **3,513** | [GAP] |
| Construction | 1,287 | 562 | 80 | 4 | 8 | **1,941** | [GAP] |
| Manufacturing | 795 | 805 | 183 | 10 | 4 | **1,797** | [GAP] |
| Arts, Entertainment and Recreation | 547 | 447 | 157 | 18 | 4 | **1,173** | [GAP] |
| Wholesale Trade | 593 | 434 | 74 | 7 | 2 | **1,110** | [GAP] |
| Finance and Insurance | 782 | 194 | 34 | 5 | 7 | **1,022** | [GAP] |
| Other | 3,165 | 1,655 | 380 | 41 | 44 | **5,285** | [GAP] |
| Unclassified | 5,295 | 2,308 | 305 | 26 | 49 | **7,983** | [GAP] |
| **Total** | **26,020** | **14,284** | **2,771** | **260** | **215** | **43,550** | **[GAP]** |

## Per-Category Matrices

One section per module. An account using four modules appears in four tables.

### Employee Self Service — 42,547 accounts (97.7% of active base)

Effectively universal; useful as a denominator rather than a differentiator.

| Vertical | Micro | Small | Mid | Large | Unknown | Total |
|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 4,171 | 1,500 | 231 | 31 | 32 | **5,965** |
| Health Care and Social Assistance | 2,801 | 1,417 | 327 | 40 | 15 | **4,600** |
| Retail Trade | 2,337 | 1,665 | 292 | 18 | 16 | **4,328** |
| Accommodation and Food Services | 1,450 | 2,216 | 535 | 44 | 13 | **4,258** |
| Professional, Scientific and Technical Services | 2,382 | 874 | 130 | 12 | 19 | **3,417** |
| Construction | 1,252 | 547 | 78 | 4 | 8 | **1,889** |
| Manufacturing | 772 | 784 | 180 | 10 | 4 | **1,750** |
| Arts, Entertainment and Recreation | 541 | 440 | 157 | 18 | 4 | **1,160** |
| Wholesale Trade | 577 | 429 | 74 | 6 | 2 | **1,088** |
| Finance and Insurance | 762 | 190 | 34 | 5 | 7 | **998** |
| Other | 3,057 | 1,622 | 378 | 39 | 44 | **5,140** |
| Unclassified | 5,281 | 2,297 | 303 | 24 | 49 | **7,954** |
| **Total** | **25,383** | **13,981** | **2,719** | **251** | **213** | **42,547** |

### Workforce Analytics — 12,230 accounts (28.1%)

| Vertical | Micro | Small | Mid | Large | Unknown | Total |
|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 654 | 651 | 142 | 18 | 1 | **1,466** |
| Health Care and Social Assistance | 618 | 731 | 230 | 21 | 3 | **1,603** |
| Retail Trade | 524 | 856 | 226 | 16 | 7 | **1,629** |
| Accommodation and Food Services | 204 | 642 | 199 | 15 | 1 | **1,061** |
| Professional, Scientific and Technical Services | 543 | 459 | 89 | 6 | 5 | **1,102** |
| Construction | 252 | 220 | 42 | 3 | 0 | **517** |
| Manufacturing | 257 | 502 | 158 | 8 | 2 | **927** |
| Arts, Entertainment and Recreation | 99 | 205 | 92 | 10 | 1 | **407** |
| Wholesale Trade | 165 | 283 | 64 | 5 | 0 | **517** |
| Finance and Insurance | 166 | 107 | 26 | 4 | 0 | **303** |
| Other | 796 | 876 | 253 | 30 | 17 | **1,972** |
| Unclassified | 297 | 347 | 74 | 6 | 2 | **726** |
| **Total** | **4,575** | **5,879** | **1,595** | **142** | **39** | **12,230** |

Workforce Analytics **Pro** is on 9 active accounts (0.02%) — effectively unsold.

### Time Management — 8,163 accounts (18.7%)

One of the two modules carrying a win-loss gap (37%).

| Vertical | Micro | Small | Mid | Large | Unknown | Total |
|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 331 | 466 | 98 | 9 | 0 | **904** |
| Health Care and Social Assistance | 478 | 596 | 187 | 11 | 2 | **1,274** |
| Retail Trade | 371 | 675 | 191 | 14 | 4 | **1,255** |
| Accommodation and Food Services | 135 | 523 | 148 | 9 | 1 | **816** |
| Professional, Scientific and Technical Services | 187 | 239 | 49 | 3 | 2 | **480** |
| Construction | 155 | 145 | 21 | 3 | 0 | **324** |
| Manufacturing | 165 | 390 | 128 | 5 | 2 | **690** |
| Arts, Entertainment and Recreation | 67 | 173 | 78 | 6 | 1 | **325** |
| Wholesale Trade | 83 | 205 | 53 | 3 | 0 | **344** |
| Finance and Insurance | 41 | 32 | 12 | 2 | 0 | **87** |
| Other | 389 | 563 | 195 | 22 | 2 | **1,171** |
| Unclassified | 187 | 253 | 48 | 5 | 0 | **493** |
| **Total** | **2,589** | **4,260** | **1,208** | **92** | **14** | **8,163** |

### Absence Management — 7,131 accounts (16.4%)

| Vertical | Micro | Small | Mid | Large | Unknown | Total |
|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 349 | 445 | 98 | 6 | 1 | **899** |
| Health Care and Social Assistance | 299 | 484 | 162 | 11 | 4 | **960** |
| Retail Trade | 253 | 477 | 132 | 11 | 3 | **876** |
| Accommodation and Food Services | 53 | 215 | 73 | 5 | 1 | **347** |
| Professional, Scientific and Technical Services | 380 | 330 | 54 | 2 | 3 | **769** |
| Construction | 102 | 121 | 22 | 1 | 0 | **246** |
| Manufacturing | 166 | 368 | 120 | 5 | 2 | **661** |
| Arts, Entertainment and Recreation | 39 | 86 | 50 | 4 | 1 | **180** |
| Wholesale Trade | 113 | 216 | 57 | 4 | 0 | **390** |
| Finance and Insurance | 120 | 93 | 20 | 3 | 0 | **236** |
| Other | 429 | 557 | 173 | 14 | 6 | **1,179** |
| Unclassified | 140 | 196 | 49 | 2 | 1 | **388** |
| **Total** | **2,443** | **3,588** | **1,010** | **68** | **22** | **7,131** |

### Human Resources — 5,277 accounts (12.1%)

The least-adopted module, and the one carrying the largest win-loss gap (39%).

| Vertical | Micro | Small | Mid | Large | Unknown | Total |
|---|---|---|---|---|---|---|
| Other Services (except Public Administration) | 211 | 294 | 94 | 9 | 1 | **609** |
| Health Care and Social Assistance | 180 | 332 | 163 | 10 | 2 | **687** |
| Retail Trade | 164 | 305 | 112 | 11 | 6 | **598** |
| Accommodation and Food Services | 62 | 223 | 88 | 11 | 0 | **384** |
| Professional, Scientific and Technical Services | 199 | 218 | 62 | 5 | 3 | **487** |
| Construction | 88 | 89 | 32 | 1 | 0 | **210** |
| Manufacturing | 93 | 227 | 101 | 5 | 0 | **426** |
| Arts, Entertainment and Recreation | 34 | 80 | 63 | 6 | 1 | **184** |
| Wholesale Trade | 63 | 132 | 45 | 4 | 0 | **244** |
| Finance and Insurance | 78 | 61 | 21 | 1 | 0 | **161** |
| Other | 332 | 457 | 169 | 25 | 13 | **996** |
| Unclassified | 91 | 146 | 49 | 4 | 1 | **291** |
| **Total** | **1,595** | **2,564** | **999** | **92** | **27** | **5,277** |

### Multi-module adoption

The FY27 strategy sets a target of **32% → 35%**. Payworks' own definition of "multi-module" is **not stated in any source**, so the figures below are independently computed and are **not** the same metric until the definition is confirmed.

| Definition | Accounts | Share of active base |
|---|---|---|
| ≥1 of HR / Time / Absence (beyond Payroll + ESS) | 11,603 | 26.6% |
| ≥1 of HR / Time / Absence / Analytics | 12,596 | 28.9% |
| ≥2 of HR / Time / Absence | 6,293 | 14.5% |
| ≥2 of HR / Time / Absence / Analytics | 11,272 | 25.9% |

## Geographic Distribution

Not a standard axis in the OS template, but load-bearing here: the FY27 test sets **Ontario 6% share** and **Québec 3% share**, making province the axis the strategy is actually measured on.

| Province | Active accounts | Share of base | Notes |
|---|---|---|---|
| ON | 13,806 | 31.7% | Largest province; FY27 share target 6% |
| BC | 9,194 | 21.1% | |
| AB | 6,330 | 14.5% | |
| MB | 5,286 | 12.1% | |
| **QC** | **2,961** | **6.8%** | FY27 share target 3%; only 86 accounts on the Accountant channel |
| SK | 1,901 | 4.4% | |
| NS | 1,828 | 4.2% | |
| NB | 893 | 2.1% | |
| PE / NF / YT / NU / NT | 955 | 2.2% | PE 419 · NF 384 · YT 87 · NU 36 · NT 29 |
| Other / Unknown | 396 | 0.9% | |
| **Total** | **43,550** | **100%** | Equals the General matrix total |

**Language:** 41,279 accounts English (94.8%) · 2,271 French (5.2%).

**Module adoption is materially lower in Québec than Ontario** — Analytics 14.9% vs 26.9%, Time 10.5% vs 16.9%, Absence 9.7% vs 16.0%, HR 10.1% vs 12.4%. Both the multi-module target and the Québec share target point at the same under-served base.

## Aggregation Recipe

Reproducible from the source workbook. Re-run this whenever the base report refreshes.

**Source:** `Customer Base report_August_2026 (1).xlsx`, Sheet1 — 44,866 data rows × 59 columns. Read directly from the workbook, **not** from a text export: the `.txt` extraction drops empty cells, leaving rows with 39–57 fields against a 59-column header, which silently misaligns every column past `ParentCompany`. Parsing the XLSX preserves cell references and therefore column positions.

**Method** (Python stdlib — `zipfile` + `xml.etree.ElementTree` streaming over `xl/worksheets/sheet1.xml` with `xl/sharedStrings.xml`; no third-party libraries required):

1. **Load** — map each cell to its column index from the `r` attribute; resolve shared strings by index. Header row supplies column names.
2. **De-duplicate** on `CustID`, keeping the first occurrence (removes 34 rows → 44,832 unique accounts).
3. **Filter to active** — parse `LastRegularRun` as `%b %d %Y`; keep accounts whose last run is 0–365 days before the 2026-08-31 snapshot → **43,550 accounts**.
4. **Size band** — `EECount` → Micro 1–19 / Small 20–99 / Mid 100–499 / Large 500+; zero or missing → Unknown.
5. **Vertical** — `Industry` verbatim; blank → `Unclassified`; sectors outside the ten largest → `Other`. One display fix: the source value `Other Services (except Public Administration` is missing its closing parenthesis; the tables above add it. String-matching a re-run against these labels needs that one character allowed for.
6. **General matrix** — count by (vertical, size band).
7. **Module matrices** — filter to flag `= '1'` per column, then count by (vertical, size band). Columns: `ESS`, `HR`, `TM`, `AM`, `AnalyticsV2`, `AnalyticsPro`.
8. **Province / language** — count by `Province` and `Language` on the active set.

**What was deliberately not extracted:** individual customer names, `CustID` values, parent companies, franchise brand names, sales-rep and CSR names, and any per-account row. Only aggregates are recorded in this repo, per the engagement's data-handling rule.

**What cannot be produced from this source:** ARR, MRR, price, contract value, ACV, or any revenue-weighted figure — no such field exists.

## Maintenance

- **Confirm tier** (`governance/write-policy.yaml`): every edit shows the exact before/after and gets an in-session yes; headless runs file a proposal in `governance/proposals/` instead.
- **Refresh:** full refresh each quarter alongside `current-quarter.md`; between quarters `/context-update` refreshes the affected cells when an account lands, churns, or is re-segmented. Bump `_updated:` and the snapshot date on every change.
- **Sources:** the Customer Base report above; managed accounts carry `vertical`, `size_band`, and `use_cases` in [portfolio.yaml](../../customers/accounts/portfolio.yaml). Register the base report as a query in `analytics/queries/` and in `data-catalog.yaml` when the warehouse is wired.
- **Read by:** `/product-brief-draft`, `/impact-sizing`, `/prioritize-requests`, `/expansion-strategy`, `/retention-analysis`, `/activation-analysis`, `/strategy-sprint`, `/write-prod-strategy`, `/portfolio-pulse` — any work that needs segment denominators or revenue weighting.
