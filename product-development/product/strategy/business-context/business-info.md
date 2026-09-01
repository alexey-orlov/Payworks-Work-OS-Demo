# Business Information

The durable answer to: who are we, what do we sell, to whom, at what price, and how do we win.

**What belongs here:** identity, product, market, ICP and personas, value proposition, business model, GTM motion, and product principles. Things that change a few times a year at most.

**What does not:** quarterly OKRs (`../current-quarter.md`), competitor teardowns (`product/competitive-research/`), metric definitions (`analytics/metrics/`), segment counts and ARR mix ([segmentation-matrix.md](segmentation-matrix.md)), team roster and Slack channels (root `CLAUDE.md`). Every section below that overlaps one of those links out instead of copying it.

A summary of this file lives in the root `CLAUDE.md` and loads every session. When you change something here that also appears there, update both.

> **Provenance.** Every value below was extracted from Payworks' own documents during `/customize-os context-core` on 2026-08-30: the FY27 Product Strategy deck, the Product Vision, the Architecture & JTBD deck, the Company Priorities & Roadmap deck, the Product Development Workflow SOP (DRAFT, July 2026), the Roadmap Hub Maintenance SOP (DRAFT v1.2), and the August 2026 Customer Base report. Per-item quotes and sources: `os-installation/customization-facts.yaml`. Anything the sources did not state is marked `[GAP: …]` — never filled with a plausible guess.

## Company Overview

### Basic Information

**Company Name:** Payworks

**Industry:** Canadian payroll and HR software (B2B SaaS)

**Stage:** [GAP: not stated in any source — provide funding/ownership stage]

**Founded:** [GAP: no founding year stated. The decks claim "Proudly Canadian. 25+ years." and "25 years of Canadian payroll ground truth" — an operating-history claim, not a founding date]

**Size:**
- Employees: [GAP: internal headcount not stated in any source]
- Revenue: [GAP: no ARR/MRR figure in any source; the August 2026 Customer Base report carries no revenue field — see [segmentation-matrix.md](segmentation-matrix.md)]
- Funding: [GAP: not stated]

**Website:** payworks.ca

**Operating footprint:** Canada only — all 13 provincial and territorial jurisdictions. Two Canadian data centres; SOC 1 and SOC 2 certified.

---

## Product Information

### Core Product

**Product Name:** Payworks

**One-Line Description:**
A six-module Canadian payroll and HR suite on one shared database, built for Canadian businesses and the accountants and bookkeepers who advise them.

**Detailed Description:**

Payworks runs payroll, HR, time, absence, employee self-service and workforce analytics for Canadian employers on a single shared database — no rekeying between modules, hosted in two Canadian data centres, SOC 1 and SOC 2 certified. The company's stated position is correctness: *"We win by being the payroll and HR system Canadian businesses and their accountants trust to be right."* Canadian compliance is treated as home ground rather than a localization layer — CPP, EI, ESA variance across 13 jurisdictions, CRA remittances, RL-1s, and WSIB/WCB.

The stated direction is a shift in kind, not just in feature count: *"We are evolving from Canada's most trusted system of record into an intelligent system of action."* That is delivered through an **intelligence layer** — a capability running through the whole platform rather than a module or a bolted-on chatbot. It is always-on, embedded in workflow, role-aware, grounded in the customer's data, and transparent about what it is doing. It is explicitly bounded: it does not make decisions, does not act without user confirmation on consequential actions, does not claim to be human, and does not replace the expertise of administrators, accountants or bookkeepers.

Two named sub-products carry the FY27 strategy: **Aurora**, the agentic-payroll wedge aimed at segments no incumbent economically serves and doubling as the R&D lab whose proven AI flows upmarket into the core product; and **Orbit Pulse**, a correctness amplifier. The stated ambition for the suite as a whole is that *"Payworks is becoming the platform that makes Canadian businesses feel like they have a full HR and payroll department."*

### Product Categories

**Primary Category:** Payroll and HR software for Canadian employers

**Secondary Categories:** Time and attendance · absence/leave management · workforce analytics · employee self-service

**The six modules** — Payworks' own term is *modules*, delivered as one suite on one shared database. The catalog of named capabilities under each lives in `product-development/feature-index.yaml`.

