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

## 4. Git Commit Protocol
Do not use legacy conventional commits (e.g., `feat: ...`). Write beautiful, structured, and deeply informative commit messages that allow agents and humans to understand the full context without reading diffs.

**Format Pattern:**
```
[Module/Feature Name] Summary of the core change (Capitalized)

Changes:
• Detail 1: What changed and the specific file/function affected.
• Detail 2: How this impacts the bot's behavior (e.g., state management, API calls).
• Detail 3: Any edge cases handled or Telegram limits respected.

Reasoning/Context:
Brief explanation of WHY this approach was taken (e.g., "Switched to Webhooks to reduce latency", "Added FSM to handle multi-step user onboarding safely").

Next Steps (if applicable):
What needs to be done immediately following this commit.
```

**Example:**
```
[User Registration FSM] Implemented Multi-step Onboarding Flow

Changes:
• Scaffolded `UserRegistrationState` in `src/states/registration.ts` handling name, email, and age.
• Added Inline Keyboard to the `/start` handler to trigger the registration wizard.
• Connected the final FSM step to the `User` DB schema via Prisma.

Reasoning/Context:
The bot previously relied on stateless text matching which caused collisions. Moving to a dedicated FSM prevents state bleeding and ensures we gather all necessary data before inserting the user into the DB.

Next Steps:
Need to add email validation regex and rate-limiting to the registration endpoint.
```