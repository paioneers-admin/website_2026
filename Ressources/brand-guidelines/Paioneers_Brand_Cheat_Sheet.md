# Paioneers Brand Cheat Sheet

*Canonical quick-reference for brand, website, decks, articles, and client-facing deliverables. This consolidates the existing brand guideline files into one short source of truth.*

---

## 1. Brand DNA

**Paioneers should feel like:** editorial meets engineering.

- Serious, premium, technical, but accessible.
- Thin typography, generous whitespace, sharp structure.
- Cream surfaces for identity and narrative.
- Dark teal panels for live data, system views, and operational depth.
- Motion and gradients should make content feel alive, not flashy.

**Rule:** if a design choice makes the brand feel generic SaaS, it is probably wrong.

---

## 2. Core Tokens

### Colors

| Token | Hex | Use |
|---|---|---|
| `--cream` | `#FAFFEF` | Primary background, light surfaces |
| `--dark-teal` | `#032C2D` | Primary text, dark backgrounds, dark UI |
| `--teal` | `#0F7A99` | Primary accent, interaction, Account layer |
| `--periwinkle` | `#A9B8FF` | Secondary accent, Persona layer |
| `--orange` | `#F37C38` | Highlight, CTA energy, Industry layer |
| `--blue` | `#5B8DEF` | Supporting accent, Lead layer |
| `--gray-muted` | `#8FA097` | Muted text, subtle borders, disabled states |

### Gradient Scale

Use for immersive backgrounds, signal ramps, and atmospheric transitions.

| Token | Hex |
|---|---|
| `--s1` | `#D3866C` |
| `--s2` | `#CF8B7D` |
| `--s3` | `#C89495` |
| `--s4` | `#C29BAA` |
| `--s5` | `#BBA2C0` |
| `--s6` | `#B5AAD7` |
| `--s7` | `#AEB2EC` |

### Fixed Signal Layer Colors

These assignments are load-bearing and should stay consistent everywhere.

| Layer | Color |
|---|---|
| Industry | Orange |
| Account | Teal |
| Persona | Periwinkle |
| Lead | Blue |

---

## 3. Typography

### Font System

- **IBM Plex Sans** for all reading content.
- **IBM Plex Mono** for labels, metadata, navigation, buttons, pills, panel chrome.

### Type Rules

- Headings: weight `200`, tight tracking `-0.035em` to `-0.04em`, line-height `1.05` to `1.1`.
- Body: weight `300`, line-height around `1.7`.
- Strong emphasis: weight `500`.
- Mono labels: uppercase, `0.1em` to `0.16em` tracking, usually `9px` to `13px`.

### Quick Scale

| Role | Value |
|---|---|
| `xs` | `11px` |
| `sm` | `13px` |
| `md` | `16px` |
| `lg` | `20px` |
| `xl` | `clamp(28px, 3.5vw, 44px)` |
| `2xl` | `clamp(36px, 5vw, 64px)` |
| `3xl` | `clamp(48px, 6.5vw, 80px)` |

**Important:** do not switch section headlines to heavy weights like `700`. Thin headings are part of the brand signature.

---

## 4. Layout Tokens

### Spacing

Use an 8px-based scale only.

`8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 120`

### Radius

| Token | Value | Use |
|---|---|---|
| `sm` | `6px` | Pills, chips |
| `md` | `12px` | Standard cards, inner panels |
| `lg` | `20px` | Emphasis cards, quotes |
| `xl` | `28px` | Hero containers, large panels |

### Content Width

- Max content width: `1280px`
- Presentation padding: `96px` top, `60px` sides, `64px` bottom

---

## 5. Approved Gradients

### Brand Accent Gradient

Use for text accents, borders, CTA energy, and directional emphasis.

`teal → periwinkle → orange`

Example:

```css
linear-gradient(115deg, #0F7A99 0%, #A9B8FF 50%, #F37C38 100%)
```

### Sunset / Signal Gradient

Use for full-section backgrounds and immersive transitions only.

```css
linear-gradient(135deg,
  #D3866C 0%,
  #CF8B7D 14%,
  #C89495 28%,
  #C29BAA 42%,
  #BBA2C0 56%,
  #B5AAD7 70%,
  #AEB2EC 100%
)
```

---

## 6. CTA Patterns

Both CTA styles are approved. Choose based on context, not preference.

### CTA A: Dark Solid CTA

**Use when:**
- the background is light or busy
- the layout needs a clear, grounded primary action
- clarity matters more than drama

