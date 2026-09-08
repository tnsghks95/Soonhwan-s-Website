# Soonhwan Kwon — Quarto academic website

This repository contains Soonhwan Kwon's academic website, built with Quarto and automatically deployed with GitHub Pages.

## Included pages

- Home
- Research
- Publications & working papers
- Teaching
- CV

## Preview locally

Open a terminal in this folder and run:

```bash
quarto preview
```

A browser window should open. Press `Ctrl+C` in the terminal to stop the preview server.

## Deployment

The site is configured to deploy automatically through GitHub Actions when changes are pushed to `main`.

## Main customization files

- `_quarto.yml`: navigation, themes, footer, and site-wide settings
- `index.qmd`: homepage
- `research.qmd`: dissertation chapters and related projects
- `publications.qmd`: working papers and publications
- `teaching.qmd`: teaching philosophy, interests, and experience
- `cv.qmd`: web CV
- `styles.css`: visual design
- `.github/workflows/publish.yml`: automatic deployment

## Routine updates

Edit the relevant `.qmd` files, preview locally, and then commit and push changes. GitHub Actions will rebuild the site automatically.
