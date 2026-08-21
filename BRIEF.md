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
- Scope card still drifts vs fail-to-act + cart-minimum insight; Idea 1+3 leans early-warning — watch in the brief.
- Rounds 3–4 not run — student stopped after Round 2 pick.
- Soft household-size ask still optional; not in AX Spec as required input.

---

# AX SPEC — Running-low draft bag (Idea 1+3)

**What the model does:** guesses which Blinkit staples might be running low  
**How much it does alone:** model does it, person checks — because awareness already exists (cook warns); the boring part is building the list; silent auto-order is unsafe when Blinkit can’t see the fridge  
**What it looks like:** draft bag pre-filled — open manually from Order Again, or from a nudge only when it matters; remove what’s wrong — not a chat box  
**Material facts:** refresh when they open the bag or get a nudge (not every scroll) · guess from Blinkit history only · wrong often and will sound sure · no fake precision numbers

## When it's wrong
| State | What they see | The words on screen | What they can do |
|---|---|---|---|
| Wrong | Item on the draft bag that isn’t actually low | “Not running low? Remove it.” | Remove; teaches softly |
| Not sure | Soft wording, no counts | “Might be running low” | Keep or remove — no “based on N orders” |
| Slow | Loading / skeleton while bag builds | “Building your running-low bag…” | Wait, or use Order Again as usual |
| Won’t | Nothing | — | New users: do not show a bag or empty state |
| Half done | Nothing | — | Do not show a half bag; only show when there’s a real list |
| Out of date | n/a | — | Dropped — not in this project |

## Staying in control
| | How it works | Where it appears |
|---|---|---|
| What it remembers | Only Blinkit orders — not fridge, not outside buys | Implicit in how the bag is built; Order Again already shows repurchase |
| How sure it is | Guess from past orders + usual finish times; soft “might,” no scores | On items / bag copy |
| Teaching it | Remove = not needed right now — don’t re-push irritably; if they order that item again themselves, it can return to the guess | Draft bag remove · later repurchase |

**Why the other five matter less here:** Undo is just remove before checkout. Override is covered by teaching. “Where from / why” without numbers would nag. Get a person isn’t a pantry job.  

## Who does what
| The model does → | The person decides → | What's left behind → |
|---|---|---|
| Builds running-low draft bag from Blinkit orders + usual finish times | Open bag (Order Again or rare nudge); remove wrong items; checkout | Edited bag / placed order; removes soft-train; manual repurchase can bring an item back |

## Does it get better
Signal picked up: remove (soften) · manual repurchase (may return) · Effort for the person: none extra (same remove / order they already do)

## The riskiest thing I'm assuming
That a guessed draft bag will get opened and edited often enough to beat “cook already warned me, I still didn’t act” — without becoming another ignored list. · Cheapest way to find out: watch 3–5 cook-dependent people with a clickable bag for one week — count opens, removes, and checkouts from the bag.