**Style:**
- dark teal base
- cream text
- IBM Plex Mono uppercase
- tracking around `0.08em` to `0.15em`
- can hover to brighter/gradient-accented state

**Effect:** stable, direct, functional

### CTA B: Gradient Border / Gradient Fill CTA

**Use when:**
- the layout is already premium/editorial
- the CTA should feel more immersive or “hero”
- the background is dark, minimal, or atmospheric

**Style:**
- transparent or subtle base
- gradient border: `orange → periwinkle → teal`
- hover can fill with the gradient
- tracking may widen to `0.2em` on hover

**Effect:** high-energy, premium, more expressive

### CTA Selection Rule

- If in doubt on a light surface: use **CTA A**.
- If in doubt on a hero, statement block, or dark atmospheric section: use **CTA B**.
- Avoid using both CTA styles next to each other in the same component cluster.

---

## 7. Core Patterns

### Kicker

- Small mono uppercase label above section headlines
- Includes short gradient line and orange glow dot
- Used to frame sections and narrative transitions

### Light Card

- Translucent white surface
- Subtle dark-teal border
- Light blur
- Used for approachable, editorial content

### Dark Panel

- Dark teal system-style panel
- Terminal/top bar treatment
- Mono title, optional live indicator
- Used for signal feeds, dashboards, operational views

### Gradient-Bordered Card

- White or cream interior with gradient border
- Used for marquee messages, CTA cards, key statements
- Use sparingly, usually once per section or slide

### Metric Card

- Large thin numeric value
- Gradient text allowed
- Mono label below

### Frosted Header / Glass Surface

- Cream at high opacity
- Backdrop blur around `24px` for headers, `4px` to `8px` for cards
- Best for website chrome, sticky nav, floating overlays

### Dividers and Outlines

- Prefer 1px low-opacity lines over heavy shadows
- Light theme divider: `rgba(3, 44, 45, 0.12)`
- Dark theme divider: `rgba(250, 255, 239, 0.08)`

---

## 8. Motion

- Motion should feel calm and premium, never playful.
- Hover behavior: lift slightly and brighten.
- Entry behavior: soft fade-up, staggered reveal.
- Respect `prefers-reduced-motion`.

**Do not use:**
- bouncy scale jumps
- flashy color swaps
- noisy animations

---

## 9. By Medium

### Website / Landing Pages

- Use full visual language
- Ambient glows are encouraged
- Frosted header is approved
- Both CTA patterns are valid
- Dark panels should anchor data-heavy sections

### Decks / Presentations

- Use cream, dark teal, and sunset backgrounds in rotation
- Keep thin headlines and mono kickers
- Use gradient cards and dark panels selectively
- Atmosphere matters, but readability comes first

### Articles / Reports / Client Deliverables

- Use the same typography and core colors
- Dial down glows, blur, and ambient effects
- Prefer cleaner cards and simpler section separators
- Use dark panels only when showing signal/data content
- Default to CTA A unless the piece is web-native

### Internal Tooling

- Can borrow color tokens and dark panel pattern
- Does not need ambient glows or premium brand effects

---

## 10. Charts, Data, and “System” Surfaces

- Current state / muted context: subdued, dark, low-energy
- Paioneers state / active intelligence: brighter, clearer, more alive
- Minimal grids
- Signal colors should follow the fixed layer mapping
- If content is operational, use dark panel logic rather than editorial card logic

---

## 11. Logos and Assets

- Light backgrounds: `logo_black1.svg`
- Dark backgrounds: `logo_white.png`
- Favicon: `logoblack.png`

**Rule:** choose logo version by contrast, not by preference.

---

## 12. Fast Decision Rules

If you need a fast answer:

- Use `#FAFFEF` + `#032C2D` as the base pair.
- Use IBM Plex Sans for content and IBM Plex Mono for UI/chrome.
- Keep headings thin.
- Use teal, periwinkle, and orange as accents, not as a rainbow.
- Use dark panels for live/data/system content.
- Use light cards for narrative/editorial content.
- Use CTA A for clarity on light surfaces.
- Use CTA B for premium emphasis on hero or dark sections.
- Reduce effects in PDFs, reports, and article-style deliverables.

---

## 13. Scope

This file supersedes the overlapping guidance in:

- `brand_style_guide.md`
- `Paioneers_Design_System.md`
- `paioneers-brand-guidelines.md`

Those files can remain as archive/source material, but this cheat sheet should be the default reference for future work and agent prompts.
