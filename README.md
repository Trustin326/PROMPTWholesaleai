# PromptWholesale AI — Production Build

This package includes a complete GitHub Pages frontend, private product packs, Google Sheets/Apps Script backend, account flow, prompt builder, project saving, affiliate records, sales records, delivery records, legal pages, admin and reseller pages.

## What you replace
1. Stripe Payment Links in `public-site/assets/js/config.js`.
2. The deployed Apps Script Web App URL in the same file.
3. Support email.

## One-time secure setup
Stripe Payment Links alone cannot protect files on a public GitHub Pages repository. Run the included setup once:
- Create a Google Sheet and Apps Script project.
- Paste `backend/apps-script.js`, run `setupProduction()`, and deploy as Web App.
- Script Properties: `STRIPE_SECRET_KEY` and `PRODUCT_FILE_MAP` JSON.
- Upload `private-product-packs/*.zip` to private Google Drive and map each product ID to its file ID.
- Paste the Web App URL in config.js.
- In Stripe, add each Payment Link success redirect: `https://YOUR-SITE/success.html?session_id={CHECKOUT_SESSION_ID}` and metadata `product_id` matching config.

Only publish `public-site/`. Never publish `private-product-packs/` or the backend secrets.
