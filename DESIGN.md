# Design System Strategy: The Travel Companion

## 1. Overview & Creative North Star
This design system is built on the Creative North Star of **"The Sunlit Concierge."** 

We are moving away from the cold, industrial grid of traditional travel apps. Instead, we embrace an editorial layout that feels like a high-end travel magazine crossed with a friendly neighborhood rental shop. We break the "template" look through **Intentional Asymmetry**: using large, offset typography and overlapping elements where images of luggage "peek" out from behind rounded containers. The goal is to make the user feel like their journey has already begun—warm, effortless, and premium.

---

## 2. Colors: Tonal Warmth
We move beyond flat yellow by using a sophisticated spectrum of gold and amber, balanced by "Soft-Black" ink tones and cream-based surfaces.

### The Palette
- **Primary Hub (#776300 / #FFD709):** Our signature "Vibrant Yellow." Use `primary` for high-impact brand moments and `primary-container` for large, welcoming interaction areas.
- **Secondary Accents (#995200):** A burnt orange/brown used to ground the yellow, providing a sense of "leather and durability" associated with quality luggage.
- **Surface Hierarchy:** We utilize the `surface-container` tiers to create depth.
    - `surface-container-lowest`: For high-priority floating cards.
    - `surface-container-low`: For secondary content areas.
    - `surface-container-high`: For sidebars or navigation drawers that need to "step forward."

### The Rules of Engagement
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Define boundaries solely through background color shifts. A `surface-container-low` card sitting on a `surface` background provides all the definition needed.
*   **The "Glass & Gradient" Rule:** To avoid a "flat" budget feel, use semi-transparent `surface-variant` colors with a 12px backdrop-blur for floating headers. Use a subtle linear gradient from `primary` to `primary-fixed-dim` on main CTA buttons to give them a tactile, "clickable" soul.
*   **Signature Textures:** For Hero sections, use a soft radial gradient: `surface-container-lowest` at the center fading into `surface-container-low` at the edges to create a subtle "spotlight" effect on our luggage products.

---

## 3. Typography: Soft Authority
We pair the playful friendliness of the brand with the structural integrity of editorial design.

*   **Display & Headlines (Plus Jakarta Sans):** Chosen for its modern, rounded geometric shapes that echo the 'Nanum Round' aesthetic but with professional polish. 
    - Use `display-lg` (3.5rem) with tighter tracking (-0.02em) for hero headlines to create a bold, "magazine cover" look.
*   **Body & Titles (Be Vietnam Pro):** A highly legible sans-serif with soft terminals.
    - `title-lg` (1.375rem) should be used for product names.
    - `body-md` (0.875rem) is the workhorse for rental terms and descriptions.

The contrast between the oversized, friendly Headlines and the clean, structured Body text conveys a brand that is "Playful yet Professional."

---

## 4. Elevation & Depth: Tonal Layering
We reject the "drop shadow" of 2010. Our depth is organic and atmospheric.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container-low` section creates a soft, natural lift.
*   **Ambient Shadows:** If a floating element (like a "Book Now" bar) requires a shadow, use a large blur (32px) at 6% opacity. The shadow color must be a tint of `on-surface` (a warm olive-black), never pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` token at 15% opacity. It should feel like a suggestion of a line, not a hard barrier.
*   **Glassmorphism:** Use `surface-tint` at 5% opacity with a `blur-md` for "sticky" navigation elements to allow the vibrant yellow brand colors to bleed through as the user scrolls.

---

## 5. Components: Soft & Intentional
Every component follows the **ROUND_SIXTEEN** (1rem) corner radius to maintain the "Soft" brand promise.

### Buttons
*   **Primary:** Background `primary-container`, text `on-primary-container`. 1rem padding (horizontal). Use `ROUND_SIXTEEN`. No borders.
*   **Secondary:** Background `secondary-container`, text `on-secondary-container`. Use for "View Details."

### Cards & Lists
*   **The "No-Divider" Rule:** Forbid 1px dividers between list items. Instead, use a `3.5` (1.2rem) vertical spacing gap.
*   **Luggage Cards:** Use `surface-container-lowest`. Product images should have a `ROUND_SIXTEEN` radius and sit slightly offset (asymmetric) within the card.

### Input Fields
*   **Style:** Filled containers using `surface-container-high` rather than outlined boxes. This makes the form feel "less like work" and more like a conversation. Focus states use a 2px `primary` bottom-bar only.

### Specialist Component: The "Travel Timeline"
*   Instead of a standard date picker, use a horizontal scroll of `chips` representing days, using `surface-container-highest` for unselected and `primary` for selected, ensuring a tactile, playful rental experience.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical white space. Allow text to breathe with large `16` (5.5rem) margins in hero sections.
*   **Do** use "Soft-Black" (`on-surface`) for text to maintain the warm, friendly vibe. Pure #000000 is too harsh.
*   **Do** overlap elements. Let a suitcase image bleed over the edge of a container to create a sense of movement.

### Don’t
*   **Don’t** use hard 90-degree corners. Everything must feel "held and hugged" (use `ROUND_SIXTEEN` or `full`).
*   **Don’t** use "Alert Red" for errors if possible. Use the `error` token (#be2d06) which is a warmer, more sophisticated clay-red that doesn't cause panic.
*   **Don’t** crowd the UI. If in doubt, add more spacing from the `10` or `12` scale. This is a premium service; it shouldn't feel cluttered like a discount warehouse.