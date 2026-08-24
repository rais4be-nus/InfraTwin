# REFERENCE LIBRARY — INFRATWIN

Superseded the generic discovery-tips version of this file. These are the
project owner's actual chosen references, browsed and extracted directly
(real HTML/CSS pulled where the site allowed it — hex codes and font names
below are exact and sourced, not guessed, except where marked "descriptive
only"). Ranked in the order the project owner gave them.

## Design principles (project owner, stated directly)

1. **Light background, bright accent color.** `uuen.cloud` is the reference
   example for this.
2. **Concise and readable — not crowded.** `zacuaventures.com`,
   `vyzn.tech`, `woho.us` are good examples.
3. **Smooth, subtle scroll animation — not bold or laggy.** `auar.io`,
   `uuen.cloud`, `vyzn.tech` are good examples. `gravisrobotics.com` and
   `airshade.eu` are named *bad* examples — motion heavy enough to cause
   visible lag.
4. **Mobile layout matters, phone ratio only** (no tablet-specific pass
   needed). `uuen.cloud`, `zacuaventures.com`, `vyzn.tech`, `auar.io` are
   good examples.

These four principles govern every decision below — when a reference
conflicts with one of them, the principle wins, not the reference.

---

## 1. uuen.cloud — top preference

**What it is:** Cloud UBEM (urban building energy modelling) SaaS spun out
of ETH Zurich's City Energy Analyst research team — an academic
research-to-product story, structurally the closest analog to InfraTwin of
any reference here (research lab → commercial tool, same framing).

**Confirmed from source (Astro static site, design tokens in `Base.css`):**
- Background: white (`#FFFFFF`) primary, near-white grey (`#F7F7F7`) for
  subtle section breaks. No dark sections.
- Text: black (`#000000`) primary, mid-grey (`rgb(127,128,134)`) secondary,
  lighter grey (`rgb(162,161,166)`) muted/caption text.
- Accent: **two** brand hues used sparingly — a clear blue (`#1470B0`) and
  a dusty rose/mauve (`#AC6080`) — seen together in one hero moment
  (three keywords in a rotating headline, each a different accent color).
  Everywhere else the page is neutral (black/white/grey); color only
  appears at moments the copy wants emphasis.
- Border radius: moderate throughout — 4px small, 8px default, 16px large,
  999px for pills/buttons. Not sharp-cornered, not overly rounded.
- Font: **Inter** (`-apple-system, BlinkMacSystemFont, "Segoe UI",
  system-ui` fallback stack) — a clean, neutral grotesk sans. No serif, no
  monospace anywhere.
- Motion: `IntersectionObserver`-based fade/reveal on scroll, explicitly
  gated behind `prefers-reduced-motion` — this is the literal mechanism
  behind principle 3 ("smooth, subtle"). Also uses a draggable before/after
  image comparison slider and a count-up number animation (`3,500+ users`)
  — both restrained, single-purpose interactions, not decorative.
- Layout: card grids for solution types and pricing tiers, a quote grid,
  a partner-logo strip, an FAQ accordion. Sections are clearly delineated
  but not boxed/shadowed — mostly whitespace doing the separating.

**Follow:** the white/near-white base with sparse, purposeful color;
the IntersectionObserver fade-on-scroll pattern (with reduced-motion
fallback) as the *only* scroll animation; Inter or an Inter-adjacent
grotesk sans; moderate (not zero, not heavy) corner rounding.

**Don't copy:** the specific blue/mauve pair (that's uuen's brand, not
InfraTwin's) — InfraTwin needs one accent color of its own, not two;
the pricing-tier card layout (not relevant, no pricing section here); the
FAQ accordion (not part of InfraTwin's approved outline).

---

## 2. auar.io

**What it is:** Automated Architecture — construction robotics/AI company
(deployable robotic MicroFactories + AI production software). The single
closest reference in *subject matter* to InfraTwin: robotics + AI +
built-environment, same category.

**Confirmed from source (`global.css`):**
- Background: warm cream/beige, not stark white — `#F3EDE9` (primary
  cream), `#FCFCFA` (near-white), `#DBD0C6` (tan/beige section variant).
- Text: near-black (`#141414`), dark grey (`#2D2D2D`), warm grey
  (`#616161`, `#706161`).
- Accent: a single vivid lime/chartreuse (`#D8FF3C`), with tints/shades
  for states — `#C2E636`, `#EBFF9D` (light), `#8DA724` (dark/olive). Used
  as the one bright color against an otherwise warm-neutral palette —
  a strong, literal example of principle 1.
- Layout: classic funnel — hero → problem statement → two-product
  showcase → five-step process → impact metrics → press → CTA. Full-width
  photography of real equipment/operations, not stock imagery.

**Follow:** warm off-white rather than clinical white (softer than
uuen's pure white); exactly one saturated accent color used sparingly
against a neutral field; real product/hardware photography over
illustration.

**Don't copy:** the specific lime-green hue (auar's brand identity, not
InfraTwin's); the client-logo/press-carousel section (no equivalent
traction material confirmed yet for InfraTwin, per the Step 1 outline).

---

## 3. zacuaventures.com

**What it is:** Zacua Ventures — VC fund investing in built-environment
founders. Not a product company, but useful for restraint.

**Confirmed from source:** fonts are **DM Sans** (weights 400/500/700,
italic 500) and **Public Sans** (400), loaded via Google Fonts (Salient
WordPress theme). Open Sans is a residual theme default, not actually the
displayed font.

**Descriptive (from rendered content, not raw CSS):** black text on
white/light background, no aggressive color blocking, three-pillar
framework ("Ideate. Build. Scale.") stated with heavy surrounding
whitespace, portfolio grid, team section.

**Follow:** the restraint itself — hierarchy built from type size/weight
contrast rather than color or boxes; generous margins around short,
declarative headline statements (this is the core of principle 2).

**Don't copy:** VC-fund-specific sections (portfolio grid, "send your
deck" CTA) — not relevant to a product pitch page.

---

## 4. vyzn.tech (English)

**What it is:** B2B SaaS for building/construction carbon and performance
optimization, "ETH Zürich technology" — another academic-spinout SaaS
analog.

**Confirmed from source:**
- Colors found in page: deep blue (`#1c4c98`, `#1c3461`), near-white
  background (`#f4f4f7`), amber/gold accent (`#F8B400`), slate grey
  (`#6b7280`), a secondary brown/tan (`#9a6b43`). (Note: this corrects an
  earlier AI-generated guess of "teal/cyan" — the real accent reads as
  deep blue paired with a warm amber highlight, not teal.)
- Fonts: **Poppins** (400/500/600/700) for the interface, **Caveat**
  (500/600, a handwritten script) apparently used sparingly for a human/
  annotation-style touch — worth noting as a technique (one warm,
  informal accent font against a clean geometric sans) rather than
  something to copy literally.

**Descriptive:** fixed minimal nav, five color-coded icon badges for
metrics (emissions/finance/energy/comfort/safety), a 3D building model
visualization, progressive-disclosure contact form.

**Follow:** color-coded small metric badges as a way to make data
scannable without a heavy chart; the general commitment to whitespace
between sections (principle 2 again).

**Don't copy:** Poppins/Caveat specifically (not evaluated against
InfraTwin's own type needs yet); the multi-step contact-form pattern (out
of scope — no forms per `DESIGN.md`).

---

## 5. woho.us/about

**What it is:** Construction/architectural technology company.

**Confirmed from source (Wix site):** font stack includes **Work Sans**
(400/700, roman + italic), **DIN Next** (light), **Helvetica** (light/
bold), and **Lulo Clean** (a bold display face, likely for one heading
treatment/logotype only, not body text).

**Descriptive:** white/light background, dark navy/charcoal text, one
electric-blue accent used consistently as a visual "arrow" motif; grid of
team headshots and partner/client logos; substantial founder bios.

**Follow:** a single confident accent color reused as a recurring visual
mark (their arrow) rather than scattered decoratively; team-bio treatment
if/when InfraTwin's team section is confirmed.

**Don't copy:** the arrow motif itself (that's woho's specific brand
device); the heavy photography-driven hero (InfraTwin's hero visual
options are different — see Step 1 image inventory).

