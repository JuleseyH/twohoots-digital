# Two Hoots Digital — Complete Brand & Design Specification

**Version:** 1.0
**Last updated:** May 2026
**Purpose:** This document is the single source of truth for all Two Hoots Digital design and development work. Any page, component, or piece of UI built for this brand should be consistent with every decision documented here. Read it in full before starting any build.

---

## 1. Brand Overview

### Who Two Hoots Digital Is

Two Hoots Digital is a boutique Meta ads and Shopify specialist service run by a single expert. The business targets ecommerce brand owners who are running paid social ads but not seeing the sales to match. The core insight underpinning the brand is that most conversion problems are not ad problems — they are funnel problems. The ads are doing their job. The store is not.

The positioning is deliberately expert and confident. Two Hoots Digital does not hedge. It does not use vague language like "helping brands grow" or "unlocking potential." It names the problem directly, explains what causes it, and offers a precise fix. The tone is that of someone who has seen this problem hundreds of times and knows exactly where to look.

### What Two Hoots Digital Sells

The primary product at this stage is the Ad + Shopify Audit. This is a fixed-price, fixed-scope service priced at £397. The client grants read-only access to their Meta Ads Manager and Shopify store. The specialist reviews both in full, records a Loom walkthrough explaining the findings, produces a written priority action checklist ordered by impact, and offers an optional 30-minute follow-up Zoom call. Everything is delivered within 3 business days.

The audit is designed to sit at the top of a funnel that leads into longer-term retainer work — ongoing ads management, landing page builds, and conversion optimisation. The audit itself is priced to be a low-risk first step for a client who is not yet ready to commit to a retainer.

### Brand Voice

The voice is punchy, direct, and confident without tipping into arrogance. It does not waffle. It does not pad. It does not use filler phrases. Every line earns its place. The tone assumes the reader is intelligent and busy — it does not over-explain, but it does make sure the key message lands.

Good examples of the voice in action:
- "Your ads work. Your store doesn't."
- "Meta says your campaigns are performing. The sales tell a different story."
- "Good ROAS, bad revenue."
- "Stop guessing. Start fixing."
- "Know exactly what's broken."

The voice never uses: phrases like "unlock your potential", "take your business to the next level", "game-changing", or any language that sounds like it was written for a generic marketing agency. It also never uses em dashes as a stylistic flourish.

---

## 2. Colour System

The Two Hoots Digital palette is built on three anchors: near-black, electric yellow, and deep purple. Black is the foundation. Yellow is action and energy. Purple is depth and expertise. They never compete — each has a defined role and sticks to it.

### Full Colour Reference

| Token name | Hex value | Role |
|---|---|---|
| `--black` | `#0B0B0B` | Page background, body background across all sections unless overridden |
| `--yellow` | `#F5E500` | Primary CTA colour, key headline accents, logo "Hoots" word, price section background, hero accent text, section label lines on black bg |
| `--yellow-dim` | `rgba(245,229,0,0.12)` | Subtle yellow overlays, not used directly in current pages |
| `--yellow-mid` | `rgba(245,229,0,0.35)` | Mid-weight yellow for glass-like effects if needed |
| `--white` | `#FFFFFF` | All body text and headings on dark backgrounds |
| `--off-white` | `#F0EDE6` | Nav CTA hover state background only |
| `--grey` | `#9A9A9A` | Body copy, supporting text, muted text on dark backgrounds, step descriptions |
| `--dark-grey` | `#1A1A1A` | Alternative section background on non-purple, non-black sections. Hover state for deliverable items |
| `--mid-grey` | `#282828` | Hover backgrounds within dark sections |
| `--border` | `rgba(255,255,255,0.08)` | Default dividers and borders on black/dark-grey sections |
| `--border-yellow` | `rgba(245,229,0,0.3)` | Yellow-tinted borders, used on icon boxes in deliverables section |
| `--purple-bg` | `#1A0A3A` | Background for all purple sections: Diagnosis, How It Works, About |
| `--purple-bg-mid` | `#160830` | Hover states and nested items within purple sections (stat boxes) |
| `--purple-bright` | `#BB99FF` | All text, numbers, and labels written on purple backgrounds |
| `--purple-accent` | `#AA88FF` | Secondary purple text, slightly softer than bright |
| `--purple-dim` | `rgba(187,153,255,0.15)` | Subtle purple overlays, used in photo frame gradient |
| `--border-purple` | `rgba(187,153,255,0.25)` | All borders within or bordering purple sections |

