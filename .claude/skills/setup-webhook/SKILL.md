---
name: setup-webhook
description: Use this skill to configure and scaffold webhook endpoints for the telegram bot.
tools: ["Bash", "Write", "Edit"]
---
## Webhook Setup Protocol
When tasked with moving from polling to webhooks or setting up webhooks:
1. Verify the `[TECH_STACK]` web server capabilities (e.g., Express, Fastify, FastAPI, aiohttp).
2. Scaffold a secure endpoint (e.g., `/webhook/bot<SECRET_TOKEN>`) to prevent unauthorized triggers.
3. Configure the webhook setup script or handler to call Telegram's `setWebhook` method.
4. Add mechanisms to parse incoming JSON payloads into the bot framework's update handler.
5. Provide instructions for local testing (e.g., using ngrok or localtunnel).
6. Update `.claude/memory/bot_manifest.md` to reflect Webhook strategy and the port/path.