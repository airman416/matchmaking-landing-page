# Design System: Matchmaking

Visual guidelines and tokens for the Northeastern Student Matchmaking landing page.

## Creative North Star
*“The Physical Flyer”* — A design that feels like a beautifully typeset, printed piece of paper on a warm campus bulletin board. It is tactile, editorial, and human, rejecting the clinical, dynamic shapes of standard web software.

## Design Tokens

### Colors

We use a responsive, warm color palette that supports both a clean daylight mode and a cozy midnight cafe mode.

| Token Name | Light Mode Value (Daylight) | Dark Mode Value (Midnight) | Semantic Usage |
| :--- | :--- | :--- | :--- |
| `--bg-color` | `hsl(38, 25%, 97%)` (Cream) | `hsl(38, 12%, 10%)` (Charcoal) | Main page background |
| `--text-primary` | `hsl(180, 4%, 12%)` (Charcoal) | `hsl(38, 20%, 94%)` (Warm white) | Headings and high-contrast body text |
| `--text-secondary` | `hsl(30, 4%, 42%)` (Muted brown) | `hsl(38, 8%, 70%)` (Muted grey) | Paragraphs and secondary details |
| `--text-tertiary` | `hsl(30, 3%, 55%)` (Muted slate) | `hsl(38, 5%, 52%)` (Slate grey) | Footnotes, captions, and placeholders |
| `--accent-color` | `hsl(140, 20%, 25%)` (Forest Green) | `hsl(140, 18%, 42%)` (Bright Forest) | Primary CTAs, highlights, list markers |
| `--accent-hover` | `hsl(140, 20%, 18%)` | `hsl(140, 18%, 48%)` | CTA hover states |
| `--accent-light` | `hsl(140, 15%, 93%)` | `hsl(140, 15%, 15%)` | Badge background and soft highlights |
| `--card-bg` | `hsl(38, 20%, 94%)` (Soft cream) | `hsl(38, 10%, 14%)` (Deep charcoal) | Card background contrast |
| `--border-color` | `hsl(30, 8%, 88%)` (Warm grey border) | `hsl(38, 8%, 20%)` (Dark grey border) | Subtle dividers and card borders |

### Typography

- **Display Font**: `Cormorant Garamond` (Google Fonts) — an elegant, editorial, and lightweight serif with gorgeous italics.
  - Used for: Brand logo, page titles, section tags, step numbers.
  - Vibe: Intimate, physical, student-editorial.
- **Body Font**: `Instrument Sans` (Google Fonts) — a highly refined, clean sans-serif with a premium character.
  - Used for: Paragraphs, button text, FAQ answers, labels.
  - Vibe: Modern, extremely readable, highly credible.

### Spacing & Layout

- **Max Width**: `640px` (mobile-first reading column). Scales up to `860px` for multi-column details on larger screens.
- **Spacing System**:
  - `--space-xxs`: `0.25rem`
  - `--space-xs`: `0.5rem`
  - `--space-sm`: `1rem`
  - `--space-md`: `1.5rem`
  - `--space-lg`: `2.5rem`
  - `--space-xl`: `4rem`

---

## Component Guidelines

### Buttons
- **Primary CTA**: Solid background (`--accent-color`), high-contrast text (`#ffffff` or `--bg-color` in dark mode). Simple rectangular outline with slight rounding (`--radius-md: 8px`).
- **Secondary CTA**: Transparent background, border (`--border-color`), transition on background on hover.
- **Interaction**: Slight vertical translate (`translateY(-1px)`) and a soft, low-intensity box shadow on hover. No dramatic transitions.

### Cards & Spacing
- Cards (e.g. steps, details) should use a flat background (`--card-bg`) with a thin border (`--border-color`).
- Steps should feel like stacked, physical polaroids or printed paper tags. Include a subtle lift on hover to invite interaction.
- Add an optional organic paper-grain texture via a soft blend-mode gradient to enhance the "printed flyer" aesthetic.

### FAQ Accordion
- Styled using native `<details>` and `<summary>` elements.
- Clean borders below each item. Smooth rotation or symbol change (+ to −) on expand.
- Brief answers only, typeset with `text-wrap: pretty`.

---

## Motion & Transitions
- Keep motion subtle and physical.
- Use a single, premium easing function: `cubic-bezier(0.16, 1, 0.3, 1)` (ease-out-expo) for entry transitions.
- Fade-in animation on page load (`800ms`) to soften page entry.
- Hover transition speeds: `0.15s ease` for interactive buttons, `0.25s ease` for card transitions.