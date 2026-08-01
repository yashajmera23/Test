# Setup — one page, find your tool

You need four things working before Session 1:

1. Your **AI tool**, with the skills loaded
2. A **GitHub account** — the Project lane starts from a template repo
3. Your **`PROJECT_LOG.md`**, copied into your project folder and shareable
4. Your **`research.md`** text dump, if you already have research — see `RESEARCH_EXPORT_SPEC.md`

Find your tool below. Ignore the rest.

Then say **"let's begin"**. You do not need to memorise any command.

---

## Claude Code (recommended — this is what is demoed in class)

1. Make a folder for your project. Open it in Claude Code.
2. Create `.claude/skills/` and `.claude/commands/`.
3. Copy all fourteen skill folders from `skills/` and all seventeen files from `commands/`.

```
your-project/
  .claude/
    skills/
      MOLADES-master/SKILL.md
      MOLADES-research-plan/SKILL.md
      MOLADES-research-audit/SKILL.md
      MOLADES-context-build/SKILL.md
      MOLADES-ideate/SKILL.md
      MOLADES-spec/SKILL.md
      MOLADES-grill/SKILL.md
      MOLADES-flow/SKILL.md
      MOLADES-design-language/SKILL.md
      MOLADES-grounded-build/SKILL.md
      MOLADES-critique/SKILL.md
      MOLADES-state-sweep/SKILL.md
      MOLADES-iterate/SKILL.md
      MOLADES-case-assembly/SKILL.md
    commands/
      molecule-start.md    molecule-plan.md     molecule-audit.md
      molecule-context.md  molecule-ideate.md   molecule-spec.md
      molecule-grill.md    molecule-flow.md     molecule-language.md
      molecule-build.md    molecule-attack.md   molecule-sweep.md
      molecule-iterate.md  molecule-case.md     molecule-where.md
      molecule-anyway.md   molecule-log.md
  CORE_RULES.md
  QUESTION_BANK.md
  PROJECT_LOG.md       ← your log, filled in header first
  research.md          ← your text dump, if you have research
  research.pdf         ← your board export
  references/          ← screenshots
```

4. Say `let's begin`, or type `/molecule-start`. Everything else routes from there.

**Keep `CORE_RULES.md`, `QUESTION_BANK.md` and `PROJECT_LOG.md` in the project root.** The skills reference them by name and Claude Code reads them off disk when it needs them.

**You are the one setup where the log paste step is nearly automatic** — the log lives in the same folder the agent is working in. Paste it anyway when a skill hands you a block. It is the one habit that survives when you change tools.

---

## Claude Desktop (Projects)

1. Create a Project.
2. Upload to Project knowledge: `CORE_RULES.md`, `QUESTION_BANK.md`, `PROJECT_LOG.md`, your `research.md`, `research.pdf`, and your screenshots.
3. When you want to run a skill, paste the matching file from `adapters/paste/` into the chat.

Do **not** put multiple skills in the Project's custom instructions at once. They bleed into each other and you get a context build when you asked for an audit. One at a time, in the chat.

**No slash commands here.** Say it in words instead — *"run the research audit on my research"* — and paste the block.

**Your log lives as a Project doc.** Edit it in place after every skill run.

---

## Cursor

1. In your project root, create `.cursor/rules/`.
2. Copy the `.mdc` files from `adapters/cursor/` into it.
3. Copy `CORE_RULES.md`, `QUESTION_BANK.md` and `PROJECT_LOG.md` into the project root.
4. They are set to manual invocation — reference them by name: *"Use the MOLADES-research-audit rule."*

Cursor's agent reads your project files directly, so put `research.md` and your screenshots in the project folder before you start.

---

## Codex / Gemini Antigravity / other agentic tools

1. Copy `adapters/AGENTS.md` into your project root.
2. It contains every procedure, separated by headings, with the standing rules at the top.
3. Copy `CORE_RULES.md`, `QUESTION_BANK.md` and `PROJECT_LOG.md` in too.
4. Invoke by name: *"Follow the MOLADES-research-audit procedure in AGENTS.md."*

Most agentic tools read `AGENTS.md` automatically. If yours doesn't, paste the relevant section into chat instead.

---

## ChatGPT (web) / Gemini (web) / anything with no filesystem

1. Open `adapters/paste/` and pick the skill you want.
2. Paste the whole block into a **fresh conversation**. Not a continuing one.
3. Attach or paste your research.
4. If it asks for `QUESTION_BANK.md`, paste that too. It is instructed to ask rather than improvise.

**Three things that will bite you:**

- **Fresh conversation per skill.** These are long instructions. Running a context build in the same thread as your research audit means the audit's conclusions leak in as assumptions. Start clean.
- **No filesystem, so the output files are yours to maintain.** When a skill hands you a block, paste it into `PROJECT_LOG.md` immediately. Not later. Later doesn't happen.
- **No slash commands.** Say them in words. The paste blocks understand `/molecule-anyway` written as text.

---

## Your lane, and what it needs

| | **Experiment** | **Project** |
|---|---|---|
| For | A one-shot test of an idea | Work you intend to finish and show |
| Build | Single HTML file, no build step | Starter repo — framework, Tailwind, design system |
| Design system | None. Utility classes inline. | Full token set and component library |
| Deploy | Same host, drag or push | Git push |
| Case study | Optional | Expected |
| You need | A text editor and a browser | GitHub account, Node installed, the template repo |

**Project lane setup:** open the course starter repo on GitHub, click **Use this template**, name your repo, clone it, `npm install`, `npm run dev`. Connect the repo to Vercel once and every push deploys itself.

Do not switch lanes casually. Experiment → Project means rebuilding.

---

## Everyone — the log

One file. `PROJECT_LOG.md`. Copy it into your project folder, fill in the header, submit the link at Day 0.

Nine entry types: `DECISION` `PIVOT` `CRITIQUE` `CHANGE` `FAIL` `WIN` `OVERRIDE` `VERIFY` `OPEN`. Newest at the bottom. The Standing state block at the top gets overwritten in place; nothing else does.

Google Doc, Notion page, or a markdown file in the repo — doesn't matter, as long as it is one place and it is shareable.

It gets checked at the top of every session, and the check is always the same question: **pick a line, where did this come from?**

---

## When something breaks

Bring the actual transcript to the clinic hour. Not a description of what went wrong — the transcript. Nearly every failure in this pack is a framing problem visible in the first two messages, and it is invisible in a summary.

**Three failures you can fix yourself:**

- **It gave you a low intake score.** That is the system working. Go back to `RESEARCH_EXPORT_SPEC.md` and produce the text dump. Do not `/molecule-anyway` past this one on the first try.
- **It stopped asking questions and started agreeing.** Long runs degrade. Start a fresh conversation, re-paste the skill, and give it the outputs you already have rather than the whole history.
- **It wrote the thing instead of interrogating you about it.** It broke standing rule 1. Say so, point at `CORE_RULES.md`, and make it hand the work back to you. This is the exact behaviour the course exists to teach you to catch.
