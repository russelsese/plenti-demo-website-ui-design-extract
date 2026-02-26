# Design System: Plenti (plenti.com.au)

> Extracted via Skill 01 — Design System Extraction
> Platform: **Webflow**
> Source CSS: `plenti-web.shared.57049ff23.min.css`

---

## 1. Color Palette

### Primary (Brand Navy)

| Token            | Hex       | Usage                              |
|------------------|-----------|------------------------------------|
| primary-main     | `#002861` | SVG fills, icon fills, brand color |
| primary-400      | `#002a61` | Hover variant                      |
| primary-500      | `#05244d` | Darker shade                       |
| primary-dark     | `#001845` | Deep dark                          |
| primary-darker   | `#000c2e` | Deepest dark                       |
| primary-light    | `#5393cf` | Light tint                         |
| primary-lighter  | `#c5e3f7` | Very light tint / backgrounds      |
| dark-blue-hover  | `#00142f` | Link/button hover state            |

### Secondary (Blue)

| Token          | Hex       | Usage              |
|----------------|-----------|--------------------|
| secondary-200  | `#d1dbff` | Light background   |
| secondary-300  | `#a3b7ff` | Mid tint           |
| secondary-400  | `#3c66ff` | Accent / CTA blue  |
| secondary-500  | `#0b36d2` | Hover variant      |

### Neutrals

| Token         | Hex       | Usage                          |
|---------------|-----------|--------------------------------|
| neutral-100   | `#ffffff` | White / backgrounds            |
| neutral-200   | `#f1f2f4` | Light background surfaces      |
| neutral-300   | `#dbdde1` | Borders / dividers             |
| neutral-400   | `#babec5` | Disabled / placeholder         |
| neutral-500   | `#5d656f` | Secondary text                 |
| neutral-600   | `#41474e` | Body text                      |
| neutral-700   | `#2e3238` | Strong text                    |
| neutral-800   | `#0c0d0e` | Near black / headings          |

### Semantic

| Token         | Hex       | Usage              |
|---------------|-----------|--------------------|
| danger-100    | `#fae4e4` | Error background   |
| danger-200    | `#eeafaf` | Error border       |
| danger-300    | `#9e0202` | Error text / icon  |
| info-100      | `#cfe0f7` | Info background    |
| info-200      | `#99b3d7` | Info border        |
| info-300      | `#0045a5` | Info text / icon   |
| positive-100  | `#a8ebbc` | Success background |
| positive-200  | `#367057` | Success border     |
| positive-300  | `#005e0b` | Success text       |
| warning-100   | `#ffd9b9` | Warning background |
| warning-200   | `#b34300` | Warning border     |
| warning-300   | `#993100` | Warning text       |

### Utility / Brand Accents

| Name          | Hex       | Notes                     |
|---------------|-----------|---------------------------|
| sky           | `#dae5f0` | Light blue tint           |
| sky-60        | `#e9eff6` |                           |
| sky-30        | `#f4f7fb` |                           |
| pistachio     | `#a6e1c8` | Green tint                |
| pistachio-60  | `#caedde` |                           |
| pistachio-30  | `#e4f6ef` |                           |
| pistachio-120 | `#7ad3ad` | Deeper green              |
| peach         | `#ffbaa1` | Warm orange-pink          |
| peach-60      | `#ffd6c7` |                           |
| peach-30      | `#ffeae3` |                           |
| gold          | `#f6c042` | Highlight / star ratings  |
| red           | `#ff2c52` | Alert / badge             |
| red-hover     | `#e6284a` |                           |

---

## 2. Typography

### Font Families

| Variable      | Stack                          | Usage                  |
|---------------|--------------------------------|------------------------|
| Garnett       | `Garnett, Arial, sans-serif`   | Primary / headings     |
| Satoshi       | `Satoshi, Arial, sans-serif`   | Secondary / UI text    |
| Inter         | `Inter`                        | Body fallback          |

