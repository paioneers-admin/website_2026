# Paioneers Design System

*Version 0.1 — extracted from `discovery/prospects/sue/discovery_deck_alt.html`. This file is the durable reference so the visual language does not live only inside a throwaway prospect deck.*

---

## 1. Design DNA

The feel we are going for is editorial meets engineering. Thin typographic weights, generous whitespace, ambient radial glows, terminal-style dark panels when we need to show data, and soft cream backgrounds when we need to hold identity or context. Nothing is ever a static table — if the content is data, the presentation makes it feel alive, flowing, live.

The posture is serious but approachable. Technical capability is visible without being intimidating. That is the design translation of Paioneers' core brand position: deeply technical *and* accessible. The interface carries the same philosophy as the voice — it does not hide complexity, but it also does not make you earn the right to see it.

Every Paioneers-facing asset inherits from this system: decks, landing pages, proposals, dashboards, client deliverables like Weekly Action Reports and Market Intelligence Briefings. Internal tooling is exempt but can borrow the data panel pattern for consistency.

---

## 2. Color Tokens

| Token | Hex | Purpose |
|---|---|---|
| `--cream` | `#FAFFEF` | Primary background. Paioneers identity color. |
| `--dark-teal` | `#032C2D` | Primary text, dark panels, CTA base. |
| `--teal` | `#0F7A99` | Primary accent, interactive elements, Account signal layer. |
| `--periwinkle` | `#A9B8FF` | Secondary accent, Persona signal layer. |
| `--orange` | `#F37C38` | Highlight, attention, Industry signal layer, hot scores. |
| `--blue` | `#5B8DEF` | Lead signal layer. |

**Signal gradient scale** — a 7-stop ramp used for decorative gradients and heatmap-style elements. Salmon on one end, muted lavender on the other.

```
--s1: #d3866c   --s2: #cf8b7d   --s3: #c89495   --s4: #c29baa
--s5: #bba2c0   --s6: #b5aad7   --s7: #aeb2ec
```

### Signal layer assignments

The four layers of the Commercial Intel signal stack each have a fixed color. These assignments are not decorative — they are load-bearing and must stay consistent across every future build so that a sales team member can read a Paioneers asset and instantly know which layer a signal belongs to.

| Layer | Color | Token |
|---|---|---|
| Industry | Orange | `--orange` |
| Account | Teal | `--teal` |
| Persona | Periwinkle | `--periwinkle` |
| Lead | Blue | `--blue` |

### Gradient text

When a headline needs to carry visual weight, we apply a background-clipped gradient that runs from teal through periwinkle into orange:

