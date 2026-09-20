# Zspez

Static marketing site for Zspez LLC. The live product is `index.html` plus `assets/`. This file routes; it does not hold copy, CSS, or run notes.

## Cold start (stationed agent)

1. This file — where you are.
2. `icm/CONTEXT.md` — where to go.
3. The matching area `CONTEXT.md` under `icm/` — what to do.

Stop after those three reads. Do not slurp the tree.

## Where things live

| Path | Job |
|---|---|
| `index.html` | Live page: markup, CSS, carousel and form JS |
| `assets/` | Live PNG images. HTML still names missing JPGs. |
| `icm/` | System map + maintenance catalog |
| `icm/_templates/` | Copy-instantiate blanks |
| `icm/map/` | Nouns, verbs, change-impact |

## Route by task

| If | Open | Then |
|---|---|---|
| What is X / what else moves | `icm/map/CONTEXT.md` | one object or `map/effects/` |
| Safe to edit? | `icm/edit-surfaces/CONTEXT.md` | stop |
| Must not touch? | `icm/do-not-touch/CONTEXT.md` | stop |
| How to verify | `icm/verify/CONTEXT.md` | stop |
| Human / PR check | `icm/human-gates/CONTEXT.md` | stop |
| A change request | `icm/01_triage/CONTEXT.md` | then `02` → `03` → `04` |
| New card or stage | copy `icm/_templates/` | do not start from blank |

## Rules

- Do not move product files into `icm/` or numbered folders.
- Load only the contract plus its listed inputs.
- Nothing advances until a human has read the last `output/`.
- `CLAUDE.md` is a pointer here. Do not fork a second catalog.