### Colour Rules — Non-Negotiable

**Yellow is for action and energy, never atmosphere.** Yellow appears on: CTA buttons (background), key headline accent words (text colour), section label decorative lines on black sections, the price section background, the logo word "Hoots", the hero ghost background outline, and icon strokes in the deliverables section. Yellow does not appear as a section background except for the dedicated price section.

**Purple is for atmosphere and expertise, never action.** Purple appears as: full section backgrounds on Diagnosis, How It Works, and About. When text is written on a purple background, it uses `--purple-bright` (`#BB99FF`) for numbers, labels, and section tags. White is used for primary headings on purple. Grey (`#9A9A9A`) is used for body text on purple, same as on black. Purple never appears as a button colour or CTA element.

**Black is the foundation.** The default page background is `#0B0B0B`. Most sections sit on this. It is never a "colour choice" — it is the ground everything else sits on.

**Contrast hierarchy:** Yellow on black is the highest contrast pairing and is reserved for the most important elements. Purple bright on purple bg is mid-contrast and is used for supporting labels. White on black/purple is the standard for headings. Grey on black/purple is the standard for body text.

**The price section is the only inverted section.** On the yellow price section, all text flips to black. Headings are `#0B0B0B`. Body text is `rgba(0,0,0,0.6)`. The CTA button on this section is black background with yellow text — the inverse of all other CTAs.

---

## 3. Typography System

Typography is one of the most important brand decisions on this site. It is what makes it feel designed rather than templated. All three fonts were chosen deliberately and should never be swapped out for system fonts or generic alternatives like Inter, Roboto, or Arial.

### Font Stack

**Cinzel Decorative** — used exclusively for the logo. This is a high-contrast serif with Art Deco references. It communicates heritage and craft. It is never used for anything other than the two-word logo: "Two" in white, "Hoots" in yellow.

**Anybody** — the primary display and body font. This is a variable-width sans-serif with condensed options and strong italic variants. It is used for all headings, hero text, price figures, CTA button labels, and body copy. The italic variant is used for accent words within headlines (always in yellow). Weight range in use: 300 (light body text) through 900 (hero headlines and price displays).

**DM Mono** — the secondary utility font. This is a monospace font used for labels, tags, step numbers, small descriptors, and anything that needs a technical or systematic feel. It reinforces the idea that this service is methodical and precise. Used at 10–13px with generous letter-spacing (0.12em–0.25em). Always uppercase in this context.

### Google Fonts Import

Always load all three fonts from Google Fonts using this single import:

```
https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700&family=Anybody:ital,wght@0,100..900;1,100..900&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&display=swap
```

Use `<link rel="preconnect">` tags for both `fonts.googleapis.com` and `fonts.gstatic.com` before the stylesheet link for performance.

### Type Scale

