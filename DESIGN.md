---
name: Compute Tycoon
description: A miniature compute campus invites players into a real game.
colors:
  ink: "#122b35"
  text: "#f0f5e9"
  mint: "#94e6c1"
  muted: "#b5c9cb"
  line: "#38515a"
  gold: "#f6cc80"
  mint-hover: "#b6f3d9"
  ink-link-hover: "#245341"
  screenshot-build: "#24434c"
  screenshot-contracts: "#3e514d"
  screenshot-crew: "#3c4b4b"
typography:
  display:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "clamp(44px, 5.5vw, 78px)"
    fontWeight: 550
    lineHeight: 1.04
    letterSpacing: "-.035em"
  headline:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "clamp(34px, 3.7vw, 52px)"
    fontWeight: 550
    lineHeight: 1.07
    letterSpacing: "-.035em"
  title:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "28px"
    fontWeight: 550
    lineHeight: 1.13
    letterSpacing: "-.035em"
  body:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "18px"
    lineHeight: 1.6
  lead:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "24px"
    lineHeight: 1.4
  button:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 550
    lineHeight: 1.6
  label:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "14px"
    lineHeight: 1.6
rounded:
  icon: "9px"
  control: "12px"
  screenshot: "16px"
spacing:
  compact: "12px"
  inline: "20px"
  related: "24px"
  navigation: "32px"
  mobile-section: "48px"
components:
  button-primary:
    backgroundColor: "{colors.mint}"
    textColor: "{colors.ink}"
    typography: "{typography.button}"
    rounded: "{rounded.control}"
    padding: "14px 25px"
  button-primary-hover:
    backgroundColor: "{colors.mint-hover}"
    textColor: "{colors.ink}"
  text-link:
    textColor: "{colors.mint}"
  screenshot-build:
    backgroundColor: "{colors.screenshot-build}"
    rounded: "{rounded.screenshot}"
    padding: "26px 38px 0"
    height: "450px"
  screenshot-contracts:
    backgroundColor: "{colors.screenshot-contracts}"
    rounded: "{rounded.screenshot}"
  screenshot-crew:
    backgroundColor: "{colors.screenshot-crew}"
    rounded: "{rounded.screenshot}"
  feature-copy:
    textColor: "{colors.muted}"
    padding: "26px 0 0"
  faq:
    textColor: "{colors.text}"
    padding: "23px 30px 23px 0"
  navigation:
    textColor: "{colors.text}"
  footer:
    textColor: "{colors.muted}"
    typography: "{typography.label}"
    padding: "30px 0 36px"
---

# Design System: Compute Tycoon

## Overview

**Creative North Star: "The Miniature Compute Campus"**

A miniature compute campus invites players into a real game. The world inherits Compute Tycoon's low-poly campus artwork, icon, Outfit typography, and deep teal, mint, ivory, and gold palette. Its personality is warm, optimistic, and practical: a small place with room for ambitious building.

The website gives real game imagery space to carry that personality. Open sections, restrained controls, and clear typography surround the artwork. Depth comes from the scene itself and tonal screenshot wells; interface chrome stays quiet. This document records the built static HTML/CSS system, including the selected direction contract (seed `e8cb3784`). The frontmatter is normative for tokens; `styles.css` and `index.html` are the extraction sources.

**Key Characteristics:**

- Real low-poly campus imagery and unaltered gameplay screenshots.
- An open deep teal stage with ivory text and mint accents.
- Rounded Outfit lettering, compact controls, and generous section spacing.
- Tonal media wells, thin dividers, and a single restrained scene arrival.
- Native links and disclosure controls that work without JavaScript.

## Colors

Deep teal grounds the world; pale mint and ivory keep it friendly and legible, with gold reserved for keyboard focus.

### Primary

- **Campus Mint** (`mint`): primary download button, headline emphasis, contextual links, disclosure indicators, and the full-width pace-of-play section. The lighter `mint-hover` belongs to the primary button's hover state.

### Secondary

- **Focus Gold** (`gold`): keyboard focus outlines on dark surfaces. On the mint section, focus switches to deep teal.

### Neutral

- **Deep Teal Ink** (`ink`): page background and foreground text on mint surfaces.
- **Soft Ivory** (`text`): headings, primary body copy, and navigation.
- **Mist Teal** (`muted`): supporting copy, captions, availability, and footer text.
- **Slate Divider** (`line`): quiet separators beneath the header, around FAQ rows, and between content groups.
- **Screenshot Teal**, **Screenshot Sage**, and **Screenshot Slate** (`screenshot-build`, `screenshot-contracts`, `screenshot-crew`): the three gameplay image wells.
- **Forest Link Hover** (`ink-link-hover`): link hover on the mint section.

**The Surface Contrast Rule.** Mint surfaces use deep teal text and deep teal focus; dark surfaces use ivory or mist text with gold focus.

## Typography

**Display and Body Font:** Outfit, with system-ui and sans-serif fallbacks. The locally hosted variable font supports weights from 100 to 900.

**Character:** Soft geometric lettering carries both the playful game identity and clear developer information. Headings use medium weight, tight tracking, balanced wrapping, and compact line height. There is no separate mono or editorial font.

### Hierarchy

- **Display:** the frontmatter's fluid display role is used for the hero; mint emphasizes its second line.
- **Headline:** section headings follow the fluid headline role.
- **Title:** gameplay feature headings use the title role and a short measure (15ch maximum).
- **Body:** base paragraphs follow the body role and a maximum measure (68ch). Supporting gameplay and FAQ text is smaller (17px).
- **Lead:** introductory statements use the lead role; hero supporting copy is a distinct intermediate size (20px).
- **Label:** availability and footer content use the label role; campus captions are slightly larger (15px).
- **Button:** medium-weight action text uses the button role. FAQ summaries use an intermediate weight (450) and size (19px).

