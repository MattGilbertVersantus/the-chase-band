# Versantus — Visual Brand Guidelines

The complete visual system for replicating the Versantus look. Pair this with
`voice-and-tone.md` for copy.

> **Brand in one line:** Digital-first, professional but playful, warm and
> collaborative, clean and confident. Never corporate, dull, or overly complex.

---

## 1. Colour

### Core palette (authoritative — do not alter the hex values)

| Name | Hex | RGB | Role |
|------|-----|-----|------|
| Versantus Pink | `#F0146E` | 240, 20, 110 | **Primary.** The brand's lead colour — hero fills, primary buttons, links, key emphasis. |
| Versantus Purple | `#A445B2` | 164, 69, 178 | **Secondary.** Gradient partner, supporting blocks, secondary buttons/icons. |
| Versantus Amber | `#FFB800` | 255, 184, 0 | **Accent.** A spark of warmth — underlines, stat figures, small highlights, dots. Use sparingly (<10% of a layout). |

### Signature gradient

The pink→purple gradient is the single most recognisable brand device. Use it on
heroes, feature panels, large display headings (via `background-clip: text`), and
key graphic shapes.

```css
--vs-gradient:      linear-gradient(135deg, #F0146E 0%, #A445B2 100%);
--vs-gradient-soft: linear-gradient(135deg, #F0146E 0%, #A445B2 100%); /* at lower opacity for backgrounds */
```

- Default angle **135°** (top-left → bottom-right). Keep angle consistent across a set.
- For a richer "sunset" variant, amber may join at the start: `linear-gradient(135deg, #FFB800 0%, #F0146E 45%, #A445B2 100%)` — use only as an occasional feature, not the default.

### Neutrals (supporting system — harmonised with the palette)

| Name | Hex | Use |
|------|-----|-----|
| Ink | `#211B2E` | Default text on light; deep plum-charcoal (warmer than pure black). |
| Ink-soft | `#5A5566` | Secondary text, captions, metadata. |
| Paper | `#FFFFFF` | Primary light background. |
| Mist | `#F7F3F9` | Light section surface / cards (a whisper of purple). |
| Cloud | `#EDE6F1` | Hairlines, borders, dividers, disabled states. |
| Night | `#16121F` | Dark-mode / dark section background. |

### Tints & shades (for charts, hovers, states)

- Pink: hover/darker `#D1095C`, tint `#FBD0E2`, wash `#FDEEF4`
- Purple: hover/darker `#8A3398`, tint `#E7D3EC`, wash `#F4EBF6`
- Amber: hover/darker `#E0A100`, tint `#FFE9B3`, wash `#FFF6E0`

### Contrast & accessibility rules

- White text on Pink, Purple, and the gradient ✅ (passes for UI/large text).
- Pink and Purple text on white/Mist ✅ for headings & large text.
- **Never** amber text on white (fails contrast). Amber = fills, shapes, and large
  numbers on dark/coloured backgrounds, or thin underlines.
- Body text is always Ink (`#211B2E`) on light, or white on dark/coloured.

---

## 2. Typography

Two typefaces only. Both are free on Google Fonts.

### Headings — **Outfit**
Geometric, modern, friendly. Weights 500–800.
- Display / H1: 700–800, line-height **1.05–1.1**, letter-spacing **-0.02em**.
- H2–H3: 600–700, line-height 1.15, letter-spacing -0.01em.
- Used for: all headings, big stat numbers, buttons, eyebrows/labels (uppercase,
  letter-spacing +0.08em, 600).

### Body — **Open Sans**
Humanist, highly legible. Weights 400 / 600 / 700.
- Body: 400, **line-height 1.6**, max line length ~70ch.
- Lead paragraph: 400–600, slightly larger.
- UI / captions: 600 for emphasis.

### Type scale (rem, 16px base — fluid clamp recommended for web)

