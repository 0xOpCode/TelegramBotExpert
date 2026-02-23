---
name: tg-api-navigator
description: Use this skill to quickly find handlers, middleware, and API integrations within the bot's specific [TECH_STACK] codebase.
tools: ["Bash", "Grep"]
---
## Navigation Protocol for `[TECH_STACK]`
Since the stack is dynamic, use these conceptual patterns to find code:

1. **Find Command Handlers**:
   `rg -i "(command|start|help|onCommand)" --type [LANG_EXT]`
2. **Find Callback Queries (Button Clicks)**:
   `rg -i "(callback|action|onCallback)" --type [LANG_EXT]`
3. **Find State / FSM Definitions**:
   `rg -i "(state|scene|wizard|fsm)" --type [LANG_EXT]`
4. **Find API calls to Telegram**:
   `rg -i "(sendMessage|editMessage|sendPhoto|answerCallbackQuery)" --type [LANG_EXT]`