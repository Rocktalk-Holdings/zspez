# Schema — rules of this workspace

When practice and this file disagree, reconcile the same day.

## Node types

| `type:` | Lives at | Carries |
|---|---|---|
| object | `icm/map/objects/*.md` | noun card: why, shape, Hits / Does not hit |
| process | `icm/map/processes/*.md` | verb card: Input → Movement → Output |
| change-note | `icm/01_triage/output/` | one requested change |
| stage-contract | `icm/**/CONTEXT.md` | Inputs / Process / Outputs / Human check |

## Labels

`type`, `universe` (`live` / `leftover` / `ghost`), `status` (`stub` / `verified` / `stale` / `draft` / `approved`), `entity` (owning path).

`verified` requires a date, a commit or branch, and a citation. No citation → `stub`.

## Naming

- Slugs: kebab-case (`landing-page.md`).
- Stage folders: `NN_kebab-name` only where sequence matters.
- Meta folders: underscore prefix (`_shared/`, `_templates/`, `_meta/`).
- One home per fact. Link; do not copy copy or CSS into cards.

## Universes

Defined in `icm/CONTEXT.md`. Cards must declare `universe:`.
