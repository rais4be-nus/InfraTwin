# INFRATWIN — STARTUP PITCH PAGE
## Build guide

This kit mirrors the structure used to build a previous personal-portfolio
project, adapted for a single-narrative startup pitch page instead. It is
a workflow scaffold, not a template — there is no starter `index.html` or
`style.css` yet.

### What this project is
A dedicated page for **InfraTwin**'s pitch, built for the Startup
Architecture Symposium (ETH Zurich) Startup Pitch track. Audience:
symposium committee, architects, founders, investors, engineers,
roboticists — not general portfolio visitors. Tone: an evaluated pitch,
not a project showcase. Full context: `prompt for new project.md`.

### Files in this kit
```text
prompt for new project.md   — the original brief (read first)
DESIGN.md                   — project brief to fill in from the deck
CODEX_PROMPTS.md            — the build sequence, use in order
AI_SLOP_CHECKLIST.md        — anti-generic-AI-site checklist, before publish
GITHUB_PAGES_GUIDE.md       — how this repo publishes
skeletons/                  — four design-language directions to choose from
references/                 — starting points for visual references
private-inputs/             — the source decks/video (gitignored, local only)
assets/                     — published images; assets/extracted/ is raw/staging
```

### Flow
1. Read `prompt for new project.md` and `private-inputs/README.md`.
2. Open `DESIGN.md` — most of the source/logistics fields are already
   filled in from prior discussion; the content/narrative fields are not.
3. Use `CODEX_PROMPTS.md` Step 1 to read the decks and propose a content
   outline. **Wait for explicit approval before writing any code** — this
   is a hard requirement from the original brief, not just a suggestion.
4. Choose one skeleton (`skeletons/`) as the primary design language,
   distinct from the personal-portfolio site's own aesthetic.
5. Build incrementally, section by section (`CODEX_PROMPTS.md` Step 2+).
6. Run `AI_SLOP_CHECKLIST.md` before publishing.
7. Publish per `GITHUB_PAGES_GUIDE.md`.

### Known constraints already settled (don't re-litigate these)
- Video is hosted on YouTube and embedded by URL — never commit the raw
  `.mp4` (it exceeds GitHub's 100MB file limit anyway).
- `InfraTwin.pptx` is the authoritative structure; `Infrastructure
  Copilot.pptx` is a supplementary, richer-detail source — see
  `private-inputs/README.md`.
- Repo is `https://github.com/rais4be-nus/InfraTwin`, public, and the
  supervisor has confirmed the source content is cleared for public
  release. Licensing is still All Rights Reserved (`LICENSE`) — public
  visibility and reuse rights are different things.
- More content will be provided before the build proceeds far — check
  with the project owner if a section looks thin rather than filling
  gaps with invented content.
