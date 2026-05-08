---
name: Voice Agents — Arreglatech
description: Catálogo interno de agentes de voz ElevenLabs para el equipo de Arreglatech
colors:
  accent: "#6b4efa"
  accent-soft: "#8b6ef8"
  accent-tint: "#f0ebff"
  bg: "#f5f5f7"
  surface: "#ffffff"
  surface-low: "#fafafa"
  border: "#e4e4e9"
  border-active: "#6b4efa"
  text: "#1a1a2e"
  muted: "#8e8ea8"
  success: "#16a34a"
  danger: "#dc2626"
  danger-tint: "#fef2f2"
  danger-border: "#fca5a5"
typography:
  display:
    fontFamily: "Inter, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(2rem, 5vw, 3.2rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Inter, Segoe UI, system-ui, sans-serif"
    fontSize: "1.1rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Inter, Segoe UI, system-ui, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Inter, Segoe UI, system-ui, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 600
    letterSpacing: "0.09em"
rounded:
  sm: "7px"
  md: "12px"
  lg: "18px"
  full: "99px"
  circle: "50%"
spacing:
  xs: "0.45rem"
  sm: "0.8rem"
  md: "1.2rem"
  lg: "1.5rem"
  xl: "2rem"
  xxl: "4rem"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.full}"
    padding: "0.7rem 2rem"
  button-primary-hover:
    backgroundColor: "{colors.accent-soft}"
    textColor: "#ffffff"
  button-danger:
    backgroundColor: "{colors.danger-tint}"
    textColor: "{colors.danger}"
    rounded: "{rounded.full}"
    padding: "0.7rem 2rem"
  button-danger-hover:
    backgroundColor: "#fee2e2"
    textColor: "{colors.danger}"
  card-agent:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "1.5rem"
  card-agent-active:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
---

# Design System: Voice Agents — Arreglatech

## 1. Overview

**Creative North Star: "The Signal Room"**

This is a control room, not a landing page. Someone on the Arreglatech team opens it with a specific goal: start a voice session, assess an agent, close the loop. The design serves that intent without friction. Every element either carries state or enables action — nothing decorates for its own sake.

The system lives in a well-lit office environment, on a laptop or a secondary monitor. Light mode is correct here: this is a working tool, not a cinematic experience. The surface is cool-white with a faint gray warmth, the accent is a precise violet-indigo that signals interactivity without performing excitement. The grid of three agent cards communicates availability at a glance; the active state communicates focus.

What this system explicitly rejects: the SaaS landing-page convention of gradient cards, purple hero blobs, and "AI-powered" orb animations that confuse decoration with functionality. No navy-gray corporatism either — this is a modern internal tool, not an enterprise procurement page. And no sterile minimalism that strips out all personality in the name of "clean."

**Key Characteristics:**
- State is always legible: idle / active / locked are visually unambiguous
- Accent used sparingly — only on interactive and active elements
- Cards earn their existence: three agents, three decision points, no nesting
- Typography is single-family (Inter), differentiated through weight and scale
- Motion is functional: pulse for live status, orb glow for active session, talking bars for voice activity

## 2. Colors: The Signal Palette

A restrained palette where the accent carries all interactivity — its scarcity is the point.

### Primary
- **Signal Violet** (`#6b4efa`): The single interactive color. Used on the call button, active border, live dot, label highlight, and all hover states. Never decorative.
- **Soft Violet** (`#8b6ef8`): Gradient end-stop on the primary button. Not used independently.
- **Violet Tint** (`#f0ebff`): Background tint for hover states on ghost controls and the lock overlay icon. Never a card background.

### Neutral
- **Page Ground** (`#f5f5f7`): The page background. Slightly cool, not pure white — creates separation from cards without contrast noise.
- **Surface White** (`#ffffff`): Card and panel backgrounds.
- **Surface Low** (`#fafafa`): Reserved for secondary surfaces or nested content. Rarely used.
- **Border Rest** (`#e4e4e9`): All resting borders. Consistent, quiet.
- **Border Active** (`#6b4efa`): Card border when a session is live. Same as accent — state change is color change.
- **Ink** (`#1a1a2e`): All primary text. Tinted toward the accent hue, never pure black.
- **Muted** (`#8e8ea8`): Labels, placeholders, secondary text. Reliably lower contrast than Ink.

