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

## Field guide palette (print kit and the "Field guide" style)

| Code | Hex |
|---|---|
| EN | #263f67 |
| PL | #bd3f32 |
| ES | #ba8950 |
| EU | #6b8296 |
| BE | #5a6c4d |
| LA | #aa6e79 |
| NEW | #777777 |
| ink | #28231f |
| muted | #766e61 |
| paper | #f4eedf |

Okabe-Ito stays the default style. The print kit section (`.kit`) always uses the Field guide palette, independent of the style switch.

## Planned paper mapping (Zebra Mildliner, not yet in the page)

EN Mild Blue, PL Mild Vermilion, ES Mild Orange, EU Mild Smoke Blue, BE Mild Blue Green, LA Mild Magenta, +1 Mild Gray, ∑ black pen.

## Belarusian rule

Every example is written in Cyrillic and łacinka, separated by "/". Where classical łacinka marks assimilative softness, give that variant too.

## Pages

- `site/index.html` (EN) is primary and served at `/`. `site/ru/index.html` is the Russian option at `/ru/` and must be kept in sync with it.
- Dark colour scheme is the default: `<html data-theme="dark">` in both pages.
- Pages are single-file HTML with inline CSS and JS. No build step. Static files (images, PDFs) live in `site/assets/`. The only external resource allowed is Google Fonts.
- Print kit: cover pasted onto p. 1; field guide and section dividers are tipped-in extra leaves, so page numbers do not change. Divider page ranges are computed from the `plan` array.
- The A4 print file is the MD A6 PDF imposed 4-up at 100 × 141 mm (95%), so pages fit the notebook without trimming and stay 5 mm clear of the paper edge; order 1-12, then 13 plus copies of 10-12.
- Any page edit must keep `node --check` passing for the inline script.
- Page allocation lives in the `plan` array and the `tabs` array. Change both together, in both pages, and update the local ADR in `docs/decisions/` (gitignored, not published).
- No personal data on public pages.

## Commits

verb-Description, imperative, short. Examples: "Add notebook layout page", "Configure Pages deployment".
