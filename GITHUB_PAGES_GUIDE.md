# GITHUB PAGES — QUICK GUIDE (INFRATWIN)

## Repository
Already created: `https://github.com/rais4be-nus/InfraTwin` (public).

Unlike a personal `username.github.io` repo, this is a **project site** —
it publishes under a sub-path, not at the account's root domain.

## Minimal published site structure

```text
/
├── index.html
├── style.css
├── script.js        # optional
└── assets/
```

## Publish
1. Commit and push to `main` on `origin` (`rais4be-nus/InfraTwin`).
2. Open the repo on GitHub → **Settings**.
3. Open **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`.
6. Save.
7. Visit:

`https://rais4be-nus.github.io/InfraTwin/`

Publishing may take a few minutes. Note the trailing repo name in the
URL — it's not `rais4be-nus.github.io` alone.

## Common problems

### 404
Check: repo spelling, `index.html` exists at repo root, Pages is
deploying the correct branch.

### CSS/JS not loading, or working locally but not when published
Use **relative** paths, e.g. `<link rel="stylesheet" href="style.css">`
— never a leading `/style.css`, which would resolve to the domain root
(`rais4be-nus.github.io/style.css`) rather than the project sub-path
(`rais4be-nus.github.io/InfraTwin/style.css`). This is the most common
break when moving from a user-site to a project-site repo.

### Images not loading
Repository-relative paths: `<img src="assets/diagram.jpg">`. File names
are case-sensitive once published, even if your local filesystem isn't.

### Video
The 1-minute demo video is hosted on YouTube, not in this repo — embed it
by URL (`<iframe>`), don't try to serve it as a local file.

## Before every push
- Confirm with the project owner first — the repo being public doesn't
  mean every change is pre-approved to deploy.
- Run `AI_SLOP_CHECKLIST.md`.
- Check nothing in `private-inputs/` or `assets/extracted/` got staged —
  both should stay gitignored.
