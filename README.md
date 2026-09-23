# polyglot-notebook

A personal project about learning several languages in one paper notebook: a blank Midori MD A6 with 176 pages. English is the main language, with sections for Polish, Spanish, Basque and Belarusian, a reserve slot for one more language, and a little Latin. Sections are marked with coloured tabs on the fore edge of the notebook.

## What is here

- `site/index.html` - layout ideas page: page allocation bar, colour system, edge-tab map, page mockups, four switchable styles.
- `site/ru/index.html` - the same page in Russian.
- `content/ru/notebook-starter-content.md` - starter content per language (tables, rules, constructions, phrases), keyed to notebook page numbers. In Russian.

## Run locally

```bash
python3 -m http.server 8000 --bind 127.0.0.1 --directory site
```

Then open http://127.0.0.1:8000/

## Languages

| Code | Language | Role |
|---|---|---|
| EN | English | main |
| PL | Polish | active |
| ES | Spanish | active |
| EU | Basque | active |
| BE | Belarusian | maintenance, every example in Cyrillic and łacinka |
| +1 | reserve | slot for one more language |
| LA | Latin | reading only |

## Page allocation

| Section | Pages | Count |
|---|---|---|
| front matter | 1-7 | 7 |
| EN | 8-37 | 30 |
| PL | 38-52 | 15 |
| ES | 53-67 | 15 |
| EU | 68-82 | 15 |
| BE | 83-92 | 10 |
| +1 reserve | 93-107 | 15 |
| LA | 108-111 | 4 |
| shared spreads | 112-119 | 8 |
| open section | 120-155 | 36 |
| lists from the back | 156-176 | 21 |

Reasons are recorded in [docs/decisions/0001-notebook-page-allocation.md](docs/decisions/0001-notebook-page-allocation.md).

## Licence

- Code: MIT, see [LICENSE](LICENSE).
- Page content (texts, layouts, starter content): [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
