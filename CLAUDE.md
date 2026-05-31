# Two Hoots Digital — Claude Code Project Brief

Read this file before touching anything. It is the single source of truth for this project.

---

## What This Project Is

A 4-page marketing funnel for **Two Hoots Digital**, a Meta ads and Shopify CRO specialist service run by Julia. The funnel captures leads via a free guide, converts them immediately via a tripwire offer, and sells a £397 audit service.

The full brand spec is in `TWOHOOTS.md`. Read it before writing any code or copy.

**The visual reference for all pages is `index.html`.** Before building any new page, read `index.html` in full and match its design exactly.

---

## Visual Design Direction — Read This First

The site uses a **Tokenix-inspired dark aesthetic**. This is not negotiable. Every page must match `index.html` exactly in terms of visual style. Here is what that means:

### Atmosphere & Backgrounds
- Page background: `#08080F` (near black, not pure black)
- Dark sections alternate between `linear-gradient(135deg, #0D0D1A 0%, #100820 100%)` and `linear-gradient(135deg, #0D0820 0%, #0D0D1A 100%)`
- Every section has **glowing radial orb elements** — large blurred circles of purple or yellow light using `filter: blur(80px)`. These float with a CSS `orbFloat` keyframe animation.
- A **grain overlay** is applied to the entire page via `body::after` using an SVG fractalNoise texture at low opacity.
- **Sparkle/star SVG elements** are scattered around hero sections and the final CTA. They use a `sparklePop` keyframe animation.

### Colours
| Token | Hex | Usage |
|---|---|---|
| `--black` | `#08080F` | Page background |
| `--black-mid` | `#0D0D1A` | Dark section backgrounds |
| `--black-card` | `#111122` | Card backgrounds |
| `--yellow` | `#F5E500` | CTAs, accents, hero headline accent, marquee, section label lines |
| `--yellow-glow` | `rgba(245,229,0,0.15)` | Button hover shadows |
| `--purple-bright` | `#BB99FF` | Text/labels on purple/dark sections, step numbers, sparkles |
| `--border` | `rgba(255,255,255,0.07)` | Default dividers |
| `--border-yellow` | `rgba(245,229,0,0.25)` | Yellow-tinted borders |
| `--border-purple` | `rgba(187,153,255,0.2)` | Purple-tinted borders |
| `--grey` | `#8A8A9A` | Body copy |
| `--white` | `#FFFFFF` | Headings |

**Yellow sections (price/conversion):** background `#F5E500`, ALL text must be `#0B0B0B`. CTA button on yellow = black bg + yellow text.

### Typography
- **Anybody** (Google Fonts) — all headings, body, buttons. Variable width. Use italic for accent words in yellow.
- **DM Mono** (Google Fonts) — section labels, tags, step numbers, small details. Always uppercase with wide letter-spacing.
- **Cinzel Decorative** (Google Fonts) — logo only.
- NEVER use Inter, Roboto, Arial, or system fonts.

Always load all three from Google Fonts with preconnect tags.

### Navigation
- Fixed, full width, `z-index: 50`
- `background: rgba(8,8,15,0.85)` with `backdrop-filter: blur(20px)`
- `border-bottom: 1px solid var(--border)`
- Left: logo. Right: yellow CTA button linking to `index.html#get-audit`
- No nav on `tripwire.html`

### Key Components

**Section labels:** DM Mono, 10px, uppercase, letter-spacing 0.25em, with a short line before them using `::before`. Yellow on dark sections, `--purple-bright` on purple/gradient sections. Fade in on scroll.

**CTA buttons (on dark bg):** Yellow background, black text, Anybody 800, uppercase. Hover: lift + yellow glow shadow. No border radius.

**CTA buttons (on yellow bg):** Black background, yellow text. Same hover treatment.

**Cards (deliverables):** `background: var(--black-card)`, 1px gap grid with `var(--border)` as grid background. On hover: lift `translateY(-2px)` + a yellow gradient line sweeps across the top using `::after` with `scaleX` transition.

**Diagnosis cards:** `background: var(--black-mid)` on gradient purple background. On hover: purple left border slides up using `::before` with `scaleY` transition.

**Step numbers:** 64x64px square, `border: 1px solid var(--border-purple)`, `background: var(--black)`. On hover: border colour brightens to `--purple-bright` with a purple glow shadow.

**Stats:** Large Anybody 900, yellow, with a radial yellow glow behind each card. Numbers count up from zero when scrolled into view using IntersectionObserver + setInterval.

**FAQ accordion:** Click to open/close. `+` icon rotates 45deg when open. Max-height transition for smooth open/close. Only one item open at a time.

**Marquee strip:** Scrolling yellow text band between hero and first content section. DM Mono uppercase. Pauses on hover. Uses `@keyframes marquee` with `translateX`.

### Animations & Interactions
- **Custom cursor:** 10px yellow dot with lag tracking via rAF. Grows to 40px on hover over interactive elements. `mix-blend-mode: difference`.
- **Hero line:** A yellow gradient line that draws from 0 to 120px width on page load (CSS transition, triggered by JS `setTimeout`).
- **Badge dot:** Pulsing yellow dot in hero badge using `pulseDot` keyframe.
- **Orb float:** All orbs float up and down with `orbFloat` keyframe (8s, ease-in-out, infinite).
- **Sparkles:** Star SVGs pulse with `sparklePop` keyframe (scale + rotate, 3s infinite).
- **Fade up:** All cards, steps, and content blocks fade up on scroll via IntersectionObserver at 0.1 threshold. Once visible, observer detaches.
- **Section labels:** Fade in via IntersectionObserver at 0.2 threshold.

