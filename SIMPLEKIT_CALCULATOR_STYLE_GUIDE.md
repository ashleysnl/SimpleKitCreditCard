# SimpleKit Calculator Style Guide

Use this guide when generating or refining a SimpleKit calculator inside a ChatGPT Project. It is based on the current SimpleKit starter repo structure and should keep new calculators visually aligned with the existing SimpleKit pattern.

## Purpose

Build a browser-based calculator that feels like a polished SimpleKit tool:

- clean, calm, editorial, and trustworthy
- lightweight and static-site friendly
- easy to scan on desktop and mobile
- structured around a strong hero, a clear input panel, and obvious result cards
- compatible with the shared SimpleKit shell loaded from `https://core.simplekit.app`

## Non-Negotiables

- Keep the shared shell integration:
  - `window.SimpleKitPage`
  - `data-simplekit-header`
  - `data-simplekit-support`
  - `data-simplekit-footer`
  - `https://core.simplekit.app/core.css`
  - `https://core.simplekit.app/core.js`
- Keep the Google Analytics snippet in the document head unless SimpleKit changes tracking globally.
- Assume no build step is required by default.
- Favor semantic HTML, accessible labels, and keyboard-friendly controls.
- Keep the page static-first. Client-side JavaScript should enhance the tool, not require a framework.

## Brand Feel

The calculator should feel:

- trustworthy, not flashy
- premium, but still practical
- modern, but not sterile
- content-led, not dashboard-heavy

Avoid:

- harsh black-and-white contrast
- overly playful illustrations
- enterprise SaaS dashboard styling
- cramped forms
- neon accents or loud gradients
- generic “AI app” styling

## Visual Direction

### Color System

Use this starter palette as the default foundation:

- `--starter-ink: #18263a`
- `--starter-muted: #5e7087`
- `--starter-line: rgba(24, 38, 58, 0.12)`
- `--starter-surface: rgba(255, 255, 255, 0.95)`
- `--starter-surface-soft: rgba(255, 255, 255, 0.82)`
- `--starter-brand: #0f6abf`
- `--starter-brand-2: #13a39a`
- `--starter-brand-deep: #0b345f`
- `--starter-accent: #f08a38`

Use color roles this way:

- ink for headings, body text, and high-importance labels
- muted for supporting copy and helper text
- brand blue and teal for key actions, gradients, and section identity
- accent orange for focus states or small emphasis only

### Backgrounds

Prefer layered soft backgrounds over flat fills:

- subtle radial gradients
- pale blue to off-white page washes
- white or near-white panels on top

Default page background pattern:

- radial tint in one corner
- second radial tint on the opposite side
- soft vertical linear gradient underneath

### Typography

Use a contrast between editorial headings and practical UI text:

- headings: `"Iowan Old Style", "Baskerville", "Georgia", serif`
- body/UI: inherit from the shared shell or system default

Typography rules:

- large serif hero heading
- compact uppercase kickers with heavy weight and letter spacing
- plain readable paragraph text
- avoid decorative display fonts

### Shape Language

Use rounded corners generously:

- hero: `28px`
- main panels: `20px`
- inner cards: `18px`
- inputs: `14px`
- pill buttons: `999px`

The UI should feel soft and approachable, not sharp-edged.

### Shadow and Depth

Use soft depth, not dramatic elevation:

- hero shadow: `0 24px 54px rgba(16, 33, 58, 0.08)`
- card/panel shadow: light and diffuse

Depth should separate layers gently, especially between:

- page background
- hero
- content panels
- result cards

## Layout Pattern

Structure every calculator with this overall flow:

1. Shared SimpleKit header mount
2. Hero section
3. Intro or trust panel
4. Main calculator section
5. Results section
6. Optional help/methodology section
7. Shared support mount
8. Shared footer mount

### Hero

The hero should include:

- eyebrow/kicker
- clear calculator title
- one-sentence subtitle
- one short proof/trust paragraph
- primary CTA
- secondary CTA
- small trust row or summary chips
- optional side highlight card

Hero layout:

- two-column on desktop
- single-column below `900px`
- white text on a blue-to-teal gradient

### Main Calculator Area

Use a two-column layout:

- left: form/input card
- right: results stack

Desktop behavior:

- input column slightly narrower than results column
- both aligned to the top

Mobile behavior:

- collapse to one column
- keep the input card above results

### Panels

All major sections should be wrapped in a panel style:

- light border
- white or translucent white surface
- rounded corners
- soft shadow
- internal padding around `18px` to `22px`

## Component Rules

### Section Kickers

Use small uppercase labels for section framing:

- bold
- tight
- letter-spaced
- blue by default inside white panels
- slightly translucent white inside dark hero areas

Examples:

- `Input Section`
- `Results`
- `Methodology`
- `Build Notes`

### Buttons

Use three button tiers:

- primary: blue/teal gradient with white text
- secondary on dark backgrounds: translucent white with white text
- tertiary/panel button: white with border and dark text

Button rules:

- minimum touch height `44px`
- pill radius
- slight hover lift
- no oversized shadows
- clear focus ring using the orange accent tint

### Form Fields

Inputs should be simple and calm:

- full width
- `12px 14px` padding
- white background
- soft border
- rounded corners
- visible label above every field

Forms should use:

