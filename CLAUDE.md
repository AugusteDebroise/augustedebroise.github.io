# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
bundle install                 # Install Ruby gem dependencies
bundle exec jekyll serve       # Start dev server at http://localhost:4000
bundle exec jekyll build       # Build site to _site/
```

The site auto-regenerates on file changes during `jekyll serve`. There is no test suite or linter.

## Architecture

This is a Jekyll-based academic personal website deployed via GitHub Pages on the `gh-pages` branch.

### Content is data-driven via YAML files:
- `_data/settings.yml` — navigation menu, social links, contact info
- `_data/research.yml` — publications, working papers, works in progress
- `_data/cv/education.yml` — education history
- `_data/cv/academic-experience.yml` — academic positions

Most content changes go in these YAML files, not in Markdown pages. The Markdown pages (`index.md`, `research.md`, `cv.md`, etc.) mostly just specify a `layout:` in their frontmatter and rely on the corresponding layout to render the data.

### Layouts and includes:
- `_layouts/` — 9 page templates (home, cv, publications, courses, contact, people, page, post, default)
- `_includes/` — reusable components (head, header, footer, research, contact)
- `_sass/main.scss` + `assets/css/main.scss` — SCSS compiled by Jekyll; `assets/css/style.css` for extra custom CSS

### Static assets:
- `assets/libs/` — vendored Bootstrap and Font Awesome (do not edit)
- `assets/img/` — profile photos and research diagrams
- `assets/cv/` — CV PDF files

### Courses and people:
- `courses/` — individual course pages as Markdown files
- `people/` — team member pages (currently disabled via `_config.yml`)