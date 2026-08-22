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

### Content outline (fill in after reading the decks)
1.
2.
3.

### What's present but should probably be left out

### What's a typical pitch element but missing/thin here (flag, don't invent)

---

## 3. Audience & tone

Audience: symposium committee, architects, founders, investors, engineers,
roboticists.
Tone: evaluated pitch, not project showcase — precise, credible, confident
without hype.

---

## 4. Primary design language

- [ ] Editorial
- [ ] Architecture / Minimal
- [ ] Technical / Research
- [ ] Experimental

To be chosen after reading the deck's own visual material (`Web design.docx`,
extracted images) — must read as informed by architecture/robotics/AI in
the built environment, and **distinct from the personal-portfolio site's
own aesthetic** (that one landed on Technical/Research — this project
should not just repeat it wholesale, even if the same skeleton ends up
fitting; the specific typographic/colour/layout choices should differ).

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
