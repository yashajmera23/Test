# Blinkit — Home Pantry Tracker — Build Log

**Project:** Home Pantry Tracker feature for Blinkit (quick commerce)
**Started:** 2026-08-01

> The skills write to this file. Newest entry at the bottom.

---

## Where things stand

```
Bet:        Auto pantry tracking + reminders will improve D14 retention — but research shows the real break is fail-to-act + cart minimum, not early warning alone (scope drift — not yet rewritten)
Evidence:   thin — ⚠️ GAPPED at synthesis stage; n=2 interviews; survey n=15 (12 cook-dependent inferred from recruitment)
Files:      SCOPE.md [x] · RESEARCH.md [x] · BRIEF.md [x] · DESIGN_LANGUAGE.md [x] · build [x] · live [x]
Rounds:     0
Open:       Scope card vs problem statement drift; JTBD cuts trail missing; no app-store triangulation; Social JTBD outcome assumed
Next: /molades-brief confirm → /molades-build (attack fixes)
```

---

## Entries

### DECISION · 2026-08-01 · molades-start (migrated from v0.3)
**Decided:** Project lane — case study, intend to finish and show
**Rejected:** Experiment lane
**Because:** Student stated they want to complete this as a case study project
**Confidence:** assumed

### DECISION · 2026-08-01 · molades-research (migrated from v0.3 audit)
**Decided:** Enter build phase at synthesis stage with verdict ⚠️ GAPPED — research usable but thin on filtering and scope alignment
**Rejected:** “Early auto-reminder / virtual shelf alone is the retention fix”; Social JTBD “seen as responsible” clause as observed
**Because:** Cart/low-value chain holds (survey Q3 + P2 AAA). Fail-to-act holds (P2). Filter stage absent. Social outcome has no cite. Emotional “what’s next” anxiety is inferred. Several quotes named in audit were not in uploaded atomic notes.
**Confidence:** inferred

### LEARNED · 2026-08-01 · molades-research
**Believed:** The problem is lack of early stockout warning (virtual shelf + reminders)
**Found:** Cook already warns 1–2 days early; user forgets to act. Cart ₹150 minimum blocks single low-value reorders. Lead time is category-dependent.
**Changed:** Problem shifted from “notify earlier” to “convert awareness into bundled action”
**What this made worthless:** Scope card hypothesis as written — needs deliberate rewrite before build

### DECISION · 2026-08-01 · molades-define
**Decided:** Running low section inside Order Again; 4 screens (Running low, Bundle review, Kitchen setup, inherited Checkout); bundle only surfaces at ≥ ₹150; Blinkit-only tracking as retention bet
**Rejected:** Home entry point; new bottom-nav tab; sub-₹150 partial bundle UI; cross-platform import; manual pantry entry; cook/flatmate accounts
**Because:** Screenshots show Order Again already has category-grouped reorder; research shows single low-value alerts useless and cart minimum is systemic blocker; P1 cross-platform behaviour means Blinkit-only tracking incentivises consolidation
**Confidence:** inferred

### DECISION · 2026-08-01 · molades-language
**Decided:** Blinkit-matched language — green #318616 accent, 8pt spacing, 12px card radius, spacious consumer density, Order soon status in Bought Earlier blue pill style; system font stack substitute
**Rejected:** Amber urgency pills; Gift Card serif/decorative styling; yellow promo gradients on product surfaces; drop shadows on cards
**Because:** Feature must look native inside Order Again; Bought Earlier pill is existing repurchase signal; product grids use bordered flat cards not elevated shadows
**Confidence:** inferred

### LEARNED · 2026-08-01 · molades-language
**Rounds run:** 2
**Biggest gap between round 1 and final:** Section heading size and card padding — first probe read slightly heavier than Blinkit product rows
**Did not close:** Custom Blinkit typeface — using system stack substitute; letterforms won't match exactly

### DECISION · 2026-08-01 · molades-build
**Decided:** Slice 1 — Order Again with Running low section + Bundle review sheet; single HTML file in `docs/`; Gilroy fonts; states switchable via demo bar (ready, loading, error, empty, kitchen setup)
**Rejected:** Framework/build step; greyscale pass; single-shot full app; invented product data without sample labels
**Because:** DESIGN.md defines two places for first slice; LANGUAGE.md + probe provide grounded styling; stack must open by double-click for case study deploy
**Confidence:** inferred

### LEARNED · 2026-08-01 · molades-build
**Tried:** Kitchen setup modal on first visit via localStorage
**Expected:** User completes setup once then sees Running low
**Actually happened:** Modal correctly blocks interaction until Save — works as designed
**Cost:** n/a
**Now know:** Demo state switcher needed for portfolio to show empty/loading without clearing localStorage

### CHANGE · 2026-08-01 · molades-build
**Changed:** Deployed interactive prototype to `docs/index.html` (GitHub Pages)
**Caused by:** molades-build slice 1 complete
**Result:** Live URL at https://yashajmera23.github.io/Test/

### CHANGE · 2026-08-01 · molades-language
**Changed:** LANGUAGE.md and probe now use Gilroy (Light, Regular, Medium, Bold, Heavy) from `fonts/`
**Caused by:** Student supplied Gilroy font files
**Result:** Type scale dimension closed; probe re-rendered as `probe-round3-gilroy.png`

### LEARNED · 2026-08-21 · pack-update
**Believed:** Skills matched the previous 12-step spine (define / synthesise / stress / craft / challenge).
**Found:** Course blocks 01–13 shipped — Ideas, Ideas-with-AI, Brief, Attack, Test replace/reshape several steps; files are BRIEF.md and DESIGN_LANGUAGE.md.
**Changed:** Installed block pack as Cursor skills; old commands alias to new ones. Project DESIGN.md / LANGUAGE.md copied to BRIEF.md / DESIGN_LANGUAGE.md.
**What this made worthless:** Nothing in the Blinkit build — next step is still attack/stress on the live prototype (`/molades-attack`).

