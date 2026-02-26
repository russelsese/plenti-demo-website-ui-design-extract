# Skill 01: Design System Extraction

Extract the complete visual design system from a downloaded website's HTML and CSS files.

---

## Goal

Produce a structured design token document that captures all visual identity decisions,
enabling faithful reproduction of the site's look and feel.

---

## Inputs

- Downloaded site files (HTML, CSS, JS)
- Target URL or page(s) to analyze

---

## Steps

### 1. Color Palette

- Search CSS for custom properties: `grep -r "color" --include="*.css"`
- Look for `:root` block — design tokens are usually defined here
- Categorize each color found:
  - **Primary** — main brand color (buttons, links, highlights)
  - **Secondary** — supporting brand color
  - **Accent** — call-to-action or emphasis color
  - **Neutrals** — grays used for text, borders, backgrounds
  - **Semantic** — success (green), error (red), warning (yellow), info (blue)

### 2. Typography

- Search for `@font-face` or `font-family` declarations
- Identify the font stack for body and headings (Google Fonts? Adobe? Self-hosted?)
- Document for each text style (h1–h6, body, caption, label, button):
  - `font-family`
  - `font-weight`
  - `font-size` (and responsive variants)
  - `line-height`
  - `letter-spacing`
  - `text-transform` (uppercase labels?)

### 3. Spacing Scale

- Look for spacing tokens in `:root` (e.g. `--spacing-sm`, `--gap-4`)
- Identify the base unit — typically `4px` or `8px`
- Check padding/margin values on repeated elements (cards, sections, containers)
- Map out the scale (e.g. 4, 8, 12, 16, 24, 32, 48, 64, 96px)

### 4. Border Radius

- Search for `border-radius` values across components
- Note where each radius is applied:
  - Buttons
  - Cards / panels
  - Inputs / form fields
  - Badges / tags
  - Images

### 5. Shadows / Elevation

- Search for `box-shadow` declarations
- Document each unique shadow value and what component uses it
- Note any layering pattern (e.g. card hover elevates shadow)

### 6. Iconography

- Look for `<svg>` elements — are they inline or referenced?
- Check for icon font links (`font-awesome`, `remixicon`, etc.) in `<link>` tags
- Check for sprite sheets or icon component imports in JS
- Note icon sizes and stroke widths used

---

## 2. Layout & Grid

### Grid System

- Inspect the main container class — note `max-width` and `padding`
- Identify the column system (CSS Grid or Flexbox-based)
- Count columns used in multi-column sections
- Note gutter widths between columns

### Breakpoints

- Search CSS for `@media` queries
- List each breakpoint value and label it (xs, sm, md, lg, xl)
- For each breakpoint, note how the grid/layout changes

### Section Structure

- Identify the repeating section pattern (e.g. `<section>`, `<div class="container">`)
- Note typical section anatomy: background color, top/bottom padding, inner max-width
- Map page into named sections (hero, features, testimonials, CTA, footer)

### Whitespace Patterns

- Measure vertical spacing between sections (padding-top/bottom on section elements)
- Note whether spacing is consistent or varies by section type

---

## 3. Components

### Navigation

- Document header HTML structure
- Note: sticky behavior, transparent-on-scroll, background color on scroll
- Mobile menu: hamburger icon, drawer vs. dropdown, animation
- Active/current link styling

### Hero / Banner

- Image treatment: full-bleed, contained, background-image vs `<img>`
- Text overlay positioning and contrast handling
- CTA button placement and wording

### Cards

- Card anatomy: image, tag, title, body, CTA
- Image aspect ratio (16:9, 4:3, 1:1?)
- Hover state: shadow, scale, border, overlay
- Card grid: how many columns at each breakpoint

### Buttons

- Variants: primary, secondary, ghost/outline, link-style
- Sizes: sm, md, lg
- States: default, hover, focus, active, disabled, loading
- Icon usage: left icon, right icon, icon-only

### Forms

- Input field styling: border, background, focus ring
- Label positioning: above, floating, inline
- Validation: error message placement, error border color, success indicator
- Placeholder text style

### Footer

- Column count and link groupings
- Social media icons
- Legal/copyright row
- Newsletter signup (if present)

---

## 4. Content Structure

### Page Hierarchy

- Map heading usage across the page (one H1?, multiple H2s?, H3 for cards?)
- Note how subheadings and body copy relate visually (size contrast, weight contrast)

### Copy Tone

- Identify voice: formal, conversational, friendly, authoritative
- Note use of second person ("you", "your")
- List power words and emotional triggers used in CTAs

### CTA Strategy

- List every CTA on the page with its wording and placement
- Note primary vs. secondary CTA hierarchy
- Identify repeated CTAs and where they appear in the page flow

---

## 5. Interaction & Behavior

### Animations

- Scroll-triggered reveals: which elements animate in on scroll?
- Hover transitions: duration and easing (e.g. `transition: 0.2s ease`)
- Page load animations

### Interactive States

- Document hover, focus, and active states for: links, buttons, cards, nav items
- Check `:focus-visible` styling for accessibility

### Dynamic Components

- List all interactive components: calculators, sliders, accordions, tabs, modals
- Note the library used (if any) — Alpine.js, React, Stimulus, vanilla JS
- Document the user interaction flow for each

---

## 6. Assets

### Images

- Photography style: lifestyle, product, abstract, illustrated
- Aspect ratios used across the site
- Image treatment: rounded corners, drop shadows, color overlays, duotone
- File formats: WebP, JPEG, PNG, SVG

### Illustrations / Graphics

- Style: flat, isometric, line art, 3D
- Color palette alignment with brand colors
- Reuse patterns (same illustration style across pages?)

### Logos

- Primary logo formats: horizontal, stacked, icon-only
- Usage contexts: header (which variant?), footer, favicon
- Color variants: full color, white, dark

---

## Output Format

Save results to `docs/design-system.md` using this structure:

```md
# Design System: [Site Name]

## Colors
| Token        | Value   | Usage          |
|--------------|---------|----------------|
| Primary      | #XXXXXX | Buttons, links |
| ...          |         |                |

## Typography
| Style   | Font     | Weight | Size | Line Height |
|---------|----------|--------|------|-------------|
| H1      | ...      | 700    | 48px | 1.2         |
| ...     |          |        |      |             |

## Spacing Scale
Base unit: Xpx
Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96

## Border Radius
| Context | Value |
|---------|-------|
| Button  | 8px   |
| ...     |       |

## Shadows
...

## Breakpoints
| Label | Value  |
|-------|--------|
| sm    | 640px  |
| ...   |        |
```
