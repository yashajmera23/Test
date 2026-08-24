# Blinkit — Home Pantry Tracker — Build Log

> **Superseded by `LOG.md`** (Molades v0.7). Entries through 2026-08-01 were migrated. Use `LOG.md` going forward.

# Blinkit — Home Pantry Tracker — Build Log (v0.3 archive)

**Designer:** [your name]
**Lane:** Project
**AARRR stage:** Retention (Primary) / Revenue (Secondary)
**Started:** 2026-08-01
**Repo:** none
**Live URL:** not yet

---

> **One file. This one.**
>
> Every skill in this pack ends by handing you a block. Append it to the timeline below. Newest at the **bottom** — this log is a story and stories read forward.
>
> Do not tidy it. Do not go back and rewrite an entry because it now looks naive. The naive entry is the evidence that you learned something, and in Session 5 it is worth more than anything you wrote after you already knew the answer.

---

## Standing state

Update these lines in place. This is the only part of the file you overwrite.

```
Lane:            Project
Rung:            5 — Extracted (⚠️ GAPPED)
Artefacts:       PRODUCT_CONTEXT.md [ ] · SPEC.md [ ] · FLOW.md [ ] · design.md [ ] · build [ ] · deployed [ ]
Rounds:          0
Provisional:     Research readiness DECISION (scope card vs HMW drift unresolved) — explore only, do not build on it
Open debt:       Scope card mechanism drift; JTBD filter/cuts absent; Social JTBD outcome assumed; no app-store triangulation; survey cook-dependent count inferred from recruitment
Overrides open:  0
Next command:    /molecule-context
```

---

## Timeline

Nine entry types. Use the tag that is true, not the one that sounds best.

`DECISION` · `PIVOT` · `CRITIQUE` · `CHANGE` · `FAIL` · `WIN` · `OVERRIDE` · `VERIFY` · `OPEN`

<!-- Append below. Newest at the bottom. -->

### `DECISION` — 2026-08-01 · Pre-work · Lane

**Decided:** Project lane
**Rejected:** Experiment lane
**Because:** Case study — intend to finish and show this work
**Confidence:** assumed
**Provisional:** no

### `OPEN` — 2026-08-01 · App-store triangulation never collected

**Question:** What do Blinkit / Instamart / Zepto store reviews say about stockouts, reminders, cart minimums, and cook-driven reordering?
**Blocks:** Secondary triangulation named in the research plan; claims about notification fatigue and cart friction rest on interview + survey only
**Owner:** you

### `OPEN` — 2026-08-01 · JTBD cuts trail not produced

**Question:** Which candidate jobs were considered and dropped, and why did these three survive?
**Blocks:** Defensibility of Functional / Emotional / Social JTBD in critique
**Owner:** you

### `DECISION` — 2026-08-01 · Pre-work · Research readiness audit

**Decided:** Entering the build phase at rung 5 with the verdict ⚠️ GAPPED. Intake: Legibility 4/5 · Substance 4/5. Scope: drifted (mechanism) — scope card not yet rewritten.
**Rejected:** “Early auto-reminder / virtual shelf alone is the retention fix” as an unverified carry-forward from the original hypothesis; Social JTBD outcome clause as `observed`.
**Because:** Cart/low-value chain holds (survey Q3 + P2 AAA). Fail-to-act holds (P2). Filter stage absent. Social “seen as responsible / drops the ball” has no cite in the handoff. Emotional “what’s next” anxiety is inferred. Several quotes named in audit were not in uploaded atomic notes.
**Confidence:** inferred
**Provisional:** yes

### `OPEN` — 2026-08-01 · Will the scope card hypothesis be rewritten to match Insight 2 + cart bundling, or will the HMW move back?

**Question:** Which document is wrong — scope card feature/hypothesis, or problem statement — and what is the one-sentence updated hypothesis if the card changes?
**Blocks:** PRODUCT_CONTEXT and every downstream claim about what the product does
**Owner:** you

---

### `DECISION` — [YYYY-MM-DD] · [Session/Stage] · [Title]

**Decided:**
**Rejected:**
**Because:**
**Confidence:** observed / inferred / assumed
**Provisional:** yes / no

