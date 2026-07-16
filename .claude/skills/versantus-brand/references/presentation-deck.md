# Versantus — Presentation / Slide Decks

How to build an on-brand slide deck (webinar, Lunch & Learn, pitch, all-hands). Always
start from `assets/presentation-template.html` — don't improvise a deck from scratch, or
the look drifts (dark-everything, small type, weak numbering). This page is the spec that
keeps every deck consistent.

## Format

- **16:9, 1280×720** base canvas; the template auto-scales to any screen.
- Self-contained HTML: keyboard nav, click nav, speaker notes, fullscreen, print-to-PDF.
- Export to PDF with **P** (or Chrome → Print → Save as PDF, margins None, backgrounds ON).

## The look (non-negotiable — this is what keeps decks strong)

1. **White / mist is the default surface.** Dark and gradient are *accents*, not the base.
   A deck that's dark on every slide is off-brand and flat. Rhythm to aim for:
   - **Gradient** → title and closing only (plus the odd big-finish slide).
   - **Section dividers** → mist, with the large gradient number.
   - **Content** → alternate white and mist.
   - **Dark (`#20212C`)** → 2–4 "statement" moments across the whole deck, for contrast.
2. **Headlines dominate.** Outfit **800**, big (h1 ≈ 76px, h2 ≈ 52px), tight leading,
   negative tracking. Don't shrink them to fit — cut words instead.
3. **The big gradient number is the signature.** Every section divider gets one
   (`01`, `02`…) in the pink→purple gradient. This is the "clever numbering" — use it.
4. **Amber is a spark.** The accent bar, an underline, divider/takeaway numerals. Never a
   background, never body text on white.
5. **Only brand colours.** Pink, purple, amber + ink/paper/mist/dark from `:root`. Do not
   invent shades (no rogue "eggplant", no off-brand navy). If you need a dark, it's
   `#20212C`.
6. **One idea per slide. Lots of whitespace.** Bullets are short prompts you talk to, not
   paragraphs you read out.

## Slide types (classes in the template)

Set a **surface** and (optionally) a **layout** class on each `<section class="slide …">`:

| Surface | Class | Use |
|---|---|---|
| White (default) | *(none)* | Most content slides |
| Mist | `s-mist` | Alternate content; section dividers |
| Dark | `s-dark` | Statement moments, takeaways (sparingly) |
| Gradient | `s-grad` | Title, closing, big finish |

| Layout | Class | What it gives you |
|---|---|---|
| Title | `title` | Eyebrow, big headline, `.lead`, `.meta` (presenter) |
| Divider | `divider` | Large gradient `.num`, eyebrow, section title |
| Statement | `statement` | Centred big headline + one `.lead` line |
| Content | *(default)* | `h2` + `ul.points`, or `.cols`/`.card`, or `ol.takeaways` |
| Closing | `closing` | Headline + `.contact` |

Reusable pieces: `.eyebrow`, `.bar` (amber), `.lead`, `.accent` / `.amber-word` /
`.grad-word` for emphasised words, `ul.points`, `.cols` + `.card`, `ol.takeaways`,
`.quote`, `.statnum`.

## Speaker notes

Add `data-notes="…"` to any slide; press **S** to toggle the notes drawer. Great for
rehearsing and for sharing the deck as a self-explaining file.

## Structure that works

1. **Title** (gradient) — talk title + presenter.
2. **Intro / hello** — one slide, who you are, why it's relevant.
3. **Agenda** — the route, 4–7 items.
4. Repeat per section: **Divider (number)** → 2–4 **content** slides → optional
   **statement** to land the point.
5. **Takeaways** (dark) — the 3–5 things to remember.
6. **Closing** (gradient) — "Any other questions?" + contact.

## Workflow

1. Copy `assets/presentation-template.html`.
2. Outline sections; give each a numbered divider.
3. Fill content slides — one idea each, short bullets, big headline.
4. Write copy in the Versantus voice (`voice-and-tone.md`): clear, warm, jargon-free,
   British English, sentence case.
5. Add `data-notes` for your talking points.
6. Check the surface rhythm (not too dark), then run the `brand-guidelines.md` checklist.
7. Press **P** to save a PDF for sharing.

## Common mistakes (the drift to avoid)

- ❌ Every slide dark → ✅ white/mist default, dark as accent.
- ❌ Small headlines that "fit the text" → ✅ big Outfit 800, fewer words.
- ❌ Faint ghost numbers → ✅ bold gradient divider numbers.
- ❌ New colours (eggplant, navy) → ✅ brand palette only; dark is `#20212C`.
- ❌ Paragraphs on slides → ✅ short bullets, the detail goes in speaker notes.
