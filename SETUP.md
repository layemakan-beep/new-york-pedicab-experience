# Custom booking test

This package adds `booking.html`, a custom guest counter, live total, date and time selection, and a secure server-side Square checkout endpoint.

## Current state

- Mock availability is enabled so the interface can be reviewed without touching the live Square calendar.
- Square payment is disabled until sandbox credentials are configured.
- The existing live website remains unchanged.

## Local test

1. Install Node.js 18 or newer.
2. Run `npm install`.
3. Copy `.env.example` to `.env` and load those variables in the hosting environment.
4. Run `npm start`.
5. Open `http://localhost:3000/booking.html`.

## Before production

Connect a Square Developer sandbox application, map every tour to its Square service variation and team members, replace mock availability with Square Bookings API availability, reserve the selected appointment before or during checkout, handle payment and booking webhooks, and deploy the server to a secure Node.js host. Never put the Square access token in HTML, JavaScript, GitHub Pages, or GitHub source control.
