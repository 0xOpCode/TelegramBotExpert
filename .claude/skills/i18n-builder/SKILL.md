---
name: i18n-builder
description: Use this skill to scaffold and manage internationalization (i18n) strings for the telegram bot.
tools: ["Bash", "Write", "Edit"]
---
## i18n Build Protocol
When tasked with adding multiple languages to the bot:
1. Setup a directory structure for locales (e.g., `/locales/en.json`, `/locales/ru.json`) consistent with `[TECH_STACK]`.
2. Extract hardcoded strings from handlers and keyboards into the default locale file.
3. Integrate the i18n middleware for the chosen framework (e.g., `fluent`, `i18next`, or custom `gettext` implementation).
4. Configure the middleware to detect user language from `update.message.from.language_code` or DB.
5. Create a language switcher flow `/language` (using `tg-ux-engineer` if needed) to allow manual overrides.
6. Verify fallback mechanisms for missing translations.