# 0001. Notebook page allocation

Status: accepted

## Context

One blank Midori MD A6 notebook (176 pages) holds several languages: EN as the main language, PL, ES and EU as active languages, BE in maintenance mode, LA for reading, and room for one more language later. Each section needs its own edge tab so it can be opened by feel. Paper cannot be reallocated after the fact, so the split has to leave room for growth.

## Decision

Source of truth: the `plan` array in `site/index.html`. Edge tabs: the `tabs` array in the same file.

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

Total: 176.

Reasons:

- PL, ES and EU get equal blocks (15 pages each). None of them is prioritised over the others.
- The +1 reserve is a block of its own, so a new language gets its own edge tab instead of sharing space.
- Lists (mistakes, false friends, phrases, beautiful words, resources) grow from the back of the notebook towards the middle.
- When any language section is full, it continues in the open section (120-155).

## Consequences

- EN has the largest block; BE and LA are small by design.
- The open section is the only buffer. When it is used up, the notebook is full.
- Any change to the allocation must update the `plan` array, the `tabs` array and this ADR together, in both `site/index.html` and `site/ru/index.html`.
