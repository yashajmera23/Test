# Molades — the command sheet

**Thirteen skills, one chain.** Molecule Academy of Designers.

---

## You only need to remember one thing

Say **"let's begin"**, or run `/molades-start`.

Everything else happens on its own. Every skill ends by naming the next command.

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
  /molades-scope ──────────► SCOPE.md              the bet
        ▼
  /molades-landscape ──────► SCOPE.md              what already exists
        ▼
  /molades-research ───────► RESEARCH.md           plan it, or check it
        ▼
        └── go and collect the data ──┐
                                      ▼
  /molades-making-sense ───► RESEARCH.md           notes → clusters → problem
        ▼
  /molades-ideas ──────────► BRIEF.md (ideas)      one idea that survives
        │
        └── or /molades-ideas-ai ──► AX Spec       when the answer is a model
        ▼
  /molades-brief ──────────► BRIEF.md              screens, path, states
        ▼
  /molades-language ───────► DESIGN_LANGUAGE.md    look + test screen
        ▼
  /molades-build ──────────► something openable    full colour, first screen
        ▼
  /molades-attack ─────────► stress + craft tables break it, then measure it
        ▼
  /molades-build ──────────► rebuild from the brief
        ▼
  /molades-test ───────────► findings in LOG.md    real people, real tasks
        ▼
  /molades-case ───────────► CASE_STUDY.md         assembled from LOG.md
```

`LOG.md` is written by the skills at every step.

---

## Every command

| # | Command | What it does | Writes |
|---|---|---|---|
| 1 | `/molades-start` | Where you are → one next step | `LOG.md` |
| 2 | `/molades-scope` | Idea → the bet | `SCOPE.md` |
| 3 | `/molades-landscape` | Competitors: convention, divergence, gaps | `SCOPE.md` |
| 4 | `/molades-research` | Plan research, or check what you collected | `RESEARCH.md` |
| 5 | `/molades-making-sense` | Notes → clusters → problem statement | `RESEARCH.md` |
| 6 | `/molades-ideas` | Constraint rounds → one surviving idea | `BRIEF.md` |
| 7 | `/molades-ideas-ai` | Replaces Ideas when the answer is a model | AX Spec |
| 8 | `/molades-brief` | Shape, screens, main path, imperfect states | `BRIEF.md` |
| 9 | `/molades-language` | References → matched design language | `DESIGN_LANGUAGE.md` |
| 10 | `/molades-build` | Full-colour prototype from your files | code / URL |
| 11 | `/molades-attack` | Stress + craft + accessibility, five fixes | `BRIEF.md` / log |
| 12 | `/molades-test` | Real people try to finish the job | `LOG.md` |
| 13 | `/molades-case` | Case study from the log only | `CASE_STUDY.md` |
| — | `/molades-where` | Status block + next command | — |

### Kept for older logs

| Old command | Now runs |
|---|---|
| `/molades-synthesise` | `/molades-making-sense` |
| `/molades-define` | `/molades-brief` |
| `/molades-stress` | `/molades-attack` |
| `/molades-craft` | `/molades-attack` |
| `/molades-challenge` | `/molades-attack` |

---

## Your files

| File | What it is |
|---|---|
| `LOG.md` | Decisions, changes, learned, critiques. Case study source. |
| `SCOPE.md` | The bet + landscape |
| `RESEARCH.md` | Plan, data, clusters, problem statement |
| `BRIEF.md` | Idea trail + screens + path + states |
| `DESIGN_LANGUAGE.md` | Type, spacing, colour, shape, density |
| `CASE_STUDY.md` | Assembled at the end |

Older projects may still have `DESIGN.md` / `LANGUAGE.md` — those map to `BRIEF.md` / `DESIGN_LANGUAGE.md`.
