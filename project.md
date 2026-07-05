# 🍕 Margherita Papers

Konrad & Natalia review pizza. A tiny Hugo site — lifestyle / memoir-style blogging, strictly non-commercial, updated less than once a month. Name chosen 2026-07-05; domain **MargheritaPapers.com** (buy once design is locked).

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
2. [x] Choose a name from a large set of proposals → [names.md](names.md) — **chosen: Margherita Papers** (MargheritaPapers.com)
3. [x] Choose a design direction → [design/](design/) — **chosen: The Broadsheet, then simplified** (one serif + one sans, h1/h2/text, light-only newsprint). Built as a custom Hugo theme.

### Phase 2 — Build the whole website

1. [x] Scaffold Hugo + minimal theme, GitHub Pages deploy — done (custom theme in [layouts/](layouts/), sample content, deploy workflow ready in [.github/workflows/hugo.yml](.github/workflows/hugo.yml)). See [README.md](README.md).
2. [ ] Pull all the old reviews from Konrad, including photos ← **next**
3. [ ] Write 1–2 posts → Konrad has a look, requests changes
4. [ ] Write the rest

### Ship

- [ ] Buy domain: **MargheritaPapers.com**
- [ ] Enable GitHub Pages (Settings → Pages → GitHub Actions) + uncomment `push:` trigger
- [ ] Publish

## Stack (planned)

Hugo + **hugo-bearblog** (winner — ~6 KB pages, zero JS; runner-up: Etch; shortlist in [research.md](research.md)), deployed to GitHub Pages via the official Actions flow, custom domain on top. Photos as page bundles with a resize render-hook.
