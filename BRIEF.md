# BRIEF

**Project:** Blinkit — Home Pantry Tracker  
**Date:** 2026-08-21  
**Solving:** How might we help urban working professionals who depend on their cook for kitchen management to act on low-stock signals before things run out — without requiring them to manually track or place single low-value orders — so they feel in control of their household even when they're not physically present in the kitchen?  
**What this means for design:** Convert awareness into action without manual tracking or lonely low-value orders — not “notify earlier” alone.

## Constraints
1. Stuck with Blinkit's cart minimum and existing checkout — adding a room, not rebuilding the house. *(saw it — student confirmed)*
2. “Away from kitchen” dropped for now — the squeeze is low cart value. *(worked it out — student)*
3. Blinkit does **not** know what's in the kitchen or what the cook bought elsewhere — nothing pretends it sees the fridge. *(saw it — student corrected)*
4. Guardrail: pantry tracking stays useful if they keep ordering on Blinkit — that's the retention hook. *(worked it out — student)*
5. Works without the cook installing anything. *(saw it — student confirmed)*

## Ideas
| # | Idea | The move underneath | Round | Out of ten |
|---|---|---|---|---|
| Idea 1 | Keep a list of what they ordered, warn before runout, one tap into cart | give it memory + remind at a time | obvious | 8 |
| Idea 2 | Push: “milk finishes in a few days” with Add | remind at a time | obvious | 9 |
| Idea 3 | A “Running low” strip on home | make the invisible visible | obvious | 8 |
| Idea 4 | Optional “how many people at home?” to guess usage | let the person teach it | obvious | 6 |
| Idea 5 | Same low items in Order Again, ready to re-add | show what you did last | obvious | 8 |
| Idea 6 | “Remind me on the next order”; surface when bag clears ₹150 | defer the decision / change when it happens | Round 2 | 3 |
| Idea 7 | After every order, optional “reorder milk in 10 days?” — no ongoing shelf | change when it happens | Round 2 | 4 |
| Idea 8 | Cart opens already holding cheap staples over the minimum | remove the choice | Round 2 | 4 |
| Idea 9 | Paste/forward cook’s list → cart over ₹150 | change who starts it | Round 2 | 3 |
| Idea 10 | Lonely item: “₹40 alone — add these two, you’re over ₹150” | make the cost visible | Round 2 | 4 |
| Idea 11 | Standing order tops up on a fixed day | let the system decide | Round 2 | 3 |

## Thrown away, and why
| # | Idea | Why it went |
|---|---|---|
| Idea 2 | Push when milk’s low | Same move as Idea 1+3; nine-out-of-ten first-minute idea |
| Idea 5 | Low items in Order Again alone | Same move as Idea 1+3 |
| Idea 4 (as separate product) | Household-size setup wall | Folded into Idea 1+3 as a quiet optional notch — not its own idea |
| Idea 7 | One-shot reorder schedule | Left on the table — not competing this round |
| Idea 8 | Cart pre-fill staples | Student: creates confusion in cart |
| Idea 9 | Paste cook’s list | Student: too much effort for a quick-delivery app |
| Idea 10 | Show cost-to-minimum at lonely item | Left on the table — not competing this round |
| Idea 11 | Standing order | Left on the table — not competing this round |
| Idea 6 | Remind me on next order @ ₹150 | Lost the final pick — student kept normal Idea 1+3; A/B effort add-ons rejected |
| Paths A & B | One-tap from notification / park until next order on top of 1+3 | Student: both looked like different ideas; locked normal 1+3 |

## What survived
**Winner: Idea 1+3** — virtual memory of what they ordered, shown as running-low (e.g. home / Order Again), with a soft optional household-size ask (not prominent, skippable).  

**Lost:** Idea 6 — deferred “next order” bundling past ₹150. Student chose the normal tracker + surface path over attaching A/B effort shortcuts.

## Open
- Predicting “finishes in a few days” without knowing the kitchen is a model guess — Block 7 (Ideas when a model is involved) is next if we keep that prediction.
- Scope card still drifts vs fail-to-act + cart-minimum insight; Idea 1+3 leans early-warning again — flag for brief.
- Rounds 3–4 not run — student stopped after Round 2 pick.
