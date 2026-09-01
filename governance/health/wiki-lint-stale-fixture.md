---
date: 2026-08-31
type: deliberate-stale-fixture
removable: true
---

# Deliberate Stale Item — Wiki-Lint Demo Fixture

This file records one deliberately stale nav entry introduced so that `/wiki-lint` has
something concrete to catch and repair during a live demo. Remove this file and fix the
stale entry once the demo is complete.

## What is stale

**File:** `product-development/product/user-insights/CLAUDE.md`
**Section:** `### Files`
**Current text:** `_None yet — /process-meeting files...`
**What it should say:** A one-line entry for the performance-management synthesis:

```
- [performance-management-2026-08-31.md](performance-management-2026-08-31.md) — Cross-interview synthesis across 13 records, 4 accounts, 2026-06-22→2026-08-12
```

## Why it was left stale

Intentional — as a demo fixture to make `/wiki-lint`'s nav-staleness detection visible.
The synthesis exists on disk; the nav index was not updated when it was written.

## How to fix (after the demo)

Edit `product-development/product/user-insights/CLAUDE.md` — replace the `_None yet —`
line with the entry above.

## Why this is a realistic stale item

This is exactly the nav-staleness class that accumulates in production: a file was written
by a skill (`/user-research-synthesis`) but the CLAUDE.md nav update is a separate write
that can be skipped or lost if a session ends early. Wiki-lint's job is to catch and
fix it mechanically.
