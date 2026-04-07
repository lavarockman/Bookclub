# Design System Strategy: The Intellectual Catalyst

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Curated Sanctum."** 

Standard dashboards feel like utilities; this system must feel like a high-end, private library merged with a modern productivity suite. We are moving away from the "SaaS-default" look by embracing **Editorial Asymmetry**. By utilizing a generous `display-lg` scale and overlapping layout elements, we create a sense of momentum and growth. We prioritize "breathable" layouts where the negative space is as intentional as the content itself. The goal is to make the user feel like they are entering a premium space for self-actualization, not just another task manager.

## 2. Colors & Surface Philosophy
This palette leverages deep, authoritative blues (`primary`) to ground the user, while using vibrant greens (`tertiary`) and oranges (`secondary`) to signify growth and kinetic energy.

### The "No-Line" Rule
Standard 1px borders are strictly prohibited for sectioning. They create visual noise and "trap" content. Instead, define boundaries through **Tonal Transitions**. Use `surface` as your base and `surface-container-low` for sidebar navigation. A section’s end is marked by the start of a new background color, not a line.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of premium cardstock.
*   **Base Layer:** `surface` (#f7f9fb)
*   **Content Sections:** `surface-container-low` (#f2f4f6)
*   **Active Interaction Cards:** `surface-container-lowest` (#ffffff)
*   **Navigation/Utility Sidebars:** `surface-container` (#eceef0)

### The "Glass & Gradient" Rule
To inject "soul" into the dashboard:
*   **Hero Areas:** Use a subtle linear gradient from `primary` (#002045) to `primary_container` (#1a365d) at a 135-degree angle.
*   **Floating Progress Modals:** Use Glassmorphism. Apply `surface_container_lowest` at 80% opacity with a `24px` backdrop blur. This ensures the vibrant accents of the dashboard bleed through, maintaining a sense of "vibrancy" even in static modals.

## 3. Typography: The Editorial Voice
We utilize a dual-typeface system to balance professional authority with modern readability.

*   **The Authority (Manrope):** All `display`, `headline`, and `title` levels use Manrope. Its geometric yet warm construction feels "modern-professional." 
    *   *Usage Tip:* Use `display-lg` for daily motivation quotes or "Books Read" counters to create a high-impact editorial focal point.
*   **The Utility (Inter):** All `body` and `label` levels use Inter. It is the gold standard for dashboard legibility.
    *   *Hierarchy Hint:* Always use `on_surface_variant` (#43474e) for `body-md` descriptions to ensure the `headline` levels in `primary` remain the clear focal point.

## 4. Elevation & Depth: Tonal Layering
We reject heavy drop shadows in favor of **Tonal Lift**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on top of a `surface-container-low` background. The subtle shift from #f2f4f6 to #ffffff creates a "soft lift" that feels natural and premium.
*   **Ambient Shadows:** For "floating" elements like dropdowns or active book cards, use a shadow with a `40px` blur, 0px offset, and 6% opacity, tinted with the `primary` color. This mimics natural light passing through a high-end lens.
*   **The Ghost Border:** If a progress bar or input field requires a boundary, use `outline_variant` (#c4c6cf) at **20% opacity**. It should be felt, not seen.

## 5. Signature Components

### The "Achievement" Button
*   **Primary:** Background: `secondary_container` (#fc820c); Text: `on_secondary_container` (#5e2c00).
*   **Shape:** `xl` roundedness (1.5rem) for a pill-shaped, friendly feel.
*   **State:** On hover, shift background to `secondary` (#964900). No shadows; the color shift provides the feedback.

### Progress Chips
*   **Action Chips:** Use `tertiary_fixed` (#a3f69c) background with `on_tertiary_fixed` (#002204) text.
*   **Design Note:** Use these for "Finished Reading" or "Goal Met" tags. The green provides an "energetic achievement" signal against the deep blue backgrounds.

### Book Insight Cards & Lists
*   **Rule:** **Forbid dividers.** To separate books in a list, use a vertical spacing of `1.5rem` and alternating background shifts between `surface_container_low` and `surface_container_lowest`.
*   **Imagery:** Book covers should use `md` (0.75rem) rounded corners to match the UI's friendly aesthetic.

### Activity Inputs
*   **Style:** `surface_container_highest` background with a `none` border. On focus, transition the background to `surface_container_lowest` and apply a 1px "Ghost Border" using `primary` at 30% opacity.

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical margins. If the left margin is 48px, try a right margin of 64px for a contemporary editorial feel.
*   **Do** use `display-sm` for numbers and metrics. Make the data the hero.
*   **Do** embrace "White Space as a Feature." If a section feels crowded, remove a container, don't add a border.

### Don't
*   **Don't** use pure black (#000000) for text. Always use `on_surface` (#191c1e) to maintain a sophisticated, soft-contrast look.
*   **Don't** use the `full` (9999px) roundedness on large cards; it looks "bubbly" and juvenile. Keep large containers at `xl` (1.5rem).
*   **Don't** stack more than three levels of surface nesting. If you need a fourth level, use a subtle gradient instead of another color shift.