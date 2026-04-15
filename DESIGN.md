# Design System: The Heirloom Editorial

## 1. Overview & Creative North Star
**Creative North Star: The Timeless Curator**
This design system moves beyond the digital ephemeral to mimic the tactile, high-end experience of bespoke stationery. It is built on the principle of "Intentional Stillness." We are not building a high-frequency interface; we are designing a digital sanctuary for a significant life event. 

To break the "template" look, we lean into **Editorial Asymmetry**. This means moving away from centered, boxed-in content and instead utilizing vast amounts of white space (`surface`), staggered imagery, and high-contrast typography scales. The interface should feel like a page from a high-end fashion or bridal monograph—breathtakingly simple yet deeply intentional.

---

## 2. Colors
Our palette is a dialogue between warmth and groundedness. The `surface` tokens provide a creamy, tactile foundation, while `primary` (Terracotta) and `secondary` (Deep Navy Ink) act as the ink and seal of the experience.

*   **Primary (#b35528):** Used sparingly for calls to action and focal highlights. It represents the "clay" and warmth of the union.
*   **Secondary (#14203a):** A deep "Deep Navy Ink" anchor. Use this for subtle depth and high-end accents to provide a crisp, authoritative contrast.
*   **Tertiary (#fff6d7):** A soft, parchment-inspired highlight color used for badges, subtle accents, or decorative elements.
*   **Neutral (Off-white / #fcfaf5):** This is your canvas. It is not "empty space"—it is a premium material.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to section content. Traditional "dividers" are a sign of lazy design. 
*   **Boundaries:** Define sections solely through background shifts. Transition from `surface` to `surface-container-low` or `surface-container-high` to signal a new thematic block.
*   **Signature Textures:** For high-impact elements like the "RSVP" button or "Our Story" hero, use a subtle linear gradient from `primary` (#b35528) to `primary_container`. This adds a "silk-screened" depth that flat hex codes cannot replicate.

---

## 3. Typography
The typography system is a dance between the classical (`notoSerif`) and the contemporary (`manrope`).

*   **Display & Headline (Noto Serif):** These are our "Artistic Statement" tokens. Use `display-lg` for the "R&R" monogram and names. They should feel monumental. Encourage tight letter-spacing for large headlines to create a sophisticated, editorial "logo-type" feel.
*   **Body & Labels (Manrope):** Clean, utilitarian, and breathable. These handle the logistics (dates, locations, instructions). 
*   **Hierarchy as Identity:** Use a dramatic scale jump between `display-lg` (3.5rem) and `body-md` (0.875rem). This high-contrast pairing is what separates high-end editorial from generic web layouts.

---

## 4. Elevation & Depth
In this design system, depth is organic, not mechanical.

*   **The Layering Principle:** Treat the UI as a series of stacked fine-paper sheets. 
    *   *Base:* `surface`
    *   *Cards/Sections:* `surface-container-lowest` (this creates a soft "lift" against the off-white background).
*   **Ambient Shadows:** If an element must "float" (e.g., a modal or floating action button), use a shadow tinted with `on_surface` at 4% opacity with a 32px blur. It should feel like a soft shadow cast by a physical card in natural sunlight.
*   **The "Ghost Border" Fallback:** If accessibility requires a border (e.g., input fields), use `outline_variant` at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** For the navigation bar or fixed headers, use `surface` at 80% opacity with a `20px` backdrop-blur. This allows the artistic leaf illustrations in the background to bleed through softly as the user scrolls.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` background with `on_primary` (White) text. Use `full` roundedness (pill-shaped) for a softer, romantic feel.
*   **Secondary:** `surface_container_high` background with `primary` text. No border.
*   **Interaction:** On hover, the primary button should shift to `primary_container` with a soft ambient shadow.

### Cards
*   **Construction:** Forbid dividers. Use `surface-container-lowest` for the card body and `surface-container-low` for a "header" area within the card.
*   **Padding:** Use compact spacing (`spacing: 2`) to maintain a clean, organized hierarchy without feeling overly sparse or overly dense.

### Input Fields
*   **Style:** Minimalist. Use a "bottom-line only" approach or a very faint `outline_variant` (15% opacity) box. The focus state should transition the bottom line to `secondary` (#14203a), signaling sophisticated reliability.

### Artistic Accents (Custom Component)
*   **Leaf Overlay:** Use the artistic leaf illustration as a `position: absolute` element, z-indexed behind text but above the background. Apply a slight parallax effect on scroll to give the digital page a living, breathing quality.

---

## 6. Do's and Don'ts

### Do
*   **Do use asymmetrical grids.** Place a photo 2/3rds to the left and text 1/3rd to the right, overlapping slightly.
*   **Do embrace balanced whitespace.** Utilize `spacing: 2` to ensure the editorial layout feels intentional and structured.
*   **Do use the "Deep Navy Ink" (`secondary`) for small, high-density text** like RSVP deadlines—it provides a crisp, authoritative contrast to the terracotta.

### Don't
*   **Don't use 100% black.** Use `on_surface` for all "black" text to keep the look soft and expensive.
*   **Don't use sharp 0px corners.** While we want sophisticated, the `roundedness: 1` setting ensures a subtle roundedness that prevents the design from feeling aggressive or "brutalist."
*   **Don't use standard system fonts.** Stick strictly to the Noto Serif / Manrope pairing to maintain the brand's signature "High-End Editorial" voice.