# icm — maintenance map

One job: route a later agent (or a phone reviewer) to the right shelf. The live site stays at the repo root.

Form: **system map** of `index.html` + `assets/`, plus a **maintenance pipeline** (`01_triage` → `04_pr`). Product code is not moved here.

## Inputs

- Working (this run): the task (from chat or a change note)
- Reference (every run): `../AGENTS.md` (already read on cold start)

Do NOT load: every card under `map/`, stage `output/` from an old run, or `index.html` unless the next contract lists it.

## Process

1. Match the task to a Catalog row (or to the `AGENTS.md` route table).
2. Open only that folder's `CONTEXT.md`.
3. Stop. This file does not perform the change.

## Outputs

- The next path to open (spoken or written). No artifact unless you are adding a shelf from `_templates/`.

## Human check

A person can name the next folder from `AGENTS.md` plus this file, without opening a card.

## Universes

| Universe | Meaning here |
|---|---|
| **live** | In force: `index.html`, `assets/*.png`, in-page CSS/JS |
| **leftover** | Present but not the main path: `onerror` image hide |
| **ghost** | Named, not wired: `assets/hero-*.jpg`, `assets/focus-bg.jpg`, form POST |

## Name collisions

| Word | Means | Does not mean |
|---|---|---|
| Hero | Hero section + carousel (`index.html` ~L567) | The PNG files in `assets/` (different names) |
| Focus | `#focus` flip-card section | The missing `focus-bg.jpg` |
| CTA | Hero buttons **or** `#contact` form — say which |
| Contact | In-page form (no network) | Footer `mailto:hello@zspez.com` |

## Catalog

| Folder | Job |
|---|---|
| `map/` | What X is and what a change hits |
| `edit-surfaces/` | Files a human or agent may edit |
| `do-not-touch/` | Files and moves that need a gate |
| `verify/` | How to prove a change |
| `human-gates/` | Markdown / phone-PR checks |
| `01_triage` … `04_pr` | Maintenance run (numbered) |
| `_shared/` | Factory: brand pointers, verify list |
| `_templates/` | Blank stamps |
| `_meta/` | Schema |

Status of a run: scan `01_triage/output/` … `04_pr/output/` for real notes. A `.gitkeep` is not complete.