**Self-hosted via Webflow CDN:**
- **Garnett**: Light (300), Regular (400), Medium (500)
- **Satoshi**: Light (300), Regular (400), Medium (500), Bold (700), Black (900)

### Font Size Scale

| Token | px   | Responsive (clamp)                                      |
|-------|------|---------------------------------------------------------|
| 25    | 12px | —                                                       |
| 50    | 14px | `clamp(.875rem, .19vw + .83rem, 1rem)`                  |
| 75    | 15px | —                                                       |
| 100   | 16px | `clamp(1rem, .19vw + .96rem, 1.125rem)`                 |
| 200   | 18px | `clamp(1.125rem, .19vw + 1.08rem, 1.25rem)`             |
| 250   | 20px | `clamp(1.25rem, .38vw + 1.16rem, 1.5rem)`               |
| 300   | 24px | `clamp(1.5rem, .75vw + 1.32rem, 2rem)`                  |
| 400   | 28px | `clamp(1.75rem, 1.13vw + 1.49rem, 2.5rem)`              |
| 500   | 32px | `clamp(2rem, 1.5vw + 1.65rem, 3rem)`                    |
| 600   | 40px | `clamp(2.5rem, 1.5vw + 2.15rem, 3.5rem)`                |
| 700   | 48px | `clamp(3rem, 2.25vw + 2.47rem, 4.5rem)`                 |
| 800   | 56px | —                                                       |
| 900   | 72px | —                                                       |

### Font Weights

| Name      | Value |
|-----------|-------|
| Light     | 300   |
| Regular   | 400   |
| Medium    | 500   |
| Semi-bold | 600   |
| Bold      | 700   |
| Black     | 900   |

### Line Heights

| Token | Value |
|-------|-------|
| 100   | 22px  |
| 200   | 24px  |
| 300   | 28px  |
| 400   | 32px  |
| 500   | 34px  |
| 600   | 40px  |
| 700   | 48px  |
| 800   | 54px  |
| 900   | 62px  |

### Letter Spacing

| Token | Value   | Direction |
|-------|---------|-----------|
| 50    | +.12px  | Positive  |
| 100   | +.09px  | Positive  |
| 200   | +.08px  | Positive  |
| 300   | -.08px  | Negative  |
| 400   | -.17px  | Negative  |
| 500   | -.36px  | Negative  |
| 600   | -.42px  | Negative  |
| 700   | -.64px  | Negative  |
| 800   | -.72px  | Negative  |
| 900   | -.96px  | Negative  |

> Pattern: small text uses positive letter-spacing; large display text uses negative tracking.

---

## 3. Spacing Scale

**Base unit: 4px**

| Step | Value |
|------|-------|
| 1    | 4px   |
| 2    | 8px   |
| 3    | 12px  |
| 4    | 16px  |
| 5    | 20px  |
| 6    | 24px  |
| 8    | 32px  |
| 10   | 40px  |
| 12   | 48px  |
| 14   | 56px  |
| 16   | 64px  |

**Rem equivalents also used:** `0.25rem`, `0.5rem`, `0.75rem`, `1rem`, `1.25rem`, `1.5rem`, `2rem`, `2.5rem`, `2.75rem`, `3.5rem`

**Section vertical padding:** typically `2rem` / `4rem` with mobile variants (`2rem-on-mobile`, `4rem-on-mobile`)

---

## 4. Border Radius

| Value   | Usage context              |
|---------|----------------------------|
| `0px`   | Sharp / reset              |
| `4px`   | Small elements / tags      |
| `8px`   | Inputs, small cards        |
| `12px`  | Cards, panels              |
| `16px`  | Larger cards               |
| `24px`  | Feature sections           |
| `32px`  | Pill-shaped containers     |
| `40px`  | Large pill containers      |
| `100px` | Fully rounded / pill       |
| `50%`   | Circular icons / avatars   |
| `100%`  | Circle (same as 50% usage) |

> SVG `rx="14"` used on circular button elements in the calculator.