| Element | Font | Size | Weight | Case | Letter-spacing | Line-height | Notes |
|---|---|---|---|---|---|---|---|
| Logo | Cinzel Decorative | 11px | 400 | uppercase | 0.1em | — | "Hoots" in yellow |
| Hero headline | Anybody | clamp(52px, 7vw, 100px) | 800 | uppercase | -0.03em | 0.95 | Accent word italic yellow |
| Section heading large | Anybody | clamp(40px, 5vw, 68px) | 800–900 | uppercase | -0.025em | 1.0 | Accent word italic yellow |
| Section heading medium | Anybody | clamp(32px, 4vw, 52px) | 800 | uppercase | -0.02em | 1.05 | Used in diagnosis heading |
| Price amount | Anybody | 80px | 900 | — | -0.04em | 1 | Black on yellow bg |
| Price currency symbol | Anybody | 32px | 700 | — | — | — | `rgba(0,0,0,0.5)` on yellow |
| CTA button | Anybody | 15px | 800 | uppercase | 0.06em | — | Yellow text on black bg |
| Deliverable title | Anybody | 18px | 700 | — | -0.01em | — | White on black |
| Diagnosis item title | Anybody | 17px | 700 | — | -0.01em | — | White on purple |
| Step heading | Anybody | 16px | 700 | — | -0.01em | — | White on purple |
| Body text | Anybody | 16–17px | 300 | — | — | 1.6–1.65 | `#9A9A9A` |
| Body strong | Anybody | 16–17px | 500 | — | — | — | `#FFFFFF` |
| Diagnosis body | Anybody | 14px | 300 | — | — | 1.6 | `#9A9A9A` |
| Deliverable desc | Anybody | 14px | 300 | — | — | 1.65 | `#9A9A9A` |
| Section label | DM Mono | 10px | 400 | uppercase | 0.25em | — | Yellow on black, purple-bright on purple |
| Hero tag | DM Mono | 11px | 400 | uppercase | 0.2em | — | Yellow |
| Nav CTA | DM Mono | 11px | 400 | uppercase | 0.12em | — | Black on yellow |
| Step number | DM Mono | 13px | 400 | — | — | — | Purple-bright on purple bg |
| Price detail line | DM Mono | 11px | 400 | uppercase | 0.15em | — | `rgba(0,0,0,0.5)` on yellow |
| Guarantee line | DM Mono | 10px | 400 | uppercase | 0.12em | — | `rgba(0,0,0,0.45)` on yellow |
| Stat label | DM Mono | 10px | 400 | uppercase | 0.15em | — | `#9A9A9A` on purple |
| Footer copyright | DM Mono | 11px | 400 | — | 0.05em | — | `#9A9A9A` |

---

## 4. Layout System

### Grid & Spacing

The layout is built on a simple set of principles. Content is constrained to a max-width of 1200px and centred with `margin: 0 auto`. Sections have consistent padding of `100px 48px` on desktop and `72px 24px` on mobile. No border radius is used anywhere — all corners are sharp and square. This is intentional and important to the brand aesthetic.

Grid dividers between items (in diagnosis, deliverables, and stats) are created by setting a `gap: 1px` on the grid parent and giving the parent a background colour matching the border colour. This creates clean hairline dividers that feel more polished than using borders on individual items.

### Breakpoints

| Breakpoint | Behaviour |
|---|---|
| Default (>900px) | All multi-column layouts active. Nav at full width. Section padding 100px 48px. |
| 900px | Nav collapses to 24px padding. Diagnosis grid: 2-col to 1-col. Deliverables: 3-col to 1-col. Process steps: 4-col to 2-col. Price section: 2-col to 1-col. About: 2-col to 1-col. Section padding: 72px 24px. |
| 600px | Process steps: 2-col to 1-col. About stats: 3-col to 2-col. Hero bottom stacks. Scroll indicator hidden. |

### Section Rhythm

The page alternates between black sections and purple sections. This alternation creates visual breathing room and prevents the page from feeling monotonous. The sequence on the audit page is:

1. Hero — black
2. Diagnosis — purple
3. What's Included — black
4. How It Works — purple
5. Price — yellow
6. About — purple
7. Final CTA — black
8. Footer — black

Each purple section is bordered top and bottom with `1px solid var(--border-purple)`. Each black section flows naturally into the page background.

---

## 5. Components

### Navigation

The nav is fixed to the top of the viewport and fades from `rgba(11,11,11,0.95)` at the top to transparent at the bottom, so it blends with whatever section sits behind it as the user scrolls. It sits at z-index 50.

- Left: Logo (`Two` in white Cinzel Decorative + `Hoots` in yellow, 11px, letter-spacing 0.1em, uppercase)
- Right: Nav CTA button (`Get the audit` — DM Mono, 11px, uppercase, letter-spacing 0.12em, black text on yellow background, 10px 20px padding, no border radius)
- Nav CTA hover: background transitions to `--off-white` (`#F0EDE6`), lifts 1px

### Section Labels

Every section begins with a label — a small piece of DM Mono text that names the section. On black sections this is yellow (`#F5E500`). On purple sections this is bright purple (`#BB99FF`). The label has a decorative line after it using `::after` pseudo-element: `flex: 1; max-width: 60px; height: 1px`. On black sections the line is `var(--border-yellow)`. On purple sections it should match the purple border colour.