| Token | Size | Use |
|-------|------|-----|
| display | 3.5–4.5rem | Hero headline |
| h1 | 2.75rem | Page title |
| h2 | 2rem | Section title |
| h3 | 1.5rem | Sub-section |
| lead | 1.25rem | Intro paragraph |
| body | 1rem | Default |
| small | 0.875rem | Captions, meta |
| eyebrow | 0.8rem, uppercase, +0.08em | Labels above headings |

**Pairing tip:** an eyebrow (Outfit, uppercase, pink) above a large Outfit headline,
with one key word wrapped in the gradient, is the signature heading treatment.

---

## 3. Layout & shape

- **Whitespace is part of the brand.** Be generous; let content breathe.
- **Corner radius:** small 8px, medium 16px, large 24px, pill 999px (buttons & tags).
- **Spacing scale (8pt):** 4, 8, 12, 16, 24, 32, 48, 64, 96px.
- **Grid:** 12-column on web; centre key content, max-width ~1200px.
- **Shadows:** soft and coloured, never harsh black.
  - card: `0 10px 30px rgba(33, 27, 46, 0.08)`
  - lifted/brand: `0 16px 40px rgba(240, 20, 110, 0.22)`
- **Shapes:** rounded blobs, soft circles, and gradient arcs as decorative motifs.
  Avoid sharp/aggressive geometry.

---

## 4. Components

### Buttons
- **Primary:** pink fill, white text, pill radius, Outfit 600. Hover → `#D1095C` + lift.
- **Secondary:** transparent with 1.5px pink border, pink text. Hover → pink wash fill.
- **On gradient/dark:** white fill, pink text; or white outline.
- Padding ~`0.85em 1.6em`. Optional arrow "→" after label.

### Cards
- Paper or Mist background, radius 16–24px, soft card shadow, generous padding (24–32px).
- Optional 4px top border or left bar in pink or the gradient.

### Tags / pills
- Mist or pink-wash background, pink text, pill radius, Open Sans 600, small.

### Stats / numbers
- Big number in Outfit 700–800, coloured pink or amber; label below in Open Sans, Ink-soft.

### Links
- Pink, 600 weight; underline on hover (amber or pink underline accent works well).

### Icons & illustration
- Simple, rounded, line or duotone (pink + purple). Friendly, not clinical.
- Photography: bright, real, human — team and people-focused, warm and candid.

---

## 5. Logo usage

> If an official logo file is supplied, always use it; never recreate it.

- Give the logo clear space (≥ the height of its mark on all sides).
- Use full-colour on light backgrounds; reversed/white on pink, purple, gradient, or
  dark surfaces. Never place the coloured logo on a busy or low-contrast background.
- Don't stretch, recolour, rotate, add effects, or place on clashing colours.

---

## 6. Do / Don't

**Do**
- Lead with pink; use the pink→purple gradient as the hero device.
- Keep Outfit for headings and Open Sans for body, every time.
- Use amber as a small, intentional spark.
- Keep layouts clean, spacious, rounded, and warm.
- Write in plain, human, confident language.

**Don't**
- Don't introduce off-brand colours (no corporate navy, no teal, no random brights).
- Don't make amber a dominant or background colour.
- Don't use heavy black shadows, sharp aggressive angles, or cramped layouts.
- Don't mix in other fonts, or use Outfit for long body copy.
- Don't sound corporate, jargon-heavy, dull, or overcomplicated.

---

## 7. Pre-delivery checklist

- [ ] Pink is the lead colour; pink→purple gradient appears on the hero/feature.
- [ ] Amber used sparingly (<10%), never as body text on white.
- [ ] Headings = Outfit; body = Open Sans; correct weights & line-heights.
- [ ] Only brand colours + harmonised neutrals used (no off-brand hues).
- [ ] Rounded corners, soft coloured shadows, generous whitespace.
- [ ] Contrast passes (white text on colour; Ink on light).
- [ ] Copy is clear, warm, jargon-free, confident (see voice-and-tone.md).
- [ ] Logo (if used) has clear space and correct colourway.
- [ ] Feels digital-first, playful-yet-professional — not corporate or cluttered.
