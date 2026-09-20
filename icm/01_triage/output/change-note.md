---
type: change-note
status: approved
universe: live
---

# Change note

## Request

Apply ICM-Architect leave-behind (maintenance map). System map + maintenance runbook; slim AGENTS.md; icm/ with CONTEXT.md for edit surfaces / do-not-touch / verify / human MD gates. Do not mass-move product code. Open a PR on the default branch. Walk-test in the PR body.

## Universe

live (new catalog). Subject tree stays live at repo root.

## Surfaces

- `AGENTS.md` — L0 routing
- `CLAUDE.md` — pointer
- `icm/**` — catalog, map, templates, runbook
- Not in scope: `index.html`, `assets/`

## Hits / Does not hit

- **Hits:** agent cold start, maintenance pipeline, map cards
- **Does not hit:** page copy, CSS, JS, image bytes or `src=`

## Verify

ICM walk test (entry → `icm/CONTEXT.md` → one contract). Confirm `git diff --name-only` has no `index.html` or `assets/`.

## Human gate

Phone review: docs-only PR, product files untouched, walk-test in the PR body.
