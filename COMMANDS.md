# Molades — the command sheet

**Twelve skills, thirteen commands, one chain.** Molecule Academy of Designers.

---

## You only need to remember one thing

Say **"let's begin"**, or run `/molades-start`.

Everything else happens on its own. Every skill ends by naming the next command, so you're never choosing from a menu — you finish a step, it tells you what's next, you run it.

```
"let's begin"
     ↓
/molades-start ──────────► reads what you have, sends you one place
```

---

## The chain

```
  /molades-start
        │
        ▼
  /molades-scope ──────────► SCOPE.md          the bet
        ▼
  /molades-landscape ──────► SCOPE.md          what already exists
        ▼
  /molades-research ───────► RESEARCH.md       plan it, or check it
        ▼
        └── go and collect the data ──┐
                                      ▼
  /molades-synthesise ─────► RESEARCH.md       notes → clusters → jobs → problem
        ▼
  /molades-define ─────────► DESIGN.md         objects, places, flows, states
        ▼
  /molades-language ───────► LANGUAGE.md       type, spacing, colour + component sheet
        ▼
  /molades-build ──────────► a live URL        full colour, first screen
        ▼
  /molades-stress ─────────► DESIGN.md         break it on purpose
        ▼
  /molades-craft ──────────► DESIGN.md         rulers, contrast, targets
        ▼
  /molades-build ──────────► a live URL        rebuild from the document
        ▼
  /molades-challenge ──────► findings          attack it, route each finding
        ▼
        └── fix → /molades-build → challenge again  (× 3 rounds)
        ▼
  /molades-case ───────────► CASE_STUDY.md     assembled from LOG.md
```

`LOG.md` is written by the skills at every step. You never fill it in.

---

## Every command

| # | Command | What it does | Reads | Writes |
|---|---|---|---|---|
| 1 | `/molades-start` | Works out where you are, sends you one place | everything | `LOG.md` |
| 2 | `/molades-scope` | Idea → the bet: product, feature, stage, metric, user, hypothesis | — | `SCOPE.md` |
| 3 | `/molades-landscape` | Competitive analysis. Convention, divergence, gaps and why they're gaps | `SCOPE.md` | `SCOPE.md` |
| 4 | `/molades-research` | Plans research if you have none, checks it if you do | `SCOPE.md` | `RESEARCH.md` |
| 5 | `/molades-synthesise` | Notes → clusters → jobs → problem statement. AI drafts, you correct | `RESEARCH.md` | `RESEARCH.md` |
| 6 | `/molades-define` | Objects, places, flows, architecture, states. Text, not wireframes | `RESEARCH.md` | `DESIGN.md` |
| 7 | `/molades-language` | References → matched design language, via a build-compare-correct loop | `DESIGN.md` | `LANGUAGE.md` |
| 8 | `/molades-build` | Builds it in full colour, grounded in your files. Ends with a live URL | `DESIGN.md` `LANGUAGE.md` | code, a URL |
| 9 | `/molades-stress` | Breaks it on purpose — Nothing, Too much, Wrong, Waiting | the build | `DESIGN.md` |
| 10 | `/molades-craft` | Visual + accessibility, against rulers not taste. PASS / FAIL / CAN'T TELL | the build | `DESIGN.md` |
| 11 | `/molades-challenge` | Attacks whatever you have, at any stage. Routes findings to the real layer | anything | `LOG.md` |
| 12 | `/molades-case` | Assembles the case study from the log and nothing else | `LOG.md` | `CASE_STUDY.md` |
| — | `/molades-where` | Status: what's done, what's open, what's next | `LOG.md` | — |

---

## Your files

```
SCOPE.md        the bet, and the competitive landscape
RESEARCH.md     plan, data, clusters, jobs, problem statement
DESIGN.md       objects, places, flows, architecture, states
LANGUAGE.md     type, spacing, colour, shape, density
LOG.md          decided / found / changed / learned  ← written for you
CASE_STUDY.md   the output
```

**All uppercase, deliberately.** An earlier version used `design.md` alongside `DESIGN.md` and they collided into one file on macOS.

---

## How it talks to you

Short replies. Plain words. One question at a time, at the end.

If it ever starts sounding like a technical document — long paragraphs, jargon, three questions at once — tell it *"too long, say that again simply"* and it will. That's a bug, not you.

---

## The two rules that never bend

1. **It never invents evidence.** No quotes, no personas, no "users would probably say". If it sounds like user evidence and no human said it, it's fabrication with good grammar.
2. **It won't let you build on a foundation that isn't there.** Two checks, both about foundations: real data before synthesis, a written plan before building.

Everything else is a note and a nudge, never a stop. Getting told your metric is vague doesn't block you — it gets logged and you keep moving.

---

## What it does at every step

```
SHOW     an example from a different project — what good looks like
DRAFT    a first version of yours, wrong in places on purpose
ASK      one question: what's wrong with it?
DECIDE   you change it, and the reason goes in your log
```

**The drafts are wrong deliberately.** Finding what's wrong and saying why is the part you're learning — and *"the first version said X, I changed it to Y because the data said Z"* is a stronger portfolio sentence than anything a blank page produces.

---

## Going backwards is normal

Research that kills your original bet is the **best** thing that can happen in the first three weeks. It gets logged as `LEARNED`, and it's the entry that carries your case study.

When a finding says the problem was wrong rather than the screen, the system routes you back to `/molades-scope` or `/molades-synthesise` instead of patching a screen.

---

## If you're stuck

| Situation | Run |
|---|---|
| No idea where you are | `/molades-where` |
| Lost mid-session | `/molades-start` |
| Something feels wrong and you can't name it | `/molades-challenge` |
| You don't know what a step should produce | Ask for that step's example — every skill has one |

---

## Session map — Product Anatomy Base

Base assumes you already have a problem statement. Commands 2–5 are pre-work.

| Session | Title | Commands |
|---|---|---|
| Pre-work | — | `scope` · `landscape` · `research` · `synthesise` |
| 01 | Spec → First Build | `define` · `language` · `build` |
| 02 | The Iteration Engine | `challenge` · `build` |
| 03 | Craft Pass | `stress` · `craft` · `build` |
| 04 | Feedback & Fix Sprint | `challenge` · `build` |
| 05 | Case Study Assembly | `case` |
| 06 | Present · Verify · Ship | — present and defend it live |

---

## Setup

`Setup_By_Tool.md` — one page per tool. Claude Code is smoothest; everything works everywhere, you just do one mechanical step by hand (screenshot, save a file, paste a block).

Then copy `LOG.md` into your project folder and say **"let's begin"**.
