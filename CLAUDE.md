# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-based static website for Clarity d.o.o. (clarity.hr), deployed via GitHub Pages. The site serves as:
- A personal/company landing page for Ivan Klaric's software engineering consultancy
- Marketing pages for products like Clarity Notes (a note-taking application)
- Concept validation pages like "Email to Self, But Better"

## Architecture

**Static Site Generator**: Jekyll with the `pages-themes/slate` remote theme

**Key Content Pages**:
- `index.md` - Main landing page
- `emailtoself.md` - Product concept validation page with embedded Google Form
- `legal.md` - Legal information for Clarity d.o.o.
- `notes/index.md` - Product page for Clarity Notes with embedded roadmap iframe

**Configuration**:
- `_config.yml` - Jekyll configuration with remote theme and plugins

**Deployment**:
- Automated via GitHub Actions (`.github/workflows/jekyll-gh-pages.yml`)
- Triggers on pushes to `main` branch
- Builds Jekyll site and deploys to GitHub Pages

## Development Commands

Since this is a Jekyll site hosted on GitHub Pages, development typically involves:

**Local preview** (requires Jekyll installed):
```bash
bundle exec jekyll serve
# Site will be available at http://localhost:4000
```

**Deploy**:
```bash
git push origin main
# GitHub Actions workflow automatically builds and deploys
```

## Content Structure

All content pages use Jekyll front matter with `title` and optional `description` fields. The site uses Markdown with some embedded HTML for special elements (iframes, images with alignment).

## Important Notes

- External content is embedded via iframes (Google Forms, Clarity Notes public pages)
- CNAME file indicates custom domain configuration
- No build/test commands needed locally - GitHub Actions handles deployment
