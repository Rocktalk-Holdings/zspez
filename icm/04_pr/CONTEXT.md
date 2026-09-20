# 04_pr — draft the pull request

One job: write a PR a phone reviewer can finish without opening the repo.

## Inputs

- Working (this run): `../01_triage/output/change-note.md`
- Working (this run): `../02_change/output/change-log.md`
- Working (this run): `../03_test/output/test-notes.md`
- Reference (every run): `../human-gates/CONTEXT.md`

Do NOT load: the full map; do not start a second change in this PR.

## Process

1. Draft `output/pr-draft.md`: title, files, test proof, walk-test if the map changed.
2. Open the PR against `main`. Keep the body short.
3. Stop. Merge is a human gate.

## Outputs

- `output/pr-draft.md`
- The GitHub PR

## Human check

Owner uses `../human-gates/CONTEXT.md` on their phone. Nothing merges until they approve.
