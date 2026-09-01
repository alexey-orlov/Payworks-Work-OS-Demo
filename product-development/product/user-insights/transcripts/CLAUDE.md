# Transcripts — the central raw archive

Customer-facing raw transcripts — interviews AND customer calls — in one flat home:
`{YYYY-MM-DD}-{account}-{type}.md` (type: `interview` | `call`). Every file carries tag
frontmatter (`date`, `type`, `customers`, `areas`, `features`, `initiatives`, `themes`)
per `governance/link-schema.yaml` — the tags are what make one conversation findable
from every module it touched. Bodies are immutable; tags are filing metadata, corrected
only via `/retag-transcript` (each change logged in `tag-amendments:`). Summaries stay
with their owners: call summaries in `customers/accounts/{slug}/calls/summaries/`,
interview session reports one level up (`../{date}-interview-insights.md`) — read those
first; come here only when the summary falls short. Internal meeting and retro
transcripts are operational records and stay under `product/meetings/`.

**Read this when:** The summary isn't enough and you need the verbatim conversation, or
you're querying by tag (customer, area, feature, initiative).

## Contents

### Files

- [2026-08-27-northwind-landscaping-call.md](2026-08-27-northwind-landscaping-call.md) — Northwind Landscaping expense discovery call: Controller + HR Manager (first 17 min); receipt flow, job coding, approval chain, payroll register, status visibility, commercial renewal signal
- [2026-06-22-northwind-landscaping-interview-1.md](2026-06-22-northwind-landscaping-interview-1.md) — Northwind Landscaping — Discovery Interview + Prototype Review, HR Manager & Operations Manager, 2026-06-22 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-06-22-northwind-landscaping-interview-2.md](2026-06-22-northwind-landscaping-interview-2.md) — Northwind Landscaping — Discovery Interview + Prototype Review, District Manager, 2026-06-22 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-06-22-northwind-landscaping-interview-3.md](2026-06-22-northwind-landscaping-interview-3.md) — Northwind Landscaping — Discovery Interview + Prototype Review, Regional Operations Manager, 2026-06-22 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-06-23-northwind-landscaping-interview.md](2026-06-23-northwind-landscaping-interview.md) — Northwind Landscaping — Discovery Interview + Prototype Review (Operations Director), 2026-06-23 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-06-24-northwind-landscaping-interview.md](2026-06-24-northwind-landscaping-interview.md) — Northwind Landscaping — Discovery Interview + Prototype Review (Site Operations Manager), 2026-06-24 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-08-maplewood-recreation-interview.md](2026-07-08-maplewood-recreation-interview.md) — Maplewood Recreation — Discovery Interview + Prototype Review, 2026-07-08 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-10-northwind-landscaping-interview.md](2026-07-10-northwind-landscaping-interview.md) — Northwind Landscaping — Discovery interview + prototype review, site supervisor, 2026-07-10 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-15-cascadia-countertops-interview.md](2026-07-15-cascadia-countertops-interview.md) — Cascadia Countertops — Discovery interview + HR-admin prototype review, 2026-07-15 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-17-northwind-landscaping-call.md](2026-07-17-northwind-landscaping-call.md) — Northwind Landscaping — HR Leadership Call, 2026-07-17 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-22-cascadia-countertops-interview.md](2026-07-22-cascadia-countertops-interview.md) — Cascadia Countertops — Prototype review, employee and manager surfaces, 2026-07-22 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-07-29-harbourview-grocers-interview.md](2026-07-29-harbourview-grocers-interview.md) — Harbourview Grocers — Discovery Interview (Office Manager / HR + Payroll Administrator), 2026-07-29 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-08-05-northwind-landscaping-call.md](2026-08-05-northwind-landscaping-call.md) — Northwind Landscaping — Reverse Demo, 2026-08-05 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-08-12-harbourview-grocers-interview.md](2026-08-12-harbourview-grocers-interview.md) — Harbourview Grocers — Prototype Review + Current-Workflow Walkthrough, 2026-08-12 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-08-13-northwind-landscaping-call.md](2026-08-13-northwind-landscaping-call.md) — Northwind Landscaping — Follow-Up Call (HR Manager), 2026-08-13 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-08-18-birchbark-books-call.md](2026-08-18-birchbark-books-call.md) — Birchbark Books & Accounting — Channel Research Call, 2026-08-18 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was
- [2026-08-20-acme-corp-call.md](2026-08-20-acme-corp-call.md) — Acme Corp — Expense Discovery Call, 2026-08-20 (raw transcript) — Raw material, immutable. Customer-side speakers appear under role tokens; the record was

## Writers

`/process-meeting` (interview and customer-call categories) files transcripts here with
their tags proposed from content — raw transcripts handed straight to
`/user-research-synthesis` are delegated to `/process-meeting` for filing too; the
synthesis skill never writes here. `/retag-transcript` corrects tags. Transcripts are the faithful record — raw
names may appear here; the roles-only PII rule applies to the summary layer, never
retroactively to transcripts.
