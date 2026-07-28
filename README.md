# Soonhwan Kwon — Quarto academic website

This repository contains a ready-to-edit academic website built with Quarto and automatically deployed with GitHub Pages.

## Included pages

- Home
- Research
- Publications & working papers
- Teaching
- CV
- Public engagement & media

The draft content is tailored to a political scientist working on housing policy, policy feedback, inequality, and political behavior. Review every page before publishing, especially titles, project status, dates, and biographical details.

## 1. Install the required software

Install:

- Git
- Quarto
- RStudio, Positron, or VS Code (optional but convenient)

Confirm installation in a terminal:

```bash
quarto --version
git --version
```

## 2. Preview locally

Open a terminal in this folder and run:

```bash
quarto preview
```

A browser window should open. Press `Ctrl+C` in the terminal to stop the preview server.

## 3. Create the GitHub repository

For the clean address `https://YOUR_USERNAME.github.io`, create a public GitHub repository named exactly:

```text
YOUR_USERNAME.github.io
```

For example, if your GitHub username is `soonhwankwon`, the repository must be named `soonhwankwon.github.io`.

## 4. Push this project to GitHub

Run these commands inside the project folder. Replace the remote URL with your own repository URL.

```bash
git init
git add .
git commit -m "Create academic website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

GitHub Desktop can be used instead of terminal Git.

## 5. Turn on GitHub Pages

In the repository on GitHub:

1. Open **Settings**.
2. Select **Pages** under **Code and automation**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Open the **Actions** tab and check that “Publish Quarto website” finishes successfully.

The workflow automatically runs `quarto render` and publishes `_site` whenever a change is pushed to `main`.

## 6. Add the real CV

Copy the current CV PDF to:

```text
assets/files/Soonhwan_Kwon_CV.pdf
```

Then open `cv.qmd` and uncomment the download-button line.

## 7. Replace the monogram with a photograph

Copy a square or portrait photograph into `assets/img/`, for example:

```text
assets/img/soonhwan.jpg
```

Then replace this line in `index.qmd`:

```markdown
![](assets/img/soonhwan-monogram.svg)
```

with:

```markdown
![](assets/img/soonhwan.jpg)
```

## 8. Add a custom domain

After buying a domain:

1. Rename `CNAME.example` to `CNAME`.
2. Replace its contents with the domain, such as `soonhwankwon.com`.
3. Configure the same custom domain in **GitHub repository → Settings → Pages**.
4. Configure the required DNS records with the domain registrar.
5. Enable **Enforce HTTPS** after GitHub issues the certificate.

Do not publish `CNAME.example` as an active `CNAME` until the domain has been purchased and configured.

## Routine updates

Edit `.qmd` files, preview locally, and then run:

```bash
git add .
git commit -m "Update research website"
git push
```

The site will rebuild automatically.

## Main customization files

- `_quarto.yml`: navigation, themes, footer, and site-wide settings
- `index.qmd`: homepage
- `research.qmd`: dissertation chapters and projects
- `publications.qmd`: working papers and publications
- `teaching.qmd`: teaching information
- `cv.qmd`: web CV and PDF link
- `media.qmd`: public scholarship
- `styles.css`: visual design
- `.github/workflows/publish.yml`: automatic deployment