- a grid with 2 columns on desktop when appropriate
- 1 column on mobile
- grouped cards for related inputs
- short helper copy only where it reduces confusion

Avoid:

- placeholder-only labeling
- dense inline forms
- long unbroken stacks with no grouping

### Result Cards

Primary outputs should appear in a grid of cards.

Result card pattern:

- rounded card
- thin border
- pale tinted background wash
- small uppercase label
- strong headline value
- short supporting sentence

Good result card content:

- main number
- comparison
- summary statement
- confidence note
- assumption reminder

### Status / Summary Banner

Use a top results status area when helpful:

- short summary sentence
- optional bold label
- soft blue/teal tinted background
- polite `aria-live` region for updates

### Info Cards

If the calculator needs explanation, use a 3-card info grid for:

- how to use it
- what assumptions it makes
- when the result is most useful

## Spacing System

Use relaxed spacing. Default rhythm should feel airy, not compact.

Recommended values from the starter:

- between page sections: `18px`
- panel padding: `22px`
- inner card padding: `16px` to `18px`
- form grid gaps: `12px` to `14px`
- row/button gaps: `8px` to `10px`

## Responsive Rules

At widths below `900px`:

- convert all multi-column content grids to one column
- stack panel headers vertically
- stack form toolbar actions naturally

At widths below `640px`:

- reduce outer page margins
- keep panel padding around `18px`
- preserve readable tap targets and card spacing

Mobile priorities:

- form first
- result summary second
- extra explanation later

## Content Style

Write copy in a SimpleKit voice:

- plain-English
- helpful
- calm
- specific
- concise

Preferred style:

- “Estimate your monthly payment”
- “Adjust the assumptions to compare scenarios”
- “This result is a planning estimate, not financial advice”

Avoid:

- hype language
- jargon-heavy copy
- robotic feature descriptions
- long blocks of explanatory text above the calculator

## Calculator UX Rules

For a SimpleKit calculator, ChatGPT should generate:

- a clear primary question near the top
- obvious default values
- instant recalculation on input/change when feasible
- a reset action if the form is non-trivial
- share/copy-link support only if it is genuinely useful
- URL parameter syncing when sharing state is valuable

When there are assumptions:

- surface them near the results
- do not bury them in footnotes only

When there is one main answer:

- show it first
- support it with 2 to 5 secondary cards

## Accessibility Rules

- Include a skip link to the main content.
- Use semantic landmarks: `header`, `main`, `section`, `aside`, `footer` mount areas.
- Pair every input with a visible text label.
- Ensure `:focus-visible` states are clear.
- Use `aria-live="polite"` for dynamic result summaries.
- Keep sufficient contrast for text, borders, and controls.
- Do not rely on color alone to communicate meaning.

## Implementation Pattern

Keep the repo structure simple:

```text
/
  index.html
  assets/
    css/
      styles.css
    js/
      app.js
```

Expected responsibilities:

- `index.html`: structure, metadata, shell mount points, tool content
- `assets/css/styles.css`: local tool styling only
- `assets/js/app.js`: form state, calculation logic, rendering, URL sync, share/reset helpers

JavaScript style expectations:

- small, readable functions
- no framework requirement
- sanitize dynamic HTML output when rendering strings
- keep state handling straightforward
- bind form `input` and `change` events

## SEO and Metadata

Each calculator should update:

- page title
- meta description
- canonical URL
- Open Graph title/description/url
- Twitter title/description
- JSON-LD
- visible hero title and intro copy

Metadata and on-page copy should match closely.

## Prompt Block For ChatGPT Project

Paste or adapt this into your ChatGPT Project instructions:

```text
Build this as a SimpleKit calculator using the existing SimpleKit starter conventions.

Design requirements:
- Keep the shared SimpleKit shell integration and static-site structure.
- Use a polished editorial calculator layout with:
  - a gradient hero
  - rounded white panels
  - a two-column calculator/results section on desktop
  - stacked single-column layout on mobile
- Use this palette as the base:
  - ink #18263a
  - muted #5e7087
  - brand #0f6abf
  - brand-2 #13a39a
  - brand-deep #0b345f
  - accent #f08a38
- Use serif display headings like Iowan Old Style/Baskerville/Georgia and practical readable UI text elsewhere.
- Use pill buttons, soft borders, light shadows, and generous spacing.
- Prefer small uppercase section kickers, strong result cards, and concise helper copy.
- Keep the experience trustworthy, calm, and premium, not flashy or dashboard-like.

Code requirements:
- Keep HTML semantic and accessible.
- Keep JavaScript framework-free unless explicitly requested.
- Use clear form labels, live-updating results where appropriate, and `aria-live="polite"` for dynamic result summaries.
- Keep CSS modular and tool-specific in `assets/css/styles.css`.
- Keep calculations and UI rendering in `assets/js/app.js`.

Avoid:
- generic SaaS dashboard styling
- cramped spacing
- harsh black/white contrast
- purple-heavy AI-style aesthetics
- unnecessary frameworks
```

## Final Check

Before approving a generated SimpleKit calculator, confirm that it:

- looks like a SimpleKit tool, not a generic web app
- preserves shared shell integration
- has a strong hero, clean inputs, and obvious result hierarchy
- works well at mobile widths
- uses consistent tokens, spacing, and rounded surfaces
- keeps metadata and visible copy aligned
- stays accessible and static-friendly
