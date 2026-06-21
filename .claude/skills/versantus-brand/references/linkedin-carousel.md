# Versantus — LinkedIn Carousel

How to create an on-brand LinkedIn carousel (a "document post"). LinkedIn carousels are
uploaded as a **multi-page PDF**; each PDF page is one swipeable slide.

Pair this with `brand-guidelines.md` (visuals) and `voice-and-tone.md` (copy). The
ready-to-edit deck is `assets/linkedin-carousel-template.html`.

## Specs

| Item | Spec |
|------|------|
| Format | PDF (one page = one slide) |
| Aspect ratio | **4:5 portrait** — fills the most feed space on mobile |
| Slide size | **1080 × 1350 px** (template default). 1:1 / 1080×1080 also valid |
| Slides | **6–10** is the sweet spot (cover + 4–8 content + CTA) |
| Max file | 100 MB / 300 pages (you'll never get near this) |
| Safe margins | Keep text ≥ 64px from every edge; LinkedIn rounds the corners |
| Text size | Big. Headings ≥ 48px, body ≥ 28px — it's read on a phone |

## Structure (the proven shape)

1. **Cover / hook (slide 1)** — gradient background. One bold promise or question +
   "Swipe →". This is the scroll-stopper; spend the most effort here. No logo clutter.
2. **Context / why it matters (slide 2)** — set up the problem or the stakes in one
   simple idea. Light background.
3. **Value slides (slides 3–N)** — *one idea per slide.* Number them (01, 02, 03…),
   short heading + 1–2 lines. Don't crowd. Alternate accents (pink → purple → amber).
4. **Proof / example (optional)** — a stat, a result, or a mini case point.
5. **CTA / close (final slide)** — dark or gradient background. Recap in one line + a
   clear next step ("Read the full guide →", "Get in touch →", "We're hiring →") and the
   Versantus wordmark + URL.

Rules of thumb:
- **One idea per slide.** If a slide has two ideas, split it.
- **Continuity:** same footer, slide numbers, and accent rhythm across the deck.
- **Front-load the value.** Assume many people only see slides 1–2.
- **End with one action**, not three.

## On-brand visual recipe for a deck

- **Cover & CTA:** pink→purple `--vs-gradient`, white text, an amber blob/dot for warmth.
- **Content slides:** white or `--vs-mist` background, Ink text, a coloured number chip
  and a thin accent bar. Rotate accent colour per slide (pink, purple, amber).
- **Type:** Outfit for headings & numbers, Open Sans for body. Big and confident.
- **Consistent footer:** small "Versantus" wordmark + slide number, every slide.
- Keep it clean and spacious — the brand is never cramped.

## Copy guidance (see voice-and-tone.md)

- Cover hook = a benefit, a bold claim, or a genuine question. No clickbait.
- Headings in sentence case, punchy. Body in plain, human language — jargon-free.
- British spelling. At most one exclamation mark across the whole deck.
- Write the **post caption** too: a 1–2 line hook that earns the swipe, 2–4 short lines
  of context, a soft CTA, and 3–6 lower-key hashtags
  (e.g. #UXDesign #Drupal #DigitalAgency #Oxford).

## Workflow

1. Decide the **angle** (one topic) and outline 6–10 slides — one idea each.
2. Copy `assets/linkedin-carousel-template.html`. Add/remove `<section class="slide">`
   blocks to match your slide count; edit copy and per-slide accent.
3. Write the cover hook and the CTA first; fill the middle.
4. Export to **PDF** (see below) at 1080×1350 per page.
5. Draft the LinkedIn caption.
6. Run the `brand-guidelines.md` checklist; confirm one idea per slide and big text.

## Exporting the HTML deck to PDF

The template includes `@page { size: 1080px 1350px; margin: 0 }` so each slide prints as
one correctly-sized page.

- **Quick (manual):** open the HTML in Chrome → Print → Destination *Save as PDF* →
  paper size *Custom / match*, margins *None*, *Background graphics ON*. Save, upload to
  LinkedIn as a document.
- **Automated (headless Chrome):**
  ```bash
  chrome --headless --disable-gpu --no-pdf-header-footer \
    --print-to-pdf=versantus-carousel.pdf \
    assets/linkedin-carousel-template.html
  ```
- Verify: PDF has the right number of pages, each is portrait 4:5, backgrounds/gradients
  rendered, and no text is clipped at the edges.

Then on LinkedIn: **Create post → Document (paperclip/"Add a document") → upload the PDF
→ give it a title → publish** with your caption.
