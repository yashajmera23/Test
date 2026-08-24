# DESIGN

**Project:** Blinkit — Home Pantry Tracker  
**Date:** 2026-08-01  
**Solving:** How might we help urban working professionals who depend on their cook for kitchen management to act on low-stock signals before things run out — without requiring them to manually track or place single low-value orders — so they feel in control of their household even when they're not physically present in the kitchen?

---

## Words we're using

| We call it | Not | Because |
|---|---|---|
| Running low | Pantry, virtual shelf, low-stock alert | Participants described items "running out" and "running low" — not pantry tracking |
| Order Again | New tab, Home section | Feature lives inside existing Order Again tab |
| Saved for later | Wishlist, planned cart | P2 wanted a list separate from urgent orders; Blinkit Checkout already has "Move to wishlist" |
| Order soon | Urgent, critical, out of stock | Status before runout — matches research lead-time framing |
| Home | Kitchen address | Blinkit already labels delivery address as "Home" |

**One word everywhere:** "Running low" is the section name, the notification copy, and the status label — not "Low stock" on one screen and "Running out" on another.

---

## Screens

| Screen | Job |
|---|---|
| **Running low** (section on Order Again) | See what's predicted to run out soon — only when bundle is orderable |
| **Bundle review** | Confirm grouped items before they hit the cart |
| **Kitchen setup** (first time only) | Calibrate household size so consumption estimates make sense |
| **Checkout** (existing) | Pay — inherited, not redesigned |

---

## Where they hang off the existing app

```
Order Again tab (existing)
  └ Running low section          NEW — sits above "Frequently bought"
       └ Bundle review            reached when user taps "Order what's running low"
            └ Checkout (existing) reached via "Add to cart"

Order History (existing)
  └ unchanged — reorder per past order still works separately

Home (existing)
  └ no new section — entry is Order Again only

NOT ADDING:
  · new bottom-nav tab
  · Home banner or card
  · changes to Checkout layout beyond receiving bundled items
  · cross-platform order import
```

**Constraint:** Adding a room, not knocking the house down. Order Again gets one new section; Checkout, Home nav, and Order History stay as they are.

**Strategic bet (Blinkit-only):** Tracking only works on Blinkit orders. Users who split across Zepto/Amazon (like P1 Ritika) cannot get full coverage — intentional incentive to consolidate grocery orders on Blinkit for pantry visibility.

---

## The main path

**Organiser reorders before cook runs out — 5 steps**

1. **Order Again** → Running low section visible (bundle ≥ ₹150)
2. **Tap "Order what's running low"** → Bundle review
3. **Review items** → tap "Add to cart"
4. **Checkout** (existing) → Place order
5. **Done** → back to Order Again; fulfilled items drop off Running low

**Cut from path:** naming individual items, choosing delivery slot (inherited), manual item entry, category-by-category ordering

---

## Other routes

| Route | What happens |
|---|---|
| **First-time user** | Kitchen setup modal on first visit to Order Again → asks household size → section empty until enough order history |
| **Notification tap** | Deep-links to Running low section on Order Again |
| **Urgent one-off order** | User orders via normal search/cart — does not clear Running low; urgent cart and saved bundle stay separate |
| **Bundle not yet ₹150** | Running low section hidden — no partial or sub-threshold state shown |

---

## When it's not perfect

### Running low section
| State | What user sees |
|---|---|
| **Empty** | Section not shown — no items meet ₹150 bundle threshold yet |
| **Loading** | Skeleton cards while predictions calculate from order history |
| **Error** | "Couldn't update your kitchen — pull to refresh" |
| **Done** | Items disappear after successful order |
| **Too much** | Cap visible items (e.g. 8) with "View all" — open: exact cap TBD at build |
| **Not allowed** | Section hidden if no home address set or no order history |

### Kitchen setup (first time)
| State | What user sees |
|---|---|
| **Empty** | n/a — modal always has a default household size pre-selected |
| **Error** | "Couldn't save — try again" with retry |
| **Done** | Modal dismisses; never shown again unless user resets in Account |

### Bundle review
| State | What user sees |
|---|---|
| **Empty** | Should not occur — only reachable when bundle ≥ ₹150 |
| **Loading** | Prices fetching — show spinner on total |
| **Error** | Item unavailable — show which item failed, offer to remove and recalculate |
| **Done** | Transition to Checkout with items added |

### Checkout (inherited)
| State | Handled by existing Blinkit — not redesigned |

---

## Not in this project

- **Cross-platform tracking** — Zepto, Amazon, Instamart orders are not imported. Blinkit-only is the retention bet: consolidate orders here to get tracking.
- **Cook or flatmate accounts** — one person orders; cook has no app access.
- **Manual pantry entry** — users cannot add items Blinkit hasn't delivered to their home address.
- **New bottom-nav tab** — lives inside Order Again.
- **Home screen entry point** — Order Again only.
- **Sub-₹150 bundle UI** — section hidden until bundle is orderable; no "add ₹X more" state.
- **Category-specific notification timing UI** — lead times differ by category (research finding) but user-facing controls for this are out of scope; logic runs in background.

---

## What breaks if this ships

- **Order Again gets longer** — new section above Frequently bought pushes category tiles down; returning users scroll more.
- **"Frequently bought" vs "Running low" confusion** — two similar-looking sections on same screen; must be visually distinct (status labels, different card treatment).
- **Wishlist naming collision** — Checkout already has "Move to wishlist"; Running low must not use wishlist language.
- **Users with thin Blinkit history** — feature invisible until enough orders to predict and bundle; cold-start users see nothing.
- **Notification fatigue** — one more push channel; must only fire when bundle is actionable (≥ ₹150), not per-item.

---

## Open

- Exact household-size options in Kitchen setup (2 / 3 / 4+ people?)
- Visual treatment to distinguish Running low from Frequently bought
- Notification copy and persistence behaviour (research says persistent until acted — detail at build)
- Scope card hypothesis still drifted from research — update SCOPE.md before build
- JTBD cuts trail, app-store triangulation still missing (see LOG.md)
