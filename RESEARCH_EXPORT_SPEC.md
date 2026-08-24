# How to hand your research over so it can actually be read

Your research is on a FigJam or Miro board. Boards are built for humans standing in front of a screen. Exported, they become one enormous flat image with 6pt text, no reading order, and colour doing all the work. A model given that will either fail loudly or — worse — guess quietly.

This takes about twenty minutes and it's the highest-return twenty minutes in the pre-work.

---

## The one thing that matters most

**Export the text as text, in a companion file.**

Everything else here is optimisation. This is the fix.

Alongside your PDF, produce a plain `research.md` (or a Google Doc, or a `.txt`) containing the *typed contents* of your board: every sticky, every cluster name, every quote. Not a summary — the actual strings.

Fast ways to get it:

- **Miro** → select a frame → *Export* → **CSV**. Gives you every sticky's text. Repeat per frame, paste into one file under headings.
- **FigJam** → select stickies → copy → paste into a doc. It pastes as text.
- Either → select all in a section, copy, paste, add a heading. Repeat.

A model reading `research.md` outperforms the same model reading a beautiful 40-page PDF export, every time. If you only do one thing on this page, do this.

---

## The PDF, done properly

Still worth sending — it carries the spatial relationships the text dump loses.

**One section per page, not one page.** Frame each stage separately and export frame-by-frame. A single 8000px-wide page is unreadable at any zoom a model can use.

**Zoom so the smallest text is comfortably readable.** Open the PDF yourself. If you have to zoom to read a sticky, so does the model — except it can't. Re-export bigger.

**Put a typed heading on every frame before exporting.** Not a sticky. A text element, large, top left. `03 — RAW DATA · SURVEY RESULTS`. Frames without headings arrive as an unlabelled pile.

**Page one is a typed index.** Typed, not stickies. This single page repairs most of what the export breaks:

```
1  Index (this page)
2  Scope card
3  Hypothesis
4  Research questions + methods
5–8  Raw data — survey (5–6), interviews (7), store reviews + community (8)
9–11  Affinity clusters
12  Jobs to be done
13  Problem statement
```

**Never let colour carry meaning alone.** If pink stickies mean pain points, a legend page must say so in text. Half of colour meaning is lost in export and none of it is reliable.

**Keep it under 25 pages.** Past that, split it and say what's in each part.

---

## Order

Hand it over in the order the work actually happened — whatever that order was for you.

**If your process looped, restarted or skipped things, say so up front.** Most real processes do. One line at the top of `research.md`: *"My process ran X → Y → back to X → Z. I never did A because B."* You'll be asked anyway; saying it first saves a round trip and it's a better answer than the tidy version.

---

## What to upload

1. `research.md` — the text dump. **This is the one that matters.**
2. `research.pdf` — the board export. Optional but useful.
3. Screenshots — for `/molades-landscape` and `/molades-language`, of the app and the references. **Separate image files, not embedded in the PDF.**

That last one catches people out. A screenshot inside a PDF export is usually too small and too compressed to extract a colour or a type size from. Send the originals.

---

## The check before you send

Open your own `research.md` and read only that. Ask:

> If I'd never seen my board, could I tell what the clusters were, what the raw data said, and how the problem statement was reached?

If no, the model can't either — and it'll tell you so rather than guessing. Better to find out now than at the top of a session.
