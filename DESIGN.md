---
name: Azniezul Islami portfolio
description: One-page developer portfolio; warm off-white, near-black ink, one sienna accent, one typeface, hairlines only.
colors:
  ground: "#F5F4F0"
  ink: "#1A1917"
  ink-2: "#5F5B54"
  rule: "#DDD9D0"
  accent: "#B4471B"
  accent-ink: "#8F3612"
typography:
  display:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.4rem, 4.2vw, 3.4rem)"
    fontWeight: 600
    lineHeight: 1.02
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 500
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  body-small:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 500
    letterSpacing: "0.08em"
rounded:
  none: "0"
  focus: "2px"
spacing:
  page-pad: "clamp(1.25rem, 5vw, 4rem)"
  column-gap: "clamp(2rem, 6vw, 5rem)"
  page-top: "clamp(3rem, 10vh, 6rem)"
  section-gap: "clamp(4rem, 10vh, 6.5rem)"
  heading-below: "1.75rem"
  row-gap: "2.25rem"
  date-col: "7rem"
  row-col-gap: "1.5rem"
  para-gap: "1.1rem"
components:
  link-body:
    textColor: "{colors.ink}"
    typography: "{typography.body}"
  link-body-hover:
    textColor: "{colors.accent-ink}"
  nav-link:
    textColor: "{colors.ink-2}"
    typography: "{typography.label}"
  nav-link-hover:
    textColor: "{colors.ink}"
  nav-link-active:
    textColor: "{colors.ink}"
  skip-link:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.ground}"
    padding: "0.6rem 1rem"
  tech-list:
    textColor: "{colors.ink-2}"
    typography: "{typography.body-small}"
  section-heading:
    textColor: "{colors.ink-2}"
    typography: "{typography.label}"
---

# Design System: Azniezul Islami portfolio

## Overview

**Creative North Star: "The Typeset Resume"**

A conventional two-column developer portfolio (brittanychiang.com is the quality bar) done as a well-set document rather than a product UI: a sticky identity rail on the left, a scrolling column of experience and projects on the right, and nothing on the page that is not text, space, or a one-pixel line. Hierarchy comes from scale, weight and tracking inside a single typeface; separation comes from whitespace and hairlines; colour is one warm accent that appears only when the reader touches something or the scroll reaches a section.

Confirmed rejections (the world was chosen against them): gradient or filled buttons, cards around lists, pill-shaped tech tags, drop shadows, status badges, section counters, more than one accent, and monospace used as decoration.

**Key Characteristics:**
- Warm off-white paper with near-black ink and a single burnt-sienna accent.
- One family (Archivo 400/500/600) for every role, tabular figures throughout.
- Zero radius, zero shadow; hairlines (`1px` of `rule`) are the only drawn structure.
- Every list row is a date column beside content; tech names are plain text separated by middle dots.
- One signature motion: the nav marker hairline that extends and turns accent on the active section.

## Colors

Warm neutrals with one hot accent; the accent is a response to the reader (hover, focus, selection, active section), never a surface.

### Primary
- **Burnt Sienna** (`accent`): link underline on hover, the active nav marker, the focus ring (`2px` outline, `3px` offset) and text selection background. Never a fill behind text, never a button.
- **Sienna Ink** (`accent-ink`): the darker sienna that body-link text turns on hover, so accent text stays legible on the ground.

### Neutral
- **Paper** (`ground`): the only background on the page; also the text colour on the two inverted elements (skip link, selection).
- **Ink** (`ink`): headings, names, body links at rest, strong runs inside secondary prose.
- **Soft Ink** (`ink-2`): the working secondary; positioning line, section headings, dates, organisation lines, description paragraphs, tech lists, labels, footer.
- **Hairline** (`rule`): one-pixel rules (coursework rows, footer top), the resting link underline, and the resting nav marker.

### Named Rules
**The One Accent Rule.** Sienna appears only as a reaction: hover underline, hovered link text (`accent-ink`), active nav marker, focus ring, selection. At rest the page is ink on paper; no accent surface or accent fill exists.

