# edit-surfaces — what you may change

One job: name the files a later agent or a non-developer may edit without a restructure.

## Inputs

- Working (this run): the change request (or `../01_triage/output/change-note.md` if it exists)
- Reference (every run): `../map/effects/CONTEXT.md`
- Reference (every run): `../do-not-touch/CONTEXT.md`

Do NOT load: `_templates/`, prior run `output/` folders, or a full slurp of `index.html` until the request names a section.

## Process

1. Match the request to a row below.
2. Open only those paths.
3. If the request is not on this list, stop and write a note in triage — do not invent a new surface.

## Outputs

- A short list of paths you will edit (usually written into the triage change note)

## Human check

The path list is short enough to read on a phone. Nothing from `do-not-touch` is on it.

## Surfaces (live)

| You want to change | Edit | Also open |
|---|---|---|
| Headline, lede, button labels | `index.html` hero (~L569–L575) | `#contact` wording if the promise changes |
| Method / focus / values copy | the matching `<section>` in `index.html` | `../_shared/brand.md` (pointers only) |
| Colors, radius, type | `:root` in `index.html` (~L8–L26) | hover/focus styles that use those tokens |
| Nav or footer links | `header.nav` / `footer` | matching `href="#…"` IDs |
| Contact email | footer mailto (~L867) | any visible email string |
| Photos | files in `assets/` **or** the `src=` strings | `../map/objects/image-assets.md` |
| Map or runbook | the named `icm/**/CONTEXT.md` | `_templates/` if you add a type |

Safe for a Markdown-only owner: files under `icm/` (contracts, cards, notes). Page copy still lives in `index.html` — that is HTML, not Markdown.
