# PRDs

Product requirements documents, subfoldered by product area. **Files key by INITIATIVE
slug** — one PRD per initiative (`{initiative-slug}-product-brief.md`), filed under the initiative's
primary (first-listed) area; a feature's history is the sequence of its initiatives' PRDs.
Every file carries `initiatives:` frontmatter per `governance/link-schema.yaml`.

**Read this when:** You need a spec. The catalog (`feature-index.yaml`) says which area a
feature lives in; the initiative pages targeting it link the PRDs.

## Contents

### Subfolders

- [examples/](examples/) — Reference PRDs showing the expected shape and depth. Not live specs
- [general/](general/) — PRDs not yet assigned to a product area. Retag into a real area when one emerges
- `{area}/reviews/` — Review artifacts for that area's initiatives, all keyed by initiative slug: `[initiative-slug]-challenge-[YYYY-MM-DD].md` (`/product-brief-challenge` — dated, one per run), `[initiative-slug]-red-team.md` (`/red-team`), `[initiative-slug]-assumption-map.md` (`/assumption-map`), `[initiative-slug]-premortem.md` (`/pre-mortem`), `[initiative-slug]-[job-slug]-micro-job-challenge-[YYYY-MM-DD].md` (`/micro-job-challenge` — dated, one per run)

- [performance-management/](performance-management/) — PRDs for the Performance Management module (HR 1.0); first brief filed 2026-08-31

### Created on demand

- `{area}/` — one folder per product area in `feature-index.yaml`, created when that area's first PRD is filed. Add a one-line entry above for every area folder you create, and give the new folder a 5-line `CLAUDE.md` stub plus a `reviews/` subfolder.
