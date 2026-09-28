# Connecting REAL orders

The current website deliberately does **not** pretend that clicking “Place Order” sends a real order to you. It stores a submitted order in the browser's localStorage and shows a confirmation screen.

For a real student business, the simplest low-maintenance setup is Google Forms + Google Sheets.

## Option A — Google Forms + Google Sheets (recommended)

1. Create a Google Form with these fields:
   - Name
   - School
   - Pickup date
   - Pickup time
   - Order details
   - Total quantity
   - Total price
   - Notes
2. In the form's Responses tab, choose “Link to Sheets.”
3. Share the form link with customers.
4. Either:
   - Replace the site's order form with an embedded Google Form, or
   - Add a small connector service that POSTs the site's order data to the form.

### Important technical note
Google Forms is designed primarily around its own form UI. Direct browser POSTs to Google Forms can be brittle because Google may change field IDs and anti-abuse behavior. For a student business, embedding the Google Form is the most dependable no-code route.

## Option B — Form backend service

You can use a form endpoint provider that accepts HTML form POSTs. Add its endpoint to the `<form action="...">` and use `method="POST"`. Follow that provider's current instructions and privacy terms.

## Option C — Firebase / Supabase

For a more advanced setup, create a small database table for orders and use a server-side function/API endpoint to accept orders. Do NOT put secret API keys in `app.js`.

## Before going live
- Replace placeholder Instagram/email in `config.js`.
- Replace sample products/prices.
- Set your real ordering/pickup rules.
- Decide how customer data will be handled.
- Test a complete order from a phone and a computer.
- Don't collect more personal information than you actually need.
