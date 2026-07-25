# Brand Colors

Define your color palette here. Claude will use these to customize the Tailwind theme.

Source: extracted from the live proudtosmile.com CSS (real brand colors — client confirmed on
intake call the new site should use Proud To Smile's own blue/green palette, NOT the
pdp.carenetic.digital design reference's colors). These take priority over the reference site.

## Primary Colors

**Primary:** #1249E9 (Blue)
- Used for: Primary CTA buttons, dividers/`<hr>`, full-width CTA/banner sections
- Hover state: #0E3ABA (darker blue)
- Light tint: #416DED

**Secondary:** #1E7641 (Green)
- Used for: Footer background, secondary CTAs ("Read all Reviews", "Learn more"), nav hover accents
- Dark shade: #185E34 (footer sub-bar)
- Light tint: #4B9167 (~48% opacity section wash)

**Accent:** #75E0FF (Light Cyan)
- Used for: Secondary/outline button background, decorative section tints (~29% opacity)
- Dark: #5DB3CC / Light: #90E6FF

## Neutral Colors

**Text:** #0E0E0E (near-black)
**Muted Text:** #3E3E3E
**Background:** #ffffff (White)
**Surface:** #ffffff (Card/panel background)
**Border:** #CCCCCC

## Semantic Colors

**Success:** #10b981 (Emerald)
**Warning:** #f59e0b (Amber)
**Error:** #ef4444 (Red)
**Info:** #3b82f6 (Blue)

---

## Color Format Notes

For Tailwind v4 with oklch, colors will be converted automatically.
You can also provide oklch values directly:

```
Primary: oklch(0.5 0.2 265)
```
