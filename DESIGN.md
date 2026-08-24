# DESIGN.md
## InfraTwin — Pitch Page Brief

Logistics/source fields below are already settled from prior discussion.
Content/narrative fields are intentionally left blank — fill them in via
`CODEX_PROMPTS.md` Step 1 (read the decks, propose an outline, get
approval) rather than guessing ahead of that step.

---

## 1. Site purpose

Single-narrative startup pitch page for InfraTwin, submitted for/referenced
in the Startup Architecture Symposium (ETH Zurich) Startup Pitch track.
Not a portfolio, not a company marketing site — a pitch, read the way a
symposium committee would evaluate one.

---

## 2. Content sources

Primary (authoritative structure): `private-inputs/InfraTwin.pptx` (10 slides)
Supplementary (richer detail, older structure): `private-inputs/Infrastructure Copilot.pptx` (11 slides)
Working notes: `private-inputs/Web design.docx`
Demo video: `private-inputs/1 minute video.mp4` → to be hosted on YouTube, embedded by URL (get the URL from the project owner before building that section)

Extracted images from all of the above are staged, unprocessed, in
`assets/extracted/` (63 files) — browse there rather than re-opening the
decks for images.

**Do not invent content, numbers, or claims not present in the decks.** If
a typical pitch section (the ask, team bios, contact info, traction) is
missing or thin, flag it and ask rather than filling it in. More content
will be provided by the project owner before the build proceeds far.

### Content outline (approved)
1. Hero — title, tagline, one-line positioning
2. Problem — current workflow bottlenecks (InfraTwin.pptx slide 3 +
   Infrastructure Copilot.pptx slide 2 problem framing)
3. Solution — Infra.SENSE → Infra.SEG → Infra.DT loop (slide 4)
4. Infra.SENSE — capture innovation + PoC numbers (slides 5–6)
5. Infra.SEG + Infra.DT — understand & deliver innovation + PoC (slides 7–8–10)
6. Video — YouTube embed (https://youtu.be/-iOz_pBza9o)
7. Team / backed by — Vincent Gan (PI, RAIS4BE Lab, NUS) + Jingxuan Li,
   real CV-sourced credentials (grants incl. LTA/NRF, ISARC 2026 co-chair,
   publications), real conference photos
8. Footer — lab/contact

Additional real source material provided by project owner beyond the two
decks (all in `private-inputs/`, gitignored):
- `profile.jpg` — Jingxuan Li headshot
- `ISARC/` — conference photos of Jingxuan Li and Vincent Gan at
  ISARC 2026/IGLC34 (Vincent Gan: Co-chair, Local Organising Committee) and
  EEHB 2024
- `NUS3D/` — real robot hardware photos (clean product shots) + NUS3D
  dataset segmentation figures
- `Portfolio-JingxuanLi-NUS_compressed 300ppi.pdf` — BArch studio
  portfolio (Chongqing University, 2019–2022); pages 7–8 excluded per
  project owner's instruction. Architecture-to-robotics trajectory used
  as founder-background credential only — studio project content itself
  (Arctic Data Center, etc.) is out of scope for this pitch.
- Vincent Gan's CV (fetched from `cde.nus.edu.sg`) and rais4be.com — real,
  citable grants, awards and publications; resolves the earlier LTA-logo
  clearance flag from Step 1 (LTA is a confirmed real funding partner via
  "AI-assisted scan-to-BIM technology..." grant, National Research
  Foundation / AI Singapore Programme / Land Transport Innovation Fund,
  9.2023–2.2025)

### What's present but should probably be left out
- The competitor/reference robot collage (`infratwin-image4.png` /
  dji-aerial.com, eenewseurope.com, droneblocks.io citations) — not
  InfraTwin's own hardware.
- Tiong Seng Group logo (LTA is now confirmed via Vincent Gan's public CV;
  Tiong Seng's relationship is still unconfirmed — leave out unless
  clarified).
- InfraTwin.pptx slide 2 ("Introduction/Research Focus/Ongoing
  R&D/Future Work") and slide 9 (duplicate of slide 8) — no clear content,
  not used.

### What's a typical pitch element but missing/thin here (flag, don't invent)
- The ask — still absent from all source material. No section built for
  this; add only if the project owner provides it.
- Market sizing (TAM/SAM/SOM) — still absent, only customer-type
  categories exist.
- The "~S$X0,000 savings" figure remains an unresolved placeholder in the
  source deck — not used anywhere on the page.

---

## 3. Audience & tone

Audience: symposium committee, architects, founders, investors, engineers,
roboticists.
Tone: evaluated pitch, not project showcase — precise, credible, confident
without hype.

---

## 4. Primary design language

- [ ] Editorial
- [x] Architecture / Minimal
- [ ] Technical / Research
- [ ] Experimental

Chosen after browsing 9 project-owner-supplied reference sites (uuen.cloud,
auar.io, zacuaventures.com, vyzn.tech, woho.us, vaulted.swiss, foldcast.com,
airshade.eu, layered.ch) — see `references/REFERENCE_LIBRARY.md` for the
sourced hex/font/layout extraction and synthesis. Warmed with a confident
single accent colour and real product photography rather than the plain
skeleton's austerity. Naturally distinct from the personal-portfolio site's
Technical/Research language (no monospace, no metadata rails — none of the
references use that vocabulary either).

**Typography:** Inter (grotesk sans), one weight range, no serif/mono.
**Colour:** light background (white / near-white), near-black text, one
accent — **signal blue** (`#1470B0`-family), confirmed by project owner
despite a noted visual proximity to the personal-portfolio site's own blue
accent (project owner's explicit call). Built as CSS custom-property
tokens so the exact hue can still be refined once real content is in
place, and to support the day/night toggle below.
**Motion:** scroll-triggered opacity/translate fade only (uuen.cloud's
`IntersectionObserver` mechanism), gated behind `prefers-reduced-motion`.
No parallax.
**Distinctive move:** a raw-scan → segmented → BIM comparison echoing
uuen.cloud's before/after slider, mapped onto InfraTwin's own
Infra.SENSE → Infra.SEG → Infra.DT arc.

---

## 5. Structure

Single-page, single-scroll by default, matching a pitch narrative — not
portfolio-style multi-page navigation. Confirm with the project owner if
the deck's content genuinely seems to warrant more than one page/section
group before building multi-page navigation.

---

## 6. Global constraints

- static site: plain HTML/CSS + minimal JS, no framework, no server-side
  runtime dependency, publishable directly via GitHub Pages;
- responsive; semantic HTML; readable CSS; minimal JS;
- no more than 2 typefaces; no more than 1 accent colour;
- day/night (light/dark) theme toggle, added per project owner request —
  light is the default ("day mode", per reference-library principle 1),
  dark is an additional toggle-able mode, not the default;
- local preview available before every review (simple dev server);
- build incrementally, section by section — not all at once;
- **do not deploy or push anything without the project owner's explicit
  confirmation**, even though the repo is already set to public.

---

## 7. Avoid by default
(same anti-slop list as `AI_SLOP_CHECKLIST.md` — see that file before
publishing)

---

## 8. Publishing

Repo: `https://github.com/rais4be-nus/InfraTwin` (already created, public)
Publishes to: `https://rais4be-nus.github.io/InfraTwin/`
License: All Rights Reserved (`LICENSE`) — placeholder copyright holder,
confirm the exact entity/named founders before treating it as final.
Content clearance: project owner has confirmed the source material (from
their supervisor) is cleared for public release — this does not by itself
cover the demo video (external host, separate consideration) or anything
added later that wasn't in the original decks.