CSS:
```css
.section-label {
  font-family: 'DM Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--yellow);
  margin-bottom: 48px;
  display: flex;
  align-items: center;
  gap: 16px;
}

.section-label::after {
  content: '';
  flex: 1;
  max-width: 60px;
  height: 1px;
  background: var(--border-yellow);
}
```

### CTA Buttons

The primary CTA button appears in two contexts:

**On dark/purple backgrounds:**
- Background: `#0B0B0B` (black)
- Text: `#F5E500` (yellow)
- Font: Anybody, 15px, weight 800, uppercase, letter-spacing 0.06em
- Padding: 20px 44px
- No border radius
- Hover: background goes to `#111`, lifts `translateY(-2px)`, adds subtle shadow `0 8px 32px rgba(0,0,0,0.25)`
- Active: snaps back `translateY(0)`

**On the yellow price section:**
- Background: `#0B0B0B` (black)
- Text: `#F5E500` (yellow)
- Identical styling — the inversion of the section background means this button visually pops without needing to change

```css
.cta-btn {
  display: inline-block;
  background: var(--black);
  color: var(--yellow);
  font-family: 'Anybody', sans-serif;
  font-size: 15px;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  padding: 20px 44px;
  transition: background 0.2s ease, transform 0.15s ease, box-shadow 0.2s ease;
  cursor: pointer;
}

.cta-btn:hover {
  background: #111;
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(0,0,0,0.25);
}
```

### Deliverable Items

Each deliverable card sits in a 3-column grid on desktop, 1-column on mobile. The grid uses `gap: 1px` with a `var(--border)` background to create hairline dividers.

Each item has:
- A 40x40px square icon box with `border: 1px solid var(--border-yellow)`, containing an 18x18px SVG with `stroke: var(--yellow)`, `fill: none`, `stroke-width: 1.5`
- A title in Anybody 18px weight 700
- A description in Anybody 14px weight 300, `#9A9A9A`
- A `::before` pseudo-element that creates a 2px yellow top border that animates in from the left on hover (`transform: scaleX(0)` → `scaleX(1)`, transform-origin left, 0.3s ease)
- Hover background: transitions to `var(--dark-grey)` (`#1A1A1A`)

### Diagnosis Items

The diagnosis grid is 2-column on desktop, 1-column on mobile. The grid uses `gap: 1px` with `var(--border-purple)` background.

Each item has:
- A number (`01`–`04`) in DM Mono 11px, `var(--purple-bright)`, flex-shrink 0
- A title in Anybody 17px weight 700, white
- A description in Anybody 14px weight 300, `#9A9A9A`
- Background: `var(--purple-bg)` (`#1A0A3A`)
- Hover: background goes to `var(--purple-bg-mid)` (`#160830`)

### Process Steps

Four steps in a horizontal row (2x2 on tablet, 1-col on mobile). A faint line runs across the top connecting all four, positioned at `top: 28px` (aligning with the centre of the step number boxes).

Each step has:
- A 56x56px square box with `border: 1px solid var(--border-purple)`, `background: var(--black)` (deliberately black even though surrounding section is purple, so it punches through)
- Step number in DM Mono 13px, `var(--purple-bright)`
- Heading in Anybody 16px weight 700
- Description in Anybody 13px weight 300, `#9A9A9A`

### Ghost Background Elements

Used in two places to add texture and visual depth:

**Hero:** The text `£397` is absolutely positioned on the right side of the hero, vertically centred. It is enormous (clamp 280px–520px), italic, Anybody weight 900, `color: transparent`, `-webkit-text-stroke: 1px rgba(245,229,0,0.07)`. It is purely decorative, `pointer-events: none`, `user-select: none`.

**Price section:** The text `£397` is a CSS `::before` pseudo-element on `.price-section`, positioned right -40px, vertically centred, same enormous sizing (clamp 200px–380px), but this time `color: rgba(0,0,0,0.06)` — very dark transparent on the yellow background. This creates the same ghost effect but inverted for the yellow section.

### Grain Overlay

