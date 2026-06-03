# openaleph.org

Production website for **OpenAleph** — the open-source platform to search documents
and structured data for investigative newsrooms and research organizations,
developed by the Data and Research Center (DARC). <https://openaleph.org>

Built with [MkDocs](https://www.mkdocs.org/) + [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
Content is plain markdown under `docs/`, built and deployed to S3 on every push to
`main`.

> **Forked from the dataresearchcenter.org website repo.** Only the design layer
> (`darc-zensical.css`, loaded by URL) is shared upstream — see
> [Design system](#design-system). Everything else (pages, branding, nav, deploy)
> is openaleph-specific.

## Setup

```bash
python -m venv .venv && . .venv/bin/activate
pip install -r requirements.txt
```

## Develop & build

```bash
mkdocs serve        # http://localhost:8000 (live reload)
mkdocs build        # → ./site
```

Image optimization (the `optimize` plugin) runs in CI only — it's gated on
`CI=true`. To run it locally you also need the `pngquant` binary (`apt install
pngquant` / `brew install pngquant`); Pillow comes from `requirements.txt`:

```bash
CI=true mkdocs build
```

## Layout

```
docs/
  *.md                   pages (index, start, managed, faq, about)
  blog/                  blog plugin: index + posts/ (the "News" section)
  assets/                images — icons/ (feature symbols), blogs/, logo + favicon
  stylesheets/           tokens · components · site · extra
  javascripts/           scroll-color.js
  overrides/             Material template overrides (header, footer, main, nav)
mkdocs.yml               theme, nav, markdown_extensions, plugins
requirements.txt
.github/workflows/publish.yml   build (+ optimize) and sync ./site to S3 (bucket: openaleph.org)
```

## Authoring

Components are plain markdown + small wrapper classes (`.screen`, `.hero`,
`.grid.cards`, `.btn`, …). See the component table in [`CLAUDE.md`](CLAUDE.md#components)
and the existing pages (`docs/index.md`, `docs/start.md`) for copy-pasteable patterns.

## Design system

The shared, cross-DARC design layer is `darc-zensical.css`, loaded at build time
from [`zensical-theme-darc`](https://github.com/dataresearchcenter/zensical-theme-darc).
Keep project-specific styling out of it — use the local layers instead:

- `docs/stylesheets/tokens.css` — design tokens (colors, spacing, stroke, radii)
- `docs/stylesheets/components.css` — `.screen`, `.hero`, `.grid.cards`, `.btn`, `.section-icon`, profile cards
- `docs/stylesheets/site.css` — layout chrome (drawer, header + breadcrumb, footer, typography, list markers)
- `docs/stylesheets/extra.css` — last-mile overrides
