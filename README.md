# Baked by Piper — Website

A polished, responsive static website for a student-run cookie business.

## Files
- `index.html` — entire site and page sections
- `styles.css` — design and responsive styling
- `app.js` — navigation, menu, cart, calculator, validation, confirmation
- `config.js` — **EDIT THIS FIRST** for products, prices, schools, and contact info
- `CONNECTING_ORDERS.md` — how to connect real order submissions
- `assets/` — folder for your own product photos if you want to add them later

## Open it
Double-click `index.html` or right-click → Open with a browser.

The site is static, so it works without a server. Google Fonts load when internet is available; the site still functions if they don't load.

## What is actually functional?
- Responsive navigation and mobile hamburger menu
- Menu generated from `config.js`
- Add-to-order buttons
- Quantity +/- controls
- Automatic item count and price totals
- Required-field validation
- Date cannot be selected before today
- Confirmation modal with generated order number
- Orders saved locally in the browser (`localStorage`)
- Contact form UI validation
- No fake claim that orders were sent to a real inbox

## Important
A browser-only site cannot safely send real orders to you by itself. Follow `CONNECTING_ORDERS.md` before accepting real customers.

## Adding photos
Replace the emoji visual in `config.js`/`app.js` with image URLs or extend the product objects with an `image` field. For local images, put files in `assets/` and use paths like `assets/chocolate-chip.jpg`.

## Google Sites
Google Sites does not function as a normal static-hosting platform where you upload an arbitrary HTML/CSS/JS folder and have it run as a website. The easiest Google-connected workflow is:
1. Publish this static site with a static host such as GitHub Pages or another static host.
2. In Google Sites, use Insert → Embed → URL to embed the published site, if you specifically need a Google Sites shell.
3. For real orders, connect the form to Google Forms/Sheets or a small backend as described in `CONNECTING_ORDERS.md`.