A full-viewport fixed pseudo-element on `body::after` applies a subtle film grain to the entire page:

```css
body::after {
  content: '';
  position: fixed;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events: none;
  z-index: 100;
  opacity: 0.6;
}
```

This is non-negotiable. Without it the page feels flat and digital. It adds the subtle tactile quality that makes the design feel considered.

### Custom Cursor

A yellow dot (10px diameter) tracks the mouse with a slight lag effect, achieved via `requestAnimationFrame` with exponential easing (`cx += (mx - cx) * 0.15`). On hover over interactive elements (links, buttons, cards), it grows to 36px with a smooth transition. Uses `mix-blend-mode: difference` so it inverts against whatever it moves over — on yellow elements it becomes a dark dot, on dark elements it becomes a bright dot. `pointer-events: none` so it never interferes with clicks.

---

## 6. Animation & Motion

### Scroll-triggered Fade Ups

Every content block uses a `.fade-up` class which starts as `opacity: 0; transform: translateY(28px)` and transitions to visible when the element enters the viewport. This is handled via `IntersectionObserver` with a threshold of `0.12` — the animation triggers when 12% of the element is visible.

Transition: `opacity 0.7s ease, transform 0.7s ease`

Stagger delays are applied to nth-children (0.1s, 0.2s, 0.3s) so grid items within a section animate in sequence rather than all at once.

Once visible, the observer is detached (`observer.unobserve(e.target)`) so the animation only plays once.

### Scroll Indicator

In the hero, a vertical scroll indicator sits bottom-right. It is DM Mono 10px, vertical writing mode, with an animated line below it. The line pulses using a CSS keyframe animation:

```css
@keyframes scrollLine {
  0%, 100% { opacity: 0.3; transform: scaleY(1); transform-origin: top; }
  50% { opacity: 1; transform: scaleY(0.5); transform-origin: bottom; }
}
```

Duration 2s, ease-in-out, infinite. This is hidden at the 600px breakpoint.

### Hover Transitions

All transitions use `ease` timing function unless otherwise noted. Standard durations:
- Background colour changes: 0.2s
- Transform (lift on CTA): 0.15s
- Deliverable top border reveal: 0.3s
- Cursor size change: 0.2s
- Nav CTA: 0.2s background + 0.15s transform

---

## 7. Page Sections — Full Spec

### 7.1 Navigation

**HTML structure:** `<nav>` containing `.logo` (anchor tag) and `.nav-cta` (anchor tag).

**Logo markup:** `Two<em>Hoots</em> Digital` where `<em>` is styled with `font-style: normal; color: var(--yellow)`.

**Behaviour:** Fixed, full width, z-index 50. Background fades from near-black to transparent vertically so the hero image shows through as you scroll.

**Nav CTA text:** `Get the audit`
**Nav CTA link:** Points to `#get-audit` (the price section anchor)

---

### 7.2 Hero

**Layout:** Full viewport height (`min-height: 100vh`), flex column, content pinned to bottom-left (`justify-content: flex-end`). Padding: `0 48px 80px`.

**Ghost element:** `<div class="hero-bg-number">£397</div>` — positioned absolute, right side, vertically centred. Outline text using `-webkit-text-stroke`.

**Tag line:** `Ad + Shopify Audit`
Font: DM Mono. Colour: `#F5E500`. Has a 32px yellow line before it (`::before`).

**Headline:**
```
Your ads work.
Your store
doesn't.
```
"doesn't." is wrapped in `<span class="accent">` which applies `color: var(--yellow); font-style: italic`.

**Subtext:**
`Meta says your campaigns are performing. But the sales aren't landing. The problem isn't your ads — it's the gap between the click and the checkout. We find it and fix it.`

"Meta says your campaigns are performing." is wrapped in `<strong>` for white emphasis.

Font: Anybody 17px weight 300. Colour: `#9A9A9A`. Max-width 440px.

**Scroll indicator:** DM Mono, `Scroll`, vertical writing mode, bottom right of hero.

---

### 7.3 Diagnosis Section

**Background:** `#1A0A3A` (purple-bg)
**Section label:** `Sound familiar?` — DM Mono, `#BB99FF`
**Heading:**
```
You're spending money.
Not seeing results.
```
"Not seeing results." in yellow (`#F5E500`).

