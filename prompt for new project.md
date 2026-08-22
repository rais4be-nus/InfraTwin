# Project: Startup Pitch Page — ETH Zurich Startup Architecture Symposium

## Context

This is a new, standalone web project — separate from my existing personal
portfolio project. It is a dedicated single-narrative page for a startup
company pitch, built for submission/reference in connection with the
**Startup Architecture Symposium** at ETH Zurich
(https://startups.arch.ethz.ch/), which runs a "Startup Pitch" track
(application portal: https://ita.arch.ethz.ch/events/Startup-Application-Portal.html).

The audience is the symposium committee and attendees (architects, founders,
investors, engineers, roboticists) — not general portfolio visitors. Tone and
structure should read as an evaluated pitch, not a personal project showcase.

## Primary content source

I will upload a `.pptx` slide deck — this is the **primary and authoritative
source of content** for the site (problem, solution, product, team, market,
traction, ask, etc., however the deck is structured). Before writing any code:

1. Read and extract all text, structure, and any embedded images/diagrams
   from the deck.
2. Summarize the deck's narrative arc back to me in plain text and propose a
   page section outline mapped to it, before building anything.
3. Do not invent content, numbers, or claims not present in the deck. If a
   section of a typical pitch (e.g. "the ask," team bios, contact info) is
   missing or thin in the deck, flag it explicitly and ask me rather than
   filling it in.

## Environment setup

- Set up a **new, separate project directory** — do not modify or reuse the
  existing portfolio project's repo or files. Copy over only the reusable
  front-end scaffolding (build tooling, base styles, layout system,
  responsive breakpoints) as a starting point if it saves time, not the
  portfolio's content, navigation, or multi-page structure.
- Keep it a **static site** (plain HTML/CSS/JS, or a static-site generator
  with no server-side runtime dependency) so it can be published directly
  via GitHub Pages with no build server required, or with a simple static
  build step I can run locally before pushing.
- Single-page (or very short multi-section, single-scroll) layout by
  default, matching a pitch narrative rather than portfolio-style multi-page
  navigation — confirm with me if the deck's content seems to warrant more
  than one page.
- Set up local preview (e.g. a simple dev server or `npx serve`) so I can
  review before publishing.

## Workflow expectations

1. Confirm the extracted content outline with me first.
2. Propose a visual direction (informed by the symposium's own visual
   language if relevant — architecture/robotics/AI in the built environment
   — but distinct from my personal portfolio's aesthetic) before full build.
3. Build incrementally section by section, not all at once.
4. Prepare the project for GitHub Pages deployment (correct relative paths,
   a `README.md` explaining the repo, and a note on whether this repo should
   be public or private given it's a company pitch — flag if any content
   from the deck looks sensitive/confidential before I push it to a public
   repo).
5. Do not deploy or push anything without my explicit confirmation.

## Out of scope for now

- No backend, database, forms, or payment integration.
- No reuse of portfolio page content or navigation structure.
- No publishing/deployment actions — I will handle git push and any GitHub
  Pages / DNS configuration myself once the local build is approved.
