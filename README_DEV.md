# README_DEV.md – Developer Guide

## Prerequisites
- Node.js v18+ and npm
- MongoDB (local or Atlas)
- Internet for email OTP

## Setup
1. Unzip project and open terminal in folder.
2. Copy .env.example to .env and configure:
   ```bash
   cp .env.example .env
   ```
   Edit .env with:
   ```env
   PORT=3000
   MONGO_URI=mongodb://127.0.0.1:27017/atpac
   JWT_SECRET=your_strong_secret
   EMAIL_HOST=smtp.example.com
   EMAIL_PORT=587
   EMAIL_USER=your-user
   EMAIL_PASS=your-pass
   EMAIL_FROM="ATPAC <no-reply@atpac.gov.in>"
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

## Run the Server
Development mode:
```bash
npm run dev
```
Production:
```bash
npm start
```
Visit http://localhost:3000.

## Testing OTP Login
- Request OTP, check console for Ethereal preview URL if SMTP not set.
- Verify OTP to login.

## Testing Trip Recording
- Start Trip → allow geolocation.
- End Trip → fill details → Save Trip.
- View history below dashboard.

## Tips
- Use HTTPS or localhost for geolocation.
- Test multiple devices.
- Inspect DB using MongoDB Compass.