```css
background: linear-gradient(115deg, var(--teal) 0%, var(--periwinkle) 50%, var(--orange) 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

Used on marquee words inside H1s ("SUE × **Paioneers**", "Zien wat **beweegt**", "Richting **2026**") and on metric card values.

---

## 3. Typography

Two fonts. That is the whole system.

- **IBM Plex Sans** — everything the reader actually reads. Weights 200 through 600, italic available at 300.
- **IBM Plex Mono** — everything the reader sees but does not read as prose: kickers, labels, metadata, pills, slide counters, panel titles, slide footers.

### Headings

Headings use weight **200**. The thinness is deliberate and is one of the most distinctive marks of the brand. If someone replaces 200 with 400 "to make it more legible", they have stripped the brand of its feel.

Letter-spacing on headings is tight (`-0.035em` to `-0.04em`). Line-height is tight (1.05 to 1.1). The combination gives headlines a confident, pulled-together look without any extra ornamentation.

### Body

Body text runs at weight **300**, line-height **1.7**, color at 72% opacity against `--dark-teal` so it reads as soft rather than sharp. Leads and subheads sit at **1.8** line-height and a slightly lower opacity (62%) for a gentler visual rhythm.

Strong text moves to weight **500** and full `--dark-teal` opacity. Italic stays at 300 but gets a 90% opacity bump because italics are used as emphasis, not decoration.

### Mono labels

Mono text is always uppercase, always tracked open (`0.1em` to `0.16em`), always small (9–11px typical). Used for kickers, panel titles, score pills, slide footers, metadata. The tracked uppercase mono is how the interface speaks to itself — it is the voice of the UI chrome, not the content.

### Fluid type scale

The scale clamps so it breathes with viewport size. Below are the named tokens.

| Token | Value |
|---|---|
| `--t-xs` | `11px` |
| `--t-sm` | `13px` |
| `--t-md` | `16px` |
| `--t-lg` | `20px` |
| `--t-xl` | `clamp(28px, 3.5vw, 44px)` |
| `--t-2xl` | `clamp(36px, 5vw, 64px)` |
| `--t-3xl` | `clamp(48px, 6.5vw, 80px)` |

---

## 4. Spacing & Radius

Spacing is a single linear scale in multiples of 8. No ad-hoc values — everything snaps to the scale.

```
--sp-1: 8     --sp-2: 16    --sp-3: 24    --sp-4: 32
--sp-5: 40    --sp-6: 48    --sp-7: 56    --sp-8: 64
--sp-10: 80   --sp-12: 96   --sp-15: 120
```

Radius scale is four steps, used consistently across cards, panels, buttons, pills.

| Token | Value | Typical use |
|---|---|---|
| `--r-sm` | `6px` | Small pills, inline chips, topic list items |
| `--r-md` | `12px` | Light cards, founder cards, dark panels (inner) |
| `--r-lg` | `20px` | Quote blocks, emphasized cards |
| `--r-xl` | `28px` | Large dark panels, hero containers |

Max content width inside any slide or container is **1280px**. Slide padding is **96px top, 60px sides, 64px bottom** — the extra top padding gives the scroll-snap a natural breathing point as each slide enters.

---

## 5. Motion

Two easing curves carry the entire motion language. One is for taste — opacity, background, color changes feel calm. The other is for physics — transforms and reveals feel springy.

```css
--ease:   cubic-bezier(0.4, 0, 0.2, 1);    /* opacity / background / color */
--spring: cubic-bezier(0.16, 1, 0.3, 1);   /* transforms / reveals / hovers */
```

### Hover convention

Hover states follow one rule: lift and brighten. The element moves up 2–4px via `translateY(-2px to -4px)`, picks up a soft shadow (`0 4px 20px rgba(3,44,45,.07)` or `0 8px 32px rgba(3,44,45,.08)`), and the background opacity climbs from roughly 55% to 85%. No color changes, no scale jumps — the hover is a breath, not a statement.

On rows that expand (sig-rows, dlv-rows) the lift is combined with a chevron rotation and a progressive reveal of detail content.

### Entry animations

The cover slide uses two keyframes, staggered by role:

```css
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}

@keyframes panelIn {
  from { opacity: 0; transform: translateY(20px) scale(.98); }
  to   { opacity: 1; transform: translateY(0) scale(1); }
}
```

Kicker enters first, headline a beat later, lead one more beat, metadata another, panel last — a 100ms cascade. The effect is a room coming into focus rather than a slide loading.

### Accessibility override

Every motion block is wrapped so that `@media (prefers-reduced-motion: reduce)` shortens durations to a millisecond. This is not optional and is never removed.

---

## 6. Core Patterns

### Kicker

The kicker is the small mono label that sits above every section headline. It has three parts: a short gradient line coming in from the left, the mono-uppercase label itself, and an orange glowing dot on the right. The dot glow uses `box-shadow: 0 0 8px rgba(243,124,56,.5)`.

The kicker is how the reader knows what kind of content is about to land. "Discovery Call" announces a meeting. "Topic 1" announces a question block. "Samenvatting" announces a wrap-up. "De data layer" announces the intelligence foundation. The kickers carry the narrative spine of a deck.

### Light card

The base card pattern. A translucent white background (`rgba(255,255,255,.55)`), a 1px border at about 7% opacity of dark teal, a 4px backdrop blur, and hover states that bump the background to 85% opacity and add a soft shadow. These cards float over the ambient glows and noise of the slide background, so they never feel like boxes cut out of a page.

Use for topic lists, founder cards, metric cards, and any content that is supposed to feel approachable rather than operational.

### Dark panel

The operational counterpart to the light card. A `--dark-teal` background, a terminal-style bar at the top with three traffic-light dots (red, yellow, green), a mono uppercase panel title, and a pulsing green "Live" indicator on the right.

The dark panel is where data lives. Signal feeds, account cards, live metrics, anything that wants to feel alive and operational rather than editorial. Never use it for identity or philosophy content — those belong on the cream surface.

The panel bar is not decoration. It tells the reader "this is a system, not a slide". It is the single most distinctive pattern in the Paioneers visual language and should be used sparingly so it keeps its weight.

### Gradient-bordered primary card

A white content area with a 1.5px gradient border running teal → periwinkle → orange, built via the `padding-box` / `border-box` trick:

```css
background:
  linear-gradient(rgba(255,255,255,.85), rgba(255,255,255,.85)) padding-box,
  linear-gradient(90deg, var(--orange), var(--periwinkle), var(--teal)) border-box;
