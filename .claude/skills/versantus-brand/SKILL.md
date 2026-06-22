---
name: versantus-brand
description: Apply the Versantus brand and visual design language to any deliverable. Use whenever creating or restyling Versantus-branded content — social graphics and captions (LinkedIn / Instagram), landing pages, slide decks, emails, HTML/CSS components, banners, or marketing copy. Ensures correct colours (pink #F0146E, purple #A445B2, amber #FFB800), typography (Outfit headings, Open Sans body), the signature pink→purple gradient, and a voice that is clear, warm, playful-yet-professional, and jargon-free.
---

# Versantus Brand

Replicate the Versantus visual identity and tone of voice exactly. Versantus is an
Oxford-based digital agency — "transformative digital solutions" for ambitious
organisations. The brand is **digital-first, professional but playful, warm,
collaborative, clean and confident.** It is never corporate, dull, or overly complex.

## When to use this skill

Use it for ANY Versantus-branded output: social posts, landing pages, decks, emails,
ads, web components, diagrams, or copywriting. If the user mentions Versantus, or asks
for something "on brand", apply this skill.

## The non-negotiables (memorise these)

| Token | Value | Use |
|-------|-------|-----|
| **Pink** (primary) | `#F0146E` | Hero colour, primary buttons, key highlights, links |
| **Purple** (secondary) | `#A445B2` | Gradient partner, secondary accents, supporting blocks |
| **Amber** (accent) | `#FFB800` | Sparingly — highlights, underlines, stats, a pop of warmth |
| **Signature gradient** | `linear-gradient(135deg, #F0146E 0%, #A445B2 100%)` | Hero backgrounds, large headings, key shapes |
| **Headings** | **Outfit**, weight 500–700 | All headings, big numbers, buttons |
| **Body** | **Open Sans**, weight 400 / 600 | Paragraphs, UI text, captions |

Rules:
1. **Pink is the lead.** Pink → purple is the signature gradient and should appear on
   most hero/feature surfaces. Amber is a spark, not a base — keep it under ~10% of any layout.
2. **Outfit for headings, Open Sans for body. Never swap them.** Headings are tight and
   confident (line-height ~1.1, letter-spacing slightly negative). Body is relaxed
   (line-height ~1.6).
3. **Clean and spacious.** Generous whitespace, soft rounded corners (8–24px), no clutter.
4. **Accessible contrast.** Pink and purple on white pass for large text; for body-size
   text on coloured fills use white. Never put amber text on white.
5. **Tone:** clear, honest, jargon-free, human. Confident without being salesy.

## Workflow

1. **Identify the medium** (social card, web page, deck, email, copy-only) and the
   correct dimensions / format.
2. **Load the system.** For visual work, start from `assets/versantus-tokens.css` — it
   defines every colour, font, spacing, radius and shadow as CSS variables. Link the
   Google Fonts (Outfit + Open Sans) shown below. Don't invent new colours.
3. **Build from a template.** Use `assets/social-card-template.html` (1080×1080 / 1080×1350
   posts), `assets/linkedin-carousel-template.html` (multi-slide PDF carousels), or
   `assets/landing-template.html` (web sections) as the starting structure, then adapt content.
4. **Write the copy** using `references/voice-and-tone.md`.
5. **Check against the brand checklist** in `references/brand-guidelines.md` before
   delivering.

## Required fonts (always include)

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Open+Sans:wght@400;600;700&display=swap" rel="stylesheet">
```

## Quick recipe — the Versantus look in one block

```css
:root {
  --vs-pink:   #F0146E;
  --vs-purple: #A445B2;
  --vs-amber:  #FFB800;
  --vs-ink:    #211B2E;   /* deep plum-charcoal text */
  --vs-paper:  #FFFFFF;
  --vs-mist:   #F7F3F9;   /* light surface */
  --vs-gradient: linear-gradient(135deg, #F0146E 0%, #A445B2 100%);
}
h1, h2, h3 { font-family: "Outfit", sans-serif; font-weight: 700; line-height: 1.1; letter-spacing: -0.02em; color: var(--vs-ink); }
body, p   { font-family: "Open Sans", sans-serif; line-height: 1.6; color: var(--vs-ink); }
.btn      { background: var(--vs-pink); color: #fff; border-radius: 999px; padding: .85em 1.6em; font-family: "Outfit"; font-weight: 600; }
.hero     { background: var(--vs-gradient); color: #fff; }
.highlight{ color: var(--vs-pink); }            /* or wrap a word in the gradient */
```

## Reference files

- `references/brand-guidelines.md` — full visual system: palette + tints, typography
  scale, gradients, components, logo usage, do/don't, and the pre-delivery checklist.
- `references/voice-and-tone.md` — how Versantus writes: principles, sentence patterns,
  vocabulary, social caption formulas, and worked before/after examples.
- `references/linkedin-carousel.md` — how to build a LinkedIn carousel (document post):
  specs, slide structure, copy guidance, a **caption generator** with ready-made example
  captions, the 4:5 vs 1:1 ratio choice, and how to export the deck to PDF.
- `assets/versantus-tokens.css` — drop-in CSS variables + base styles.
- `assets/social-card-template.html` — ready-to-edit Instagram/LinkedIn post.
- `assets/linkedin-carousel-template.html` — multi-slide LinkedIn carousel (4:5 portrait, 1080×1350), print-to-PDF ready.
- `assets/linkedin-carousel-square-template.html` — square 1:1 carousel variant (1080×1080), print-to-PDF ready.
- `assets/landing-template.html` — ready-to-edit web page / section.

Sources: brand fundamentals are the canonical Versantus spec; positioning and voice
verified from public Versantus channels (versantus.co.uk, LinkedIn, Instagram).
