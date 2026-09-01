# Stakeholder Profiles

Living master file — who the stakeholders are, what they care about, and how to communicate with them. **Edit it in place** whenever someone joins, leaves, or changes what they care about. This is not a template: there is exactly one copy, and skills read it as ground truth (meeting prep, Slack drafts, decision docs, prioritization all pull from here).

Names, GitHub handles, and Slack IDs live in the root `CLAUDE.md` Team table — this file covers what the table can't: priorities, decision style, and how to get buy-in.

> Personal managing-up notes — how your manager evaluates *you*, what to withhold, career positioning — belong in your personal OS, never here. See the Privacy Contract in the root `CLAUDE.md`.

> **⚠ Role-level only — names are missing by design, not by oversight.**
> These profiles were derived on 2026-08-30 from the Product Development Workflow SOP (DRAFT, 28 July 2026), the Roadmap Hub Maintenance SOP (DRAFT v1.2), the FY27 Product Strategy deck and the Terminology Proposal. Those documents define **roles and what each role owns and approves** — they do not supply a roster, and the individuals they do name were deliberately not copied in.
> **What each profile still needs from a person:** the name behind the role, communication preference, decision style, and what actually earns a yes. Fill those in place — the responsibilities and approval authority below are already sourced and can stand.

## Executive Leadership

### VP, Product Management — the approving executive
**Name:** [GAP: not available from the source documents — fill from the org chart]

**Standing in the process:** the FY27 Product Strategy is authored under the byline "FY27 · VP Product Management". Together with the Senior Manager, Product Management, this role constitutes **"Product Leadership"** — the body that approves the Product Brief and KPI Framework.

**Cares about:**
- The FY27 test as stated: Ontario 6% share, Québec 3%, retention 94%+, multi-module adoption 32→35%, Aurora live in market, AI attributed to revenue
- Correctness as the compounding mechanism — Data → AI → Trust
- Holding the coupled bet together: "Product and channel are one coupled bet, not two"
- The strategic refusals holding: no general-purpose HR feature-parity race, no enterprise upmarket, no international, no autonomous-AI positioning

**Decision authority:** approves the Product Brief and the KPI Framework at the Chat 1 gate. Note the SOP's own clarification — *"'Product Leadership Approval' in this context refers to leadership sign-off on the Product Brief — not Value Package."*

**Best way to get buy-in:** lead with the revenue or retention consequence, not the feature. Tie the ask to one of the six FY27 test numbers, name which portfolio role it serves (retention floor / wallet-share expansion / correctness amplifier), and show the KPI Framework's Tier 1 Outcome metric with its baseline source. A brief with placeholder sections or an unpopulated tier *"will not pass the Product Leadership Approval checkpoint."*

**Red flags:** proposals that read as feature-count parity with general-purpose HR suites; anything implying enterprise upmarket or geographic expansion beyond Canada; AI framed as autonomous or decision-making.

**Communication preference / cadence:** [GAP: not stated]

---

### VP of Product — roadmap escalation
**Name:** [GAP: not available from the source documents]

**Standing in the process:** the final escalation point for the weekly Product Roadmap Hub update — if the Hub owner is unavailable, escalation runs Hub delegate → Product Operations Manager → MGT, Product → VP of Product, who decides whether the weekly update may be delayed.

**Cares about:** the Roadmap Hub staying current as the portfolio source of truth; the weekly management update going out on time.

> **⚠ Open question for a person:** the sources use both "VP, Product Management" and "VP of Product". They may be the same person or two roles. Confirm before addressing either by title in a document.

---

