---
name: payment-gateway-setup
description: Use this skill to integrate Telegram Payments (Provider Payments) or external crypto gateways.
tools: ["Bash", "Write", "Edit"]
---
## Payment Gateway Protocol
When tasked with integrating payments into the bot:
1. **Telegram Payments (Native)**:
   - Ensure the bot token and payment provider token (`PROVIDER_TOKEN` via BotFather - Stripe, Tranzzo, etc.) are set in `.env`.
   - Implement the `sendInvoice` method to create the payment payload (title, description, payload, prices).
   - Crucial: Handle the `pre_checkout_query` update within 10 seconds using `answerPreCheckoutQuery` (otherwise it times out).
   - Finally, handle the `successful_payment` update to grant the user their service/goods.
2. **Crypto Payments (e.g., Crypto Pay, Ton)**:
   - Scaffold API endpoints or Webhooks to receive payment confirmations from the third-party gateway.
   - Design the `tg-ux-engineer` flow for creating invoices.
3. Validate and record all transactions in the `[TECH_STACK]` database schema.