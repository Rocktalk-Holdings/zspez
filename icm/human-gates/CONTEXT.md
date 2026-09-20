# human-gates — Markdown and phone PR

One job: tell a non-developer what to read before anything merges. Review is expected on a phone.

## Inputs

- Working (this run): `../04_pr/output/pr-draft.md` and the GitHub PR
- Working (this run): `../03_test/output/test-notes.md`
- Reference (every run): `../do-not-touch/CONTEXT.md`

Do NOT load: the full `index.html` diff unless the PR says copy or layout changed.

## Process

1. Read the PR title and the first screen of the body on your phone.
2. Confirm the walk-test / test notes name files you recognize.
3. Open the Files tab. Reject a surprise move of `index.html` or `assets/`.
4. If copy changed, read the new sentences aloud. If they are not what you asked, comment; do not merge.

## Outputs

- Approve, comment, or request changes on the PR. The next agent reads that decision.

## Human check

You (the owner) can answer: what changed, how it was checked, and whether any do-not-touch row was crossed. If you cannot, ask for a shorter PR body.

## Phone checklist

- [ ] Title is one line you understand.
- [ ] Body lists files, not a lecture.
- [ ] Test notes say how they opened the page.
- [ ] No folder move of the live site.
- [ ] Address, email, and legal name unchanged unless you asked.
- [ ] Images: if the PR claims photos work, you see a screenshot of a visible photo — not an empty frame.
- [ ] ICM-only PRs do not rewrite page copy "while we were here."
