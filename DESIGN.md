---
version: alpha
name: FOSS for Enterprise
description: >-
  Dracula-themed enterprise presentation design: deep purple-slate canvas,
  vibrant pastel accents, high-contrast link styling, and SVG icon masks.
colors:
  primary: "#bd93f9"
  bg-canvas: "#282a36"
  bg-card: "#44475a"
  text: "#f8f8f2"
  muted: "#6272a4"
  cyan: "#8be9fd"
  green: "#50fa7b"
  orange: "#ffb86c"
  pink: "#ff79c6"
  pink-link: "#ff9fd6"
  purple: "#bd93f9"
  purple-light: "#d2b5ff"
  red: "#ff5555"
  red-light: "#ff8585"
  yellow: "#f1fa8c"
typography:
  display:
    fontFamily: Helvetica Neue, Helvetica, Arial, sans-serif
    fontSize: 2.1em
    fontWeight: 700
  heading:
    fontFamily: Helvetica Neue, Helvetica, Arial, sans-serif
    fontSize: 1.4em
    fontWeight: 700
  body:
    fontFamily: Helvetica Neue, Helvetica, Arial, sans-serif
    fontSize: 32px
    fontWeight: 400
  mono:
    fontFamily: monospace
rounded:
  sm: 4px
  md: 8px
components:
  page:
    backgroundColor: "{colors.bg-canvas}"
    textColor: "{colors.text}"
  card:
    backgroundColor: "{colors.bg-card}"
    rounded: "{rounded.md}"
  card-purple:
    backgroundColor: "{colors.purple-light}"
    textColor: "{colors.bg-canvas}"
    rounded: "{rounded.md}"
  card-cyan:
    backgroundColor: "{colors.cyan}"
    textColor: "{colors.bg-canvas}"
    rounded: "{rounded.md}"
  card-orange:
    backgroundColor: "{colors.orange}"
    textColor: "{colors.bg-canvas}"
    rounded: "{rounded.md}"
  card-red:
    backgroundColor: "{colors.red-light}"
    textColor: "{colors.bg-canvas}"
    rounded: "{rounded.md}"
---

# DESIGN.md

The visual design specification of the FOSS for Enterprise presentation deck.

## Overview

The visual design is built on the classic [Dracula](https://draculatheme.com/) color scheme: a dark purple-slate canvas (`#282a36`), crisp high-contrast foreground (`#f8f8f2`), dark slate cards (`#44475a`), and vibrant Dracula pastel accents for enterprise licensing categories and risk tiers.

The theme format is Quarto RevealJS (`theme: dracula`). Custom styles are defined in `style.css` and mirrored in the front matter above. `style.css` is strictly calibrated against the Dracula palette, so changing the base theme breaks accessibility and contrast.

## Colours

- **Canvas & Typography:**
  - `bg-canvas` (`#282a36`): Default dark canvas background for all slides.
  - `text` (`#f8f8f2`): Crisp off-white foreground text.
  - `muted` (`#6272a4`): Comments, secondary metadata, and footer text.
- **Card Backing:**
  - `bg-card` (`#44475a`): Default dark panel background for cards and comparisons.
- **Enterprise Accents & Taxonomy:**
  - `purple-light` (`#d2b5ff`): Permissive licenses and strategic open-source highlights.
  - `cyan` (`#8be9fd`): Tooling, automation, and software bill of materials (SBOM).
  - `orange` (`#ffb86c`): Weak copyleft licenses, compliance warnings, and supply-chain risks.
  - `red-light` (`#ff8585`): Strong copyleft / AGPL restrictions and critical vulnerabilities.
  - `pink-link` (`#ff9fd6`): Link color calibrated for accessible contrast across dark slides and `#44475a` cards.
- **Mermaid Backing:**
  - Mermaid edge label text is explicitly set to `#282a36` to ensure contrast against light edge boxes.

## Typography

- **Headings & Body:** Default clean sans-serif stack (`Helvetica Neue`, `Helvetica`, `Arial`, `sans-serif`).
- **Code:** Monospace stack for license identifiers (SPDX), command lines, and configurations.

## Layout & Components

- **Cards:** Fenced divs styled with `background-color: #44475a` and 8px border-radius for structured information cards.
- **Callouts:** Standard Quarto callouts styled to inherit dark Dracula palettes with increased code font size (`0.75em`).
- **Icons:** SVG mask icons (`.deck-icon`) using Font Awesome Free paths rendered in `currentColor`.

## Do's and Don'ts

- **Do** retain `theme: dracula` in `index.qmd` front matter.
- **Do** reuse the established Dracula palette tokens for cards and semantic emphasis.
- **Do** use `#ff9fd6` for links to guarantee contrast across cards and background.
- **Don't** introduce ad-hoc light backgrounds that clash with Dracula's dark presentation canvas.
