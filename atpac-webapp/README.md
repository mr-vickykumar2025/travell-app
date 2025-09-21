# ATPAC Travel Data Web App (Express + MongoDB + Vanilla JS frontend)

## What you get
- Passwordless Email OTP authentication (request OTP, verify OTP)
- JWT cookie-based session
- Create trips (origin/destination coordinates, start/end times, mode, purpose, accompanying travellers)
- View trip history
- Simple static frontend (public/) + Express API
- Uses Nodemailer: if SMTP not configured, a test Ethereal account will be used and a preview URL will be printed in server logs.

## Quick start (local)
1. Install Node.js (v18+) and MongoDB.
2. Extract the zip and open terminal in the project folder.
3. Copy `.env.example` to `.env` and adjust environment variables.
4. Install dependencies:
   ```
   npm install
   ```
5. Start server:
   ```
   npm start
   ```
   or during development:
   ```
   npm run dev
   ```
6. Open `http://localhost:3000` in your browser.

## Notes
- Geolocation in browsers requires HTTPS or `localhost` for `navigator.geolocation`.
- For OTP email testing, if you don't configure SMTP, the server will create a test Ethereal account and print a `preview` URL in the console — open that URL to view the OTP message.
