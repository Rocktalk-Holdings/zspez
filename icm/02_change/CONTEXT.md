# 02_change — edit the named files

One job: apply only the surfaces on the approved change note.

## Inputs

- Working (this run): `../01_triage/output/change-note.md`
- Reference (every run): `../do-not-touch/CONTEXT.md`
- Working (this run): the subject files the note listed (`index.html`, `assets/…`, or `icm/…`)

Do NOT load: other sections of `index.html` "to tidy"; prior run notes.

## Process

1. Confirm the note is not `blocked` and a human has read it.
2. Edit only listed paths.
3. Write `output/change-log.md`: path, what changed, what you refused to touch.

## Outputs

- Edits on the subject files
- `output/change-log.md`

## Human check

The change log paths match the note. Diff has no surprise `index.html` move and no extra copy rewrite.
