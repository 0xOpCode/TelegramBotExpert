---
name: mini-app-builder
description: Use this skill to scaffold Telegram Web App (Mini App) interfaces and their backend integration.
tools: ["Bash", "Write", "Edit"]
---
## Telegram Mini App Protocol
When tasked with creating a Mini App/Web App for the bot:
1. **Frontend**: Scaffold a basic HTML/JS/CSS structure or integrate with the existing `[TECH_STACK]` frontend framework (React/Vue/Svelte).
2. Include the official Telegram Web App JS library (`https://telegram.org/js/telegram-web-app.js`).
3. **Backend**: Create the secure API endpoint to validate `initData` sent from the Mini App using the bot's secret token.
4. **UX**: Configure the Main Button or Back Button interactions as requested. Ensure the app is responsive to Telegram's theme colors (`tg.themeParams`).
5. Wire up the inline keyboard or menu button in the bot to launch the Web App URL.
6. Document the setup and required URL configuration for BotFather in `.claude/memory/bot_manifest.md`.