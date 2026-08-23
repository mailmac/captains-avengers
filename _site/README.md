# Captain's Avengers — Jekyll Starter

This is a Jekyll-based engineering team documentation site for GitHub Pages.

## Local setup

Install Ruby, then from the repository root:

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000.

## GitHub Pages

1. Create a public GitHub repository named `captains-avengers`.
2. Push this project to `main`.
3. Open **Settings → Pages**.
4. Under **Build and deployment → Source**, select **GitHub Actions**.
5. The included `.github/workflows/pages.yml` builds Jekyll and deploys `_site`.
6. Open the Pages URL shown by GitHub.

## Jekyll concepts

Markdown content → front matter → Jekyll → layouts/includes → generated HTML → `_site/` → GitHub Pages.

A page can start with:

```yaml
---
layout: page
title: Database troubleshooting
permalink: /database-troubleshooting/
---
```

Then write the page as Markdown.
