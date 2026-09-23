# polyglot-notebook: conventions

## Language codes

EN, PL, ES, EU, BE, LA, +1 (NEW), ∑ (shared).

## Colour tokens (Okabe-Ito)

| Code | Hex |
|---|---|
| EN | #0072B2 |
| PL | #D55E00 |
| ES | #E69F00 |
| EU | #56B4E9 |
| BE | #009E73 |
| LA | #CC79A7 |
| NEW | #7f7f7f |
| shared | #1f1f1f |

Okabe-Ito yellow is left out on purpose: it is invisible on cream paper.

## Planned paper mapping (Zebra Mildliner, not yet in the page)

EN Mild Blue, PL Mild Vermilion, ES Mild Orange, EU Mild Smoke Blue, BE Mild Blue Green, LA Mild Magenta, +1 Mild Gray, ∑ black pen.

## Belarusian rule

Every example is written in Cyrillic and łacinka, separated by "/". Where classical łacinka marks assimilative softness, give that variant too.

## Pages

- `site/index.html` (EN) is primary and served at `/`. `site/ru/index.html` is the Russian option at `/ru/` and must be kept in sync with it.
- Dark colour scheme is the default: `<html data-theme="dark">` in both pages.
- Pages are single-file and self-contained. No build step. The only external resource allowed is Google Fonts.
- Any page edit must keep `node --check` passing for the inline script.
- Page allocation lives in the `plan` array and the `tabs` array. Change both together, in both pages, and update the local ADR in `docs/decisions/` (gitignored, not published).
- No personal data on public pages.

## Commits

verb-Description, imperative, short. Examples: "Add notebook layout page", "Configure Pages deployment".
