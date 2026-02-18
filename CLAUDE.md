# CLAUDE.md — barnabybaker.github.io

This file provides context and conventions for AI assistants working on this repository.

## Project Overview

This is a personal website hosted via **GitHub Pages** at `https://barnabybaker.github.io`. It is a static HTML site with no build tooling, frameworks, or dependencies.

## Repository Structure

```
barnabybaker.github.io/
├── index.html      # Main (and currently only) page
├── README.md       # Minimal repo description
└── CLAUDE.md       # This file
```

## Technology Stack

- **Pure HTML5** — no frameworks, no templating engines
- **GitHub Pages** — automatic deployment on push to `master`
- **No build step** — edit files and push; changes go live immediately
- **No package manager** — no npm, Gemfile, or other dependency files

## Development Workflow

### Branching

- `master` — production branch; pushes here deploy to GitHub Pages automatically
- `claude/<session-id>` — branches created by Claude AI during sessions

### Making Changes

1. Edit HTML/CSS/JS files directly (no build step required)
2. Commit with a descriptive message
3. Push to the appropriate branch

### Deployment

GitHub Pages deploys automatically from `master`. There is no CI/CD pipeline or staging environment.

## Conventions

### HTML

- Use HTML5 doctype: `<!DOCTYPE html>`
- 2-space indentation
- Keep markup semantic where possible
- Include a `<meta name="viewport">` tag for responsive design when adding CSS

### File Organization

- `index.html` is the site entry point
- Place images in an `assets/images/` directory (create as needed)
- Place CSS in `assets/css/` or inline in `<style>` tags for single-page sites
- Place JavaScript in `assets/js/` or at the bottom of `<body>`

### Commits

- Write clear, descriptive commit messages
- One logical change per commit

## Key Facts for AI Assistants

- There is no test suite — validate changes by inspecting HTML structure
- There is no linter — follow existing code style
- Do not introduce build tooling unless explicitly requested
- Do not add external dependencies (npm packages, etc.) unless explicitly requested
- The site owner is **Barnaby Baker**
- All content changes (text, images, links) should be placeholders or clearly marked `<!-- TODO -->` when real content is not yet available
