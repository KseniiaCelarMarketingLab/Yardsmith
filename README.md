# Yardsmith Stables website

Static site. No build step.

## Deploy on Vercel
1. Push this folder to a GitHub repository (the files at the repo root).
2. In Vercel: Add New → Project → import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `.` (root).
4. Deploy.

## Pages
- index.html — Home
- product.html — Product
- team.html — For Your Team / For Every Yard
- investors.html — For Investors
- request-access.html — Forms (#demo, #investors, #question)

SiteHeader.dc.html and SiteFooter.dc.html are shared components loaded by every page. support.js is the runtime; keep it next to the pages.

## Forms
Forms post to FormSubmit. The first submission sends an activation email to the receiving inbox — confirm it once, then all requests arrive.