### Layout
- Max content width: `1200px`, centred with `margin: 0 auto`
- Section padding: `100px 60px` desktop
- No border radius anywhere — everything square
- Grid dividers: `gap: 1px` on grid parent with border colour as background

### Responsive
- 900px: 2-col grids go 1-col, nav padding reduces, section padding drops to `72px 24px`
- 600px: all grids 1-col, hero font size reduces, nav CTA hides

---

## The 4 Pages

### 1. `index.html` — Audit Sales Page (BUILT)
Sells the £397 Meta Ads + Shopify Audit. Already built. Do not modify unless specifically asked.

**Sections in order:**
1. Nav
2. Hero — "You're not bad at ads. Your store is losing the sale." + badge + animated line + marquee
3. Diagnosis (gradient purple bg) — 4 pain point cards
4. Deliverables (dark bg) — 6 delivery cards in 3-col grid
5. Process (gradient purple bg) — 4 steps with connecting line
6. Stats (dark bg) — 3 animated counting numbers
7. Price (yellow bg) — objection-handling copy + checklist + CTA
8. About (gradient purple bg) — Julia bio + photo placeholder
9. FAQ (dark mid bg) — 5 questions accordion
10. Final CTA (dark bg) — large heading + orbs + sparkles
11. Footer

### 2. `lead-magnet.html` — Free Guide Opt-in Page (TO BUILD)
**Headline:** "Meta says your ads are working. Your Shopify store disagrees."
**Goal:** Capture email in exchange for free guide
**After opt-in:** Redirect to `tripwire.html`

**Sections:**
1. Nav (same as index)
2. Hero — headline + subheadline + opt-in form (name + email + button). Form submits to `tripwire.html` for now. Hero has orbs and sparkles.
3. Marquee strip (same style as index)
4. What's inside the guide — 4 items in a 2-col grid, same card style as deliverables
5. Who it's for — 2-col layout, left text, right a visual stat or pull quote
6. Social proof — 2 testimonial cards (placeholder text). Dark card style with purple border.
7. About Julia — same as index about section, shorter
8. Second opt-in CTA — same form repeated, centred, with orb glow behind
9. Footer

**Form styling:** Fields have `background: var(--black-card)`, `border: 1px solid var(--border-yellow)`, white text, no border radius. Submit button = full yellow CTA button.

**Copy direction:**
- Pain-first: clicks with no sales, don't know why
- Guide promises to show them exactly where the leak is
- Free, no credit card, straight to their inbox
- Julia's voice throughout — direct, blunt, no waffle

### 3. `tripwire.html` — Audit Offer Page (TO BUILD)
Shown immediately after guide opt-in. Short and focused.

**No nav** — nothing to distract.

**Sections:**
1. Small header — just the logo, centred
2. Hero — "Wait — before your guide lands in your inbox..." Acknowledge the opt-in warmly. Pivot to the audit offer.
3. Condensed offer — what's included (4 items max), price, CTA
4. Reassurance line — read-only access, no obligation, 3 day turnaround

**Tone:** Warmer than the audit page. They just did something good. Not pushy.
**Length:** Short. Under 5 sections. Get in, make the offer, get out.

### 4. `thankyou.html` — Thank You Page (TO BUILD)
One page, two states controlled by URL parameter `?type=guide` or `?type=audit`.

**Guide state:** "Your guide is on its way. Check your inbox." + link to audit page
**Audit state:** "You're booked. You'll hear from Julia within 24 hours."

Keep it simple. Big confirmation message, what happens next, minimal design. Still uses the same dark aesthetic and fonts.

---

## Shared Elements

### styles.css
Create this file and put all shared styles in it: CSS reset, variables, fonts, nav, footer, cursor, orb, sparkle, grain overlay, section label, CTA button, fade-up animation. Link from every HTML page.

### File Structure
```
/
├── index.html
├── lead-magnet.html
├── tripwire.html
├── thankyou.html
├── styles.css
├── CLAUDE.md
└── TWOHOOTS.md
```

---

## Julia's Voice — Copy Rules

- Direct and blunt. Says what it means.
- Short sentences. Often fragments. That's fine.
- No corporate language. No "unlock your potential". No "game-changing".
- Humour is dry and self-aware, not try-hard.
- Calls problems by their name. Doesn't soften bad news.
- Uses "I" not "we" — this is a one-person business.
- Numbers and specifics over vague claims.
- Never uses em dashes as a stylistic flourish.

Good examples:
- "You're not bad at ads. Your store is losing the sale."
- "I'm pretty blunt. If your product page is terrible, I'll tell you."
- "Not 3 weeks. Not 'we'll be in touch'. Three working days."
- "Running a bath with the plug out."

---

## CRO Principles

1. **Pain before solution** — establish the problem before offering the fix
2. **Specificity converts** — "your bounce rate is costing you sales" beats "improve conversions"
3. **Objection handling** — anticipate "is this worth it?" and answer it directly
4. **One CTA per page** — repeated, not varied
5. **Social proof near the CTA** — don't let them leave without seeing it
6. **Benefits not features** — "you'll know exactly what to fix" not "includes written report"
7. **Outcome-first copy** — lead with what they get, not what you do

---

## What's Still Needed

- **Payment link:** CTA buttons link to `#`. Replace with Stripe link when ready.
- **Email form:** Lead magnet form submits to `tripwire.html` for now. Will connect to email platform later.
- **Julia's photo:** Placeholder in about sections. Add real photo when available.
- **Testimonials:** Placeholder text throughout. Replace with real quotes.
- **Stats:** `100+` is a placeholder. Update when ready.

---

## Hosting

Deploys to **Hostinger** via GitHub. Push to the connected GitHub repo and Hostinger auto-deploys. No build step — plain HTML/CSS/JS.