border: 1.5px solid transparent;
```

Used for marquee statements where we want the reader to stop and read, not skim. Examples: the one-line value proposition on slide 3, the CTA card on slide 15. Should appear at most once per slide.

### Signal row (sig-row)

The expandable row pattern that carries individual signals. Each row has a colored avatar, a name, a metadata subline, a score pill, and a chevron. Clicking or hovering expands the row to reveal a signal-strength progress bar (animated from 0 to target width via `scaleX` over 600ms with spring easing) and an "Open in feed →" action button.

Four layer variants exist — Industry, Account, Persona, Lead — and each uses its layer color for the avatar background, the score pill, and the progress bar fill. This is where the color tokens earn their keep: a reader should be able to glance at a signal row and know instantly which layer it came from.

### Journey flow

Three nodes arranged horizontally ("now" bottom-left, "obstacle" middle, "goal" top-right) connected by a dashed SVG path with a gradient stroke running orange → periwinkle → teal. The path has an arrowhead marker at the goal end. Used on summary slides where we need to show current state, the blocker, and the target in one visual beat.

### Timeline steps

Three circular nodes connected by a horizontal gradient line, each carrying a mono-labeled number (01, 02, 03), a heading, and a short description. The three nodes use different accent colors (teal, periwinkle, orange in sequence). Used to show a linear process — ICP Workshop → Data Layer → Activation — at a glance.

### Deliverable row (dlv-row)

A three-column grid pattern for listing deliverables: a colored numbered dot on the left, content in the middle (heading + description), and a column of mono tag chips on the right. Each row has a subtle gradient wash that fades in on hover (different color per row position), and the dot scales up to 1.12 on hover. This is the pattern used on slide 14 ("Fundament + activatie") to show the three layers of the model.

### Metric card

Centered card with a large gradient-text numeric value (36px, weight 200), a mono uppercase label below it, and the standard light card background. Used in CTA clusters where we need to surface three or four key numbers — time commitment, participants, dates.

### CTA button (gcta)

The one button style. Dark-teal base, mono uppercase label, tracked at `0.15em`. On hover, a polygon-clipped gradient fill sweeps in (teal → periwinkle → orange) and the letter-spacing widens to `0.2em`. The polygon clip gives the button an angled chevron shape that feels like forward motion rather than a flat rectangle.

---

## 7. Ambient effects

### Glows

Every slide has two or three radial-gradient glows positioned off-canvas. They are large (560–720px), low-opacity (0.1–0.22), and use the core accent colors — teal, periwinkle, orange. The glows are what make the cream background feel atmospheric instead of flat.

```css
.glow--teal   { top: -20%; right: -5%;  width: 720px; height: 720px;
  background: radial-gradient(circle, rgba(15,122,153,.22) 0%, transparent 65%); }
.glow--peri   { bottom: -20%; left: -8%; width: 560px; height: 560px;
  background: radial-gradient(circle, rgba(169,184,255,.18) 0%, transparent 65%); }
.glow--orange { top: 40%; left: 40%; width: 300px; height: 300px;
  background: radial-gradient(circle, rgba(243,124,56,.1) 0%, transparent 65%); }
