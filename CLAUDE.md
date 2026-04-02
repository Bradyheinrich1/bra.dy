# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal website for Brady Heinrich (bradyheinrich.com). A static site with no build step, no framework, and no dependencies — vanilla HTML, CSS, and JavaScript.

## Development

No build or install step. Open `index.html` in a browser or serve with any static HTTP server:

```sh
python3 -m http.server 8000
```

## Deployment

Hosted on Render as a static site (configured in `render.yaml`). All routes rewrite to `/index.html`. Deploys automatically on push to main.

## Architecture

- **Pages**: `index.html` (homepage with profile and projects)
- **Styles**: Single stylesheet `css/styles.css` — mobile-first, uses CSS custom properties for theming. Fonts: Saira (body) and Roboto Slab (headings) from Google Fonts.
- **JavaScript**: `js/main.js` — minimal, only handles profile image fallback.

## Key Conventions

- All pages include `noindex, nofollow, noai` meta tags and a comprehensive `robots.txt` blocking all crawlers. Maintain this on new pages.
- Some content is intentionally commented out (stealth startup project card). Don't uncomment without being asked.
- Favicon is an SVG (`favicon.svg`). All pages link to it.