**Grid:** 2×2, `gap: 1px`, `background: var(--border-purple)`

**Item 01 — Good ROAS, bad revenue**
Meta says 4x return. Your bank account disagrees. The numbers look fine until you look closer.

**Item 02 — Traffic but no conversions**
People are landing on your store. They're not buying. Something between the ad and the checkout is killing the sale.

**Item 03 — You've changed the creative, the copy, the targeting**
Tweaked everything you can think of. Still the same results. Because the problem isn't the ad.

**Item 04 — You don't know where it's breaking**
The data tells you something's wrong. It doesn't tell you what to actually do about it.

Numbers `01`–`04` in DM Mono, `#BB99FF`.

---

### 7.4 What's Included

**Background:** Black (`#0B0B0B`)
**Section label:** `What's included` — DM Mono, yellow
**Heading:**
```
A full diagnosis
and a fix list.
```
"diagnosis" wrapped in `<span class="accent">` — yellow italic.

**Grid:** 3-column desktop, 1-column mobile. `gap: 1px`, `background: var(--border)`.

**Item 1 — Meta Ads Review**
Campaign structure, audience targeting, creative performance, budget allocation. We look at what's actually running and what it's actually doing.

**Item 2 — Shopify Store Audit**
Landing pages, product pages, cart, checkout. Every step a customer takes after clicking your ad — we find where they're dropping off and why.

**Item 3 — Loom Walkthrough**
A recorded 10–15 minute video walking you through exactly what we found, what it means, and what to do first.

**Item 4 — Priority Action Checklist**
A written list of fixes, ordered by impact. No vague advice — specific changes, specific reasons, specific expected outcomes.

**Item 5 — 30-Minute Follow-Up Call**
Optional Zoom to go through the findings together, ask questions, and get absolute clarity on what to tackle first.

**Item 6 — 3 Business Day Turnaround**
You'll have everything within 3 working days of access being granted. No waiting weeks for a report that's already out of date.

Each item has a 40×40px icon box with yellow SVG icon, yellow border.
Top border animation on hover: yellow line slides in from left, 2px height, 0.3s.

---

### 7.5 How It Works

**Background:** `#1A0A3A` (purple-bg)
**Section label:** `How it works` — DM Mono, `#BB99FF`
**Heading:**
```
Simple.
Fast. Done.
```
"Done." in yellow (`#F5E500`).

**4 steps, horizontal row:**

**Step 01 — Book & pay**
Secure your spot. You'll get a confirmation and a short onboarding form straight away.

**Step 02 — Grant access**
Share read-only access to your Meta Ads Manager and Shopify. Takes five minutes.

**Step 03 — We dig in**
Full review of your ads and store. We look at everything — not just the obvious stuff.

**Step 04 — You get answers**
Loom video, action checklist, and optional Zoom — all delivered within 3 business days.

Step number boxes: 56×56px, `border: 1px solid var(--border-purple)`, `background: var(--black)`, number in DM Mono 13px `#BB99FF`.
Connecting line runs behind all four boxes at `top: 28px`, 1px, `rgba(255,255,255,0.08)`.

---

### 7.6 Price Section

**Background:** `#F5E500` (yellow)
**Anchor id:** `get-audit`
**Ghost element:** CSS `::before` pseudo-element containing `£397`, enormous, `color: rgba(0,0,0,0.06)`, positioned right

**Left column:**
Section label: `Investment` — DM Mono, `rgba(0,0,0,0.4)`
Heading:
```
Stop guessing.
Start fixing.
```
Colour: `#0B0B0B` (black). Anybody, clamp 40px–68px, weight 900, uppercase.

Body text: `One audit. One clear picture of where your money is going and what's blocking the sales. Everything you need to make a decision — nothing you don't.`
Colour: `rgba(0,0,0,0.6)`. Max-width 380px.

**Right column:**
Price display: `£397` — `£` symbol is 32px weight 700 `rgba(0,0,0,0.5)`, `397` is 80px weight 900 `#0B0B0B`
Price detail line: `One-time payment · No monthly fees` — DM Mono, `rgba(0,0,0,0.5)`