```

Mix and match per slide. A cover slide might have all three; a list slide might have one. Never zero — flat backgrounds break the feel.

### Noise overlay

An inline SVG with `feTurbulence` at opacity 0.035, layered behind content. Adds tactile texture without visible grain. The noise is what keeps the cream from reading as a plastic gradient — it gives the surface a slight paper-like quality.

```css
.slide::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg...%3E");
  pointer-events: none;
}
```

### Backdrop blur

Translucent cards carry a 4–8px backdrop filter so they sit softly on top of the glows rather than punching through them. This is what makes the light card pattern feel like frosted glass instead of semi-transparent plastic.

---

## 8. Voice of the UI

The microcopy that lives inside the interface — not the content, the chrome — follows its own voice rules.

- **Data labels** are mono uppercase with wide tracking: `SIGNAL STRENGTH · 82%`, `NEW HIRE`, `M&A`, `REGULATORY`, `TECH SHIFT`.
- **Score pills** use mono caps with short, category-style words: `Hot`, `Funding`, `Headcount`, `Regulatory`, `Tech shift`, `Engagement`, `Intent`, `Email`, `Title shift`, `DMU`.
- **Action buttons** inside rows follow the pattern `verb in noun →`: "Open in feed →", "Plan de volgende sessie", "Explore Revenue Engine →".
- **Kicker prefixes** carry the deck's narrative: `Discovery Call`, `Wie wij zijn`, `In één zin`, `Waarom we hier zitten`, `Samenvatting`, `Ons proces in één beeld`, `De data layer`, `Bovenop de layer`, `Volgende stap`. They set the tone of the slide in three or four words.
- **Live indicators** pulse subtly (2.2s ease-in-out infinite, opacity 1 → 0.4 → 1). Even when the data on screen is static, the pulse says "this is a live system".

The voice-of-UI rule: never write marketing copy inside the chrome. Chrome is operational, functional, understated. The content does the work; the chrome stays out of the way.

---

## 9. When to apply this system

Every Paioneers-facing asset uses these tokens and patterns.

- **Decks and presentations** — full system, all patterns available, scroll-snap structure.
- **Landing pages and marketing sites** — full color system and typography, selected patterns (kicker, light card, dark panel for data sections, gradient-bordered primary card for hero CTAs).
- **Proposals and business cases** — typography and color system, light card pattern for content blocks, no ambient effects if delivered as PDF.
- **Client deliverables** (Weekly Action Reports, Market Intelligence Briefings) — typography and color system, dark panel pattern for signal data, dial down the ambient glows depending on medium (PDF vs. live web).
- **Internal tooling** — exempt from the ambient effects, but can borrow the dark panel pattern for any data-display surface so that internal and external tools feel related.

---

## 10. Source of truth

The canonical implementation lives in the `<style>` block of `discovery/prospects/sue/discovery_deck_alt.html`. When this Design System file disagrees with the deck, the deck wins until we extract the CSS into a dedicated `paioneers-design.css` stylesheet. Every token, pattern and micro-interaction in this document can be traced back to a specific selector in that deck file — if something feels wrong, open the deck and look at the source.

Future work: extract `paioneers-design.css` as a standalone stylesheet, vendor the IBM Plex font locally, document a small React/Vue component library for the patterns that show up more than once.

---

## 11. Open questions

- **Logo and wordmark** — not yet defined in the deck. The cover slide uses a gradient-text treatment on the Paioneers word itself; whether that is the official mark or a placeholder is open.
- **Iconography** — the deck uses a handful of SVG icons (arrow markers, chevrons, traffic-light dots), but there is no documented icon system. Something to define once the visual language is more widely applied.
- **PDF exports** — the design works beautifully on a web canvas, but translating the ambient glows and backdrop blur into print-ready PDFs needs its own treatment. Open question for deliverable rendering.
- **Client-branded variants** — if a client-facing deliverable needs to carry the client's brand colors alongside Paioneers', how do we blend without breaking the signal-layer color assignments? Unsolved.