> A decision entry is not valid without a rejected alternative and a reason. "Chose bottom nav" is a note. "Chose bottom nav over a hamburger because three of the five JTBDs are reached in under two taps, and the hamburger hid all of them behind one" is a decision. Only the second survives an interview.

---

### `PIVOT` — [YYYY-MM-DD] · [Stage] · [Title]

**Was:**
**Now:**
**What forced it:** [the specific finding, test result, or critique]
**What became worthless:** [the work this threw away — be honest, this number is the point]
**What survived:**

> A pivot is not a decision that changed. It is a decision that changed **and invalidated work downstream of it.** If nothing downstream died, it was a revision — log it as `DECISION`. Pivots are the most valuable entries in this file, and the ones students hide.

---

### `CRITIQUE` — [YYYY-MM-DD] · [Stage] · Source: [self / grill / model / peer / user / facilitator]

**Finding:**
**Severity:** blocker / major / minor
**Root layer:** object model / flow / state / surface
**Action:** fixed / deferred / rejected
**Reasoning:**

> Log it even when you disagree. **Especially** when you disagree — a critique you rejected with a stated reason is stronger evidence of judgement than one you accepted without thinking.

---

### `CHANGE` — [YYYY-MM-DD] · [Stage]

**Changed:**
**Caused by:** [the `CRITIQUE` or `VERIFY` entry above that forced it]
**Type:** decision / pixel
**Result:**

> Every change needs a cause pointing at an earlier entry. A change with no cause is polish, and polish is not evidence. `decision` means the thing the product does is now different. `pixel` means it looks different. Both are legitimate. Only one counts toward a round.

---

### `FAIL` — [YYYY-MM-DD] · [Stage] · [Title]

**Tried:**
**Expected:**
**Actually happened:**
**Cost:** [time, or what it blocked]
**What you now know that you did not:**

> Log the ones that were your fault. Especially those. A build that broke, a prompt that produced garbage, a research method that returned nothing usable, a whole afternoon lost to a setup problem. In Session 5 this is the section that makes the case study believable — every real project has these and every fake one does not.

---

### `WIN` — [YYYY-MM-DD] · [Stage] · [Title]

**What worked:**
**Why it worked:** [the mechanism, not the feeling]
**Reusable?** [would this work on the next project, or was it specific to this one]

> "Why it worked" is the whole entry. "The onboarding flow tested well" is a mood. "Three of three testers completed signup without asking a question, because the plan choice was moved after the first success instead of before it" is a mechanism you can use again.

---

### `OVERRIDE` — [YYYY-MM-DD] · [Stage]

**Skipped:** [what was missing]
**Proceeded because:** [your reason — "no time" is an acceptable reason, honestly stated]
**Unverified as a result:** [which claims now rest on nothing]
**Closed on:** [date you fixed it, or "open"]

> This section is not a confession. Constraints are real. What separates a designer from someone who guessed is knowing exactly which parts of the work rest on nothing, and saying so before anyone asks. An override with no entry here is the only kind that hurts you.

---

### `VERIFY` — [YYYY-MM-DD] · [Stage] · [What was tested]

**Method:** [usability session / state sweep / accessibility pass / heuristic walk]
**Participants:** [n, and who they actually were — or "n/a"]
**Held up:**
**Broke:**
**Confidence after:** observed / inferred / assumed

---

### `OPEN` — [YYYY-MM-DD] · [Question]

**Question:**
**Blocks:** [what cannot proceed until this is answered]
**Owner:** [you / facilitator / engineering / nobody yet]

> Close these by editing the entry and adding `**Closed:** [date] — [answer]`. Do not delete them. An open question that was answered is a decision with a paper trail.

---

## The Session 5 test

In Session 5 you assemble your case study from this file and nothing else. No memory, no reconstruction.

If you can do it in ninety minutes, the log worked.

If you find yourself trying to remember what happened in Week 1, it didn't — and the case study you write from memory will come out as process language, which is exactly what gets a portfolio rejected. Process language is what people write when they have forgotten the specifics and are describing the shape of the work instead of the work.

**The three entries that make a case study, in order of value:** the `PIVOT` that cost you the most, the `FAIL` you caused yourself, and the `CRITIQUE` you rejected and were right to reject. Everything else is context around those.
