# ATTACK — check yourself

**Build:** https://yashajmera23.github.io/Test/ · or open `docs/index.html`  
**Job:** Open Running low → check → remove wrong → Add all to cart  
**Date:** 2026-08-23

Use the dark **Demo** menu (top-right). Tick each row after you try it.

---

## How to check each finding

| # | Demo / action | What you should notice | Severity | Your tick |
|---|---|---|---|---|
| 1 | **Not enough — no entry** | No Running low entry on Order Again | By design | [ ] |
| 2 | **Too much (many items)** → open sheet → scroll | List is long; **Add all to cart** scrolls away (not sticky yet) | Major | [ ] |
| 3 | **Ready** → open sheet → look at oil name | Long name wraps; Remove still there | Minor | [ ] |
| 4 | **Ready** → Remove items until **1 left** | You can still tap Add all (enough-rule only hides entry after close) | Major | [ ] |
| 5 | **Ready** → Remove all | Add all disappears | By design | [ ] |
| 6 | **Loading sheet** | “Building Running low…”; Close (×) still works | Minor | [ ] |
| 7 | **Ready** → mash **Add all** twice | Only one cart add (button disables) | Holds | [ ] |
| 8 | **Sheet error** | Error line + list still there | Open | [ ] |

---

## Stress table (from the pass)

| Condition | What should happen | What did happen | How bad |
|---|---|---|---|
| Nothing — &lt;2 items | No entry, no sheet | Entry hidden | — (by design) |
| Too much — many staples | Scroll + sticky Add all | Scrolls; **footer not sticky** | Major |
| Too much — long name | Wraps; Remove hittable | Wraps | Minor |
| Wrong — cook already bought | Remove; soft teach | Remove only in UI | Minor |
| Wrong — remove to 1 in open sheet | Don’t allow thin Add all | Still can Add all with 1 | Major |
| Wrong — remove every item | Add all hidden | Hidden | — |
| Waiting — loading | Show loading; can leave | Skeletons + Close | Minor |
| Waiting — double Add all | One register | Disables while loading | — |

---

## Fixing next (cap 5)

1. Sticky **Add all to cart** while list scrolls  
2. If removes leave &lt;2: disable Add all or close + hide entry  
3. Longer-life staples only — write the rule in the brief  
4. Loading: Close always obvious  
5. Optional soft line after Remove (can return if ordered on Blinkit again)

**Not fixing:** Knowing what’s in the fridge.

---

## Your predictions vs build

| Kind | You said | Build |
|---|---|---|
| Nothing | Don’t show | Holds |
| Too much | Sticky button | **Not built yet** — check with Too much demo |
| Wrong | Still guess; buy on Blinkit next | Remove works; teach copy thin |
| Waiting | One-time register | Holds |

---

After you tick the table, say what you’d change first — then we do the craft rulers / fix pass.