### Semantic
- **Live Green** (`#16a34a`): Active session dot and status bar pulse only. Signals a real-time connection.
- **Danger Red** (`#dc2626`): Hang-up button text and end-session button. Paired with `#fef2f2` tint background.

### Named Rules
**The Scarcity Rule.** Signal Violet appears on at most 10% of any screen surface at any given time. When everything is accented, nothing is. The color's communicative power depends on its rarity.

**The No-Purple-Surface Rule.** Violet tint (`#f0ebff`) is a hover state, not a card or section background. No purple gradients on any non-interactive surface.

## 3. Typography

**Body Font:** Inter (with Segoe UI, system-ui, sans-serif fallback)

A single typeface throughout. Inter at this size range is precise and highly legible on screens — appropriate for a working tool. The personality comes from the weight contrast between the display heading (700), card names (600), labels (600, tracked), and body copy (400). No decorative typefaces; no serif.

**Character:** Clinical clarity with just enough weight contrast to create a real hierarchy. The tracked uppercase labels (`letter-spacing: 0.09em`) act as wayfinding — they're the only place the system uses letterspacing as a design element.

### Hierarchy
- **Display** (700, `clamp(2rem, 5vw, 3.2rem)`, lh 1.1, ls -0.03em): Page title only. "Voice Agents." One use.
- **Headline** (600, 1.1rem, lh 1.3, ls -0.01em): Agent card names — "Cindy", "Vanessa", "Tripti."
- **Body** (400, 0.95rem, lh 1.5): Subtitle text and status messages. Max line length 65ch.
- **Label** (600, 0.78rem, tracked 0.09em, uppercase): Agent column headers. Also used for the Arreglatech logotype in the header.
- **Small** (500, 0.78–0.85rem): Button text, status bar text, end-session button.

### Named Rules
**The Single Family Rule.** Inter only. No mixing of typefaces for accent or display. Weight and scale create all hierarchy.

## 4. Elevation

The system uses a **state-driven elevation model**: surfaces are flat at rest, and elevation signals active state — not decoration.

Resting cards carry a barely-visible ambient shadow (`0 1px 3px rgba(0,0,0,.06), 0 4px 16px rgba(0,0,0,.04)`) that separates them from the page ground without drawing attention. When a session is active, the card gains both a violet border and a deeper shadow with a violet tint (`0 0 0 1px #6b4efa, 0 8px 32px rgba(107,78,250,.15)`). The elevation change is a state signal, not a hover decoration.

### Shadow Vocabulary
- **Ambient Rest** (`0 1px 3px rgba(0,0,0,.06), 0 4px 16px rgba(0,0,0,.04)`): All agent cards at rest. Barely perceptible — just enough to lift from the gray background.
- **Active Session** (`0 0 0 1px #6b4efa, 0 8px 32px rgba(107,78,250,.15), 0 1px 3px rgba(0,0,0,.06)`): Active card. The 1px inset ring + violet diffusion communicates a live connection.
- **Status Bar** (`0 1px 6px rgba(0,0,0,.06)`): The floating session indicator at the top. Lighter than card elevation — it's contextual, not structural.

### Named Rules
**The State-as-Elevation Rule.** Shadows change only when state changes. Hover does not increase elevation on cards. Only an active voice session earns the full shadow treatment.

## 5. Components

### Call Button (Primary Action)
The only pill-shaped element in the interface. Its roundness signals "tap me" in a page that otherwise uses rectangular-ish containers.

- **Shape:** Pill (radius 99px)
- **Primary — Start Call:** Signal Violet to Soft Violet gradient background, white text, `padding: 0.7rem 2rem`, shadow `0 4px 14px rgba(107,78,250,.35)`
- **Hover:** `filter: brightness(1.08)` — subtle brighten, no layout shift
- **Active state:** `transform: scale(0.96)` on press
- **End Call variant:** Danger Tint background (`#fef2f2`), Danger Red text (`#dc2626`), `border: 1px solid #fca5a5` — same pill shape, color role inverts to destructive

