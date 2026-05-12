[README.md](https://github.com/user-attachments/files/27645608/README.md)
# Elastic Blogs Consolidation Prototype

A working prototype exploring the unification of four Elastic web properties — Search Labs, Observability Labs, Security Labs, and the corporate Blog — under a single design system, navigation pattern, and component library.

## What this is

A single-file HTML/CSS/JS prototype demonstrating proposed page templates, navigation structure, and interaction patterns across all four properties. It is intended as a visual and structural specification for design and engineering, not as production code.

The prototype covers 18 distinct views including lab homes, article detail pages, series articles (tutorials), tag/filter pages, author pages, and the corporate blog category pages, with a working hash-router that switches between them.

## View it

- **Live**: deploy via GitHub Pages (see below), or open `index.html` directly in any modern browser.
- **Locally**: clone the repo and open `index.html` — no build step, no dependencies, no server required.

## Deploy with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Source: **Deploy from a branch**, Branch: `main`, Folder: `/ (root)`.
4. Save. The site is live at `https://YOUR_USERNAME.github.io/REPO_NAME/` within a minute.

## Repo contents

- `index.html` — the prototype itself, fully self-contained (~5,700 lines, no external dependencies)
- `HANDOFF.md` — technical handoff documentation: file architecture, component patterns, design tokens, common edit recipes, and conventions to preserve when iterating

## Stack and approach

- Pure HTML, CSS, and vanilla JavaScript inside a single file
- Hash-based routing (no history API, no server)
- CSS custom properties for all design tokens
- No frameworks, no build tools

This intentional simplicity is a feature: the prototype is portable, easy to host, easy to fork, and trivial to translate into any production framework (React, Vue, Astro, etc.) by lifting the component CSS and treating the JS router as a conceptual spec.

## Design source

The prototype implements components from the Elastic design system in Figma:

- **Components library** — global navigation, tags/chips, button system (primary, secondary, tertiary)
- **Site reference** — Search Labs page layouts adapted as the foundation, extended to Observability Labs, Security Labs, and corporate Blog patterns

## How to iterate

The prototype is designed for continued editing in a Claude conversation. To resume work:

1. Upload `index.html` and `HANDOFF.md` to a new Claude chat.
2. Reference `HANDOFF.md` first — it documents every architectural decision, where to find components in the file, and common edit recipes.
3. Make changes, download the updated `index.html`, and `git commit` the new version.

Each iteration keeps the public Pages URL unchanged, so reviewers always see the latest version on refresh.

## Status

This is an in-progress prototype. Several known issues are tracked in `HANDOFF.md` under "Open follow-ups," including subnav information architecture for individual labs (which requires editorial alignment before being finalized).

## Notes

This prototype is a working draft for internal design and engineering review. Visual placeholders (gray blocks where article images would appear) are intentional — image treatments and final imagery are out of scope for the structural prototype.
