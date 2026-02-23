# Telegram Bot Master Protocol

## 1. Architectural Standards
- **Event-Driven**: Always separate command handlers, callback query handlers, and message handlers logically.
- **State Management**: Use Finite State Machines (FSM) or session stores for multi-step user conversations. Never rely on stateless message text matching for complex flows.
- **Rate Limiting**: Always account for Telegram's limits (30 msgs/sec overall, 1 msg/sec per user). Implement delays or queueing for bulk broadcasting.
- **MarkdownV2/HTML**: Strictly escape user input before sending it back via ParseMode to prevent formatting injection errors.

## 2. Agent Handoffs
- Use `tg-architect` for defining database schemas, webhook vs polling strategies, and FSM design.
- Use `tg-ux-engineer` for designing InlineKeyboards, WebApps (Mini Apps), and BotFather commands.
- Use `tg-sec-auditor` to verify that private data isn't leaking in logs or unprotected commands.

## 3. Dynamic Tech Stack
- The current stack is `[TECH_STACK]`. All scripts, linters, and bash commands must align with this ecosystem (e.g., pip/npm/go mod).