### DECISION · 2026-08-21 · molades-ideas
**Decided:** Restart at Ideas against the problem statement (act on low-stock without manual track / single low-value orders). Prior brief/build parked until one idea is chosen here.
**Rejected:** Treating the already-built pantry tracker as the locked idea without running Ideas rounds
**Because:** Student asked to go back to Ideas with the new block
**How sure:** worked it out

### DECISION · 2026-08-21 · ideas
**Decided:** Idea 1+3 — remember what they ordered, show running-low, soft optional household-size ask (not a setup wall)
**Rejected:** Idea 2, 5 (same move); Idea 4 as separate product (folded as quiet notch); Idea 7, 10, 11 (not competing); Idea 8 (cart confusion); Idea 9 (too much effort); Idea 6 and paths A/B (student locked normal 1+3)
**Because:** Student: currently the idea is good; A/B made it look like different ideas — keep normal 1+3
**How sure:** worked it out

### DECISION · 2026-08-21 · ai
**Decided:** Level = model does, person checks. Surface = draft bag from Order Again + rare nudge. Control = what it remembers (Blinkit only), how sure (soft guess, no numbers), teaching (remove softens; manual repurchase can bring back)
**Rejected:** Person-only; suggest-only; silent auto-order. Chat box. Wrong-state empty for new users / half bag / out-of-date. “Based on N orders” copy. Forever-ban on remove
**Because:** Student — draft bag check/remove; open from Order Again; nudge only when it matters; new users see nothing; teach without irritating; repurchase can restore
**How sure:** worked it out

### DECISION · 2026-08-21 · brief
**Decided:** Shape = sheet + Order Again entry; name = Running low; screens = Order Again, Running low sheet, Cart, Checkout; main path 5 steps (open → check → Add all to cart → checkout → pay); show only when enough items (≥2 guessing)
**Rejected:** Full pantry flow; section-only with no sheet; Draft bag / Separate cart naming; pay on sheet; empty/half sheet for thin lists; fridge knowledge, auto-order, cook login
**Because:** Student — sheet with re-entry if closed; Running low name; Add all to cart after check; hide when not enough items
**How sure:** worked it out

### DECISION · 2026-08-21 · molades-language
**Decided:** Keep matched Blinkit language (Gilroy, #318616, 8pt, sheet + Order Again). Primary sheet CTA copy = Add all to cart. Fridge/pantry opening animation parked.
**Rejected:** Rebuilding language from scratch without re-pasted screens; fridge theatre as default motion; amber urgency pills
**Because:** Student — screens already shared earlier; park fridge, ship the sheet first
**How sure:** worked it out (language saw it in prior match; fridge park = student choice)

### LEARNED · 2026-08-21 · molades-language
**Rounds run:** 3 (prior session) — reused, not re-looped
**Biggest gap between round 1 and final:** density / heading size (prior)
**Did not close:** Original Blinkit screenshot files not in repo now — values from DESIGN_LANGUAGE.md; re-paste if anything looks wrong in build

### DECISION · 2026-08-23 · build
**Decided:** Slice 1 — Order Again with Running low **entry** + Running low **sheet** (check, remove, Add all to cart). Demo states: ready, loading, error, not enough (no entry), nudge. Kitchen setup wall removed. Fridge motion not built.
**Rejected:** Full list on Order Again; Order what's running low CTA; kitchen setup modal; pay on sheet; inventing live Blinkit stock data
**Because:** BRIEF.md shape + words; DESIGN_LANGUAGE.md tokens; sample items labelled as sample
**How sure:** worked it out

### LEARNED · 2026-08-23 · build
**Tried:** Keep old inline Running low cards + new sheet
**Expected:** Match brief “entry opens sheet”
**Actually happened:** Old build put the full list on Order Again — contradicted brief priority (list lives on sheet)
**Cost:** full rewrite of docs/index.html
**Now know:** Entry must be a summary control; checklist only on the sheet or people skip the check step

### CHANGE · 2026-08-23 · build
**Changed:** Student confirmed slice 1 runs and looks good (entry → sheet → Add all to cart)
**Caused by:** Student test of https://yashajmera23.github.io/Test/ / docs/index.html
**Result:** Ready for /molades-attack — Cart/Checkout inherited, not in this slice

### CRITIQUE · 2026-08-23 · attack · Source: self
**Finding:** Add all footer not sticky under long lists — scrolls away with sheet
**Severity:** major
**Layer:** moments
**Action:**

### CRITIQUE · 2026-08-23 · attack · Source: self
**Finding:** Can Add all with 1 item still in open sheet (&lt; enough threshold)
**Severity:** major
**Layer:** steps
**Action:**

### CRITIQUE · 2026-08-23 · attack · Source: self
**Finding:** Longer-life staples filter not specified in build — research constraint not encoded
**Severity:** major
**Layer:** the bet / things
**Action:**

### DECISION · 2026-08-23 · attack
**Decided:** Drop Running low error sheet. Keep scroll for many items. Nudge stays but must match Blinkit (await screenshots). Order Again suggestions persist after Add all; empty Running low still shows normal suggestions not labelled Running low. Remove concept → Home nudge only (draft — awaiting confirm).
**Rejected:** Designing a custom error sheet; hiding Order Again Running low after cart add
**Because:** Student — not in Blinkit system; want suggestions always; remove from nudge on home
**How sure:** worked it out (confirm pending on remove-only-on-nudge)