| Module | What it does | Primary roles |
|---|---|---|
| **Payroll** | Process, remit, report — compliant, accurate payroll every pay period | Admin, Bookkeeper, Accountant, Owner |
| **Human Resources** | Lifecycle, benefits, talent — hire to retire | Admin, Manager, Employee |
| **Time Management** | Capture hours, schedule shifts, enforce provincial compliance automatically | Admin, Manager, Employee |
| **Absence Management** | Request, approve, track — time off through to payroll with no rekeying | Employee, Manager, Admin, Owner |
| **Employee Self Service** (ESS) | 24/7 employee access to pay, documents, schedule and leave | Employee |
| **Workforce Analytics** | Dashboards, insights, custom Pro reporting — no spreadsheets | Owner, Admin, Manager, Accountant |

**Portfolio roles** — how the FY27 strategy assigns each part of the portfolio a job:

- **Retention floor:** HR PMS · Time · Scheduling · Absence
- **Wallet-share expansion:** Expense · Perform · Onboarding · Comp — "payroll-native modules on the compliance moat"
- **Correctness amplifiers:** Orbit Pulse · pre-run compliance flagging · anomaly detection · reconciliation intelligence — "where AI investment concentrates", described as a horizontal AI layer, not a module

**Technology Stack:**
- Frontend / Backend / Database / Mobile: [GAP: no stack detail stated in any source — collect from Engineering into `engineering/tech-constraints.md`]
- Infrastructure: two Canadian data centres; shared Canadian database across all six modules; SOC 1 and SOC 2 certified

---

## Target Market

### Customer Segments

Qualitative target definitions only. The quantitative mix of the actual base — account counts by vertical × size band, overall and per module — lives in [segmentation-matrix.md](segmentation-matrix.md). Company size and industry below use that file's canonical band and vertical names.

Payworks' own vocabulary for who it serves: **"Canadian businesses and their accountants"**, operating in the **"Canadian SMB payroll and HR workflow"**.

**Primary Customer:**
- **Who:** Administrator — the daily power user who configures, processes, and owns compliance across every module; alongside the Owner who carries the liability
- **Company size:** Micro and Small bands dominate — 60% of active accounts have 1–19 employees, 33% have 20–99 (median 14). See [segmentation-matrix.md](segmentation-matrix.md)
- **Industry:** Broad SMB spread, led by Other Services, Health Care & Social Assistance, Retail Trade, Accommodation & Food Services, and Professional/Scientific/Technical Services
- **Geography:** Canada only, 13 jurisdictions. Strategy concentrates first on **Ontario and Québec**, "where the compliance moat has the most bite"
- **Budget:** [GAP: no pricing or spend band stated in any source]

**Secondary Customer:**
- **Who:** Accountants and bookkeepers — external advisors and hands-on processors who are simultaneously a user segment and the primary distribution channel ("One firm brings a book of clients")
- **Company size:** Accounting and bookkeeping firms carrying a book of SMB clients. 2,983 active accounts (6.9% of the base) are tagged to the Accountant channel today
- **Industry:** Accounting / professional services
- **Geography:** Canada; today concentrated in BC (1,018) and ON (836)
- **Budget:** [GAP: not stated]

**Also served:** multi-location **franchisee operators** managing cross-site labour costs, provincial variance and delegated administration across 2–20+ locations. 1,822 active accounts (4.2% of the base) carry a franchise brand tag, spread across 35 distinct brands and concentrated in food service, retail and personal services; the largest single brand accounts for 521 of them.

### Ideal Customer Profile (ICP)

**Firmographics:**
- Company size: Canadian SMB — the served base centres on 1–99 employees (93% of active accounts)
- Industry: sector-agnostic SMB, with density in services, health care, retail, food service and professional services
- Geography: Canada, 13 provincial and territorial jurisdictions; Ontario and Québec are the FY27 growth concentration
- Tech stack: [GAP: no stated technical requirement]
- Growth stage: [GAP: not stated]

