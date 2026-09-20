# verify — prove the change

One job: say how to test this repo. There is no package manager and no CI.

## Inputs

- Working (this run): `../02_change/output/change-log.md` (or the files you just edited)
- Reference (every run): `../_shared/verify-checklist.md`
- Reference (every run): `../do-not-touch/CONTEXT.md`

Do NOT load: object cards unless Hits named a process you must exercise.

## Process

1. Serve or open the page (below).
2. Run only the checklist rows the change can hit.
3. Write what you did and what you saw to `../03_test/output/test-notes.md`.

## Outputs

- `../03_test/output/test-notes.md` — commands, viewport, pass/fail per row

## Human check

A person can repeat the same open-and-click path from the notes on a phone or laptop. "Looks fine" without a URL or file path does not count.

## How to open the page

From the repo root (pick one):

```bash
python3 -m http.server 8080
```

Then open `http://127.0.0.1:8080/`. Or open `index.html` as a file. Both work: there is no bundler.

## Minimum proof by change type

| You changed | Minimum proof |
|---|---|
| Copy or tokens | Screenshot or notes for the section + one other section that must not have changed |
| Nav / IDs / hrefs | Click every edited link |
| Carousel JS | Dots, hover-pause, and reduced-motion (or state you did not have that preference) |
| Flip cards | Keyboard focus on one card; hover on another |
| Form | Valid submit + empty/invalid submit |
| Image `src` or files | The image is visible (not hidden by `onerror`) |
| ICM docs only | Walk test: `AGENTS.md` → this catalog → one contract; no product diff |

## Known baseline

Hero and focus photos do not display: HTML asks for `.jpg` names that are not in git. PNGs exist under different names. Record that as baseline, not as your regression, unless you touched those paths.
