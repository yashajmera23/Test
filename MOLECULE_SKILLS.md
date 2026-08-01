# Molecule Skills — v0.3

The build system for **Product Anatomy · Base**. Molecule Academy of Designers.
Fourteen skills, seventeen commands, one log.

Every skill obeys four rules, and they are the whole point:

1. **AI attacks, structures, and pressure-tests. It does not write.**
2. **Agreement is the default and tells you nothing.**
3. **Everything traces to something you actually did.** Pick any sentence: *where did this come from?*
4. **AI never plays the user.** No invented quotes, no simulated interviews, no personas, no "users would probably say". Anything that sounds like user evidence and did not come from a human is fabrication with good grammar.

The skills are deliberately **prose only** — no scripts, no tool calls, no filesystem assumptions. That is what makes them work identically in Claude Code, Claude Desktop, Cursor, Codex, Antigravity, ChatGPT and Gemini.

---

## Start here

Say **"let's begin"**. That's it.

You are in guided mode. The system reads what you already have, tells you where you are, and gives you one next command. You never need to memorise the list below.

The list exists for the other case: a working professional who wants one piece of this pack inside their own process. Every skill also runs standalone.

---

## The spine

```
HYPOTHESIS → RESEARCH → CONTEXT → IDEATE → SPEC → GRILL → FLOW → BUILD → CRITIQUE → ITERATE → VERIFY → NARRATE
```

You cannot skip left in guided mode. Building before context produces the average of everything the model has seen. Verifying before building verifies nothing. Narrating before iterating produces a case study about a first draft.

---

## The commands

| Command | Does | Skill |
|---|---|---|
| `/molecule-start` | Works out where you are and sends you one place | `MOLADES-master` |
| `/molecule-plan` | Design the research you have not done yet | `MOLADES-research-plan` |
| `/molecule-audit` | Is my research finished? Blunt verdict, rung 0–7. | `MOLADES-research-audit` |
| `/molecule-context` | Turn research into a grounded `PRODUCT_CONTEXT.md` | `MOLADES-context-build` |
| `/molecule-ideate` | Twelve concepts, then one chosen and defended | `MOLADES-ideate` |
| `/molecule-spec` | Object model first. Produces `SPEC.md`. | `MOLADES-spec` |
| `/molecule-grill` | Interrogate the spec until it breaks or holds | `MOLADES-grill` |
| `/molecule-flow` | Places, steps, state coverage. Produces `FLOW.md`. | `MOLADES-flow` |
| `/molecule-language` | Turn references into a buildable `design.md` | `MOLADES-design-language` |
| `/molecule-build` | Build it, grounded in the spec and the flow | `MOLADES-grounded-build` |
| `/molecule-attack` | Hostile critique — heuristic walk or panel of three | `MOLADES-critique` |
| `/molecule-sweep` | Every state of every screen | `MOLADES-state-sweep` |
| `/molecule-iterate` | Turn findings into logged rounds | `MOLADES-iterate` |
| `/molecule-case` | Assemble `CASE_STUDY.md` from the log and nothing else | `MOLADES-case-assembly` |
| `/molecule-where` | Status: what's done, what's open, what's next | `MOLADES-master` |
| `/molecule-anyway` | Override a gate and proceed, stamped | any |
| `/molecule-log` | Paste-ready log block for what just happened | any |

Lost? Say `/molecule-start`. It will not ask you what you want to do — it works it out and gives you one command.

---

## Your lane

At the start you pick one, and it changes what gets built.

| | **Experiment** | **Project** |
|---|---|---|
| For | A one-shot test of an idea | Work you intend to finish and show |
| Build | Single HTML file, no build step | Starter repo — framework, Tailwind, design system |
| Design system | None. Utility classes inline. | Full token set and component library |
| Deploy | Same host, drag or push | Git push |
| Case study | Optional | Expected |

Neither is the lesser one. Picking Project for status and then drowning in setup is the worse choice. Switching Experiment → Project means rebuilding, so decide once.

