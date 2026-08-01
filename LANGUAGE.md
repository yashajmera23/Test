# LANGUAGE.md

**Project:** Blinkit — Home Pantry Tracker  
**Type:** feature addition  
**References:** Blinkit app screenshots — Home, Order Again, Order History, Checkout, product detail, product grid, Previously Bought category, Similar products, All details sheet, Support chat, Gift Cards, Blinkit Money (Aug 2026)  
**Status:** Matched in 2 rounds — 6 of 6 passing

> Values are estimated from proportion in reference images. They were not measured. Treat them as a scale that has been checked, not as truth.

---

## Type scale

| Name | Size | Weight | Used for |
|---|---|---|---|
| Display | 22px | 700 | Page title ("Order Again") |
| Heading | 18px | 700 | Section headers ("Running low", "Frequently bought") |
| Body | 15px | 600 / 400 | Product names, button labels, form labels |
| Caption | 12px | 400 / 600 | Secondary facts, helper text, status pills, MRP |

**Family:** Blinkit uses a custom sans-serif in-app. Substitute: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif` (`inferred` — closest free match; letterforms will not be identical).

---

## Spacing

**Base:** 8px  
**Steps in use:** 8 · 12 · 16 · 24

Card internal padding: 12px (`inferred` from product cards). Section gaps: 16px. Page horizontal margin: 16px.

---

## Palette

| Role | Value | Job |
|---|---|---|
| Surface | `#F6F6F6` | Page background behind cards (`observed` on Order Again, product grids) |
| Surface raised | `#FFFFFF` | Cards, sheets, input fields (`observed`) |
| Ink | `#1A1A1A` | Product names, prices, headings (`observed`) |
| Ink muted | `#696969` | Secondary text, delivery time, helper copy (`inferred` — reads darker than generic #9CA3AF) |
| Accent | `#318616` | Primary CTA fill, ADD border/text, links (`observed` on Add to cart, ADD buttons) |
| Signal | `#E23744` | Errors, destructive (`observed` on non-veg indicator; standard Blinkit red) |

**Status pill (Order soon):** `#E3F2FD` background · `#1565C0` text (`inferred` — matches "Bought Earlier" light-blue pill pattern on product detail)

**Discount / offer blue:** `#256FEF` for "X% OFF on MRP" (`observed` on product cards — not used on Running low cards)

---

## Shape

**Radius:** 12px cards · 8px buttons and inputs · 4px status pills · 24px floating cart pill (`inferred`)  
**Elevation:** 1px `#E8E8E8` border on cards; no drop shadow on list cards (`observed` — product cards use border/light separation, not heavy shadow)  
**Button height:** 48px primary CTA · 32px outlined ADD (`inferred`)  
**Inputs:** 44px height, 1px border, 8px radius (`observed` on Gift Card form)

---

## Density

**Spacious consumer** on Order Again and category grids — 2-column product layout, ~72–80px card content height, 3–4 items visible per fold (`observed`). Running low section should match Frequently bought tile density, not checkout density.

---

## Navigation

**Inherited, non-negotiable:** Bottom tab bar — Home · Order Again · Categories · Print · District. Running low lives inside Order Again; no new tab. Floating green "View cart" pill when cart has items (`observed`).

---

## Interface tone

Direct, short, transactional. No full sentences where a label works.

Real strings from references:
- "Add to cart"
- "Bought Earlier"
- "View cart"
- "Inclusive of all taxes"
- "Move to wishlist"

Running low copy should match: "Order what's running low" not "Proceed to checkout with selected pantry items."

---

## Match report

### Round 1
| Dimension | Result | Note |
|---|---|---|
| Type scale | ⚠️ | Section heading 20px too large vs Order Again section titles (~18px) |
| Spacing rhythm | ✅ | 8pt base confirmed |
| Density | ⚠️ | Card padding 16px — reference product rows read ~12px |
| Colour roles | ✅ | Green accent, grey surface, blue status pill aligned |
| Shape | ⚠️ | Button radius 8px — Add to cart reads ~10px, slightly rounder |
| Hierarchy | ✅ | Title → status → facts order matches product cards |

**Fixing:** heading 20→18, card padding 16→12, button radius 8→10. Round 2.

### Round 2 (final)
| Dimension | Result | Note |
|---|---|---|
| Type scale | ✅ | |
| Spacing rhythm | ✅ | |
| Density | ✅ | |
| Colour roles | ✅ | |
| Shape | ✅ | |
| Hierarchy | ✅ | |

Probe saved: `probe/probe.html` · `probe/probe-round2.png`

---

## Inherited and non-negotiable

- Blinkit green primary CTA (`#318616`)
- White cards on `#F6F6F6` page background
- Outlined green ADD button (white fill, green border)
- Bottom tab navigation — no new tab for Running low
- Floating green View cart pill when items exist
- "Home" as delivery address label
- Existing Checkout screen — not restyled

---

## Mine to decide

- **Order soon pill colour** — matched "Bought Earlier" blue rather than amber urgency. Rejected amber: Blinkit already uses blue for repurchase signals; amber reads as promo.
- **Section placement** — Running low above Frequently bought. Rejected Home banner: student decision in DESIGN.md.

---

## Do NOT inherit

- **Gift Card decorative serif + gold gradient** — marketing screen only, not product UI
- **Blinkit Money yellow polka-dot hero** — onboarding promo, not list/browse surfaces
- **Ad tags on product cards** — not relevant to Running low
- **Support chat bubble styling** — different context; order list format is useful reference for item copy, not visual treatment
- **Heavy drop shadows** — Blinkit product UI uses borders and flat cards, not Material-style elevation

---

## Confidence

**Observed in images:** Surface colours, green CTA, ADD outline style, bottom nav, card-on-grey layout, real UI strings  
**Inferred:** Exact hex values, type sizes from proportion, status pill blue, spacing steps, font substitute  
**Assumed, nothing behind it:** Exact Blinkit custom font name

---

## Generation constraints

Use only the sizes, steps and palette roles above. Do not introduce a new size, step or colour. If something seems to need one, that is a hierarchy problem — solve it with the existing scale.
