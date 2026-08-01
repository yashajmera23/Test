# Blinkit — Home Pantry Tracker — Build Log

**Project:** Home Pantry Tracker feature for Blinkit (quick commerce)
**Started:** 2026-08-01

> The skills write to this file. Newest entry at the bottom.

---

## Where things stand

```
Bet:        Auto pantry tracking + reminders will improve D14 retention — but research shows the real break is fail-to-act + cart minimum, not early warning alone (scope drift — not yet rewritten)
Evidence:   thin — ⚠️ GAPPED at synthesis stage; n=2 interviews; survey n=15 (12 cook-dependent inferred from recruitment)
Files:      SCOPE.md [x] · RESEARCH.md [x] · DESIGN.md [x] · LANGUAGE.md [x] · build [x] · live [x]
Rounds:     0
Open:       Scope card vs problem statement drift; JTBD cuts trail missing; no app-store triangulation; Social JTBD outcome assumed
Next:       /molades-stress
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