---

## What is in this folder

```
CORE_RULES.md            The four rules, the four gates, the override. Canonical.
PROJECT_LOG.md           Your log. One file. Nine entry types. Copy it into your project.
QUESTION_BANK.md         What a skill asks instead of making something up.
RESEARCH_EXPORT_SPEC.md  How to hand Miro/FigJam research over so it can be read.
Setup_By_Tool.md         Installation, one page per tool.

skills/                  Canonical skills — Claude Code, Claude Desktop
commands/                Slash commands for Claude Code
adapters/AGENTS.md       Codex, Gemini Antigravity, other agentic tools
adapters/cursor/         Cursor rules (.mdc)
adapters/paste/          ChatGPT web, Gemini web, anything with no filesystem
```

---

## The four gates, one paragraph each

**Gate 1 — score before you interpret.** Every skill that reads your material scores it out of 5 for Legibility and Substance *before* touching it. Score 3 or below and it stops and offers three routes: re-upload, answer questions, or `/molecule-anyway`. This exists because a beautiful forty-page board export is often unreadable to a model, and the failure mode is not an error — it is a confident audit of nothing.

**Gate 2 — never move ahead in doubt.** If a skill is unsure what you meant, it asks. One question, waits, continues. One question at a time is literal — the moment it batches five, you answer the easy one and the important one dies. An assumption made silently at context stage is a fabrication three steps later, and by then nobody remembers which line it was.

**Gate 3 — thin brief means questions, not content.** When a required field has no basis in what you gave it, the skill names the field and hands you questions from `QUESTION_BANK.md` — built on Garrett's five planes from *The Elements of User Experience*, with triggers from *Universal Principles of Design*. It does not fill the field in. An empty field with a question next to it is more useful than a filled one nobody chose.

**Gate 4 — every run ends in the log.** A skill run that produced no log entry did not happen. Every skill ends by handing you a paste-ready block for `PROJECT_LOG.md`. This is the step that gets dropped when a session runs long, and it is the one that costs you Session 5.

---

## The log

One file. `PROJECT_LOG.md`. Newest entry at the bottom, because a log is a story and stories read forward.

Nine entry types: `DECISION` `PIVOT` `CRITIQUE` `CHANGE` `FAIL` `WIN` `OVERRIDE` `VERIFY` `OPEN`.

In Session 5 you assemble your case study from this file and nothing else. No memory, no reconstruction. If you can do it in ninety minutes, the log worked.

**The three entries that make a case study, in order of value:** the `PIVOT` that cost you the most, the `FAIL` you caused yourself, and the `CRITIQUE` you rejected and were right to reject. Everything else is context around those.

Do not tidy it. Do not rewrite an entry because it now looks naive. The naive entry is the evidence that you learned something.

---

## `/molecule-anyway`

You can always overrule the system. Say `/molecule-anyway` and it proceeds on what exists.

It pushes back once — one sentence, the specific cost — then complies fully and stamps the output with what was missing. The stamp is the point. An override is a decision, and it goes in your log alongside every other decision you made.

Use it when you need to. A student stuck at a gate learns nothing. A student who overrode a gate and wrote down why has a case study.

---

## Before you run anything

1. **Set up your tool** from `Setup_By_Tool.md`.
2. **Create a GitHub account** if you don't have one. The Project lane starts from a template repo.
3. **Copy `PROJECT_LOG.md` into your project folder** and fill in the header. It is not admin — in Session 5 you assemble your case study out of it instead of writing one from memory. Students who keep it finish.
4. **If you already have research:** read `RESEARCH_EXPORT_SPEC.md` and produce the `research.md` text dump. Twenty minutes, and the highest-return twenty minutes in the pre-work. Then say "let's begin".
5. **If you don't:** just say "let's begin". It will route you to `/molecule-plan`.

Bring a broken run to the clinic hour with the actual transcript, not a description of it.