---

## 5. Shadows / Elevation

| Level  | Value                              | Usage          |
|--------|------------------------------------|----------------|
| 100    | `0px 0px 2px 0px`                  | Subtle / focus |
| 200    | `0px 4px 8px 0px`                  | Card resting   |
| 300    | `0px 12px 24px -4px`               | Card hover     |
| 400    | `-20px 20px 40px -4px`             | Modal / drawer |
| 500    | `-40px 40px 80px -8px`             | Large overlay  |
| 600    | `0px 0px 40px -4px`                | Glow / ring    |
| 700    | `0px 24px 48px 0px`                | Hero / feature |

**Utility shadows:**
- `0 0 0 1px #0000001a, 0 1px 3px #0000001a` — border + lift
- `0 0 3px #3336` — subtle glow

---

## 6. Layout & Grid

### Container

| Property   | Value  |
|------------|--------|
| Max-width  | `940px` (Webflow `w-container`) |
| Max-width (legacy) | `82rem` / `83rem` (navigation) |
| Tablet max | `728px` |

### Breakpoints

| Label | Value  | System     |
|-------|--------|------------|
| xs    | 320px  | Custom     |
| s     | 480px  | Custom     |
| sm    | 479px  | Webflow    |
| md    | 640px  | Custom     |
| md    | 767px  | Webflow    |
| lg    | 991px  | Webflow    |
| lg    | 1024px | Custom     |
| xl    | 1440px | Custom     |

### Layout Primitives

- `w-layout-blockcontainer` — block container
- `w-layout-hflex` — horizontal flex row
- `w-layout-vflex` — vertical flex column
- `w-layout-grid` — CSS grid
- `w-container` — max-width centered container

### Section Structure

Each page section follows this pattern:
```
<section class="legacy_page_section [variant]">
  <div class="legacy_page_container">
    <div class="legacy_container">
      [content]
    </div>
  </div>
</section>
```

---

## 7. Components

### Navigation

- **Desktop**: `legacy_desktop_nav_component`
  - Logo: `legacy_nav_logo` → `Plenti_Logo_Navy.svg`
  - Left links: Borrow, Invest
  - Right: Log In dropdown
- **Mobile**: `legacy_mobile_nav` with hamburger toggle `legacy_mobile_nav_button`
- Dropdown: `legacy_nav_dropdown_container` → `legacy_nav_dropdown_pages` → `legacy_nav_dropdown_item`

### Hero / Banner

- Layout: `legacy_hero_two_col` (text left, media right)
- Text: `legacy_hero_text_block w-richtext`
- Rate display: `legacy_hero_rate` → `legacy_hero_rate_lockup` (left/right) → `legacy_hero_rate_number` + `legacy_hero_rate_pa`
- CTA: `legacy_floater_cta w-button` — "Get your rate"
- Floating CTA block: `legacy_get_rate_floater_component`

### Buttons

| Class                            | Variant          |
|----------------------------------|------------------|
| `legacy_floater_cta w-button`    | Primary CTA      |
| `legacy_generic_button w-button` | Generic primary  |
| `legacy_calculator_result_button w-button` | Form submit |
| `legacy_comparison_tab w-button` | Tab (inactive)   |
| `legacy_comparison_tab selected w-button` | Tab (active) |
| SVG icon button (28×28)          | Icon-only        |

**Icon button style:** `width:28px; height:28px; padding:0; background:none;`

### Cards

**Loan type / navigation card:**
- `home_nav_cards card-mobile`
- Contains: SVG icon + title + subtitle
- Variants: `home-navigation`, `why-choose-plenti`

**Article card:**
- `legacy_articles_list_card w-inline-block`
- Contains: image + title (line-clamp-2) + description

**Feature card (Why Choose Plenti):**
- Titles: "Great Rates", "Flexible loans", "Award winning", "Speedy process"

### Accordion

