# 🍕 Margherita Papers

Konrad & Natalia review pizza. A small, slow, memoir-style Hugo site — no scores, ever.

- **Design:** planning + mockups in [design/](design/); the built site is a tiny custom theme in [layouts/](layouts/) (one serif + one sans, warm newsprint, light only).
- **Planning docs:** [project.md](project.md) · [research.md](research.md) · [names.md](names.md)

## Run it locally

Needs [Hugo **extended**](https://gohugo.io/installation/) (v0.163+):

```bash
hugo server        # → http://localhost:1313
```

## Add a review

```bash
hugo new reviews/some-place/index.md
```

That scaffolds the fixed nine-field list in the front matter. Fill it in, write the memoir below it, drop photos in the same folder, and flip `draft = false`:

```markdown
+++
title = "Some Place"
date = 2026-07-05
number = 3
place = "City, Country"

[review]
style = "…"
base = "…"
crown = "…"
cheese = "…"
tomatoes = "…"
oliveOil = "…"
leoparding = "…"
alveolation = "…"
beauty = "…"
+++

The memoir goes here.

![The pizza, folded](photo.jpg)
```

Photos added with `![caption](photo.jpg)` are resized to ~1400px WebP automatically at build time (see [layouts/_default/_markup/render-image.html](layouts/_default/_markup/render-image.html)). While drafting you can use `{{</* pizza caption="…" */>}}` as a placeholder where a photo will go.

Any field left `""` renders as a blank line rather than being dropped — the list is always the same nine rows.

## Deploy (GitHub Pages)

1. Repo **Settings → Pages → Source → GitHub Actions**.
2. In [.github/workflows/hugo.yml](.github/workflows/hugo.yml), uncomment the `push:` trigger.
3. Push to `main`; the site builds and deploys itself.
4. **Custom domain:** buy `margheritapapers.com`, add it under Settings → Pages → Custom domain, and point DNS — apex `A` records to GitHub Pages (`185.199.108–111.153`), `www` `CNAME` to `0xkkonrad.github.io`. Tick *Enforce HTTPS*.

`baseURL` in [hugo.toml](hugo.toml) is set to the intended domain; the workflow overrides it with the live Pages URL until the domain is attached.
