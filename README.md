# CarbonClose — Landing Page

Static landing page for a **compliance-grade carbon & ESG telemetry** startup (meter-level + supply-chain emissions data with regulator-proof audit trails — "closing the books" for carbon under CSRD). No build step, no dependencies — plain HTML/CSS/JS.

## Rebranding (company name / domain)

Edit the three values at the top of **`config.js`**:

```js
const BRAND = {
  companyName: "CarbonClose",
  domain: "carbonclose.example.com",
  contactEmail: "hello@carbonclose.example.com"
};
```

Every occurrence of the company name, domain, and email in the page is injected from this file at load time. Nothing else needs to change.

## Deploy to GitHub Pages

1. Create a new GitHub repo and push this folder's contents to it:
   ```sh
   git init
   git add .
   git commit -m "Landing page"
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`** → Save.
3. The site goes live at `https://<user>.github.io/<repo>/`.

For a custom domain, add it under **Settings → Pages → Custom domain** (GitHub creates a `CNAME` file) and point your DNS at GitHub Pages.

## Files

| File | Purpose |
|---|---|
| `index.html` | Page structure & copy |
| `style.css` | All styling (theme variables at top of file) |
| `config.js` | Brand config + injection script |

## Notes

- Theme: moss green + cream with an editorial twist — **Source Serif body, Libre Franklin headings**, paired vertical ledger-rule hero band (`--ink`, `--accent`, `--leaf` in `style.css`).
- Hero visual is a pure HTML/CSS **carbon close ledger**: an emissions table with per-line evidence badges, a verified total row, a "period locked" chip, and a rotated double-ring **assurance stamp**.
- The email form shows a confirmation message client-side; wire it to Formspree, Buttondown, or your own endpoint to actually collect emails.
- Logo is an inline SVG C-with-checkmark mark in `index.html` (nav + footer) — swap both `<svg class="logo-mark">` blocks to change it.