### Agent Card
Three-column grid, each card an independent call surface. Cards are the right affordance here: three discrete items with independent state and action. Not nested.

- **Shape:** 18px radius, `aspect-ratio: 9/14`, overflow hidden
- **Background:** Surface White
- **Border Rest:** `1px solid #e4e4e9`
- **Border Active:** `1px solid #6b4efa` + active shadow
- **Internal layout:** flexbox column, centered, `gap: 1.5rem`
- **Active state transition:** `border-color 0.35s, box-shadow 0.35s`

### Avatar Orb
Centered in the card, signals which agent is being addressed.

- **Size:** 90px × 90px, `border-radius: 50%`
- **Background:** `linear-gradient(135deg, #ede9fe, #ddd6fe)` — violet tint gradient
- **Border Rest:** `2px solid #e0d9ff`
- **Border Active:** `2px solid #6b4efa` + pulse ring animation (`orb-pulse`, 2s ease-in-out)

### Refresh Button (Ghost Control)
- **Shape:** 26×26px, 7px radius
- **Default:** no background, `border: 1px solid #e4e4e9`, Muted icon color
- **Hover:** violet border, Signal Violet icon, Violet Tint background
- **Active:** spin animation (0.5s linear) on click

### Lock Overlay
Appears over inactive cards when a session is running. Uses backdrop blur — purposeful glassmorphism, not decorative.

- **Background:** `rgba(245,245,247,.88)` + `backdrop-filter: blur(8px)`
- **Content:** lock icon on Violet Tint square (44px, 12px radius) + muted caption text
- **z-index:** above all card content

### Status Bar
Floating pill at the top of the grid when a session is active.

- **Background:** Surface White, `border: 1px solid #e4e4e9`, ambient shadow
- **Content:** Live Green pulse dot + session label + End Session button
- **End button:** Danger Red text, `border: 1px solid #fca5a5`, tint hover

### Talking Indicator
Five vertical bars, animated in sequence. Only visible on the active card.

- **Color:** Signal Violet bars
- **Animation:** `scaleY` between 0.3 and 1 on alternate timing (staggered 0.1s), 1s duration
- **Heights:** 6 / 14 / 20 / 14 / 8 px — symmetrical bell curve shape

## 6. Do's and Don'ts

### Do:
- **Do** use Signal Violet exclusively for interactive and active-state elements. If it's not clickable or live, it doesn't get the accent color.
- **Do** change elevation (border + shadow) as the state signal for an active session. The card visually "comes forward" when the call is live.
- **Do** use uppercase tracked labels (`letter-spacing: 0.09em`) only for wayfinding: column headers, the logotype. Not for button text or body copy.
- **Do** keep the three-card grid as the only layout structure. No nesting, no sub-cards, no panels-within-panels.
- **Do** let motion serve state: pulse for live indicators, orb glow for active session, talking bars for audio activity. All animations are status communications.

### Don't:
- **Don't** use purple or violet gradients on any non-interactive surface. No gradient card backgrounds, no gradient section fills. This is the SaaS-generic reflex this system explicitly rejects.
- **Don't** introduce navy blue, mid-gray, or enterprise palette colors. Corporativo frío is an anti-reference by name.
- **Don't** strip away all personality in the name of cleanliness. Minimalismo sin personalidad is on the anti-reference list — the design has a point of view.
- **Don't** use glassmorphism decoratively. The lock overlay blur is functional (blocks interaction, signals locked state). Blur on any other element requires the same justification.
- **Don't** use `border-left` or `border-right` greater than 1px as an accent stripe on any card, list item, or callout. Rewrite with full borders or background tints.
- **Don't** add a gradient to the "Voice Agents" heading or any other text. The gray gradient on "Agents" in the current heading is an absolute-ban pattern (gradient text) — it should be replaced with a solid Muted color (`#8e8ea8`).
- **Don't** animate layout properties (width, height, padding, margin). Transitions are limited to `transform`, `opacity`, `border-color`, `box-shadow`, `color`, `background`.
- **Don't** use `linear` easing for any user-facing transition. Default to `ease-out` or `cubic-bezier(0.4, 0, 0.2, 1)`.