**The Two-Ink Rule.** Text is `ink` or `ink-2`, nothing in between. Emphasis inside `ink-2` prose is done by switching a `strong` run to `ink` at weight 500, not by a third grey.

## Typography

**Display Font:** Archivo (with Helvetica Neue, Arial, sans-serif)
**Body Font:** Archivo (same family)

**Character:** One grotesk carries every role; the ramp is built from size, weight (400/500/600) and tracking that tightens as size grows. `font-variant-numeric: tabular-nums` is set on `body`, so dates and years align.

### Hierarchy
- **Display** (600, `clamp(2.4rem, 4.2vw, 3.4rem)`, 1.02, `-0.025em`, `text-wrap: balance`): the name in the rail only.
- **Headline** (500, `1.25rem`, `-0.01em`): the role line under the name.
- **Title** (600, `1.125rem`, 1.3, `-0.01em`): each experience or project title. A coursework subhead is the same family at 500 / `1rem`.
- **Body** (400, `1.0625rem`, 1.6): paragraphs, capped at `62ch` in About, `60ch` in rows and footer, `52ch` in Contact, `34ch` for the rail pitch.
- **Body small** (400, `0.875rem`): dates, tech lists, skill and contact labels, footer.
- **Label** (500, `0.8125rem`, `0.08em`, uppercase, `ink-2`): section headings (the `h2` itself) and the rail nav items. This is the only uppercase voice on the page.

### Named Rules
**The One Family Rule.** Archivo at 400, 500 and 600 is the whole type system. No second face, no monospace; a tech name is body-small text, not code.

**The Heading-Is-The-Label Rule.** The tracked uppercase label is a section's `h2`, never a kicker sitting above another heading. Titles inside sections are sentence-case Title weight.

## Layout

A `1280px` max-width page with `page-pad` (`clamp(1.25rem, 5vw, 4rem)`) side padding, laid out as a two-column grid: a `34%` rail and a `minmax(0, 1fr)` main column with `column-gap` between them. The rail is `position: sticky; top: 0; height: 100vh`, a flex column with `justify-content: space-between`, so the name, role, pitch and nav sit at the top and the reach links (Email, Resume, GitHub, LinkedIn) sit at the bottom. Both columns start at `page-top` (`clamp(3rem, 10vh, 6rem)`).

Sections are separated by `section-gap` and share it as `scroll-margin-top` so anchored jumps land with the same breathing room. A section heading sits `heading-below` (`1.75rem`) above its content. Row lists (experience, projects) stack with `row-gap` (`2.25rem`); every row, coursework item, skill group and contact line is the same two-column grid: a `7rem` date or label column, a `1.5rem` gutter, then content.

At `900px` and below the page becomes one column: the rail un-sticks, its height goes auto and the nav is hidden (the sections read in order); main starts `3.5rem` down; every date-column grid collapses to a single column with `0.25rem` gap so the date sits directly above its content. Print does the same and strips link underlines.

## Elevation & Depth

None. There are no shadows, no tonal surfaces and no borders around blocks; the whole page is one flat paper. Structure is drawn only by whitespace and by one-pixel `rule` hairlines (coursework rows, footer top, the resting nav marker, the resting link underline). Two elements invert the page (`ink` on `ground` becomes `ground` on `ink`): the skip link and text selection (`accent` behind `ground`).

### Named Rules
**The Hairline Rule.** Any separation that whitespace cannot carry is a `1px solid rule` line. No shadow, no second background, no border-plus-shadow stack.

## Shapes

Square. Every box has `0` radius; the only rounded value on the page is the `2px` radius on the `:focus-visible` outline. There are no chips, pills or cards. Lines are horizontal hairlines only: the nav marker is a `1px`-tall, `2rem`-wide rule that grows to `4rem`; list separators are full-width `1px` rules.

## Components

