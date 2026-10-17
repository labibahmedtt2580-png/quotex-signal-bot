# Signal Lab — Quotex Signal Starter

Educational candle-analysis dashboard. This starter does **not** connect to Quotex, does not scrape private endpoints, does not log in to any trading account, and does not place trades.

## Requirements
- Node.js 18+
- Internet browser
- For hosting: a GitHub account and a free Node.js web service host

## Run locally
1. Install Node.js 18 or later on a computer (Android-only users can edit files in a browser IDE, then deploy through GitHub).
2. In this folder run:
   `npm install`
   `npm start`
3. Open `http://localhost:3000`.

## Use
- Tap **নমুনা ডেটা লোড** to see how the interface behaves. Sample candles are synthetic and are not live.
- To analyze real candles, paste at least 30 OHLC rows into the CSV box, oldest first:
  `open,high,low,close`
- The selected 1m/5m value labels the analysis timeframe; it does not resample candles. Supply candles from the chosen timeframe.
- CALL/PUT/WAIT are simple indicator rules for learning and are not a validated profitable strategy.

## Deploy free
1. Create a private or public repository on GitHub and upload these files.
2. On Render, choose **New → Web Service**, connect the repository.
3. Build command: `npm install`
4. Start command: `npm start`
5. Select the Free plan and deploy.
6. Open the generated `onrender.com` URL.

Free hosting may sleep when idle, and free services have limitations. Check the host's current plan terms.

## Connecting a live source
Only add a data feed that you are authorized to use and whose quotes match the target market. Keep API secrets in server-side environment variables; never place secret keys, passwords, OTPs, or session cookies in frontend code. Do not assume a generic Forex feed matches Quotex OTC prices. If no authorized matching feed is available, keep the app clearly labelled as manual/offline analysis.
