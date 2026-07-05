# 🍕 pizza

Konrad & Natalia review pizza. A tiny Hugo site — lifestyle / memoir-style blogging, strictly non-commercial, updated less than once a month.

Repo: https://github.com/0xkkonrad/pizza · Local: `/workspaces/sandbox/pizza`

## Principles

- **Very minimalistic.** Lightweight pages, near-zero JS, quiet design, boring tooling. Nothing to babysit between posts.
- **Memoir tone.** Entries are about our life with pizza in it, not consumer-guide reviews.
- **Structured opening.** Every entry starts with the review list below, then the prose.

## The review list

Every entry opens with this list. Fields are fixed; values are free-form prose. A field can be left empty rather than forced.

- Style:
- Base:
- Crown:
- Cheese:
- Tomatoes:
- Olive oil:
- Leoparding & char flavour:
- Alveolation:
- Beauty:

Example (a real one):

> - Style: neapolitan
> - Base: overall tasty, dense but not too heavy, very crispy, proper level
> - Crown: appropriate neopolitan
> - Cheese: good, creamy, well-distributed.
> - Tomatoes: very good, pungent, sweet and umami
> - Olive oil: tasted like nothing, both the table olive oil and the one the pizza
> - Leoparding & char flavour
> - Alveolation
> - Beauty: normal

## Plan

### Phase 1 — Plan & design

1. [x] Research the landscape of existing pizza-review sites → [research.md](research.md)
2. [ ] Choose a name from a large set of proposals → [names.md](names.md) — Konrad & Natalia pick

### Phase 2 — Build the whole website

1. [ ] Scaffold Hugo + minimal theme, GitHub Pages deploy
2. [ ] Pull all the old reviews from Konrad, including photos
3. [ ] Write 1–2 posts → Konrad has a look, requests changes
4. [ ] Write the rest

### Ship

- [ ] Buy domain (blocked on the name)
- [ ] Publish

## Stack (planned)

Hugo + **hugo-bearblog** (winner — ~6 KB pages, zero JS; runner-up: Etch; shortlist in [research.md](research.md)), deployed to GitHub Pages via the official Actions flow, custom domain on top. Photos as page bundles with a resize render-hook.