Checklist (5 items, custom square checkbox styling):
- Meta Ads + Shopify full audit
- Recorded Loom walkthrough
- Written priority action checklist
- Optional 30-min follow-up Zoom
- Delivered in 3 business days

CTA button: `Book your audit →` — black background, yellow text
Guarantee line: `Secure payment · Read-only access only` — DM Mono 10px, `rgba(0,0,0,0.45)`

---

### 7.7 About

**Background:** `#1A0A3A` (purple-bg)
**Layout:** 2-column, `1fr 1.4fr`, 80px gap

**Left column:**
Portrait photo frame, aspect-ratio 3/4, max-width 320px. Border: `1px solid var(--border-purple)`. Background: `#160830`. Purple dim gradient overlay (`linear-gradient(135deg, var(--purple-dim) 0%, transparent 60%)`).
Yellow badge bottom-right: 100×100px square, `background: var(--yellow)`, `color: var(--black)`, text: `Ads & Shopify Specialist`, DM Mono 9px.

**Right column:**
Section label: `Who's behind this` — DM Mono, `#BB99FF`
Heading:
```
Ads expertise.
Real results.
```
"Real results." in yellow italic.

Body copy paragraph 1:
`I'm a Meta ads specialist with a reputation for finding the leaks other people miss. I've worked with ecommerce brands who had perfectly good ad campaigns that were bleeding money because of what happened after the click.`

Body copy paragraph 2:
`Most audits tell you what's wrong. Mine tells you what to fix, in what order, and why it'll make a difference. You'll leave with a clear action list, not a 40-page PDF you'll never read.`

Stat grid (3-column, `gap: 1px`, `background: var(--border-purple)`):
- `100+` / `Accounts reviewed`
- `3` / `Day turnaround`
- `£397` / `Flat fee, no surprises`

Stat numbers: Anybody 36px weight 900, `#BB99FF`. Stat labels: DM Mono 10px, `#9A9A9A`. Stat item bg: `#160830`.

---

### 7.8 Final CTA

**Background:** Black (`#0B0B0B`), centre aligned
**Radial glow:** CSS `::before` pseudo-element, radial gradient yellow at 6% opacity, 600×600px, centred behind the content

**Heading:**
```
Know exactly
what's broken.
```
"what's broken." on its own line, in yellow italic, displayed as `<span class="accent" style="display: block;">`.

Size: clamp 48px–96px, weight 900, uppercase, letter-spacing -0.04em.

**Subtext:** `Stop tweaking ads that aren't the problem. Get the audit and find out what actually is.`
Colour: `#9A9A9A`. Max-width 420px. Centred.

**CTA:** `Book your audit — £397 →` — links to `#get-audit`

---

### 7.9 Footer

**Layout:** flex row, `justify-content: space-between`, padding `40px 48px`, border-top `1px solid var(--border)`
**Left:** Logo (same as nav, but `opacity: 0.6`)
**Right:** `© 2026 Two Hoots Digital. All rights reserved.` — DM Mono 11px, `#9A9A9A`

---

## 8. Things Still To Do

These are placeholders in the current build that need real content before the page goes live:

- **Photo:** The About section has a placeholder `div` where a real portrait photo needs to go. Replace with an `<img>` tag, same aspect-ratio (3/4), max-width 320px, positioned inside `.about-photo-frame`.
- **Payment link:** All CTA buttons currently have `href="#"`. Replace with the actual Stripe payment link or booking page URL.
- **Stats:** The `100+` accounts reviewed figure is a placeholder. Update with real numbers before launch.
- **Title tag:** Currently `Ad + Shopify Audit | Two Hoots Digital`. Keep this or update if the page URL/context changes.
- **Favicon:** Not yet added. Should use the TwoHoots logo mark if available, or default to a yellow square with a black "T".

---

## 9. Future Pages

When building additional pages — lead magnet landing page, tripwire page, full website — the following rules carry over from this document:

