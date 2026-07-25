# Proud To Smile Dentistry — Design System

Structure and layout are cloned from the design reference (pdp.carenetic.digital);
colors, typography, and all content are Proud To Smile's own, per the client's
intake call decision (2026-07-15). See `.site-factory/state.json` → `pages.notes`
and `intake/INTAKE.md` for the full rationale.

## Colors

Brand palette extracted from proudtosmile.com, defined in `src/styles/global.css`
as OKLCH 50–950 scales generated from the client's brand hex values.

| Family | Brand hex | Anchors at | Usage |
|---|---|---|---|
| `primary` (blue) | `#1249E9` | 600 | Primary buttons, links, headings accents, focus ring |
| `secondary` (green) | `#1E7641` | 600 | Footer background, secondary buttons, dark section backgrounds |
| `accent` (cyan) | `#75E0FF` | 200 | Light tints for outline-button backgrounds, section washes — not for text |
| `neutral` (gray) | — | 900 ≈ `#0E0E0E` | Body text (900), muted text (700), borders (300) |

### Contrast (WCAG 2.2 AA — verified)

| Pairing | Ratio | Result |
|---|---|---|
| White on `primary-600` (buttons) | 6.66:1 | ✅ AA/AAA |
| `primary-700` on white (links) | 9.00:1 | ✅ AA/AAA |
| `neutral-900` on white (body text) | 19.3:1 | ✅ AA/AAA |
| `neutral-700` on white (muted text) | 10.7:1 | ✅ AA/AAA |
| White on `secondary-600` (footer text) | 5.64:1 | ✅ AA |
| White on `secondary-900` (footer background) | 7.81:1+ | ✅ AA/AAA |

Semantic tokens (`--color-background`, `--color-foreground`, `--color-muted`,
`--color-border`, `--color-ring`) are mapped in `global.css` — always prefer
these over raw palette steps in new components.

**Never use `accent` for text** — it's a pale tint (L ≈ 0.85) reserved for
button/section backgrounds only; it fails contrast as a foreground color.

## Typography

Single family for both headings and body, per `intake/branding/fonts.md`:

- **Font:** Inter (400, 500, 600, 700, 800), loaded via Google Fonts `display=swap`
- **Differentiation:** weight only (headings 600–700, body 400–500) — not a second family

### Fluid type scale (`--font-size-*`, clamp mobile → desktop)

| Token | Range | Usage |
|---|---|---|
| `text-xs` | 12–12.8px | Captions, legal fine print |
| `text-sm` | 12.8–14px | Secondary text, nav dropdown items |
| `text-base` | 16–17px | Body copy |
| `text-lg` | 18–20px | Lead paragraphs |
| `text-xl` | 20–24px | h4, card titles |
| `text-2xl` | 24–30px | h3 |
| `text-3xl` | 30–38px | Large stat/quote text |
| `text-4xl` | 36–48px | h2, section headlines |
| `text-5xl` | 44–64px | h1, hero headline |

### Heading hierarchy

- **h1** — `text-5xl`, weight 700, `tracking-tight`, `leading-tight`
- **h2** — `text-4xl`, weight 700, `tracking-tight`
- **h3** — `text-2xl`, weight 600
- **h4** — `text-xl`, weight 600
- **h5** — `text-lg`, weight 600
- **h6** — `text-base`, weight 600, uppercase, `tracking-wide` (eyebrow/label style)

## Spacing & Shape

Mirrors the reference site's section rhythm and flat card/pill-button language
(structure cloned; only the palette changed):

- **Large section padding:** `--spacing-section` = 7rem (112px) top/bottom
- **Small/band section padding:** `--spacing-section-sm` = 3.5rem (56px) — e.g. insurance strip
- **Container padding:** `--spacing-content` = 2rem horizontal
- **Radius:** `--radius-sm` 3px, `--radius-md` 10px (cards), `--radius-lg` 20px (feature panels), `--radius-pill` 999px (buttons)
- **Shadows:** none — flat design; borders (`--color-border`) do the separating work, not elevation

## Components

- **`Header.astro`** — Sticky nav. Desktop dropdowns/mega-menu use native `<details>/<summary>`
  (keyboard-accessible with no custom ARIA state management needed); the hamburger-toggled
  mobile panel (nested `<details>`) is used up through `lg` (1024px) and the full desktop
  nav + CTAs only appear at `xl` (1280px) — the full nav row + phone + booking CTA cluster
  doesn't fit in the 1024px viewport, so the switch is deliberately later than the
  conventional `lg` breakpoint (verified with a 1024–1440px sweep during design review).
  Phone (primary CTA per client decision) and ZocDoc booking link are always visible
  once the desktop nav is shown.
- **`Footer.astro`** — Practice info/hours, Patient Center links, Quick Links, social
  icons (Facebook/Instagram/YouTube — real URLs only; TikTok omitted until the
  client supplies the actual profile URL), and the full legal-page link row.
- **`Hero.astro`** — Homepage hero; the `<img>` (not a CSS background) is the LCP
  element — `loading="eager"`, `fetchpriority="high"`, `decoding="sync"`.
- **`ServicesGrid.astro`** — Reusable card grid for all 14 real services. Built once
  to be reused verbatim on future location/doctor pages, matching the reference
  site's pattern of one shared grid component across multiple templates.
- **`.btn` / `.btn-primary` / `.btn-secondary` / `.btn-outline`** utility classes in
  `global.css` — pill-shaped, 44px+ min-height for touch targets.
- **`.card`** utility class — flat white card, `radius-md`, border, generous padding.

## Content & Brand Notes (do not deviate without client sign-off)

- **Clear Aligner Therapy**, not "Invisalign," is the on-page brand name throughout
  (finalized on intake call). The URL slug stays `/service/invisalign/` for SEO
  continuity — only the on-page copy changed.
- **Primary CTA is phone** (`908-221-1188`); ZocDoc online booking is secondary/promoted,
  not primary.
- **Single location** (Bernardsville, NJ) — no "Find Location" nav item or multi-location
  cards, unlike the design reference.
- All content — testimonials, provider bios, services, hours — is sourced verbatim from
  `reference/content-proudtosmile.md`. Do not fabricate reviews, stats, or staff.

## Images

All images live in `public/images/proudtosmile/` (sourced from the real
proudtosmile.com site during intake — see `reference/content-proudtosmile.md`
section 10). Favicon/app icons were generated from `practice-icon.webp` via
ImageMagick (`favicon.ico`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`,
`icon-512-maskable.png`).

Every `<img>` has explicit `width`/`height` to prevent CLS. Hero image is eager +
`fetchpriority="high"`; all others are `loading="lazy"`.
