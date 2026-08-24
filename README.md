# Molades v0.5

The build system for **Product Anatomy**. Molecule Academy of Designers.
Twelve skills, one log, one running example.

---

## Start here

Say **"let's begin"**. That's it.

The system works out what you've got, tells you where you are, and gives you one next thing to do. You never need to memorise the list below.

---

## How it works

At every step: **you get shown an example, then a first draft of yours, then one question.**

The drafts are wrong in places on purpose. Finding what's wrong and saying why is the part you're actually learning — and it's what your case study is made of. *"The first version said X, I changed it to Y because the data said Z"* is a stronger sentence than anything a blank page produces.

Two things the system won't do:

1. **Invent research you didn't collect.** No quotes, no personas, no "users would probably say". If it sounds like user evidence and no human said it, it's fabrication with good grammar.
2. **Let you build on a foundation that isn't there.** Two checks, both about foundations: real data before synthesis, a written plan before building.

Everything else is a note and a nudge, never a stop.

---

## The twelve commands

| Command | Does |
|---|---|
| `/molades-start` | Works out where you are and sends you one place |
| `/molades-scope` | Turn an idea into a bet — product, feature, stage, metric, hypothesis |
| `/molades-landscape` | Competitive analysis. What exists, and what it means for you |
| `/molades-research` | Plan the research, or check what you've collected |
| `/molades-synthesise` | Notes → clusters → jobs → problem statement |
| `/molades-define` | Objects, places, flows, states. Produces `DESIGN.md` |
| `/molades-language` | References → a design language checked against them |
| `/molades-build` | Build it, in full colour, grounded in your files |
| `/molades-stress` | Break it on purpose — Nothing, Too much, Wrong, Waiting |
| `/molades-craft` | Visual and accessibility pass, against rulers not taste |
| `/molades-challenge` | Attack whatever you have, at any stage |
| `/molades-case` | Assemble the case study from your log |

`/molades-where` gives you a status block any time you're lost.

---

## The path

```
SCOPE → LANDSCAPE → RESEARCH → SYNTHESISE → DEFINE → LANGUAGE → BUILD
  → STRESS → CRAFT → BUILD → CHALLENGE → CASE
```

Left to right is the default, not a law. Going backwards is normal — research that kills your original bet is the most valuable thing that can happen in the first three weeks, and it's the entry that will carry your case study.

---

## Two things worth knowing before you start

**There are no wireframes in this system.** Structure is decided as text in `DESIGN.md`, then built in full colour. Grey boxes take an hour, look nothing like the product, and teach nobody anything.

**`/molades-language` runs a loop.** You give it screenshots of what you want to land near. It extracts the type scale, spacing, colours and shapes, builds a test screen with them, looks at that next to your reference, scores six things, fixes the numbers that are off, and goes again — up to five rounds. You end up with a design language that's been checked against the thing it's copying, plus a component sheet you didn't have to build.

---

## Your files

Four, plus the case study at the end.

```
SCOPE.md      the bet, and what already exists
RESEARCH.md   plan, data, clusters, jobs, problem statement
DESIGN.md     objects, places, flows, architecture, states
LANGUAGE.md     type, spacing, colour, shape, density
LOG.md        everything that was decided, found, changed and learned
CASE_STUDY.md the output
```

**The skills write `LOG.md`. You don't.** In the final session you assemble your case study out of it in ninety minutes instead of writing one from memory. If your tool can't write files, each skill hands you a block to paste — paste it then, not later.

---

## The example project

Every skill uses the same running example: **adding group ordering to Swiggy, with Zomato as the competitor.** If you're ever unsure what a step is meant to produce, ask for that step's example. It's deliberately not your project — it's there so you see the shape of a good answer before you attempt your own.

---

## Setup

See `Setup_By_Tool.md`. One page, find your tool, ignore the rest.

Then:

1. **Copy `LOG.md` into your project folder.**
2. **If you already have research**, read `RESEARCH_EXPORT_SPEC.md` and produce the `research.md` text dump. Twenty minutes, and it's the highest-return twenty minutes in the pre-work.
3. Say "let's begin".

---

## What's in this folder

```
VOICE.md                 How every reply is written. Read this one first.
CORE_RULES.md            The four rules, the one gate, the working loop. Canonical.
LOG.md                   Your log. Copy it into your project.
QUESTION_BANK.md         What a skill asks when it needs to know something.
RESEARCH_EXPORT_SPEC.md  How to hand a Miro/FigJam board over so it can be read.
Setup_By_Tool.md         Installation, one page per tool.

skills/                  Canonical skills — Claude Code, Claude Desktop
commands/                Slash commands for Claude Code
adapters/AGENTS.md       Codex, Antigravity, other agentic tools
adapters/cursor/         Cursor rules (.mdc)
adapters/paste/          ChatGPT web, Gemini web, anything with no filesystem
```

The adapters are generated from `skills/`. If you're editing, edit the skill and regenerate — don't edit an adapter by hand or they'll drift.

---

Bring a broken run to the clinic hour with the actual transcript, not a description of it. Nearly every failure is visible in the first two messages and invisible in a summary.