- The colour system is fixed. Do not introduce new colours without updating this spec.
- The font stack is fixed. Always load all three fonts.
- Section labels always follow the same DM Mono treatment.
- Purple sections are for credibility, depth, and process. Yellow sections are for conversion moments. Black sections are the default.
- No border radius on any element.
- Grain overlay on every page.
- Custom cursor on every page.
- Ghost background text elements should be used on any hero or feature section to add depth.
- Scroll-triggered fade-up animations on all content blocks.
- CTA buttons are always black background with yellow text. Never reversed. Never a different colour.

### Lead Magnet Landing Page

The lead magnet page will follow the same visual language. The hero headline is locked: `Meta says your ads are working. Your Shopify store disagrees.` This should be treated with the same hero treatment as the audit page — large Anybody, uppercase, with the key phrase on its own line in yellow italic.

The page is shorter and more focused than the audit page. Its only job is to get the email address. There should be one primary CTA (opt-in form or button linking to a form) repeated at most twice down the page. The structure should be:

1. Hero with headline and opt-in form or CTA button
2. What's inside the guide (3–4 bullet points)
3. Who it's for (1–2 sentences)
4. Social proof (1–2 testimonials)
5. Second CTA
6. Short about section with photo

The guide itself should be positioned as something practical and immediately useful — not a theoretical overview, but a specific checklist or framework the reader can act on the same day. The copy should make clear that the guide alone will tell them something they did not know about their own store.

Colour treatment: same as audit page. The opt-in form fields should have black backgrounds with yellow borders (`1px solid var(--border-yellow)`) and white placeholder text. The submit button follows the standard CTA style.

### Tripwire Page

The tripwire page is shown immediately after someone opts in to the lead magnet. Its job is to present the audit offer at full price (£397) to someone who is already in a positive frame of mind having just opted in. The framing is: "Before you go — you've just unlocked the free guide. But if you want to go deeper..."

The page should be short — hero, offer summary, price, CTA. No need for the full diagnosis or how-it-works sections. The person arriving here is already warm. The copy should acknowledge the opt-in ("You just took the first step") and position the audit as the natural next move.

Visual treatment: same colour system, same fonts. Can be slightly more stripped back than the audit page — the price section can take up more of the page since that is the only conversion goal.

### Full Website

When building the full Two Hoots Digital website, the pages needed are:

- Homepage (introduces the business, links to services)
- Services page (audit, and eventually retainer packages)
- About page (full story, expertise, experience)
- Work/results page (case studies or testimonials)
- Contact page

The homepage should open with a bold hero that communicates the positioning in a single phrase. Candidate headline: `The gap between your ads and your sales. We close it.` The page should be shorter than the landing pages — its job is to route visitors to the right place, not to convert immediately.

The about page should tell the story of why Two Hoots Digital exists, what the specialist has seen repeatedly, and why the audit-first model is the right way to work. It can be longer and more personal in tone than the landing pages. The same typography and colour system applies, but the voice can be slightly warmer and less punchy.

---

## 10. Design Anti-Patterns

These are things that should never appear in Two Hoots Digital design work, regardless of trends or client requests.

**Never use:**
- Border radius on any element (not even small values like 4px — everything is square)
- Purple as a CTA or button colour (it is always atmospheric, never action)
- Yellow as a section background except on the price/conversion section
- Generic fonts — Inter, Roboto, Arial, system-ui, or any sans-serif that is not Anybody
- Gradients as primary visual elements (the grain overlay and ghost text are the texture — no gradient cards or gradient backgrounds)
- Multiple CTA styles on the same page (one button style, used consistently)
- Centre-aligned hero text (the hero is always left-aligned)
- Purple gradient on white or light backgrounds — this is the most overused "AI aesthetic" and must be avoided completely
- Emojis anywhere on the page
- Rounded icons or avatar-style treatments on brand elements

**Be careful with:**
- Adding new colours — the palette is intentionally tight. Before adding anything new, ask whether one of the existing colours can do the job.
- Soft or pastel tones — the brand is high contrast and bold. Any softening risks undermining the confidence of the positioning.
- Centring body text — body copy is always left-aligned. Only the final CTA section uses centre alignment, and only for the heading and short subtext.
- Overusing the purple bright text colour — `#BB99FF` is a supporting colour used for labels and numbers within purple sections. It should not appear on black backgrounds or be used as a headline colour outside of its defined contexts.
