# BUILD PROMPT SEQUENCE — INFRATWIN

Use these in sequence. Do not begin with one giant "build me a page" prompt,
and do not skip the confirmation gates — they're deliberate, not optional
"if you want" checkpoints.

---

## STEP 1 — READ & OUTLINE (no code)

Read:
- `private-inputs/InfraTwin.pptx` — the authoritative source for structure
- `private-inputs/Infrastructure Copilot.pptx` — supplementary detail only,
  do not let its structure override the deck above
- `private-inputs/Web design.docx` — working notes + reference images
- `DESIGN.md`

**Do not write code yet.**

Give a concise summary containing:
1. The narrative arc of `InfraTwin.pptx` as it actually reads (problem,
   solution, product, team, market, traction, ask — whatever structure the
   deck itself uses, not a forced template).
2. A proposed page section outline mapped to that arc.
3. Anything from `Infrastructure Copilot.pptx` worth pulling in to flesh
   out a section the newer deck states briefly — named specifically, not
   a wholesale merge.
4. Any typical pitch element that's missing or thin (the ask, team, market
   sizing, contact) — flagged, not filled in.
5. Any conflicts between the two decks.
6. Which extracted images (`assets/extracted/`) look usable for which
   section, and which slides need a fresh crop/export instead.

Do not invent facts, numbers, or claims not present in the decks.

**Wait for explicit approval before implementation.**

---

## STEP 2 — VISUAL DIRECTION (no code)

Propose one primary design language from `skeletons/`, informed by:
- the symposium's own context (architecture/robotics/AI in the built
  environment);
- any visual intent in `Web design.docx`;
- explicitly **distinct** from the personal-portfolio project's own
  Technical/Research treatment — even if the same skeleton category ends
  up fitting, the typography/colour/layout specifics should differ, not
  repeat it.

Cover: typography, colour (max 1 accent), grid/composition, how the video
embed and pitch imagery are treated, one distinctive move.

**Wait for approval before implementation.**

---

## STEP 3 — BUILD (incrementally)

Proceed with the approved outline and direction. Build **section by
section**, not all at once — check in as each section lands rather than
delivering the whole page in one pass.

Create: `index.html`, `style.css`, `script.js` only if needed, images in
`assets/` (never reference `assets/extracted/` — copy/process what's
needed into `assets/` proper first).

Requirements:
1. Follow the approved `DESIGN.md` outline and visual direction closely.
2. Semantic HTML, readable CSS, minimal JS, no framework.
3. Do not invent achievements, metrics, team members, or claims not in
   the source decks. Missing content stays a clearly labelled placeholder.
4. Video section embeds the YouTube URL (ask if not yet provided) —
   never references the local `.mp4`.
5. Static, GitHub-Pages-ready, mobile-checked.

After each section, briefly note what controls structure/layout/type/
colour, same as the original portfolio project's convention.

---

## STEP 4 — CRITIQUE & REVISE

Check against `DESIGN.md`, the chosen skeleton, and `AI_SLOP_CHECKLIST.md`.
Identify: generic/templated elements, what's working, hierarchy/spacing
issues, constraint violations, one distinctiveness opportunity. Revise in
place — don't rebuild from scratch.

---

## STEP 5 — UNDERSTAND & EDIT

Explain the page as a beginner would need: main sections, layout CSS,
typography CSS, spacing/colour CSS, the easiest safe place to make one
manual edit. Don't change files in this step.

---

## OPTIONAL — MOBILE QA

Typography scaling, image overflow, video-embed responsiveness, spacing,
no horizontal scroll, tap targets, reading order.

---

## BEFORE PUBLISHING

Run `AI_SLOP_CHECKLIST.md`, then `GITHUB_PAGES_GUIDE.md`. Confirm with the
project owner before any `git push` — the repo being public already
doesn't mean every future change is pre-approved for deploy.
