# アリエールジェル 価格チェッカー

## Project Overview
Single-file static web app to compare detergent prices by yen/g in-store.
Hosted on GitHub Pages.

## Files
- `index.html` — entire app (HTML + CSS + JS, no build step)

## GitHub
- Repo: https://github.com/Mochi-Shiratama/detergent
- Live URL: https://mochi-shiratama.github.io/detergent/
- Branch: `main`

## Deploy
```bash
git add index.html
git commit -m "message"
git push
```
GitHub Pages auto-deploys from `main` root.

## Architecture
- No backend, no dependencies
- Data persisted in `localStorage`:
  - `custom_products` — user-added products (array)
  - `prices` — recorded price entries (array)
- Built-in products are JS constants (not in localStorage)

## Screens
1. **メイン** — product list table with best yen/g highlighted (★)
2. **価格チェック** — select product → enter price → get cheap/normal/expensive verdict
3. **製品追加** — add new product size to localStorage
4. **記録履歴** — view all price records, filter by product, delete entries

## Judgment Criteria (vs. product's historical best yen/g)
- ≤ 1.05x → 安い！(green)
- ≤ 1.15x → 普通 (yellow)
- > 1.15x → 高い (red)
- No history → 初回記録 (gray)

## Git Config
- user.name: Mochi-Shiratama
- user.email: totamiya@gmail.com
