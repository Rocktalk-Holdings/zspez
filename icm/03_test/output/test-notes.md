# Test notes — ICM leave-behind

Viewport: docs walk (no product UI change). Product proof: `index.html` still at repo root.

## Commands

```bash
git diff --name-only -- index.html assets
# (empty)

python3 -m http.server 8080
curl -sS -o /dev/null -w "%{http_code} %{size_download}\n" http://127.0.0.1:8080/
# 200 34610 — title still "Zspez — Technology For People"
curl -sS -o /dev/null -w "%{http_code}\n" http://127.0.0.1:8080/assets/hero-101.png
# 200
curl -sS -o /dev/null -w "%{http_code}\n" http://127.0.0.1:8080/assets/hero-1.jpg
# 404 — ghost src, documented on image-assets
```

## Walk test

| Check | Result |
|---|---|
| Entry answers where / where to go | Pass — `AGENTS.md` 40 lines, route table |
| Orient in ≤3 reads | Pass — AGENTS → `icm/CONTEXT.md` → area CONTEXT |
| Stage contract complete | Pass — `01_triage` has Inputs / Process / Outputs / Human check |
| Status from `output/` | Pass — change-note + change-log present; `.gitkeep` ignored |
| Routing has no payload | Pass — no page copy in AGENTS |
| One home per fact | Pass — `brand.md` points at `index.html` |
| Product unmoved | Pass |
| What is contact form | Pass — `_index` → `contact-form.md` cites `index.html:837-848` |
| Change hero photos hits | Pass — `effects/` → image-assets + rotate-carousel; not the form |
| See lands on source | Pass — not another essay |

## Checklist rows (product)

Not re-run beyond "file still served": this PR does not edit `index.html`. Baseline image mismatch unchanged (JPG `src`, PNG files).

## Failures

None for the leave-behind. Image `src` mismatch remains a documented ghost, not this diff.
