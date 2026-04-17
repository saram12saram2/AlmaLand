# 🍎 Alma Land

> A number puzzle game inspired by the apple orchards of **Almaty, Kazakhstan** — the genetic birthplace of the modern apple.

![Alma Land gameplay screenshot](./image.png)

---

## 🎮 How to Play

- Click and drag a box around apples that add up to 10:
```
  ┌──────────┐
  │ 🍎   🍎 │  ← drag over these
  │  3     7 │
  └──────────┘
       3+7 = 10 ✅  poof! they disappear!
```

- The numbers must add up to **exactly 10** — not more, not less:
```
  3 + 7 = 10  ✅  perfect!
  2 + 5 = 7   ❌  keep dragging…
  9 + 8 = 17  ❌  too many!
```

- Score as many apples as you can before the timer hits zero! ⏱️🍎


## 🚀 Run Locally

```bash
npm install
npm run dev
```

---

## 👩‍💻

**Stack:** Vanilla JS (ES modules) + plain CSS + Vite. No frameworks, no runtime dependencies.

**How drag-select works:**
1. `mousedown` — records origin point
2. `mousemove` — draws a `#selection-box` overlay, highlights apples whose **center** falls inside it, shows running sum
3. `mouseup` — if sum === 10, apples animate `.pop` then become `.empty` slots

**Theming:** one `data-theme="light"` attribute on `<html>` flips all colors via CSS custom properties — zero JS beyond toggling it.

---

