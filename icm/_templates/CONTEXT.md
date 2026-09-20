# _templates — copy, then fill

One job: stamp a new card, stage contract, or change note. Never start from a blank page.

## Inputs

- Working (this run): the task that needs a new file
- Reference (every run): `object.md`, `process.md`, `stage-CONTEXT.md`, `change-note.md`
- Reference (every run): `../_meta/schema.md`

Do NOT load: live `index.html`, existing filled cards (except as a shape check).

## Process

1. Copy the matching blank into the destination folder.
2. Fill frontmatter and required sections. Leave unknown fields as `{braces}`, not guesses.
3. Add one catalog line if you created an object (`../map/objects/_index.md`).

## Outputs

- The new file at its real home (not a second copy here)

## Human check

Open the new file. Confirm it still has Inputs/Process/Outputs/Human check (contracts) or Hits / Does not hit (cards). Delete leftover `{placeholders}`.
