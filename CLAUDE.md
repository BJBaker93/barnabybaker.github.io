# CLAUDE.md — barnabybaker.au

This file provides context and conventions for AI assistants working on this repository.

## Project Overview

This is **Barnaby Baker's mixing engineer portfolio** hosted via **GitHub Pages** at `https://barnabybaker.au`. It is a single-page static site inspired by the [Xavier Dunn](https://xavierdunn.com.au/) Squarespace template — dark, minimal, full-viewport parallax sections.

## Repository Structure

```
barnabybaker.au/
├── index.html           # Single-page site (HTML + inline CSS + inline JS)
├── assets/images/       # TODO: Create this dir for hero, contact, logo, OG images
├── README.md            # Minimal repo description
└── CLAUDE.md            # This file
```

## Technology Stack

- **Pure HTML5, CSS3, vanilla JS** — no frameworks, no templating engines
- **Google Fonts** — Chivo (loaded via `<link>`)
- **GitHub Pages** — automatic deployment on push to `master`
- **No build step** — edit files and push; changes go live immediately
- **No package manager** — no npm, Gemfile, or other dependency files

## Site Architecture

`index.html` is a self-contained single page with three full-viewport sections:

| Section | ID | Description |
|---|---|---|
| Hero / Landing | `#landing` | Full-screen background image with parallax + scroll indicator |
| About | `#about` | Centered bio text on dark `#111` background |
| Get In Touch | `#contact` | Full-screen background image with overlay + CTA button |

### Key UI Components

- **Desktop header** (fixed top): nav links left-aligned, "BARNABY BAKER" branding centered
- **Index nav** (fixed right): vertical indicator lines that track the active section on scroll
- **Mobile bar** (< 640px): hamburger menu + centered logo, with full-screen overlay nav
- **Page loader**: black overlay that fades out on `window.load`
- **Parallax**: JS-driven `translate3d` on hero & contact background images
- **Fade-in**: `IntersectionObserver`-driven opacity/transform animation on `.fade-in` elements

### SEO

The `<head>` includes full SEO markup:
- `<title>` and `<meta name="description">`
- Open Graph tags (`og:title`, `og:description`, `og:image`, `og:url`)
- Twitter Card tags
- Schema.org JSON-LD (`@type: WebSite`)
- Canonical URL

All SEO values reference `https://barnabybaker.au` and `assets/images/og-image.jpg` (TODO).

## TODO Slots (placeholder content to replace)

Search `index.html` for `TODO` comments. Key items:

- **Hero image**: Replace Unsplash placeholder `src` with your own photo
- **Contact image**: Replace Unsplash placeholder `src` with your own photo
- **Logo**: Uncomment `<img>` tags and provide `/assets/images/logo-white.png`
- **Bio text**: Fill in location, genres, credits in the About section
- **Contact email**: Update `mailto:` href
- **OG image**: Provide `assets/images/og-image.jpg` (1200x630)
- **Favicon**: Provide `assets/images/favicon.ico` and uncomment the `<link>`
- **Alt text**: Replace `TODO:` alt attributes with real descriptions

## Development Workflow

### Branching

- `master` — production branch; pushes here deploy to GitHub Pages automatically
- `claude/<session-id>` — branches created by Claude AI during sessions

### Making Changes

1. Edit `index.html` directly (all CSS and JS are inline)
2. Commit with a descriptive message
3. Push to the appropriate branch

### Deployment

GitHub Pages deploys automatically from `master`. There is no CI/CD pipeline or staging environment.

## Conventions

### HTML / CSS / JS

- HTML5 doctype: `<!DOCTYPE html>`
- 2-space indentation throughout
- All CSS in a single `<style>` block in `<head>`
- All JS in a single `<script>` block before `</body>`
- CSS sections separated by comment banners (`/* === SECTION NAME === */`)
- Mobile breakpoint: `640px` (matching the original Xavier Dunn template)
- Colour palette: `#000` body, `#111` about section, white text with opacity variants

### File Organization

- `index.html` is the only page
- Place images in `assets/images/` (create as needed)
- If the site grows, extract CSS to `assets/css/style.css` and JS to `assets/js/main.js`

### Commits

- Write clear, descriptive commit messages
- One logical change per commit

## Key Facts for AI Assistants

- There is no test suite — validate changes by inspecting HTML structure
- There is no linter — follow existing code style
- Do not introduce build tooling unless explicitly requested
- Do not add external dependencies (npm, etc.) unless explicitly requested
- Do **not** add social media links — the owner specifically opted out
- The site owner is **Barnaby Baker**, a mixing engineer
- All placeholder content is marked with `<!-- TODO -->` comments
- The design is intentionally minimal — resist adding features that weren't requested
