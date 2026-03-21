# Credit Card Interest Calculator

This repository contains the SimpleKit Credit Card Interest Calculator, a static browser-based tool that helps people estimate:

- how long it may take to pay off a credit card balance
- how much interest they may pay over time
- the total amount paid
- how extra monthly payments can shorten payoff time and reduce interest

The tool is designed to feel calm, trustworthy, and beginner-friendly while staying practical enough for real payoff planning.

## What The Calculator Does

Users enter:

- current balance
- annual percentage rate (APR)
- monthly payment
- extra monthly payment

The app estimates:

- payoff time
- total interest paid
- total amount paid
- the effect of adding an extra monthly payment
- whether the current payment pace looks slow, moderate, or aggressive

## File Structure

```text
/
  index.html
  calculator-spec.yaml
  assets/
    css/
      styles.css
    js/
      app.js
      simplekit-tool-links.js
```

## Core Implementation Notes

- `index.html` contains the static SEO content, tool UI, FAQ, related tools, and SimpleKit shared shell mount points.
- `assets/js/app.js` handles the month-by-month payoff math, validation, URL state syncing, sample/reset actions, and share-link behavior.
- `assets/css/styles.css` contains the local tool styling for the calculator layout, form, results, FAQ, and responsive behavior.
- `assets/js/simplekit-tool-links.js` is the source of truth for live related-tool URLs inside the SimpleKit ecosystem.

## Shared SimpleKit Integration

This repo preserves the SimpleKit shared core setup:

- `https://core.simplekit.app/core.css`
- `https://core.simplekit.app/core.js`
- shared mount points for header, support section, and footer
- the existing Google Analytics snippet in the document head

The calculator remains static-site friendly and does not require a backend or build step.

## Calculation Method

The payoff estimate:

1. converts APR to a monthly interest rate
2. calculates monthly interest from the remaining balance
3. applies the base monthly payment plus any extra monthly payment
4. repeats month by month until the balance reaches zero
5. flags cases where the payment is too low to cover monthly interest

Results are planning estimates and can differ from real card issuer statements because of statement timing, daily compounding, fees, promotional rates, and new purchases.

## Local Preview

Because the app is fully static, you can preview it with a simple local server from the repo root, for example:

```bash
python3 -m http.server 8000
```

Then open:

- `http://localhost:8000/`

## Pre-Launch Checks

- confirm metadata and canonical URLs match the production subdomain
- verify related-tool links use the live SimpleKit tool catalog
- test low-payment and invalid-input edge cases
- verify the shared SimpleKit shell still mounts correctly
- review desktop and mobile layouts before deployment
