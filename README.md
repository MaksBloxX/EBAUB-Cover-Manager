# 📄 EBAUB Cover Manager (Simple)

Public cover-page maker — **no login, no database.**
Form (left) → live A4 preview (right) → 1-page PDF. Done.

## 🎨 3 Designs
1. 🧪 **Lab Report** — EBAUB official format (PDF হুবহু)
2. 🔵 **Classic Blue** — RU-style modern (navy + light boxes)
3. 🟡 **Royal Gold** — DU-style modern (maroon/gold + cream paper)

## ▶️ চালানো / Public করা
- PC-তে: `index.html` ডাবল-ক্লিক
- Public site: ফোল্ডারটা **Netlify Drop / Vercel / GitHub Pages / Tiiny.host**-এ আপলোড — ফ্রি, ২ মিনিট

## 🔧 PDF-safe CSS নিয়ম (মনে রাখো)
`html2canvas` দিয়ে PDF বানানো হয়, তাই cover-এর CSS-এ **নিষেধ**:
- ❌ CSS variables (`var(--x)`), ❌ CSS grid, ❌ flex `gap`, ❌ `:last-child`
- ✅ table, flex-row, literal colors (`#1e3a8a`), margins

## 📁 Files
```
index.html  css/style.css  js/app.js  assets/(2 logos)  vendor/(offline libs)
```
