# _shared — factory reference

One job: hold stable constraints the maintenance pipeline re-reads every run.

## Inputs

- Working (this run): none — these files change only when brand or verify rules change
- Reference (every run): `brand.md`, `verify-checklist.md`

Do NOT load: stage `output/` notes, object cards, or `index.html` from here.

## Process

1. Open only the file a contract named.
2. Treat paths in `brand.md` as the home of the fact. Do not copy page copy here.

## Outputs

- Edits to these files when a human changes brand rules or the verify list

## Human check

If you added a color, address, or checklist item, confirm it is not already stated in `index.html` — link there instead.
