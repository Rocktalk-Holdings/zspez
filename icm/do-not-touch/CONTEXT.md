# do-not-touch — stop and ask

One job: name the moves that break the site or the map. A human must approve these before work starts.

## Inputs

- Working (this run): the proposed path list from edit-surfaces or triage
- Reference (every run): `../map/CONTEXT.md`

Do NOT load: CSS/JS internals unless the request is a behavior bug.

## Process

1. Compare the proposal to the table.
2. If any row matches, write `blocked` on the change note and stop.
3. Do not "just this once" move product files into `icm/`.

## Outputs

- A yes/no on the change note: proceed, or blocked with the row you hit

## Human check

A person confirms nothing in the diff is a listed move — especially folder moves and framework rewrites.

## Do not

| Move | Why |
|---|---|
| Move `index.html` or `assets/` into numbered / `icm/` folders | Hosting and clone-to-deploy assume the root page |
| Split the page into a framework without a written gate | There is no build, no package.json, no host config |
| Delete `onerror` on `<img>` before `src` matches a real file | Broken-image icons return (commit `1023111`) |
| Point `src` at a filename that is not in `assets/` | Same as above |
| Add a real form backend or store emails | The handler is `preventDefault` only (`index.html` ~L842) |
| Hand-edit a second catalog (`CLAUDE.md` ≠ pointer) | Routing drifts |
| Invent brand copy, addresses, or metrics | One home is `index.html` |
| Archive or rename `assets/*.png` without updating every `src` | Ghost/live mismatch gets worse |
| Mass-edit ICM cards to "match" a tiny copy tweak | Cards cite; they do not restated copy |

Legal name, street address, and © line: touch only when the owner asked.
