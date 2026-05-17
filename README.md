# StyleLock

**Editorial-grade manuscript formatting for the GADING Journal for the Social Sciences (UiTM).**

StyleLock enforces the MJCET / UiTM Journal Template 2024 APA house style on every submission — paragraph by paragraph, reference by reference — so editorial boards can focus on substance, not margins.

## What's inside

This deploy folder is a **single self-contained HTML file** (~2.6 MB) that ships the whole StyleLock suite:

- **Hub** — editorial dashboard with manuscript queue and processing stats
- **Manuscript Formatter** — side-by-side editor with paragraph-by-paragraph style assignment, paginated A4/B5 preview, and live MJCET-compliant output
- **References (APA 7)** — paste-and-format reference list tool
- **Word Add-in preview** — task-pane mock that lives inside Microsoft Word

Built to the exact specification extracted from the official MJCET / UiTM template DOCX (B5 JIS paper, mirror margins, Heading A/B auto-numbering, 9 pt Times New Roman body, 357-twip hanging reference indent, etc.).

## Run locally

The deploy is a single file — just open it in a browser:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

…or serve over HTTP:

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

## Deploy to GitHub Pages

This repository ships with a `.github/workflows/pages.yml` workflow that auto-publishes on every push to `main`.

1. **Create a new repo on GitHub** (private or public).
2. **Push this folder** to it:
   ```bash
   git init
   git add .
   git commit -m "Initial StyleLock deploy"
   git branch -M main
   git remote add origin https://github.com/<your-user>/<your-repo>.git
   git push -u origin main
   ```
3. In the new repo on github.com: **Settings → Pages → Source: GitHub Actions**.
4. The first push triggers the deploy. Your site will be live at:
   `https://<your-user>.github.io/<your-repo>/`

## Deploy elsewhere (10 seconds)

- **Netlify Drop** — drag `index.html` onto [app.netlify.com/drop](https://app.netlify.com/drop)
- **Cloudflare Pages** — connect this repo, no build command needed (publish directory: `/`)
- **Vercel** — `vercel deploy` from this folder

## Tweak the design

Open the **Tweaks** panel (toolbar) to switch accent colour and paper size (B5 JIS ↔ A4) live.

## License

© 2026 UiTM. All rights reserved.