**Behavioral:**
- Current solution: [GAP: no named incumbent or status-quo alternative in any source. The vision doc characterises rivals only as "platforms that treat Canada as an afterthought"]
- Pain points: payroll and HR run on disconnected systems that do not scale; 13 jurisdictions each carry distinct employment standards and tax rules, with Québec adding a layer most solutions handle poorly; the people carrying this are generalists without backup
- Buying triggers: [GAP: not stated]
- Decision makers: Owner and Administrator inside the business; **accountants and bookkeepers are the decisive influence** — "how Canadian SMBs actually choose payroll"
- Buying process: channel-led through accounting and bookkeeping firms; see [Sales Motion](#sales-motion)

### Buyer Personas

Payworks names **seven personas** — *"Each of these personas has different usage patterns, different moments of risk, and different definitions of 'done.'"* The descriptor line for each is from the Product Vision; goals and challenges are the JTBD and pain points stated per role in the Architecture & JTBD deck. Statements in quotation marks under **Stated need** are the deck's own first-person JTBD phrasing, "from the perspective of real Payworks users" — they are documented needs, not interview quotes.

**Persona 1: "The Employee"**
- **Role:** Needs clarity and confidence around their pay, time, and leave
- **Goals:** Access pay info on any device anytime; update personal details without admin help; retrieve year-end tax documents instantly
- **Challenges:** Deduction line items use codes, not plain language; no push notification when pay or documents are available; some sensitive fields still require admin intervention; limited French support in ESS for some workflows
- **Motivations / Decision criteria:** [GAP: not stated — Employees are users, not buyers]
- **Stated need:** "When my details change, I need to update banking or contact info myself so I can ensure payroll accuracy without delays."

**Persona 2: "The Manager"**
- **Role:** Needs to act quickly and correctly on behalf of their team
- **Goals:** Build compliant schedules efficiently; approve time off; run structured performance reviews; spot absence trends early
- **Challenges:** Availability, certifications and budget balanced manually; no real-time alert when an employee approaches overtime; approval notifications delayed or missing; no visibility into which managers are overdue
- **Motivations / Decision criteria:** [GAP: not stated]
- **Stated need:** "When planning the week, I need constraint-aware scheduling tools so I can ensure coverage without breaching ESA rest and overtime rules."

**Persona 3: "The Administrator"**
- **Role:** The daily power user who configures, processes, and owns compliance across every module
- **Goals:** Process a compliant payroll run; file remittances and year-end forms; maintain a single source of truth for employee records; configure absence policy by province
- **Challenges:** Late-surfacing pre-run errors with no fix guidance; provincial rule differences require manual double-checks; remittance due dates not surfaced proactively; stat holiday calendars require annual manual updates; HR changes don't always propagate to payroll fields
- **Motivations / Decision criteria:** [GAP: not stated explicitly — the strategy's correctness thesis implies accuracy and audit as the criteria]
- **Stated need:** "When a pay period closes, I need to process payroll in five steps with guided error resolution so I can meet CRA deadlines."

**Persona 4: "The Business Owner"**
- **Role:** Time-starved decision-maker who needs a safety net, not complexity
- **Goals:** Monitor labour costs in real time; understand turnover and retention risk; stay clear of remittance and year-end liability
- **Challenges:** Cost summaries need manual export — no live owner dashboard; budget vs. actual comparison requires external setup; no proactive retention risk signals
- **Motivations:** Avoiding penalties and director liability
- **Stated need:** "When government deadlines approach, I need CRA remittances auto-submitted and T4s generated so I can avoid penalties and director liability."

**Persona 5: "The Franchisee Owner"**
- **Role:** Multi-location operator managing cross-site labour costs, provincial variance, and delegated administration across 2–20+ locations
- **Goals / Challenges / Decision criteria:** [GAP: the Architecture & JTBD deck carries no franchisee-specific JTBD or pain points — only the Product Vision descriptor above. Closest evidence: 1,822 active accounts carry a franchise brand tag. Worth a round of franchisee interviews]

**Persona 6: "The Accountant"**
- **Role:** External advisor who needs accuracy, auditability, and exportable data
- **Goals:** File remittances and year-end forms; reconcile payroll to the general ledger; share workforce insights with clients
- **Challenges:** Audit trail gaps make change tracing difficult; sharing requires CSV export then manual formatting; no scheduled report delivery to stakeholders natively
- **Motivations:** Accuracy and auditability across a book of clients
- **Buying role:** Decisive — the distribution channel, not just a user. "One firm brings a book of clients."
- **Stated need:** "When government deadlines approach, I need CRA remittances auto-submitted and T4s generated so I can avoid penalties and director liability."

**Persona 7: "The Bookkeeper"**
- **Role:** Hands-on processor who needs guided, reliable workflows with room for error prevention
- **Goals:** Process a compliant payroll run; reconcile payroll to the general ledger; calculate stat holiday and shift premiums accurately
- **Challenges:** GL export formats don't match all client charts of accounts; stat pay varies by province and manual calculation is error-prone; disconnected clocks create re-entry errors
- **Motivations / Decision criteria:** [GAP: not stated]
- **Stated need:** "When a pay period closes, I need to process payroll in five steps with guided error resolution so I can meet CRA deadlines."

---

## Value Proposition

### Problem Statement

**The Problem:**
Canadian businesses are managing payroll and HR in ways that don't scale. Time, absence, payroll and HR sit in disconnected systems, forcing owners and administrators to bridge the gaps by hand. Canada's thirteen provinces and territories each carry distinct employment standards and tax rules, and Québec adds a layer most solutions handle poorly. The people carrying this work are generalists without backup, operating in an unforgiving regulatory environment: a missed remittance or an overlooked ESA rule lands on real paycheques and can create personal legal exposure for the owner.

### Solution Statement

**Our Solution:**
One coherent suite on one shared database — six modules, zero data rekeying, hosted in Canada — plus an intelligence layer that "notices what humans miss, surfaces what matters before it becomes a problem." The intelligence layer is not a chatbot and not a feature: *"It is the way the platform thinks alongside its users — a knowledgeable colleague looking over their shoulder."* It is always-on, embedded in workflow, role-aware, grounded in the customer's data, and transparent — and it stops short of deciding or acting without confirmation. The outcome is framed in terms of user confidence: the administrator runs payroll without dread, the owner approves without confusion, the employee understands their pay without calling anyone.

### Unique Value Proposition

**What makes us different:**
1. **Canadian compliance as home ground** — built natively for 13 jurisdictions (CPP, EI, ESA variance, CRA remittances, RL-1s, WSIB/WCB), not localized after the fact
2. **Correctness that compounds** — 25 years of Canadian payroll ground truth feeds AI that reasons about Canadian compliance complexity, producing correctness at scale, which compounds into a "safe choice" position rivals cannot claim
3. **One suite, one database** — six modules that feel like one product, with no rekeying between them
4. **Service no competitor matches** — the vision doc's stated service claim, alongside the natively-Canadian foundation
5. **A channel that lowers CAC as it grows** — accountants and bookkeepers as distribution, where one firm brings a book of clients

**The compounding mechanism**, stated as three linked stages: **Data** ("25 years of Canadian payroll ground truth") → **AI** ("reasons about Canadian compliance complexity") → **Trust** ("correctness compounds into safe-choice position").

**Why customers choose us over alternatives:**
- vs. named competitors: [GAP: no strategy or competitive document names a rival. Positioning is stated only relatively — rivals are "platforms that treat Canada as an afterthought", and incumbents "do not economically serve" the segments Aurora targets. The one name that surfaces anywhere is **Wagepoint**, from initiative-level material — see [Competitive Landscape](#competitive-landscape). Fill `product/competitive-research/` before any competitive claim is used externally]
- vs. status quo / DIY: [GAP: no status-quo alternative named. Closest stated evidence is the problem statement — disconnected systems and manual bridging]

---

## Strategy & Goals

### Company Mission

**Mission Statement:** [GAP: no labelled mission statement in any source]

**Vision:**
*"Payworks is becoming the platform that makes Canadian businesses feel like they have a full HR and payroll department."* Stated as an evolution: **"We are evolving from Canada's most trusted system of record into an intelligent system of action."**

[GAP: no 3–5 year horizon is attached to the vision. The only stated horizon anywhere is the roadmap's "Next 24 Months".]

### Current OKRs and Product Strategy

OKRs, strategic themes, key initiatives, and the explicit "not doing" list are time-boxed, so they live where they actually get updated:

- **This period (FY27):** [../current-quarter.md](../current-quarter.md)
- **Longer range:** [../roadmaps/](../roadmaps/)

The durable strategy frame behind them:

- **Arena:** correctness for Canadian businesses and their accountants, concentrated first in Ontario and Québec
- **Compounding mechanism:** Data → AI → Trust (above)
- **The coupled bet:** *"Product and channel are one coupled bet, not two."* Aurora is the AI-native product wedge and the R&D lab whose proven AI flows upmarket into the core; accountants and bookkeepers are the distribution mechanism. Neither is resourced without the other.
- **Portfolio roles:** retention floor / wallet-share expansion / correctness amplifiers — see [Product Categories](#product-categories)
- **Strategic refusals:** compete on general-purpose HR feature count · chase enterprise upmarket · expand outside Canada · position AI as autonomous

---

## Market & Competition

### Market Size

**TAM / SAM / SOM:** [GAP: no market sizing in any source. The only market figures stated are the FY27 share targets — Ontario 6%, Québec 3%]

**Market Growth:** [GAP: not stated]

**Market Trends:** [GAP: not stated as trends. The strategy's implicit bet is that AI-native payroll plus the accountant channel reshapes how Canadian SMBs choose payroll]

### Competitive Landscape

Per-competitor teardowns live in [product/competitive-research/](../../competitive-research/), one folder per competitor. The cross-competitor view sits beside them: [competitive-landscape.md](../../competitive-research/competitive-landscape.md) and [competitive-matrix.md](../../competitive-research/competitive-matrix.md).

**Direct:** **Wagepoint** — described in the Payroll Hub VP2 Product Brief as *"the most frequently cited competitor in win/loss conversations."* This is the only competitor named anywhere in the material provided, and it comes from initiative-level material, not from any strategy or competitive document.

**Indirect / Status quo:** [GAP: not named anywhere.]

[GAP: **there is no competitor list.** The "Competition landscape" deck contains a title slide — "List Claude can leverage for research" — and five empty slides. The strategy and vision decks name no rival at all, characterising them only as "platforms that treat Canada as an afterthought". This is the single largest open gap in the business context. Closing it needs either the named list from the deck's author or an approved competitive-research pass.]

**Known competitive evidence (internal, from the FY27 strategy):** win-loss exits show a **37% Time Management gap** and a **39% HR gap** — i.e. deals lost where those modules were the differentiator. Closing them is the stated bar for the retention-floor portfolio.

**Our Positioning:**
The safe choice for Canadian payroll: natively Canadian across 13 jurisdictions, correct by construction, and backed by service — against "platforms that treat Canada as an afterthought."

---

## Business Model

### Revenue Model

**Primary Revenue Stream:** Subscription-style recurring billing per module — inferable only from the customer base export, which carries per-module charge dates and run counts (`HRLastChargeDate`, `TMRunCount`, and so on). The modules are separately billed; ESS is on 97.7% of active accounts while HR, Time, Absence and Analytics are each on a minority, which is what makes multi-module adoption a growth lever.

**Pricing Tiers:** [GAP: **no pricing model, tier structure, or price point appears in any source.** The customer base export has no revenue, price, or contract-value field. The only pricing-adjacent statement is a company strategic initiative: "Better price-to-value fit — Pricing & packaging." Provide the price book or a billing export to close this.]

**Known packaging facts:**
- Workforce Analytics: "No add-on required (built into HR & Absence)"; a **Pro** tier adds the Report Designer and custom collections (9 active accounts today)
- Channel and affinity programs appear as account tags in the base: LP Basic (7,006), Accountant (2,983), Chamber (1,875), CFIB (697), LP Complex (589), plus a tail of named partner-integration and referral programs (accounting firms, credit unions, banks, and dealer-system integrations) each carrying 1–270 accounts

### Key Metrics

Headline numbers only. Metric **definitions**, the SQL behind them, and dashboards live in [analytics/metrics/](../../../analytics/metrics/) — that is the source of truth whenever a number has to be reproduced or defended.

**North Star Metric:** [GAP: no metric is labelled as the North Star in any source. The nearest stated candidates are the KPI Framework's Tier 1 Outcome examples — client retention rate, revenue impact, NPS — and the FY27 retention bar of 94%+. Run `/define-north-star` to settle it deliberately rather than inheriting one by accident]

**Business:**
- ARR / MRR: [GAP: not stated in any source; no revenue field exists in the August 2026 customer base export]
- **Active accounts: 43,550** (ran a payroll within 12 months of the 2026-08-31 snapshot) — full breakdown and counting rules in [segmentation-matrix.md](segmentation-matrix.md); its General matrix total must equal this figure
- ARPU: [GAP: requires revenue data]
- Retention: **94%+ is the FY27 bar to defend** (stated as a target/floor, not a current reading)
- NRR: **toward 105%+** (stated as target direction; current NRR not stated)

**Product:**
- **Multi-module adoption: 32% today → 35% FY27 target** (per the FY27 strategy deck). Payworks' own definition of "multi-module" is not stated; independently computed from the August 2026 export, 26.6% of active accounts have at least one of HR / Time / Absence enabled beyond Payroll and ESS, and 28.9% have at least one of HR / Time / Absence / Analytics. **Do not treat the computed figures as the same metric as the 32%** until the definition is confirmed
- Module adoption on the active base: ESS 97.7% · Workforce Analytics 28.1% · Time Management 18.7% · Absence Management 16.4% · Human Resources 12.1% · Analytics Pro 0.02%
- DAU/MAU · Activation · Retention D7/D30 · NPS: [GAP: not stated]

**Market position:**
- **Ontario share: 6% FY27 target** · **Québec share: 3% FY27 target** (current shares not stated). Ontario is 31.7% of the active base today; Québec is 6.8% — the underweight province the strategy names
- Win-loss gaps to close: **37% Time Management · 39% HR**

**Efficiency:** CAC · LTV · LTV:CAC · Payback · Burn multiple: [GAP: not stated. The one stated directional claim is "The channel lowers CAC as it grows"]

**Metric Reporting Conventions** — how metric docs speak to leadership. `/feature-metrics` and the Product Brief template read this block. Payworks has its own house taxonomy, taken from the Product Development Workflow SOP:

- **Summary artifact name:** **KPI Framework** — Section 7 of the eight-section Product Brief, and a standalone artifact in the BA handoff package
- **Level names:** three tiers, always all three —
  - **Tier 1 — Outcome Metrics:** "the business result we are trying to achieve. These are the metrics leadership cares about most." Examples given: client retention rate, revenue impact, NPS
  - **Tier 2 — Product Metrics:** how clients use the feature — adoption and engagement. Examples: feature activation rate, task completion rate, frequency of use
  - **Tier 3 — Quality Metrics:** how well the feature works — stability and performance. Examples: error rate, load time, support ticket volume related to the feature
- **Required per-metric fields beyond the defaults:** a **baseline data source** identified per metric where available; **measurement frequency**. Definition of done for the framework: all three tiers populated with at least one metric each, each carrying its baseline source
- **House rule:** where a baseline is not yet available the metric is marked "Coming soon" — *"do not fabricate numbers"*

---

## Go-to-Market

### Sales Motion

**Sales Model:** Channel-led, coupled to the product bet. *"Accountants and bookkeepers are the distribution mechanism — how Canadian SMBs actually choose payroll. One firm brings a book of clients."* The channel and Aurora are resourced as one bet, not two, and "the channel lowers CAC as it grows."

**Channel state today:** 2,983 active accounts (6.9% of the base) carry the `Accountant` member tag, concentrated in BC (1,018) and Ontario (836) — Québec has just 86, against a 3% provincial share target. A further tail of accounts sits under named accounting-firm, credit-union and bank referral programs. **The channel is the strategy's engine and is currently thinnest exactly where the strategy wants growth.**

**Company GTM initiatives:** "Sales & market expansion — GTM scaling" and "Sales & market expansion — CaPDB".

**Sales Cycle:** [GAP: no deal-cycle duration stated]

**Deal Size:** [GAP: no ACV or deal-size range stated — no revenue data available]

**GTM stage gates** (from the Roadmap Hub SOP): Gate 1 Intake → Gate 2 Kickoff → Gate 3 Readiness → Gate 4 Launch.

### Marketing Strategy

**Acquisition Channels:** [GAP: no marketing or acquisition channel mix stated in any source. The only acquisition mechanism described anywhere is the accountant/bookkeeper channel above. Affinity/association tags in the customer base — Chamber (1,875), CFIB (697), Chamber HR Plus (225) — suggest association partnerships are a real motion, but no source describes them as such]

---

## Product Development

### Development Process

**Methodology:** An AI-first product development lifecycle, documented in the Product Development Workflow SOP (**DRAFT — Proposed Revisions, owner Product Operations, last updated 28 July 2026; not yet published**). Work is structured as a hierarchy: **Initiative → Value Package (VP) → Milestone → Micro-Job.**

**The workflow, end to end:**

**Phase 1 — Information Gathering & Project Setup:** discovery and evidence gathering, producing a Workflow Map (AI-Reimagined), an Opportunity Solution Tree (OST), Jobs to Be Done, a Breadth Prototype, and a knowledge-loaded Claude Project. Gated by a **Readiness Bar** (3+ sources, Workflow Map complete, every micro-job tied to a validated OST opportunity, among others).

**Phase 2 — Produce Output:** three focused chats inside one Claude Project.

| Stage | Produces | Gate |
|---|---|---|
| **Chat 1** | Product Brief (8 sections) + KPI Framework | **Product Leadership Approval** — "Do not begin Chat 2 until this is complete" |
| **Chat 2** | 3–5 Micro-Job specs + Depth Prototype (PM Draft) + Exception List | Four **Pressure Tests** must all pass before a Micro-Job locks: Before/After, Standalone, Vertical/Horizontal, Scope Sanity |
| **Chat 3** | BA Handoff package — Handoff Summary, Product Brief, KPI Framework, all Micro-Jobs, Exception List | Designer's **Translation Checkpoint** before the Dev-Ready Prototype; template-conformance check before sharing |

Then: **Design & Engineering Kickoff.**

**Approval ladder:** Product Leadership approves the Product Brief and KPI Framework — note the SOP's own clarification that *"'Product Leadership Approval' in this context refers to leadership sign-off on the Product Brief — not Value Package."* PM Lead is the first escalation for repeated pressure-test failures and missing knowledge files. Full escalation paths in [stakeholders.md](stakeholders.md).

**Definition of done** (SOP Appendix A1): Brief = all 8 sections approved with no placeholders · KPI Framework = all three tiers with ≥1 metric each plus baseline source · Micro-Jobs = 3–5 specs passing all four pressure tests with no UI language · Exception List = one entry per locked Micro-Job.

**Cadence:** the PM must stay **1–2 micro-jobs (or 2–3 sprints, whichever is greater) ahead of Dev**; slip escalates to Product Leadership immediately. Micro-jobs are sequenced riskiest-assumption-first. Design Partners commit to **biweekly** co-creation calls. The Product Roadmap Hub is updated **weekly**; its SOP is reviewed annually.

**Parallel tracking** (Roadmap Hub): a 7-phase **Build Track** — Discovery & Research → Problem & Scope Definition → Solution Design → Scoping → Planning → Build Prep → Dev Build & Test — running alongside the 4 **GTM Stage Gates**.

**Tools:**
- Project management: Monday.com
- Portfolio source of truth: the Product Roadmap Hub, hosted on the intranet
- AI workspace: Claude Projects (claude.ai) — including the Claude Project Context Pack, the living knowledge centre Dev and BA query in natural language. House rule: *"Every question answered must be written back into the pack, not sent in Slack or email."*
- Documentation / templates: SharePoint (path TBC); PM knowledge files in ShareFile
- Communication: Slack, Outlook (weekly management email), Teams (ad hoc)
- GTM tracking: initiative-specific Excel files
- Design: DSM-aligned prototypes; [GAP: no design tool named — Figma is not mentioned in any source]
- Analytics / Research: [GAP: not named]

**Document Naming Conventions** — Payworks' house terms, used across this OS. Slash commands and machine identifiers stay canonical.

| OS term | Payworks term |
|---|---|
| PRD | **Product Brief** (initiative-level, 8 sections); **VP Product Brief** at Value Package level |
| Job spec | **Micro Job** |
| Jobs breakdown | **Micro Jobs Breakdown** |
| Product area | **Module** |
| Metrics summary | **KPI Framework** |

> **Terminology in motion.** A July 2026 Terminology Proposal (DRAFT — For Review, owner Product Operations) proposes renaming **Micro-Job → "Feature Unit"** and **JTBD → "Problem Statement"**, retiring **Slice**, and consolidating **Solution Prototype → Dev-Ready Prototype**. **No decision box in that document is checked — every rename is undecided.** This OS uses the current terms (Micro Job, JTBD) until Payworks decides. When it does, re-run `/customize-os naming-conventions`.

### Team Structure

The roster — names, GitHub handles, Slack IDs, after-hours escalation — lives in the root `CLAUDE.md`, which loads every session.

**Shape of the product org:** [GAP: no headcount or per-function counts in any source]

**Roles named in the SOPs:** PM · APM · PM Lead · Product Leadership · Product Operations (Product Operations Manager) · Business Analyst · Product Designer · Engineering/Dev · MGT Product · VP of Product. Plus **Design Partners** — 3–5 named external clients who co-create with the product team before and during build, distinct from the Early Access Program.

**Reporting structure:** no formal reporting lines are stated; the SOPs define two escalation ladders — PM/APM → PM Lead → Product Leadership (workflow), and Hub delegate → Product Operations Manager → MGT Product → VP of Product (roadmap hub). Detail in [stakeholders.md](stakeholders.md).

[GAP: no squads, pods, or tribes are described. No QA, Support/Service, Sales or Marketing role appears in the process documents.]

---

## Culture & Values

### Company Values

[GAP: **no company values statement appears in any source.** The nearest artifacts are the four company priorities — Compete and win across Canada · Deliver more value for every client · Modern, competitive platform · Operational efficiency at scale (see [../current-quarter.md](../current-quarter.md)) — and the product principles below. Neither is labelled as values.]

### Product Principles

Six principles, stated as *"the criteria against which we evaluate product decisions. When tradeoffs arise, they should guide us."*

1. **Humans at the centre, intelligence at their service** — we build AI that amplifies human capability, not one that displaces it
2. **Clarity over completeness** — a platform that shows everything is a platform that communicates nothing
3. **Canadian compliance as home ground** — we operate across 13 provincial and territorial jurisdictions (CPP, EI, ESA variance, CRA remittances, RL-1s, WSIB/WCB)
4. **One coherent experience** — Payworks is a suite; it should feel like one product, not a collection of modules
5. **Designed for the generalist** — our users are not HR professionals by training
6. **Trust is earned through accuracy** — every intelligent suggestion, every automated flag, every AI-generated insight is a small deposit or withdrawal from the user's trust account

**Bounds on the intelligence layer** (product-level refusals): it does not make decisions · it does not act without user confirmation on consequential actions · it does not claim to be human · it does not replace administrator, accountant or bookkeeper expertise.

---

## Key Resources

### Communication

**Slack channels:** listed in the root `CLAUDE.md`. Payworks uses initiative channels, a GTM channel, and a product team channel; Slack is where updates land between weekly emails and where the Roadmap Hub owner is flagged. [GAP: channel names and IDs — pull with `/connect-mcps` once Slack is connected]

**Weekly management email** (Outlook): "Product Roadmap & GTM Status, Edition XX", sent weekly to management team members with the Roadmap Hub attached.

**Claude Project Context Pack:** the living knowledge centre Dev and BA query in natural language — answers are written back into the pack, never left in Slack or email.

**Meeting cadence:** agendas, transcripts, and summaries live in [product/meetings/](../../meetings/). Known cadences: weekly management update, weekly Roadmap Hub update routine, biweekly Design Partner co-creation calls, annual Hub SOP review. Periodic rollups live in [product/reports/](../../reports/).

---

**Owner:** Product Team
**Last Updated:** 2026-08-30
