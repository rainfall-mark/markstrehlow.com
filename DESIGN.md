# Design System Strategy: High-End Editorial Minimalism

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Monograph."** 

This system moves away from the noisy, modular "web block" aesthetic and toward the quiet authority of a high-end print publication. It is designed for figures whose work speaks for itself, requiring a UI that acts as a sophisticated gallery space rather than a loud storefront. We achieve this through a relentless focus on typographic rhythm, "The No-Line Rule," and intentional verticality. Instead of horizontal carousels and busy grids, we utilize a single-column editorial flow that guides the eye through a curated narrative.

## 2. Colors
The palette is a disciplined monochrome study, using light and shadow to create structure without visual clutter.

### Surface Hierarchy & Nesting
To create a premium feel, we reject flat gray backgrounds in favor of "Tonal Layering." 
- **The "No-Line" Rule:** Never use `1px` solid borders to separate sections. Use background color shifts. A section using `surface-container-low` (#f3f3f3) sitting on the main `surface` (#f9f9f9) creates a soft, sophisticated boundary that feels architectural.
- **Nesting:** Treat the UI like stacked sheets of fine vellum. An inner card (`surface-container-lowest` / #ffffff) should sit atop a `surface-container` (#eeeeee) to create a subtle "pop" that is felt rather than seen.

### Signature Textures & Glass
- **The "Glass & Gradient" Rule:** For floating headers or navigation overlays, use Glassmorphism. Implement `surface` with a `0.8` opacity and a `20px` backdrop-blur. This ensures the background content bleeds through softly, maintaining a sense of depth.
- **Micro-Gradients:** Main CTAs should not be flat. Apply a subtle linear gradient from `primary` (#000000) to `primary-container` (#1c1b1b) to give interactive elements a "weighted" feel.

## 3. Typography
Typography is the primary architecture of this system. We pair the authoritative, high-contrast **Newsreader** (Serif) with the functional clarity of **Inter** (Sans-Serif).

*   **Display & Headlines (Newsreader):** Used for personal branding, section titles, and pull quotes. The high x-height and sharp serifs convey intellectual depth.
*   **Body & Labels (Inter):** Used for narrative text and metadata. Inter provides a neutral, modern balance to the "romantic" Serif headings.
*   **Hierarchy as Identity:** Use `display-lg` (3.5rem) for the name/hero, followed immediately by `title-md` in italics for subtitles. This creates an immediate "Editorial Header" feel common in premium journals.

## 4. Elevation & Depth
In this design system, shadows are atmospheric, not structural.

*   **The Layering Principle:** Depth is strictly managed through the surface-container tiers. Use `surface-container-high` (#e8e8e8) for secondary sidebars or contextual info to "recede" into the background.
*   **Ambient Shadows:** If an element must float (e.g., a modal or floating action button), use an ultra-diffused shadow: `box-shadow: 0 10px 40px rgba(26, 28, 28, 0.06);`. The shadow color is derived from `on-surface` (#1a1c1c), ensuring it feels like a natural lighting effect.
*   **The "Ghost Border" Fallback:** If a container requires a border for accessibility, use the `outline-variant` (#c4c7c7) at **15% opacity**. This creates a "hairline" effect that suggests a boundary without creating a hard visual stop.

## 5. Components

### Buttons
- **Primary:** Solid `primary` background. Sharp corners (`none` or `sm` roundedness). Text is `on-primary` (white), using `label-md` uppercase with `0.05em` letter spacing.
- **Tertiary (Editorial Link):** No background. Use `Newsreader` italics with a `1px` underline that sits `4px` below the baseline.

### Cards & Lists
- **Rule:** Forbid divider lines. Use `spacing-8` (2.75rem) to separate list items. 
- **Structure:** Use `surface-container-low` for card backgrounds. Hover states should trigger a shift to `surface-container-lowest`, creating a subtle "lift" through color alone.

### Inputs & Fields
- **Styling:** Use "Underline-only" inputs for a cleaner editorial look. The line should be `outline-variant` at 20%. Upon focus, the line transitions to `primary` (#000000).

### Signature Component: The "Content Ledger"
A specific pattern for this system: Use a wide vertical gutter where `label-sm` metadata (dates, categories) sits to the left of the main `body-lg` text, creating an asymmetrical, scholarly layout.

## 6. Do's and Don'ts

### Do:
- **Do** use generous whitespace. If in doubt, double the margin. Use `spacing-20` (7rem) between major sections.
- **Do** use `Newsreader` for emphasis within sans-serif body text (e.g., *italics* for book titles or key terms).
- **Do** leverage "surface-on-surface" nesting to define hierarchy.

### Don't:
- **Don't** use standard 100% opaque borders. It breaks the "high-end" feel and introduces "visual noise."
- **Don't** use heavy shadows. If you can see the shadow clearly, it is too dark.
- **Don't** use bright accent colors. The only "color" allowed is the interplay of black, white, and the subtle warmth/coolness of the gray tokens.
- **Don't** crowd the layout. This system relies on the "luxury of space."