# How to hand your research to an AI so it can actually read it

Your research is on a FigJam or Miro board. Boards are built for humans standing in front of a screen. Exported, they become one enormous flat image with 6pt text, no reading order, and colour doing all the work. A model given that will either fail loudly or — worse — guess quietly.

This page is how to avoid that. It takes about twenty minutes and it is the highest-return twenty minutes in the pre-work.

---

## The one thing that matters most

**Export the text as text, in a companion file.**

Everything else on this page is optimisation. This is the fix.

Alongside your PDF, produce a plain `research.md` (or a Google Doc, or a `.txt`) that contains the *typed contents* of your board: every sticky note, every cluster name, every quote. Not a summary — the actual strings.

You can produce this fast:

- **Miro** → select a frame → *Export* → **CSV**. It gives you every sticky's text. Repeat per frame, paste them into one file under headings.
- **FigJam** → select stickies → copy → paste into a doc. It pastes as text.
- Either → select all in a section, copy, paste, add a heading. Repeat.

A model reading `research.md` will outperform the same model reading a beautiful 40-page PDF export, every time. If you only do one thing on this page, do this.

---

## The PDF, done properly

The PDF is still worth sending — it carries the spatial relationships that the text dump loses. Export it like this:

**One section per page, not one page.**
Frame each stage of your research separately and export frame-by-frame. A single 8000px-wide page becomes unreadable at any zoom a model can use.

**Zoom so the smallest text is comfortably readable.**
Open the PDF. If you have to zoom to read a sticky, so does the model — except it cannot zoom. Re-export bigger.

**Put a typed heading on every frame before you export.**
Not a sticky note. A text element, large, at the top left. `03 — RAW DATA · SURVEY RESULTS`. Frames without headings arrive as an unlabelled pile.

**Page one is a typed index.**
Typed, not stickies. List what is on each page in order. This single page repairs most of what the export breaks:

```
1  Index (this page)
2  Scope card
3  Provisional hypothesis
4  Research questions + brief
5  Methods, and why each
6–9  Raw data — survey (6–7), interviews (8), store reviews + community (9)
10–12  Affinity clusters
13  JTBD statements — full set
14  JTBD statements — filtered, with cuts justified
15  Problem statement (primary + secondary)
```

**Never let colour carry meaning alone.**
If pink stickies mean pain points, a legend page must say so, in text. Half of colour meaning is lost in export and none of it is reliable.

**Keep it under 25 pages.**
Past that, split into `research-part1.pdf` / `research-part2.pdf` and say what is in each.

---

## Order matters — use this one

Hand your research over in the order the work actually happened, whatever that order was for you. If your process was the standard one, that is:

```
Scope card
  → Provisional hypothesis
    → Research questions + brief
      → Methods, with reasons
        → Raw data
          → Affinity clusters
            → JTBD statements
              → Filtered JTBDs (with cuts justified)
                → Problem statement
```

**If your process was not this, say so up front.** Many real processes loop, restart, or skip. The skill will ask, but telling it first saves a round trip. Write one line at the top of `research.md`: *"My process ran X → Y → back to X → Z. I never did A because B."*

---

## What to actually upload

For any skill in this pack that reads your research:

1. `research.md` — the text dump. **Required.**
2. `research.pdf` — the board export. Optional but useful.
3. Screenshots — for `/molecule-language`, of the app or references. Separate files, not embedded in the PDF.

---

## The check before you send

Open your own `research.md` and read only that. Ask yourself:

> If I had never seen my board, could I tell what the clusters were, what the raw data said, and how the problem statement was reached?

If no, the model cannot either, and it will tell you so with a low intake score. Better to find out now than at the top of Session 1.