On screens at or below 700px, display type becomes `clamp(37px, 9vw, 57px)` with line height (1.07); hero body becomes (18px), lead text (22px), buttons (16px), availability (12px), and captions (13px). Feature headings become (25px), then (22px) below 380px. Feature descriptions become (15px) with line height (1.55).

## Layout

The desktop content container is centered with a maximum width (1180px) and outer gutters (48px). At or below 1000px the gutters become (32px); at or below 700px they become (20px). Broad sections alternate between paired columns and the full-width mint band. Desktop paired columns use equal widths and a gap (100px), reduced to (48px) at the intermediate breakpoint.

The header lays the brand and navigation on one line. The hero centers its type, action, and broad campus artwork. The campus normally has a maximum width (1100px), expanding to (1180px) from 1500px. On mobile it extends slightly beyond the content container (112% width with a -6% left margin) while the hero clips horizontal overflow.

Gameplay uses three equal columns, with gaps (42px), reducing to (24px) at the intermediate breakpoint. At or below 700px the features become divided horizontal rows: image (42%) beside text, with a gap (22px). Below 380px the image becomes (40%) and the gap (16px). Paired introduction, mint-band, and support sections stack on mobile. The footer wraps; its closing tagline disappears at or below 1000px.

Desktop section spacing is generous: the introduction begins with (82px) top padding, gameplay ends with (110px), the mint section uses (78px) vertical padding, and support uses (104px). Mobile reduces these to a rhythm around (48px–56px). Keep these surface-specific dimensions in their existing layout context rather than treating all values as universal spacing tokens.

## Elevation & Depth

There are no CSS box shadows. Depth comes from the real low-poly campus and the muted background colors framing the screenshots. Thin rules separate information without enclosing every section in a card.

The campus image enters once over (1.1s), using `cubic-bezier(.16,1,.3,1)`, a vertical move from (22px), and a small bottom clip. It remains visible throughout. Buttons transition their background over (0.2s ease). Reduced-motion preference disables both effects and smooth scrolling.

**The Artwork Depth Rule.** Preserve the flat interface and let actual game imagery supply the dimensional detail.

## Shapes

Controls use gently rounded corners; the app icon is more compact, while screenshot wells are slightly broader. Their exact radii live in the frontmatter. Gameplay images have rounded top corners matching the control radius and sit flush with the bottom crop of their well. At mobile widths the wells use the control radius.

Borders are thin (1px) and tonal. External-link arrows are small diagonal line marks. FAQ rows use a mint plus that becomes a minus when opened. Neither decorative pills nor a general-purpose elevated card shell is part of the built system.

## Components

### Buttons

Confident, compact mint actions. The primary App Store link uses the frontmatter's primary-button tokens, a minimum height (56px), and a diagonal arrow separated from text by (26px), reduced to (20px) on mobile. Hover uses the lighter mint variant. Keyboard focus uses an outline (3px) with offset (6px). The implementation has one filled button variant.

### Text Links

Underlined contextual links carry the same arrow and use medium weight (500). Their text/arrow gap is (24px). Support links are mint on deep teal; the mint section uses deep teal with the forest hover color. Preserve visible underlines for in-copy links and the same keyboard focus treatment.

### Cards / Containers

Gameplay features are image wells followed by open text, not boxed cards. Desktop wells crop at their fixed height, with padding and radius defined in the frontmatter; the second and third change only the tonal background. At the intermediate breakpoint wells become (370px) tall with (20px) side/top padding. On mobile they become (285px) tall with (12px) padding, then (265px) below 380px. Keep the original screenshot proportions and descriptive alternative text.

### Navigation

The header combines the existing icon and medium-weight wordmark with unadorned text navigation. The brand and nav share the base font. Desktop navigation uses (16px) text with the navigation spacing token and (10px) vertical link padding; the download link is mint. On mobile it uses (15px) text and (20px) gaps; only Support remains in the header navigation. The primary download action remains in the hero.

### Disclosure Rows

Native `details` and `summary` elements provide keyboard-operable support questions without JavaScript. Rows have tonal bottom borders; the first also has a top border. Summaries use the frontmatter padding, a mint plus/minus at the right, and mint hover text. Open responses use smaller muted body text with right and bottom padding (25px). Focus remains visibly outlined.

### Footer

A thin top rule and small muted type close the page. Copyright, privacy/contact links, and the closing line sit in a flexible row on desktop. Links retain underlines. Mobile wrapping follows the available width rather than compressing the labels.

## Do's and Don'ts

### Do:

- **Do** reuse the actual campus artwork, app icon, local Outfit font, and gameplay screenshots.
- **Do** keep the page's deep teal stage, mint actions, ivory headings, and muted supporting copy.
- **Do** preserve native link and disclosure semantics, visible focus, and reduced-motion behavior.
- **Do** keep feature text outside the screenshot wells and let mobile features become image-and-text rows.
- **Do** use the frontmatter for token values and the sidecar for motion, responsive metadata, and component previews.

### Don't:

- **Don't** introduce a second type family or substitute unrelated stock imagery for the game.
- **Don't** add shadows to the flat controls and content sections.
- **Don't** use pale text or gold focus on the mint section.
- **Don't** replace native disclosure behavior with a JavaScript requirement.
- **Don't** turn this page's hero composition into a mandatory layout for every future surface.