### Links
- **Body link** (inside prose, footer, headings): `ink` text, `1px` underline in `rule` colour offset `0.2em`; on hover the text turns `accent-ink` and the underline turns `accent`. `200ms` `cubic-bezier(.2,.7,.2,1)` on both colour and underline colour.
- **Plain link** (rail reach list, contact list, row titles): no underline at rest; on hover an `accent` underline appears. Contact links are weight 500.
- **Focus:** every focusable element gets `2px solid accent` outline at `3px` offset with a `2px` radius.

### Navigation
- Vertical list in the rail, items `0.55rem` apart, each a Label-style link in `ink-2` with a `0.9rem` gap after a marker.
- **Marker:** a `2rem` by `1px` hairline in `rule` drawn with `::before`.
- **Hover:** text turns `ink`; the marker widens to `4rem` and turns `ink`.
- **Active (`aria-current="true"`, set by an IntersectionObserver with `-30% 0px -50% 0px` root margin; the last section is marked when the page bottom is reached):** text `ink`, marker `4rem` in `accent`.
- **Motion:** width and background-color, `200ms`, `cubic-bezier(.2,.7,.2,1)`; transitions collapse to `0.01ms` under `prefers-reduced-motion`.
- **Mobile / print:** hidden.

### Row (experience, project)
- Two-column grid, `7rem` date in Body small `ink-2` (nowrap, `0.2em` top padding to sit on the title's cap line), content on the right.
- Content: Title, an optional organisation line in `ink-2`, a description paragraph in `ink-2` at `0.6rem` with `strong` runs at 500 `ink`, then a tech list at `0.75rem`.

### Tech list
- Body small `ink-2`, flex-wrapped, each name `white-space: nowrap`; every name after the first is preceded by a middle dot (`\00B7`) with `0.5rem` side margins at `0.6` opacity. Never a pill, never a border.

### Coursework list
- Same date-column grid inside a list, `0.7rem` vertical padding, `1px rule` bottom border on each item except the last; the item's first phrase is a `strong` run at 500 `ink` inside `ink-2` text.

### Skills
- Definition list on the date-column grid: `dt` in Body small `ink-2`, `dd` is a tech list. On mobile each `dd` gets `0.9rem` below it.

### Skip link
- Off-screen until focused; then `ink` background, `ground` text, `0.6rem 1rem` padding, pinned `1rem` from the top-left, `z-index` 20.

## Do's and Don'ts

### Do:
- **Do** keep every background `ground`; the only inversions are the skip link and text selection.
- **Do** put any new list on the `7rem` date-column grid with a `1.5rem` gutter, collapsing to one column at `900px`.
- **Do** separate tech names with the middle dot pattern (`\00B7`, `0.5rem` margins, `0.6` opacity) in Body small `ink-2`.
- **Do** use `1px solid rule` for any drawn separator.
- **Do** keep hover and state motion at `200ms cubic-bezier(.2,.7,.2,1)` on colour, underline colour or width only, and respect `prefers-reduced-motion`.
- **Do** cap prose at `52ch` to `62ch`.

### Don't:
- **Don't** add a second accent, a filled or gradient button, or use `accent` as a background behind text.
- **Don't** wrap lists in cards, put tech names in pills, or add a border radius anywhere but the focus ring.
- **Don't** use a shadow of any kind.
- **Don't** add a second typeface or a monospace run; the tech list is plain Archivo.
- **Don't** put a kicker or eyebrow above a heading; the tracked uppercase label is reserved for the `h2` and the nav.
- **Don't** add icons, badges, status dots or section counters.

## Additions, 2026-09-19 evening

- The name in the rail is set in the accent (`#B4471B`) and returns to ink on hover; this is the
  one place colour is used at display size.
- Skills are buttons. Hovering or focusing one highlights the project rows whose tech list
  contains it (`.row.hit`: title in accent-ink, a 1rem accent marker slides in from the left);
  the other rows drop to 35% opacity. Clicking pins the filter (`aria-pressed="true"`); clicking
  again releases it. The middle-dot separators are pseudo-content with empty alt text so they do
  not enter accessible names.
- Project rows have no date column (`.rows.plain`); years appear only in Experience.
