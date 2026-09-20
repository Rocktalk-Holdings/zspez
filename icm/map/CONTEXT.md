# map — what this site is

One job: answer *what is X* and *what else moves* without reading all of `index.html`.

The subject tree is the source of truth. Cards cite it. Cards are not a second spec.

## Inputs

- Working (this run): the noun or change you were asked about
- Reference (every run): `objects/_index.md`, then **one** card
- Reference (every run): `effects/CONTEXT.md` when the question is impact
- Reference (every run): `../CONTEXT.md` (universes and collisions)

Do NOT load: every file under `objects/` or `processes/`. The index exists so you do not.

## Process

1. Find the noun on `objects/_index.md`.
2. Open that one card (or `effects/` if you already know X).
3. Follow `See` to source if you will edit.

## Outputs

- A spoken answer: what X is, Hits, Does not hit. No new files unless you are adding a card from `_templates/object.md`.

## Human check

The answer cites a path. If two cards disagree, fix the card — do not patch `index.html` to match a card.

## Shelves

| Shelf | Job |
|---|---|
| `objects/` | Nouns: page, images, form |
| `processes/` | Verbs that actually run in the browser |
| `effects/` | If you change X, open these cards |
