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
**Winner: Idea 1+3** — virtual memory of what they ordered, shown as **Running low** (sheet + Order Again entry), soft optional household-size ask (not prominent, skippable). After check → **Add all to cart**.

**Lost:** Idea 6 — deferred “next order” bundling past ₹150. Student chose the normal tracker + surface path over attaching A/B effort shortcuts.

## Open
- Scope card still drifts vs fail-to-act + cart-minimum insight; Idea 1+3 leans early-warning — watch in build/test.
- Rounds 3–4 not run — student stopped after Round 2 pick.
- Soft household-size ask still optional; not a required screen.
- “Enough” items to show Running low: **at least 2** — *guessing*, not measured.

---

# AX SPEC — Running low (Idea 1+3)

**What the model does:** guesses which Blinkit staples might be running low  
**How much it does alone:** model does it, person checks — because awareness already exists (cook warns); the boring part is building the list; silent auto-order is unsafe when Blinkit can’t see the fridge  
**What it looks like:** **Running low** sheet pre-filled — open from Order Again entry or a rare nudge; remove what’s wrong; **Add all to cart** — not a chat box  
**Material facts:** refresh when they open Running low or get a nudge (not every scroll) · guess from Blinkit history only · wrong often and will sound sure · no fake precision numbers

## When it's wrong
| State | What they see | The words on screen | What they can do |
|---|---|---|---|
| Wrong | Item on Running low that isn’t actually low | “Not running low? Remove it.” | Remove; teaches softly |
| Not sure | Soft wording, no counts | “Might be running low” | Keep or remove — no “based on N orders” |
| Slow | Loading / skeleton while list builds | “Building Running low…” | Wait, or use Order Again as usual |
| Won’t | Nothing | — | New users / not enough items: no entry, no sheet |
| Half done | Nothing | — | Do not show a thin list; only show when there’s enough |
| Out of date | n/a | — | Dropped — not in this project |

## Staying in control
| | How it works | Where it appears |
|---|---|---|
| What it remembers | Only Blinkit orders — not fridge, not outside buys | Implicit in how Running low is built; Order Again already shows repurchase |
| How sure it is | Guess from past orders + usual finish times; soft “might,” no scores | On items / sheet copy |
| Teaching it | Remove = not needed right now — don’t re-push irritably; if they order that item again themselves, it can return to the guess | Running low remove · later repurchase |

**Why the other five matter less here:** Undo is just remove before Add all. Override is covered by teaching. “Where from / why” without numbers would nag. Get a person isn’t a pantry job.  

## Who does what
| The model does → | The person decides → | What's left behind → |
|---|---|---|
| Builds Running low from Blinkit orders + usual finish times | Open sheet (Order Again or rare nudge); remove wrong items; Add all to cart; checkout | Cart / placed order; removes soft-train; manual repurchase can bring an item back |

## Does it get better
Signal picked up: remove (soften) · manual repurchase (may return) · Effort for the person: none extra (same remove / order they already do)

## The riskiest thing I'm assuming
That a guessed Running low sheet will get opened and edited often enough to beat “cook already warned me, I still didn’t act” — without becoming another ignored list. · Cheapest way to find out: watch 3–5 cook-dependent people with a clickable sheet for one week — count opens, removes, and Add-all → checkout.

---

## The shape
**Chosen:** Sheet over Order Again **plus** a durable entry on Order Again if they close the sheet. Rare nudge opens the same sheet.

**Costs accepted:** Order Again gets busier; entry and sheet must share the same words (**Running low**) or people think they’re two features. Sheet is easy to dismiss — entry is the insurance.

**Rejected:**
- Its own screens / Pantry flow — too many steps, people drop off, biggest build
- Change-only section with no sheet — too easy to miss the check step before cart

## Words we're using
| We call it | Not | Because |
|---|---|---|
| Running low | Draft bag, pantry tracker, virtual shelf, Separate cart | Survey used “running low”; student locked this name for entry + sheet |
| Might be running low | Predicted empty, % sure, “based on N orders” | Soft guess; no fake precision (AX Spec) |
| Add all to cart | Pay / Checkout on the sheet | Check first, then land in Blinkit cart |
| Order Again | My kitchen, Pantry tab | Hang off a screen that already exists |

## Screens
- **Order Again** — where they find the Running low entry and open the sheet
- **Running low (sheet)** — where they check the guess, remove what’s wrong, Add all to cart
- **Cart** — already exists — where items land after Add all
- **Checkout** — already exists — where they pay

## Where they hang off the existing product
Order Again → Running low entry → sheet. Nudge → same sheet. Add all → Cart → Checkout.

**NOT ADDING:** Pantry tab, pay inside the sheet, cook login, fridge sync, auto-order, empty/half Running low for new or thin lists.

## What's on each screen

### Order Again
**This screen is for:** finding and opening Running low  
**Information, in priority order**
1. Running low entry *(component · only if enough items)*  
2. Existing Order Again content *(already exists)*  
**Not here:** full check list → lives on the sheet

### Running low (sheet)
**This screen is for:** checking the guess, then adding to cart  
**Information, in priority order**
1. Items that might be running low *(component · has states)*  
2. Soft “Might be running low” — no fake confidence numbers *(static)*  
3. Quantity — default from last-order prediction; user can edit *(component)*  
4. Remove on each item *(component)*  
5. Add all to cart *(component)*  
**Not here:** payment, address, household-size wall, pay button

