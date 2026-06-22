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

## Caption generator

The caption sits above the carousel in the feed — it does the job of earning the swipe.
Build it from these four parts:

1. **Hook (line 1–2):** the single most interesting promise, claim or question. It must
   stand alone — many people only ever read this line. No "I'm excited to share…".
2. **Context (2–4 short lines):** why it matters, in plain language. One line breaks.
3. **Swipe prompt + CTA:** point at the carousel, then one clear next step
   ("Swipe through for the 5 signs 👇", then "Need a hand? Let's talk →").
4. **Hashtags:** 3–6, lower-key and relevant. Group on the last line.

Rules: British spelling, sentence case, ≤1 exclamation mark, 1–4 emoji max, jargon-free,
warm and confident (see `voice-and-tone.md`). Keep it tight — the first ~2 lines show
before "…more".

### Ready-made example captions

**Insight / educational deck**
> Your website should be your hardest-working team member.
>
> But slow load times, clunky navigation and a poor mobile experience quietly send
> customers to your competitors — every single day.
>
> We pulled together 5 signs your site might be holding you back (and what to do about each).
>
> Swipe through 👉 and if any of them sound familiar, let's have a chat →
>
> #WebDesign #UXDesign #Drupal #DigitalAgency #Oxford

**Project / launch deck**
> New site, live today. 🎉
>
> We worked with [Client] to turn a slow, hard-to-update website into a fast, accessible
> platform their whole team loves running.
>
> Here's how we did it, slide by slide 👇
>
> Got an ambitious project in mind? Say hello →
>
> #CaseStudy #WebDevelopment #UX #Drupal #Oxford

**Culture / hiring deck**
> We've just been named one of the UK's Best Workplaces in Tech. Here's what that
> actually feels like day to day.
>
> Swipe for a look behind the scenes at life at Versantus 💜
>
> We're growing, too — if it sounds like your kind of place, get in touch →
>
> #LifeAtVersantus #Hiring #TechCulture #Oxford

**Thought-leadership / opinion deck**
> "Make it pop" isn't a brief. 😅
>
> Good design isn't decoration — it's the difference between users who get it and users
> who bounce. Here are 6 principles we come back to on every project.
>
> Swipe through 👉 which one does your site get wrong most often?
>
> #DesignThinking #UX #BrandDesign #DigitalAgency

> Swap `[Client]`, stats and links for the real thing. Match the caption's hook to the
> carousel's cover slide so they reinforce each other.

## Aspect ratios — 4:5 and 1:1

Two ready-made templates, same brand system:

- **`assets/linkedin-carousel-template.html` — 4:5 portrait (1080×1350).** Default. Fills
  the most feed space on mobile; best for most carousels.
- **`assets/linkedin-carousel-square-template.html` — 1:1 square (1080×1080).** Use when
  the content is also going to Instagram, or when you want a tighter, more compact deck.

Pick one ratio and keep it consistent across the whole deck — never mix page sizes in a
single PDF. Both export to PDF the same way (below).


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
