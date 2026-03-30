```markdown
# Design System Specification: Premier Garden Living

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Editorial"**

This design system is crafted to transcend the standard e-commerce experience, moving into the realm of high-end architectural journalism. For the Lugarde range, we are not just selling garden buildings; we are curating a lifestyle of heritage and precision. 

To achieve this, the system breaks the "template" look by utilizing **Intentional Asymmetry**. We move away from rigid, centered grids in favor of layouts where high-quality imagery sits slightly off-axis, overlapping with sophisticated serif typography. The interface should feel like a premium physical brochure—spacious, tactile, and authoritative. Every element is designed to breathe, utilizing an expansive white-space strategy to denote luxury and expertise.

---

## 2. Colors & Surface Philosophy

The palette blends the structural authority of professional trade (Deep Blues/Charcoal) with the warmth of high-end timber and nature.

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for sectioning. Definition between content blocks must be achieved through **Background Color Shifts**. For example, a section using `surface-container-low` should transition directly into a `surface` background. This creates a seamless, modern flow that feels engineered rather than "boxed in."

### Surface Hierarchy & Tonal Layering
The UI is treated as a series of stacked, premium materials. Use the `surface-container` tiers to define depth:
*   **Base:** `surface` (#f9f9fc) for the primary canvas.
*   **Sections:** `surface-container-low` (#f3f3f6) for secondary content areas.
*   **Elevated Components:** `surface-container-lowest` (#ffffff) for cards and interactive modules to create a "lifted" appearance without heavy shadows.

### The "Glass & Signature Texture" Rule
To add "soul" to the digital interface:
*   **Glassmorphism:** Use semi-transparent `surface` colors with a `backdrop-blur` (e.g., 20px) for floating navigation bars and modal overlays. This allows the lush greens of product photography to bleed through the UI subtly.
*   **Signature Gradients:** For primary CTAs and Hero backgrounds, use a subtle linear gradient from `primary` (#051927) to `primary-container` (#1b2e3c) at a 135-degree angle. This mimics the sheen of high-quality architectural steel or dark stained wood.

---

## 3. Typography

The typography strategy relies on the tension between a heritage-focused Serif and a high-performance Sans-Serif.

*   **Display & Headlines (Noto Serif):** Used for storytelling and brand statements. The serif denotes the "Quality-focused" heritage of the Lugarde range. Use `display-lg` (3.5rem) for hero statements with tight letter-spacing (-0.02em) to evoke a premium editorial feel.
*   **Body & Technical (Manrope):** A clean, modern sans-serif used for technical specifications and long-form descriptions. `body-lg` (1rem) should be the standard for readability, ensuring the expert tone is maintained through clarity.
*   **Labels (Manrope):** Use `label-md` (0.75rem) in all-caps with increased letter-spacing (0.1em) for category tags or "Technical Specs" headers to mimic architectural blueprints.

---

## 4. Elevation & Depth

We reject the "heavy shadow" aesthetic of the early web. Depth in this system is whispered, not shouted.

*   **The Layering Principle:** Place a `surface-container-lowest` card on top of a `surface-container-low` section. The minute difference in hex code provides enough contrast to signify hierarchy without visual noise.
*   **Ambient Shadows:** If a floating element (like a "Configure" button) requires a shadow, use an extra-diffused blur: `box-shadow: 0 20px 40px rgba(9, 29, 43, 0.06)`. The shadow color is a tinted version of `on-primary-fixed`, making it look like a natural environmental reflection.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline-variant` token at **20% opacity**. Never use 100% opaque lines.

---

## 5. Components

### Buttons: The "Precision" Set
*   **Primary:** Background: `primary` (#051927), Text: `on-primary` (#ffffff). Shape: `md` (0.375rem). Use a subtle 1px inner glow (white at 10% opacity) on the top edge to simulate a beveled, premium finish.
*   **Secondary:** Background: `secondary-container` (#d4e4d0), Text: `on-secondary-container` (#586757). Use this for "Explore Range" or "View Specs."
*   **Tertiary:** No background. Text: `primary`. Use for "Read More" with an animated underline that grows from the center on hover.

### Cards & Image Containers
*   **Rule:** Forbid the use of divider lines. 
*   **Separation:** Use `spacing-6` (2rem) as a minimum gutter between content blocks.
*   **Imagery:** Apply a `sm` (0.125rem) border radius to high-quality images. This maintains a sharp, architectural edge while softening the "raw" photo look.

### Input Fields & Selectors
*   **Field Style:** Use `surface-container-high` for the input background. Upon focus, transition to `surface-container-lowest` with a 1px "Ghost Border" using the `tertiary` (Gold/Champagne) color to signal luxury and attention.

### Architecture-Specific Components
*   **The Technical Drawer:** A slide-out panel for garden building specs (dimensions, timber type). Use a `backdrop-blur` of 30px over the main content to keep the user focused while maintaining the context of the product image.
*   **Material Swatches:** Small circular chips using `tertiary-fixed` (#ffdea5) highlights to denote premium wood finishes or metal hardware options.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical layouts where text overlaps 10% of an image to create an "Editorial" feel.
*   **Do** utilize `spacing-16` (5.5rem) or `spacing-20` (7rem) for vertical padding between major sections to emphasize the "Spacious" luxury.
*   **Do** use `tertiary` (Gold/Champagne) sparingly for high-value highlights like "Handcrafted" or "British Made" badges.

### Don’t
*   **Don't** use pure black (#000000). Always use `primary` (#051927) for text to maintain a sophisticated, deep-blue depth.
*   **Don't** use standard 1px dividers between list items. Use background color alternating or increased vertical whitespace.
*   **Don't** use high-intensity animations. All transitions (hover, fade, slide) should use a `cubic-bezier(0.4, 0, 0.2, 1)` easing over 300ms–500ms to feel deliberate and calm.

---
**Note to Designers:** This system relies on your restraint. The luxury is found in what you leave out—avoid the temptation to clutter the interface with "utility" elements. Every pixel should feel like it was placed by an architect.```