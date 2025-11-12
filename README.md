# LumenPath HMS — GitHub Pages (Jekyll)


This repository hosts a multi‑page site for the LumenPath Hospital Management System: Overview, Partner Proposal, and Implementation Playbook.


## How to publish
1. Ensure these files are in the repo root and committed to `main`.
2. In **Settings → Pages**, set **Build and deployment** to "Deploy from a branch"; Branch: `main`; Folder: `/ (root)`.
3. Your site will be available at https://shazej.github.io with pages:
- `/` (Home)
- `/proposal/`
- `/playbook/`
- `/contact/`


## Local preview (optional)
Jekyll is not required to preview basic Markdown, but for an exact build:
```bash
# requires Ruby + Bundler + jekyll (optional)
bundle add jekyll && bundle exec jekyll serve