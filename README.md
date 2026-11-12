# Aurora Market: AI Payment Firewall

An online store where every purchase made by an AI agent passes a Payment Firewall before PayPal is called.

1. **Rules engine (server code):** per-purchase limit, daily limit, blocked categories, ask-a-human threshold.
2. **AI intent check:** Gemini compares the cart with what the user asked the agent to buy. Without a key, a simple heuristic is used.
3. **PayPal sandbox:** orders are created and captured only after approval. Prices come from the server catalog, not the browser.

## Run it
Requires Node 20.6+.
```
npm install
cp .env.example .env   # add PayPal sandbox Client ID and Secret (developer.paypal.com), optional Gemini key
npm start              # http://localhost:3000
```
Pay in the PayPal popup with your sandbox personal (buyer) account.

## Demo scenarios (buttons in the cart)
Book and notebook: approved. Desk setup: needs approval. Gift cards: blocked. Over the limit: blocked.

License: MIT
