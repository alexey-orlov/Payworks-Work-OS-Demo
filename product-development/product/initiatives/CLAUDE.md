# Initiatives

One living page per initiative — the current-work layer that joins what the functional
folders separate. An initiative is a work effort ("XYZ v2.0", "XYZ global expansion")
targeting one or more durable features from `product-development/feature-index.yaml`.

**Read this when:** You need the state of a piece of current work — its goal, artifacts,
decisions, and open loops — in one page, without grepping six folders.

## Rules

- **Create** a page (copy `../handbook/templates/initiative-page-template.md`) when an
  initiative starts — first PRD draft, first scoped work. `/product-brief-draft`, `/context-update`,
  and the OS Console do this; check this folder for an existing page before creating (one
  page per initiative). **Creation requires targets**: the frontmatter names ≥1 feature
  and/or area from the catalog — an unmapped initiative cannot exist (the creator resolves
  this from context, proposing the `planned` catalog entry when the feature is new).
- **Slug** is kebab-case, immutable, and unique across areas + features + initiatives —
  the versioned pattern is `{feature}-v1`, `-v2`, … (the page name IS the initiative's id
  everywhere: artifact filenames, record frontmatter, gate verdicts).
- **Frontmatter is the machine header** — `status:`, `note:`, `updated:`, `owner:`,
  `areas:`, `features:` (+ optional `customers:`, `competitors:`), per
  `governance/link-schema.yaml`. Legacy `_status:`-style pages stay readable; `/wiki-lint`
  offers the conversion.
- **Edit in place** — the page always describes current truth. Artifacts and decisions
  are LINKED, never restated. Budget ≤120 lines.
- **`## Instructions`** (optional, ≤400 chars) is initiative-specific steering — read it
  before working the initiative and follow it. **`## Sources`** lists the initiative's
  source-of-truth folders/documents in priority order (first wins on conflict); consult
  them when drafting or folding material for this initiative.
- **Close, don't delete**: on ship/kill set `status: shipped` (or `killed`) with the
  outcome in `note:`, link the launch-gate verdict, keep the lessons. Closed pages stay —
  they hold the record, and the staleness check exempts them.
- Statuses: `exploring` · `active` · `paused` · `shipped` · `killed` (`exploring` = filed
  but not yet committed work; flip to `active` in place when the team commits). **Every
  status change appends a dated Activity line in the same change** — transitions are
  events; writers per the one-writer table in `governance/write-back-contract.md`.

## Contents

### Files

- [expense-management-vp2.md](expense-management-vp2.md) — **active** · Expense Management VP2 (A/B 2.0), the second Value Package; in definition, owner Michelle Tremblay
- [employee-onboarding.md](employee-onboarding.md) — **active** · Onboarding as its own module (HR 2.0), cross-module across HR + Payroll + ESS; owner Claire Sutton
- [performance-management-discovery.md](performance-management-discovery.md) — **active** · Discovery for Performance Management (HR 1.0); hosts the 13-record design-partner corpus, owner Margaret Foster
- [expense-management-vp1.md](expense-management-vp1.md) — **shipped** · Expense Management VP1, mobile-first limited launch; kept as the historical record VP2 and its decisions refer back to

_Append a one-line entry to the end of this list for every initiative page you create._
