# Captain's Avengers Team Site

A small, dependency-free static site intended for GitHub Pages.

## Run locally

No Node.js or build tooling is required.

### Option 1: open directly

Open `index.html` in a browser.

### Option 2: local web server

If Python is installed:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Publish with GitHub Pages

1. Create a **public** GitHub repository.
2. Copy these files into the repository.
3. Push to `main`.
4. In GitHub, open **Settings → Pages**.
5. Under **Build and deployment**, choose **GitHub Actions**.
6. The included workflow will deploy the site.
7. Open the Pages URL shown by GitHub.

The site intentionally uses plain HTML/CSS so the first experiment has almost no tooling overhead. You can migrate to React, Astro, Docusaurus, or another static-site generator later if the documentation grows.