```
.accordion-wrapper
  .accordion-header
    .accordion-heading   ← visible label
    .accordion-caret     ← SVG chevron toggle
  .accordion-body
    .accordion_body_text.w-richtext
```

- Data attrs: `data-plt-component="accordion"`, `data-plt-accordion="open-first"`

### Calculator (Repayment)

```
.legacy_calculator_field
  .legacy_calculator_field_label  ← <strong> label
  .legacy_calculator_input.w-embed
    <input class="plt-no-selection" maxlength="7" />
  .legacy_calculator_button_container
    <button data-plt-form-btn="inc 500">  ← +$500
    <button data-plt-form-btn="inc 1">    ← +$1
```

- Fields: Loan amount, Loan term, Credit history
- Result: `legacy_calculator_result_payment` + `legacy_calculator_result_button w-button`
- Input max-width: `8rem`, centered text, no border/outline

### Footer

```
.legacy_page_section.footer_section
  .legacy_footer_column (×N)
    .legacy_footer_link_header   ← column title
    .legacy_footer_link_grid     ← w-dyn-items list
  .legacy_footer_social_icon (LinkedIn, Facebook, YouTube, Apple, Google Play)
  .legacy_footer_bottom_links
    .legacy_footer_compliance-right  ← © 2025 Plenti Pty Limited
```

**Footer link columns:** Loan Types, Investing, Learn

---

## 8. Iconography

- **All icons are inline SVGs** — no external icon library (not FontAwesome etc.)
- Custom icon naming convention: `[name]_icon_legacy` (e.g. `chevron-right_icon_legacy`, `car_icon_legacy`)
- Icon sizes: `18×18`, `20×20`, `28×28`, `32×32`, `48×48`
- ViewBox sizes: `0 0 24 24`, `0 0 28 28`, `0 0 48 48`
- Colors: `fill="#002861"` (navy on light bg), `fill="#FFF"` (white on dark bg), `fill="currentColor"` (inherits)
- Icon classes: `svg_icon_36`, `svg_icon_48`, `svg_icon_60`
- Webflow icon font: `webflow-icons` (base64 TTF, internal use only)

---

## 9. Content Structure

### Page Section Order (index.html)
1. Navigation
2. Loan type cards (Personal, Car, Renovation, Debt consolidation, Wedding, Travel, Invest, Calculator)
3. Stats counter ("$7b+ funded", "27,000+ investors", "5,419 5-star reviews")
4. Why Choose Plenti (Great Rates, Flexible loans, Award winning, Speedy process)
5. Testimonials ("A 5-star experience from idea to reality")
6. Rate comparison table (Plenti vs ANZ, CommBank, NAB, Westpac)
7. Floating CTA ("Get your personalised rate")
8. Footer + Accordion disclaimer

### CTA Copy Patterns

| CTA Text                                | Type      |
|-----------------------------------------|-----------|
| "Get your rate"                         | Primary   |
| "Apply in 10 minutes"                   | Secondary |
| "Learn more"                            | Tertiary  |
| "Compare Loans"                         | Section   |
| "See how our rates stack up"            | Section heading CTA |

### Copy Tone
- **Conversational + aspirational**: "Make your big ideas a reality"
- **Second person**: "you could get your funds", "your personalised rate"
- **Speed emphasis**: "Apply in 10 minutes", "funds as soon as the next day"
- **Trust signals**: star ratings, dollar amounts, investor counts

---

## 10. Technical Notes

| Property       | Value                                |
|----------------|--------------------------------------|
| Platform       | Webflow                              |
| CSS file       | `plenti-web.shared.57049ff23.min.css` |
| Font hosting   | Webflow CDN (self-hosted)            |
| Analytics      | Google Analytics (G-CWNR6B7STD)      |
| Tracking       | Facebook Pixel, Datadog, Customer.io |
| Class prefix   | `legacy_*`, `plt-*`, `home_*`        |
| Data attrs     | `data-plt-*`, `data-wf--*`           |
| Last published | Thu Feb 26 2026                      |
