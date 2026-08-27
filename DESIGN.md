---
name: Plain Point Studio
description: A dispensary label sheet, where every app carries an honest label of what it does with your data.
colors:
  liner: "#c9d1cc"
  liner-deep: "#a9b4ae"
  liner-line: "#b6c0ba"
  stock: "#f6f7f4"
  stock-back: "#e2e5df"
  ink: "#15181a"
  ink-soft: "#4a524e"
  strip-good: "#b8e600"
  strip-note: "#ffa61a"
  strip-info: "#00b3d6"
  strip-hold: "#9aa3a8"
  url: "#056a80"
  live-dot: "#6f8c00"
  mask-opaque: "#000"
typography:
  display:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(3rem, 11.5vw, 6rem)"
    fontWeight: 800
    lineHeight: 0.86
    letterSpacing: "-0.025em"
    fontVariation: "'wdth' 66"
  headline:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(1.5rem, 1.15rem + 1.3vw, 2.25rem)"
    fontWeight: 800
    lineHeight: 0.98
    letterSpacing: "-0.02em"
    fontVariation: "'wdth' 74"
  title:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(1.1rem, 0.95rem + 0.8vw, 1.55rem)"
    fontWeight: 600
    lineHeight: 1.28
    letterSpacing: "-0.015em"
    fontVariation: "'wdth' 92"
  body:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(1rem, 0.96rem + 0.2vw, 1.0625rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  label:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "0.72rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.07em"
    fontVariation: "'wdth' 80"
  label-sm:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "0.68rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.12em"
    fontVariation: "'wdth' 84"
  action:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "0.06em"
    fontVariation: "'wdth' 86"
  record-value:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "0.92rem"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "normal"
    fontVariation: "'wdth' 88"
  strip-thai:
    fontFamily: "'Noto Sans Thai', 'Leelawadee UI', Thonburi, sans-serif"
    fontSize: "1.1em"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
rounded:
  cut: "6px"
  die: "14px"
  die-lg: "20px"
  die-master: "22px"
spacing:
  gutter: "clamp(0.75rem, 1.6vw, 1.25rem)"
  pad: "clamp(1.25rem, 2.6vw, 2rem)"
  sheet: "clamp(1rem, 3.4vw, 3rem)"
  strip-gap: "3px"
components:
  strip-good:
    backgroundColor: "{colors.strip-good}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    padding: "0.6em 0.9em"
  strip-note:
    backgroundColor: "{colors.strip-note}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    padding: "0.6em 0.9em"
  strip-info:
    backgroundColor: "{colors.strip-info}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    padding: "0.6em 0.9em"
  strip-hold:
    backgroundColor: "{colors.strip-hold}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    padding: "0.6em 0.9em"
  label-card:
    backgroundColor: "{colors.stock}"
    textColor: "{colors.ink}"
    rounded: "{rounded.die}"
    padding: "{spacing.pad}"
---

# Design System: Plain Point Studio

## Overview

**Creative North Star: "The Dispensary Label Sheet"**

The site is a printed sheet of gummed labels resting on its grey backing liner. Every app is
one die-cut label: a lot number, a name struck in condensed ink, directions in plain prose,
and a row of saturated auxiliary strips along the foot carrying the facts a person needs
before they touch the thing. The liner shows between the labels, scored down the middle with
a dashed perforation, because a sheet you can see the backing of is a sheet, not a card grid.

This world was chosen because it makes the studio's central claim structural instead of
rhetorical. A page that *says* "privacy-first" is asking to be believed; a page where every
product carries an ingredients label — including the one product that has to admit it uses a
server — has already proved it. The strips are the argument. Everything else is stock and ink.

The register is plain and industrial, never clinical. This is the label a workshop prints,
not one a pharmacy dispenses: no crosses, no hazard diamonds, no medical iconography, and the
notice color is a working amber rather than a warning red. Density is generous — the labels
are mostly quiet stock with the ink concentrated at the top and the color concentrated at the
foot.

**Key Characteristics:**
- Grey liner ground with off-white label stock floating on it, never a full-bleed page color
- Condensed Archivo ink; the width axis carries the label-print character
- Semantic color confined to the auxiliary strips, which do real informational work
- Mixed die formats and mixed corner profiles — no two label sizes repeat in a row
- Flat stock: one shadow, no borders, no gradients standing in for material

## Colors

A cool grey-green liner under near-white stock, with all saturation quarantined into the
auxiliary strips where it carries meaning.

### Primary
- **Signal Chartreuse** (`{colors.strip-good}`): The privacy strip. Applied only where a
  property genuinely holds — data on device, no account, files never uploaded. It is the most
  frequent saturated color on the sheet and the reason the sheet exists.
- **Working Amber** (`{colors.strip-note}`): The notice strip. Something the visitor must know
  before using the app — it needs a server, it needs a sign-in. Deliberately warm rather than
  red: a disclosure, not a hazard.

### Secondary
- **Instrument Cyan** (`{colors.strip-info}`): The neutral-fact strip. Platform, languages,
  licence. Carries no judgment either way.
- **Held Grey** (`{colors.strip-hold}`): The status strip. Not yet released, withdrawn,
  pending. Reads as absence of ink rather than as a color choice.

### Neutral
- **Liner Grey** (`{colors.liner}`): The page ground — the backing sheet the labels sit on.
- **Liner Shadow** (`{colors.liner-deep}`): Registration marks and any receding liner detail.
- **Perforation** (`{colors.liner-line}`): The dashed scoring line down the liner's centre.
- **Label Stock** (`{colors.stock}`): Every label body. The only surface that carries prose.
- **Backing Edge** (`{colors.stock-back}`): The strip bed behind the auxiliary row, and the
  hairline rules that divide record rows and the colophon.
- **Press Ink** (`{colors.ink}`): All display and label type; also the focus ring.
- **Soft Ink** (`{colors.ink-soft}`): Body prose, lot numbers, field names, pending states.
- **Address Blue** (`{colors.url}`): Hostnames and links only.
- **Live Dot** (`{colors.live-dot}`): The status dot beside "Live". A darkened chartreuse so it
  survives on stock at 0.6em where the strip chartreuse would not.

### Named Rules
**The Earned Strip Rule.** A `strip-good` is a factual claim about an app's data handling. An
app never receives one it has not earned, and no strip is ever chosen for visual balance. If
an app needs a server, it carries `strip-note` in plain sight — that disclosure is the design,
and softening it breaks the system.

**The Quarantine Rule.** Saturation lives in the strips. Stock, prose, headings, and liner stay
neutral; a saturated background anywhere else means a strip has escaped its bed.

## Typography

**Display Font:** Archivo Variable (fallback `'Helvetica Neue', Arial, sans-serif`)
**Body Font:** Archivo Variable (same family, normal width)
**Label Font:** Archivo Variable at 80–84% width, uppercase, tracked

**Character:** One variable family doing three jobs through its **width axis**, the way a label
press does it with one typeface and several condensed cuts. Weight alone would read as generic
UI; the compression is what makes it print. Archivo is self-hosted from `fonts/` as two woff2
subsets (latin, latin-ext) with both axes live — `wght` 400–800 and `wdth` 62%–125%.

### Hierarchy
- **Display** (800, `clamp(3rem, 11.5vw, 6rem)`, 0.86, width 66%): The studio name on the
  master label. Uppercase, tightly tracked, set to break across two lines.
- **Headline** (800, `clamp(1.5rem, 1.15rem + 1.3vw, 2.25rem)`, 0.98, width 74%): App names.
  Uppercase. The `.sub` line beneath (a product's second name, e.g. "Leafy Ledger") drops to
  label treatment rather than competing.
- **Title** (600, `clamp(1.1rem, 0.95rem + 0.8vw, 1.55rem)`, 1.28, width 92%): The tagline
  only. Capped at 24ch so it breaks where it should.
- **Body** (400, `clamp(1rem, 0.96rem + 0.2vw, 1.0625rem)`, 1.55): All prose, soft ink,
  measure capped at 64ch.
- **Label** (700, 0.72rem, tracking 0.07em, uppercase, width 80%): Auxiliary strips.
- **Label Small** (700, 0.68rem, tracking 0.11–0.14em, uppercase, width 84%): Lot numbers,
  record field names, the sheet marker, the colophon. Tracked wider than the strips because it
  sits on stock rather than on color.
- **Action** (700, 0.78rem, tracking 0.06em, uppercase, width 86%): The `Open` / `Reserved`
  line; its hostname drops to normal case in address blue.
- **Record Value** (600, 0.92rem, width 88%): Right-aligned values in the studio record. The
  only label-family role that is neither uppercase nor tracked.

Tabular figures are on globally (`font-variant-numeric: tabular-nums`), so record values and
lot numbers align down their column.

### Named Rules
**The Width-Axis Rule.** Emphasis is made by compressing, not by adding weight or size alone.
Any new display or heading role picks a `font-stretch` value first; a heading set at normal
width has left the world.

**The Latin-Only Rule.** The self-hosted subsets cover Latin. Non-Latin text (Thai, in the
Life Balance Index strip) falls back deliberately, wrapped in `lang` and released from
`text-transform` and `letter-spacing`, which damage combining marks. Never track or uppercase
non-Latin strings. The fallback is *named*, not left to the OS: `.th` declares
`"Noto Sans Thai", "Leelawadee UI", "Thonburi", sans-serif` at weight 700, so the Thai run
sits at the same optical weight as the condensed Latin beside it instead of reading as a
failed font load.

**The Drawn-Glyph Rule.** Any glyph outside the subset is drawn in CSS, never typed. The
action arrow is a rotated two-border box on `.go__do::after`, not `U+2192` — that codepoint is
absent from both the Archivo subset and Google's stock `latin` unicode-range, so typing it
silently renders a system-font arrow beside condensed Archivo. Before adding any symbol
character to copy, confirm it is in the subset or draw it.

## Layout

A centred sheet, `max-width: 1180px`, padded `{spacing.sheet}`, laid out as a vertical stack
of labels separated by `{spacing.gutter}`.

The catalogue is a **12-column grid, uneven where unevenness pays**: 7 / 5 on the first row,
then an even 4 / 4 / 4 on the second. The asymmetric first row is what makes the page a sheet
of mixed dies rather than a card grid; the second row is even because measure wins over
composition. A 3-span at this sheet width leaves ~197px — roughly 20 characters — which breaks
prose into ragged four-word lines, orphans the action row, and (because grid rows stretch to
the tallest sibling) forces ~180px of dead stock into both of its neighbours. **Difference is
carried by die profile and strip depth, never by starving a column below usable measure.**

Responsive behavior:
- **≥900px:** the master label splits into two columns (`1.55fr` prose / `minmax(280px, 1fr)`
  record), putting the studio record in the right field of the first viewport.
- **≤1000px:** catalogue spans collapse to 6, with the wide label taking the full 12.
- **≤680px:** everything goes full width; auxiliary strips drop to `flex: 1 1 45%` so short
  claims pair two-up rather than each becoming a full-bleed band of saturated colour — at
  phone width, one-per-row turns the palette into the loudest thing on the page. The liner
  perforation and the master's tab notch are both removed, since neither reads at that size.
- **320px** (the literal WCAG 1.4.10 reflow width) is verified, not assumed: no horizontal
  overflow and no clipped strip or host string.

Spacing rhythm: tight inside a label (0.5–1.4rem between elements), generous between labels.
More space sits above a heading than below it.

## Elevation & Depth

Flat stock lifted off a liner. Depth comes from **one shadow, declared once** — never a border
plus a shadow, and never both on the same element. Labels are opaque label stock on a liner
ground; there is no tonal layering, no glass, and no gradient used as material.

### Shadow Vocabulary
- **At rest** (`box-shadow: 0 1px 2px rgba(21,24,26,0.16), 0 12px 26px -14px rgba(21,24,26,0.5)`):
  A tight contact shadow plus a wide soft drop. This is a label lying on a sheet.
- **Lifted** (`box-shadow: 0 2px 4px rgba(21,24,26,0.18), 0 26px 40px -20px rgba(21,24,26,0.62)`):
  Applied on `:hover` and `:focus-within` alongside `translateY(-3px)`. Catalogue labels only —
  the master and footer never lift, because they are not actionable.

### Named Rules
**The One Elevation Rule.** Every surface declares its depth exactly once, with a shadow. A
1px border beneath a wide soft shadow is the ghost-card failure and is banned outright.

**The No Fake Physics Rule.** Paper behavior is expressed with real geometry — a die profile, a
mask-cut notch — never with a gradient shaded to imitate a curl or fold. An earlier build used
a gradient corner "peel"; it was removed for exactly this reason.

## Shapes

The form language is **die-cutting**: every label format is cut to its own profile, and no two
adjacent labels share one.

- Master label: `{rounded.die-master}` all round, plus a genuine 15px semicircular **tab notch**
  cut into its left edge with `mask-image: radial-gradient(circle 15px at 0 96px, …)`. Removed
  below 680px.
- Wide label: `6px 20px 20px 6px` — square left, round right.
- Tall label: `20px 6px 6px 20px` — the mirror of its neighbour.
- Five-span: `6px`. Three-span: `20px`. Four-span: `6px 6px 20px 20px`. Footer: `6px`.

Auxiliary strips are hard rectangles with no radius, seated in a backing-edge bed with a
`{spacing.strip-gap}` gutter, so they read as separate stickers applied to the label rather
than as a segmented control. The registration crosshair in the master record is drawn as crisp
SVG geometry (two circles, four ticks) — vector diagram, never illustration.

The one literal `#000` in the stylesheet is the opaque channel of the master label's
`mask-image` gradient — a mask value, not a palette color. It is the only color literal in the
build that is not a documented token, and it must stay that way.

### Named Rules
**The Mixed Die Rule.** Adjacent labels never share a corner profile. Adding a new label means
choosing a die that differs from both of its neighbours.

## Components

### Label (the signature component)
The only container in the system; there are no cards.
- **Corner Style:** per-format die profile (see Shapes). Never a uniform radius across a row.
- **Background:** label stock, opaque.
- **Shadow Strategy:** at-rest shadow; lifted on hover/focus for catalogue labels only.
- **Border:** none, ever.
- **Internal Padding:** `{spacing.pad}`.
- **Structure:** `.label__body` (flex: 1) over a `.strips` row pinned to the foot, so strips
  align along the bottom edge regardless of how much prose sits above them.
- **Whole-label link:** the app-name anchor carries a stretched `::before` covering the label,
  making the entire surface the target while leaving one real link in the accessibility tree.

### Auxiliary Strip
- **Style:** flat rectangle, press-ink text on its semantic color, uppercase label type.
- **Behavior:** `flex: 1 1 auto` with `white-space: nowrap` on desktop, so a row self-balances;
  at ≤680px it becomes `flex: 1 1 45%` with wrapping, pairing short claims two-up.
- **Dosage:** no label's strip bed is allowed to be entirely amber. A card whose only strips
  are notices reads as an alert banner, which inverts the meaning — the honest disclosure is
  supposed to sit *among* facts, not replace them. Runaway therefore leads with a cyan
  `Open source` before its two amber notices.
- **Contrast:** every strip color is chosen to clear 4.5:1 against press ink — measured
  chartreuse ≈13:1, cyan ≈7.3:1, amber ≈9.3:1, grey ≈7.1:1. Text on strips is never white.

### Lot Line
- **Style:** a flex row at the top of every label — lot number left in soft ink, status right.
- **Status:** `.lot__state` with a 0.6em dot. Live = live-dot green and full-ink text;
  pending = held grey dot and soft-ink text.

### Action Line
- **Style:** `Open` in uppercase label type followed by a CSS-drawn chevron (`::after`, two
  borders rotated 45°) and the literal hostname in address blue. See the Drawn-Glyph Rule.
- **Hover / Focus:** the chevron translates diagonally 3px; the app name underlines at 2px with
  a 5px offset.
- **Unavailable variant:** `Reserved` with the arrow suppressed and the host in soft ink — used
  when a product has a domain but nothing published at it.

### Record Block
- **Style:** a definition list in the master label's right field. A 2px ink rule under the
  title, 1px backing-edge rules between rows, field name left in label type, value
  right-aligned in 600 weight.
- **Purpose:** the studio's own verifiable facts (developer name, registrant, domain, count,
  stack, source), closed by a registration crosshair.

### Focus
- **Style:** `outline: 3px solid` press ink at `3px` offset, globally on `:focus-visible`.
  A `:focus` rule is declared *first*, then neutralised by `:focus:not(:focus-visible)`, so
  Safari < 15.4 — which discards any rule containing `:focus-visible` — still shows a ring.
  A skip link sits off-canvas and returns on focus.
- **Stretched target:** the whole `.label__body` is the click target, so the ring belongs on
  the card, not on the two words of the title. Inside `@supports selector(:has(a))`, the
  anchor's own outline is suppressed and `.label:has(h3 a:focus-visible)` carries it; browsers
  without `:has()` keep the anchor ring rather than losing focus indication entirely.
- **Scope:** the overlay is bounded by `position: relative` on `.label__body`, never on
  `.label`. On `.label` it would swallow the auxiliary strips, making the page's load-bearing
  disclosures unselectable and turning "Server component (Supabase)" into a link to the app.

## Do's and Don'ts

### Do:
- **Do** give every product a full strip row, and make each strip a fact you could defend.
- **Do** disclose a server, an account, or a sign-in requirement with `strip-note` in the same
  row as the good news. The honesty is the product.
- **Do** pick a die profile that differs from both neighbours when adding a label.
- **Do** reach for the width axis (`font-stretch`) before reaching for size or weight.
- **Do** keep the page free of third-party requests and executing scripts; the footer makes
  that claim in writing and the build has to keep it true.
- **Do** state a product's real status, including "Not yet released", rather than linking to
  something that 404s.

### Don't:
- **Don't** award a `strip-good` an app has not earned, or drop a `strip-note` to make a row
  look tidier.
- **Don't** put a border and a shadow on the same surface.
- **Don't** imitate paper physics with gradients — cut real geometry or leave it flat.
- **Don't** let saturation out of the strips onto stock, prose, or the liner.
- **Don't** uppercase or letter-space non-Latin text.
- **Don't** reintroduce a uniform three-up row of equal cards; the uneven span pattern is the
  whole compositional thesis.
- **Don't** add medical or hazard iconography. The world is a workshop label press, not a
  pharmacy.

<!--
Known open items, recorded rather than canonized (finish review, minor severity):
- Voluma's span-3 measure runs short and its host URL breaks mid-token at desktop.
- The master's tab notch reads more like a bump than a cut at rendered scale.
- Blank stock remains below the record column at desktop.
These are accepted trade-offs of the mixed-die composition, not rules to preserve.
-->
