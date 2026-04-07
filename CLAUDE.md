# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Marketing site for **aquarco** — AI agents that work autonomously inside sandboxed VM environments. Deployed via GitHub Pages (Jekyll) from the `main` branch.

## Development

Jekyll site processed by GitHub Pages automatically on push. For local preview:

```sh
bundle exec jekyll serve
```

Requires a `Gemfile` with `gem "github-pages"`. Without it, open any `.html` file in `_site/` after running `jekyll build`, or use `python3 -m http.server` on the built output.

## Architecture

Jekyll splits the former monolithic `index.html` into:

- **`_layouts/default.html`** — Visual chrome: all CSS, hero section (aquarium SVG with animated fish/bubbles), terminal demo, footer, and vanilla JS animations. Injects page content via `{{ content }}`.
- **`README.md`** — Homepage content (front matter sets `layout: default`, `permalink: /`). Edit this to update the "How It Works" pipeline and taglines sections.
- **`_config.yml`** — Jekyll site config (title, url, kramdown/GFM markdown).

Adding a new page: create a `.md` file with `layout: default` in the front matter. It will automatically use the same visual chrome.

## Design Constraints

The visual metaphor (aquarium / sealed glass world) is central to the brand — copy, colors, and imagery should reinforce isolation and containment.

CSS custom properties (in `_layouts/default.html`): `--bg: #060d18`, `--teal: #0d9e75` (accent), `--text: #d4e8f7`. Two Google Fonts: **Libre Baskerville** (headings/body) and **JetBrains Mono** (terminal/code/labels).

Markdown content in `main.section` is styled to match the design: `ol` renders as numbered pipeline steps, `blockquote` renders as a teal-accented callout block, `ul` renders as a card grid.