### CEO · VP Engineering · Head of Design
[GAP: **none of these roles appears in any source document.** The process SOPs are written from the product team's perspective and stop at Product Leadership. Engineering and Design appear as functions with clear responsibilities (below) but no named leader. Add these profiles from the org chart before any skill needs an executive audience outside product.]

---

## Functional Leaders

### Senior Manager, Product Management
**Name:** [GAP: not available from the source documents]

**Standing in the process:** named alongside the VP, Product Management as the second half of the approval pair — the Terminology Proposal records that approval comes from "VP, Product Management and Senior Manager, Product Management."

**Cares about / decision style / green lights:** [GAP: not described in any source beyond the approval authority above]

---

### Product Operations (Product Operations Manager)
**Name:** [GAP: not available from the source documents]

**Owns:**
- The Product Development Workflow SOP itself (currently DRAFT — Proposed Revisions, 28 July 2026, unpublished)
- The Product Roadmap Hub, its weekly update routine, and the weekly management email ("Product Roadmap & GTM Status, Edition XX")
- Claude Project access
- All five artifact templates in SOP Appendix B — every one currently `[PLACEHOLDER] — to be built by Product Ops`
- Drafting the example Micro-Job for the SOP appendix
- The July 2026 Terminology Proposal, and the five open decisions inside it

**Cares about:** consistency of process and artifacts; the Hub reflecting reality every week; templates existing so PMs stop improvising.

**How to work together:** this is the role to go to for anything about how the process itself works, what a template should contain, or where an artifact belongs. It is also the role currently blocking on the most unfinished work — five undecided terminology questions and five unbuilt templates.

---

### PM Lead
**Name:** [GAP: not available from the source documents]

**Owns:** the first escalation rung for PMs and APMs.

**Escalate to this role when:**
- A Micro-Job fails the same pressure test 3+ times — *"This usually signals a scoping problem"*
- A knowledge file is missing or stale
- The handoff sharing process needs confirming (an open SOP action: *"PM Lead to confirm sharing process and update this section before SOP is published"*)

---

### Design / Product Designer
**Name:** [GAP: not available from the source documents]

**Cares about / owns:**
- Receiving the Problem Statement and Micro-Jobs *without* UI prescriptions — the PM specifies the problem, the Designer determines the UI detail
- The **Translation Checkpoint** — verifying component feasibility before the Dev-Ready Prototype
- The **Dev-Ready Prototype**, DSM-aligned. "Designer owns the Dev-Ready Prototype" — Dev builds only from it
- Being consulted, with the BA, on Micro-Job sequencing before the order is locked

**Must-haves:** Micro-Job specs written in problem language, not interface language. A spec containing UI prescriptions fails the SOP's own definition of complete.

---

### Engineering / Dev
**Name:** [GAP: no engineering leader named in any source]

**Cares about / needs:** the Micro-Jobs, the Scope & Boundaries section, and the **Exception List** — "to understand what is being built, what is explicitly not being built." Builds only from the Dev-Ready Prototype.

**Working agreement:** Dev queries the Claude Project Context Pack in natural language before reaching out to the PM — and every answer given is written back into the pack, *"not sent in Slack or email."* The PM must stay **1–2 micro-jobs (or 2–3 sprints, whichever is greater) ahead of Dev**; slipping behind escalates to Product Leadership immediately.

---

### Sales · Customer Success · Marketing · QA
[GAP: **no source document describes these functions.** GTM stage gates exist in the Roadmap Hub SOP (Gate 1 Intake → Gate 2 Kickoff → Gate 3 Readiness → Gate 4 Launch) but no GTM-owning role is named against them. Given the accountant-and-bookkeeper channel is half the FY27 strategy, the channel-owning role is a material gap — add it before any GTM work runs through this OS.]

---

## Key Individual Contributors

### Product Manager / Associate Product Manager
**Role:** Owns every handoff artifact — Product Brief, KPI Framework, Micro-Job specs, Exception List, Handoff Summary — plus the Breadth Prototype (Phase 1) and the Depth Prototype Draft (Chat 2). Runs discovery, competitor research, and kickoff. On the Roadmap Hub, each initiative has a PM or APM owner.

**Influence:** high — the PM is the author of record for everything Design and Engineering build from.

**Review needs:** Product Leadership approval at the Chat 1 gate; PM Lead on escalations; Designer and BA consulted on Micro-Job sequencing before lock.

---

### Business Analyst
**Role:** The SOP is explicit that the BA is **not** a requirements translator: *"BA is the exception engineer — extending the exception list with implementation-level exceptions (database constraints, API limitations, legacy system quirks)."* Also validates compliance rules against the codebase.

**Specialization:** where the spec meets the actual system — legacy constraints, data limits, and the compliance rules that have to hold across 13 jurisdictions.

**When to involve:** at Chat 3 handoff as the receiving role, and earlier alongside the Designer when Micro-Job sequencing is being set.

---

### Architect · UX Researcher
[GAP: no such roles are named in any source document.]

---

## External Stakeholders

### Design Partners
**Relationship:** A small group of **3–5 named external clients** who co-create with the product team before and during build. They see the Breadth Prototype, commit to **biweekly co-creation calls**, and shape the roadmap. Explicitly distinct from the Early Access Program.

**Influence:** high and structural — they are in the process by design, not consulted ad hoc.

**Who they are:** [GAP: the SOP describes the mechanism, not the roster. Name the current Design Partners here and give each an account folder under `product/customers/accounts/`.]

---

### The accountant and bookkeeper channel
**Relationship:** Simultaneously a user persona and the primary distribution mechanism — *"Accountants and bookkeepers are the distribution mechanism — how Canadian SMBs actually choose payroll. One firm brings a book of clients."*

**Influence on product direction:** designated as half of the FY27 coupled bet, alongside Aurora. Neither is resourced without the other.

**Scale today:** 2,983 active accounts (6.9% of the base) carry the Accountant channel tag, concentrated in BC and Ontario, with Québec at 86 accounts against a 3% provincial share target. A further tail sits under named accounting-firm, credit-union and bank referral programs.

**Who to talk to:** [GAP: no individual firms or contacts are recorded here by design — the customer base export is aggregated only. Identify the anchor firms with Sales and give the strategically important ones account folders.]

---

## Communication Matrix

Derived from the SOPs' stated cadences and ownership tables. Names go in the left column once the roster is filled.

| Stakeholder | Frequency | Format | Content Type |
|-------------|-----------|--------|--------------|
| Product Leadership (VP PM + Senior Manager PM) | Per Value Package, at the Chat 1 gate | Product Brief + KPI Framework, submitted for approval | Approval decision — brief must be complete, all three KPI tiers populated with baseline sources |
| Management team | Weekly | Outlook email, "Product Roadmap & GTM Status, Edition XX", Roadmap Hub attached | Portfolio status across Build Track phases and GTM gates |
| VP of Product | Exception-only | Escalation | Whether the weekly Hub update may be delayed |
| PM Lead | As triggered | Escalation | 3+ pressure-test failures on one Micro-Job; missing or stale knowledge files |
| Design + Engineering | Per Value Package, at Chat 3 | BA Handoff package + kickoff meeting | Handoff Summary, Product Brief, KPI Framework, all Micro-Jobs, Exception List |
| Engineering / BA (ongoing) | Continuous | Claude Project Context Pack | Questions answered in the pack, never in Slack or email |
| Design Partners | Biweekly | Co-creation call | Prototype feedback, roadmap shaping |
| Product team / initiative stakeholders | Continuous | Slack — initiative channels, GTM channel, product team channel | Updates between weekly emails; flagging the Hub owner |

**Ownership table** (SOP Appendix A1) — every handoff artifact is owned by the PM/APM; audiences differ:

| Artifact | Primary audience | Owner |
|---|---|---|
| Product Brief | Design + Engineering | PM / APM |
| KPI Framework | Design + Engineering + Product Leadership | PM / APM |
| Micro-Job Specs | Engineering (primary) + Design | PM / APM |
| Exception List | Engineering + Design | PM / APM |
| Handoff Summary | Design + Engineering | PM / APM |

---

**Last updated:** 2026-08-30 — role-level profiles installed by `/customize-os context-core`; person-level detail outstanding.