---

## 6. vaulted.swiss

**What it is:** Prefabricated concrete floor systems, "15 years of
research at ETH Zurich" — another research-to-product construction-tech
spinout.

**Descriptive only** (color values weren't recoverable from static HTML —
likely rendered via a JS framework bundle not fully exposed in the fetched
markup): predominantly white/light neutral background, a lime-green
accent used sparingly (echoes auar.io's approach but a different green),
large hierarchical headlines, generous whitespace, technical sectional
diagrams as real supporting imagery rather than decoration.

**Follow:** using one real technical diagram (not a stock render) as a
key piece of hero/section imagery — directly applicable to InfraTwin,
which has real segmentation/point-cloud diagrams available.

**Don't copy:** nothing specific flagged — treat this one as a weaker
confidence reference given the extraction limits; revisit visually
(screenshot) before leaning on it hard.

---

## 7. foldcast.com

**What it is:** Swiss startup, sustainable concrete building elements made
with paper-based moulds.

**Confirmed from source:** white background (`#FFFFFF`), near-black text
(`#191819`), and a warm **orange accent (`#FF8515`)** — correcting an
earlier AI-guess of "navy blue accent," the real accent is orange, used
repeatedly through the page (6+ occurrences in the markup).

**Descriptive:** large bold headlines with generous line-height, spacious
section separation, architectural/construction photography (concrete
textures, fabrication process, team).

**Follow:** confirms the pattern across nearly every reference here —
white/near-white base, near-black text, exactly one saturated accent
color repeated consistently rather than several colors used once each.

**Don't copy:** the orange itself (foldcast's brand, not InfraTwin's).

---

## 8. airshade.eu — named bad example (motion)

**What it is:** Passive smart-shading cleantech (thermal-expansion-driven,
no electronics).

**Why it's flagged:** the project owner explicitly named this site's
scroll animation as too bold, to the point of causing visible page lag.
Structurally the page is also **dark-background** (deep navy/charcoal
with white type) — the opposite of principle 1 as well, so this reference
is a double counter-example, not just a motion one.

**Avoid:** whatever combination of parallax/staggered-reveal effects is
causing perceptible scroll lag — InfraTwin's motion should be limited to
the uuen.cloud-style simple opacity/translate fade gated behind
`prefers-reduced-motion`, nothing layered or parallax-heavy. Also avoid
dark-background sections as a default (per principle 1).

---

## 9. layered.ch

**What it is:** Construction robotics — automated spray-coating systems.

**Descriptive only** (the color values recoverable from source were
generic WordPress/Gutenberg default-palette boilerplate, not evidence of
the actual applied brand colors — not trustworthy, so not reported as
fact here): a black/beige dual-tone identity, embedded video loops and
GIFs demonstrating the robot hardware in action, gallery grid of
construction-site applications.

**Follow:** using video loops/GIFs of real robot hardware in motion as a
section treatment — relevant to InfraTwin given the YouTube video and the
real robot-platform photography already in `assets/extracted/`.

**Don't copy:** unverified — revisit visually before drawing firm
conclusions on its color system.

---

## Also referenced (not in the ranked list, named for context)

- **gravisrobotics.com** — named alongside `airshade.eu` as a bad example
  for animation weight/lag. Not separately browsed; same guidance applies
  (avoid heavy parallax/staggered scroll effects).

---

## Cross-cutting pattern (what nearly every good reference has in common)

Across uuen.cloud, auar.io, zacuaventures.com, vyzn.tech, woho.us,
vaulted.swiss, and foldcast.com — seven independently-run sites, several
of them literal research-to-product spinouts from ETH Zurich in the same
built-environment/robotics space InfraTwin sits in — the same formula
repeats:

- White or warm off-white background. Never a dark hero as the default.
- Near-black or navy text, not pure black-on-white harshness.
- **Exactly one** saturated accent color (lime, blue, orange, amber, or
  electric blue depending on the site), used repeatedly and consistently
  rather than several colors used once each. This lines up exactly with
  `DESIGN.md`'s existing global constraint of "no more than 1 accent
  colour."
- A clean grotesk sans typeface (Inter, DM Sans, Public Sans, Work Sans,
  Poppins — all close relatives), no serif, no monospace/technical
  typewriter styling anywhere in this whole set.
- Generous whitespace between sections; hierarchy from size/weight
  contrast, not color or boxes.
- Motion limited to simple scroll-triggered fade/reveal, `
  prefers-reduced-motion`-aware, plus at most one small interactive
  device (image-compare slider, count-up number) — never parallax or
  staggered multi-layer reveals.
- Real product photography/diagrams over stock imagery or generic 3D
  renders, wherever the company actually has hardware or output to show.

This reads closer to this project's **Architecture/Minimal** skeleton
category (`skeletons/architecture-minimal/DESIGN_LANGUAGE.md`) than any
of the other three — image-led, restrained typography, generous margins,
sparse navigation — but warmed up with a confident single accent color and
real photography, and explicitly not the **Technical/Research** language
(no monospace, no metadata rails, no visible-grid systems in any
reference here) — which conveniently keeps it naturally distinct from the
personal-portfolio site without having to force the distinction.
