# icm — maintenance map

One job: route a later agent (or a phone reviewer) to the right shelf. The live site stays at the repo root.

Form: **system map** of `index.html` + `assets/`, plus a **maintenance pipeline** (`01_triage` → `04_pr`). Product code is not moved here.

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

## How to walk

1. Task → row in `AGENTS.md`.
2. Open that folder's `CONTEXT.md` only.
3. Load only its Inputs. Write only its Outputs.
4. Stop at Human check.

Do NOT load: the whole of `icm/`, both `AGENTS.md` and this file as payload, or `index.html` unless the contract lists it.

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
