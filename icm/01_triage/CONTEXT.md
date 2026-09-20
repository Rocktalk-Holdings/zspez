# 01_triage — name the change

One job: turn a request into one change note before anyone edits the site.

## Inputs

- Working (this run): the human's request (chat, issue, or PR comment)
- Reference (every run): `../edit-surfaces/CONTEXT.md`
- Reference (every run): `../do-not-touch/CONTEXT.md`
- Reference (every run): `../map/effects/CONTEXT.md`
- Reference (every run): `../_templates/change-note.md`

Do NOT load: `index.html` in full; `02_change` or later; every object card.

## Process

1. Copy `../_templates/change-note.md` to `output/change-note.md`.
2. Fill Request, Surfaces, Hits / Does not hit from `map/effects`.
3. If a do-not-touch row matches, set `status: blocked` and stop.

## Outputs

- `output/change-note.md`

## Human check

Read the Surfaces list on a phone. If it names a folder move or a new backend, do not start `02_change`.
