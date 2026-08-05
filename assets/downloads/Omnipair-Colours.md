# Omnipair — Colour

Brand guidelines · Colour system
Source of truth: https://madebypuru.github.io/omnipair-brand-guidelines/simple.html#colour

One source, every colour. The palette is sampled from the horizon at first light — the **Sky Axis** — and every ramp and gradient is a contiguous slice of it.

---

## Palette inspiration

The entire Omnipair palette begins with a single photograph: **the horizon at first light**. Deep blue overhead, warm orange at the ground, turquoise where the two meet. Every brand colour is sampled directly from that image — not invented, not adjusted to a trend.

Blue sits high, turquoise mid, orange low. That vertical order becomes the Sky Axis, and the axis governs everything downstream.

**Why it matters:** because the colours come from one continuous source, they always relate. Any two Omnipair colours sit on the same gradient — which is why the system never looks assembled from parts.

---

## The Sky Axis

The master axis. One continuous gradient from deep blue to warm orange. Every colour in the system is a stop on this axis; every gradient is a contiguous slice of it. One source, every colour — the way one pool produces every function.

Primaries are stops **200**, **300**, and **600**.

| Stop | Hex | Role |
| --- | --- | --- |
| `sky/100` | `#003B6A` | Deep night blue |
| `sky/200` | `#0979E9` | **primary/blue** |
| `sky/300` | `#30E7D7` | **primary/turquoise** |
| `sky/400` | `#BFF3E8` | Horizon light |
| `sky/500` | `#F7C563` | First-light gold |
| `sky/600` | `#EF8332` | **primary/orange** |
| `sky/700` | `#CB782A` | Deep amber |

---

## Sky palette

The protocol's core voice — **infrastructure confidence, never cold**. Anchored on `primary/blue`, it lightens along its ramp: through open sky into blue light, never toward flat white.

### Ramp — primary/blue

| Step | Hex | Note |
| --- | --- | --- |
| `base` | `#0979E9` | primary/blue · sky/200 |
| `80` | `#3A94ED` | |
| `60` | `#37A9FB` | open sky |
| `40` | `#69BFFC` | |
| `20` | `#9BD4FE` | |

### Gradient

| Position | Hex | Note |
| --- | --- | --- |
| 0% | `#0979E9` | sky/200 · primary/blue |
| 55% | `#37A9FB` | blue/60 · open sky |
| 100% | `#E1F3FF` | blue light |

---

## Dawn palette

Carries the brand's warmth — **the trust signal**. Anchored on `primary/orange`, it lightens along the axis: through gold into yellow light, never toward white.

### Ramp — primary/orange

| Step | Hex | Note |
| --- | --- | --- |
| `base` | `#EF8332` | primary/orange · sky/600 |
| `80` | `#F29C5B` | |
| `60` | `#FFC652` | gold |
| `40` | `#FFDB66` | |
| `20` | `#FFEF7A` | |

### Gradient

| Position | Hex | Note |
| --- | --- | --- |
| 0% | `#EF8332` | sky/600 · primary/orange |
| 55% | `#FFC652` | orange/60 · gold |
| 100% | `#FFF6D6` | orange light |

---

## Aqua palette

Sits mid-axis — the day zone between dusk and dawn. **Clarity, liquidity, movement.** Anchored on `primary/turquoise`, it lightens along its ramp into aqua light, never toward flat white.

### Ramp — primary/turquoise

| Step | Hex | Note |
| --- | --- | --- |
| `base` | `#30E7D7` | primary/turquoise · sky/300 |
| `80` | `#59ECDF` | |
| `60` | `#83F1E7` | |
| `40` | `#ACF5EF` | |
| `20` | `#D6FAF7` | |

### Gradient

| Position | Hex | Note |
| --- | --- | --- |
| 0% | `#30E7D7` | sky/300 · primary/turquoise |
| 55% | `#83F1E7` | turquoise/60 |
| 100% | `#EDFDFB` | aqua light |

---

## Render rules — all palettes

- Gradients render **radial and soft-focus**, with grain + halftone fade.
- Gradients dissolve **to light — never to flat white**.
- Ramps lighten along the axis; they never desaturate toward grey.
- All ramps are bindable variables in `omnipair/color`.

---

## CSS custom properties

```css
:root {
  /* Sky Axis — master */
  --sky-100: #003B6A; /* deep night blue */
  --sky-200: #0979E9; /* primary/blue */
  --sky-300: #30E7D7; /* primary/turquoise */
  --sky-400: #BFF3E8; /* horizon light */
  --sky-500: #F7C563; /* first-light gold */
  --sky-600: #EF8332; /* primary/orange */
  --sky-700: #CB782A; /* deep amber */

  /* Primaries */
  --primary-blue:      var(--sky-200);
  --primary-turquoise: var(--sky-300);
  --primary-orange:    var(--sky-600);

  /* Sky ramp */
  --blue-base: #0979E9;
  --blue-80:   #3A94ED;
  --blue-60:   #37A9FB; /* open sky */
  --blue-40:   #69BFFC;
  --blue-20:   #9BD4FE;
  --blue-light:#E1F3FF;

  /* Dawn ramp */
  --orange-base: #EF8332;
  --orange-80:   #F29C5B;
  --orange-60:   #FFC652; /* gold */
  --orange-40:   #FFDB66;
  --orange-20:   #FFEF7A;
  --orange-light:#FFF6D6;

  /* Aqua ramp */
  --turquoise-base: #30E7D7;
  --turquoise-80:   #59ECDF;
  --turquoise-60:   #83F1E7;
  --turquoise-40:   #ACF5EF;
  --turquoise-20:   #D6FAF7;
  --aqua-light:     #EDFDFB;

  /* Gradients — radial, soft-focus, dissolve to light */
  --gradient-sky:  radial-gradient(circle, #0979E9 0%, #37A9FB 55%, #E1F3FF 100%);
  --gradient-dawn: radial-gradient(circle, #EF8332 0%, #FFC652 55%, #FFF6D6 100%);
  --gradient-aqua: radial-gradient(circle, #30E7D7 0%, #83F1E7 55%, #EDFDFB 100%);
}
```

---

## Still to come

These colour pages are not yet defined. Nothing below is official until it ships.

- Neutrals
- Values — RGB · CMYK
- Hierarchy & ratios
- Light & dark mode
- Functional colours
- Accessibility
- Misuse

---

*Omnipair brand guidelines · living document. Always take colour values from this file or the guideline site — never sample them from a screenshot.*
