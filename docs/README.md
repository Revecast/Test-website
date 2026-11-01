# CRM Care: subscription site

Static site (no build step). Open `index.html` to preview.

## Before launch
1. Rename "CRM Care" and edit copy/prices in `index.html`.
2. Stripe: create a recurring Product + Payment Link per tier (monthly and annual) and replace the `buy.stripe.com/REPLACE_*` URLs.
3. Audit form: create a Formspree (or Netlify Forms) endpoint and replace `REPLACE_ME`.
4. Replace the testimonial placeholders with real quotes.

## Deploy
This folder is published by GitHub Pages through `.github/workflows/pages.yml`, which runs on every push to `main` (and can be run by hand from the Actions tab).

One-time setup: in the repository go to **Settings → Pages** and set **Source** to **GitHub Actions**.

The folder also works unchanged on Netlify Drop or Vercel.

## Accessibility
- Skip link and a `<main>` landmark.
- The billing toggle is a real keyboard-reachable switch (`role="switch"`), and price changes are announced to screen readers.
- The audit form has visible labels and autocomplete hints.
- Visible focus outlines, and animation is turned off for people who ask for reduced motion.
