# EBAUB Cover Manager

Report / Assignment cover page maker for **Exim Bank Agricultural University Bangladesh (EBAUB)** — all faculties.

Fill up the form → live A4 preview → download 1-page PDF. No login, no database, works offline.

## Designs

| # | Design | Style |
|---|--------|-------|
| 1 | Standard Report | Official lab-report format (EBAUB) |
| 2 | Assignment/Report | Classic navy blue |
| 3 | Other Varsity | Royal maroon + gold |

## Features

- Live A4 preview while typing (PC + mobile)
- 1-page PDF download (high-resolution) + Print
- Faculty-wise auto logo (4 faculties) or custom logo upload
- University logo upload + watermark with opacity control
- Date shows only when picked; blank-safe fallbacks everywhere
- 100% client-side — no server needed

## Run locally

Just open `index.html` in any browser (double-click). No build step.

Or serve the folder:

```bash
cd cover-manager
python3 -m http.server 8000
# open http://localhost:8000
```

## Project structure

```
cover-manager/
├── index.html          # form + preview + footer
├── css/style.css       # site + all 3 cover designs
├── js/app.js           # templates, live preview, PDF export
├── assets/             # header logo, EXIM + faculty logos
├── vendor/             # offline libs (html2canvas, jsPDF) — do not delete
└── README.md
```

> The `vendor/` folder must stay beside `index.html`, otherwise PDF download won't work offline.

## Deploy free (GitHub Pages)

1. Upload all files to your repo (`MaksBloxX/EBAUB-Cover-Manager`)
2. Repo → Settings → Pages → Deploy from branch → `main` / root
3. Your site goes live at `https://maksbloxx.github.io/EBAUB-Cover-Manager/`

Also works on Netlify Drop, Vercel, Tiiny.host — just drag & drop the folder.

Here is [Click me](https://maksbloxx.github.io/EBAUB-Cover-Manager/)

## Developer note: PDF-safe CSS

PDF is rendered with `html2canvas`, which doesn't support everything. In cover CSS avoid:

- CSS variables (`var(--x)`), CSS grid, flex `gap`
- `object-fit` on fixed-size logo boxes (it gets ignored — match the box to the image aspect instead)
- `display:inline-block` + `% width` combos (use block + `margin:auto`)

Safe: tables, flex rows/columns, literal colors, margins, padding.

## Credits

Developed by **Md. Makshedul Islam**
Questions or suggestions? Open an issue: https://github.com/MaksBloxX/EBAUB-Cover-Manager/issues

Free to use for educational purposes.

## Previews

### For PC/Laptop:

<img width="1240" height="1354" alt="image" src="https://github.com/user-attachments/assets/871084e4-59e8-4f21-aa01-5e8cc211d8c2" />


### For Mobile:

<img width="360" height="1569" alt="image" src="https://github.com/user-attachments/assets/33dab14e-4ce1-48cb-8342-ebf2ed9782b0" />


<img width="360" height="835" alt="image" src="https://github.com/user-attachments/assets/cc38a0fc-ca17-4afd-b496-02e67989e680" />


