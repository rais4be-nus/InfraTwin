# Assets

Only put files here that are meant to be published on the live page.

Already present (ready to use, or to reprocess):
- `Application area.png`, `Picture1.png`, `Picture2.png`, `Picture3.png` —
  supporting images already exported at usable resolution.

`extracted/` (gitignored, not published) holds every image pulled directly
out of `private-inputs/InfraTwin.pptx`, `private-inputs/Infrastructure
Copilot.pptx`, and `private-inputs/Web design.docx` — 63 raw files, named
`<source>-image##.<ext>` / `<source>-media##.<ext>` by source deck. Browse
this folder to see everything available, then copy/rename/resize the ones
you actually want directly into `assets/` (mirroring the naming pattern
used on the personal-portfolio project: descriptive kebab-case names, e.g.
`assets/hero-problem-diagram.jpg`). Don't reference `assets/extracted/`
paths from `index.html` — it won't exist once pushed.
