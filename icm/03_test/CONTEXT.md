# 03_test — run the proof

One job: execute verify for the files `02_change` touched.

## Inputs

- Working (this run): `../02_change/output/change-log.md`
- Reference (every run): `../verify/CONTEXT.md`
- Reference (every run): `../_shared/verify-checklist.md`

Do NOT load: object essays; do not re-edit the site in this stage.

## Process

1. Open the page the way `verify/CONTEXT.md` says.
2. Run only the checklist rows the change can hit.
3. Write `output/test-notes.md`: command or URL, viewport, each row pass/fail.

## Outputs

- `output/test-notes.md`

## Human check

A second person can repeat the same clicks from the notes. If a row failed, do not open `04_pr` — go back to `02_change`.