### Cart / Checkout
Inherited. No new information architecture in this project.

## The main path
**Open Running low → check → Add all to cart → pay · 5 steps**

1. Order Again → tap Running low → sheet opens  
2. Check the list → remove what’s wrong  
3. Add all to cart → sheet closes, items in Cart  
4. Cart → checkout as usual  
5. Pay → done  

**Cut:** household-size wall, pay on sheet, Pantry tab, showing Running low when items aren’t enough.

## Other routes
- Rare nudge opens the same Running low sheet  
- Close sheet without adding → entry still on Order Again (if still enough items)  
- Remove down to below “enough” / empty → no Add all; don’t prioritize showing the sheet again until there’s a real list  

## When it's not perfect

### Order Again — Running low entry
- **Empty / not enough:** no entry *(at least 2 items to show — guessing)*  
- **Loading:** open  
- **Error:** open  
- **Done:** entry visible when list is worth checking  
- **Too much:** open  
- **Not allowed:** n/a  

### Running low (sheet)
- **Empty / not enough:** don’t show sheet or entry  
- **Loading:** “Building Running low…” — wait or use Order Again  
- **Error:** open  
- **Done:** after Add all — sheet closes, cart has items  
- **Too much:** open (scroll; no cap decided)  
- **Not allowed:** nothing left to add → Add all disabled or hidden  

### Cart / Checkout
Inherited Blinkit states — not redesigned here.

## Not in this project
- Knowing what’s in the fridge / what the cook bought elsewhere  
- Auto-ordering when something runs out  
- Cook login or shared household account  
- Pantry tab / full pantry flow  
- Paying inside the Running low sheet  

## What breaks if this ships
- Order Again gets a new entry — denser, one more thing to learn  
- People may open Running low instead of hunting categories on Order Again  
- Checkout path unchanged — Add all only lengthens the path by the sheet check step

### Stress pass — Running low sheet · 2026-08-23

**The job:** Open Running low, check the guess, remove what’s wrong, Add all to cart.  
**Predicted:** 4 · **Missed:** sticky footer not in build yet; long names; remove-to-1 while sheet open; loading with no escape besides close

| Condition | What should happen | What did happen | How bad |
|---|---|---|---|
| Nothing — new user / &lt;2 items | No entry, no sheet | Entry hidden (demo: Not enough). **saw it** in code | — (by design) |
| Too much — ~20+ staples | List scrolls; **Add all** stays sticky/reachable | Sheet scrolls as a whole; footer is **not** sticky — button scrolls away. **saw it** | Major |
| Too much — long name e.g. Fortune Sunflower Oil 1L | Name wraps; Remove still hittable | Wraps; no truncate. Remove still there. **saw it** | Minor |
| Wrong — cook already bought it | Remove; soft teach; don’t nag | Remove works; no “bought elsewhere” copy. Teach is remove-only in UI. **saw it** | Minor |
| Wrong — remove every item | Add all disabled/hidden; don’t prioritize empty sheet | Add all hidden when 0 items. **saw it** | — |
| Wrong — remove down to 1 while sheet open | Brief: don’t show thin lists; enough ≥2 | Still can Add all with 1 item; entry hides only after close. **saw it** | Major |
| Waiting — Building Running low… | Show loading; can’t Add all; can leave | Demo loading: skeletons + copy; Add all hidden. Close works. Hang never auto-ends in demo. **saw it** | Minor |
| Waiting — double-tap Add all | One register only | Button disables + loading for ~700ms. **saw it** | — (matches intent) |

**Fixing (cap 5):**
1. Sticky **Add all to cart** footer while list scrolls *(moments / looks)*
2. If removes leave &lt;2 items: disable Add all or close sheet + hide entry *(steps / moments)*
3. Longer-life staples only in the guess set — name the rule in brief *(the bet / things)*
4. Loading: keep Close obvious; don’t leave people with no exit *(moments)*
5. Optional: after Remove, one soft line that it can return if they order it on Blinkit again *(moments)*

**Deliberately not fixing:** Perfect fridge-knowledge for Wrong — Blinkit can’t see the kitchen (constraint).  
**Couldn't test statically:** Real slow network; real 247 SKUs; screen reader; focus order after sheet open.

## Attack decisions · 2026-08-23 (student)

**Dropped**
- Error sheet / error demo for Running low — not in Blinkit system; not designing it.

**Kept for now**
- Too much: sheet scrolls with many items (sticky Add all still open — student said scrolling is good to go).

**Nudge**
- Keep nudge behaviour; visual must match Blinkit system. Student will paste Blinkit nudge screenshots. Current prototype nudge is placeholder only.

**Flow change — Order Again persistence (draft, pending confirm)**
- Do **not** remove / hide the suggestions area on Order Again after Add all to cart.
- After Add all, still show suggestions somehow.
- If the Running low list is empty / cleared: still show suggestions, but **not** as Running low — normal suggestion treatment.
- **Remove** as a concept: from **Home nudge** only — not the primary remove model on the Order Again sheet (pending student confirm of wording).

**Layer:** steps / things — brief change before next build edit.

## Quantity (locked · 2026-08-23)
- Default qty on each Running low row comes from the **prediction / last Blinkit orders** (sample in prototype).
- User can **edit** qty before Add all to cart.
- Nudge: keep current prototype treatment for now (Blinkit nudge screenshot not available).
- Still parked: error sheet; Order Again persist / remove-only-on-Home flow change.

