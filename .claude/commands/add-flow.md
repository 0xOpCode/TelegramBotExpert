# /add-flow [DESCRIPTION]
*Example: `/add-flow "User registration wizard with email validation"`*

1. Spawn `tg-architect` to design the FSM states and database changes needed.
2. Spawn `tg-ux-engineer` to draft the prompts, error messages, and Inline Keyboards.
3. Write the resulting implementation to the codebase.
4. Update `.claude/memory/bot_manifest.md` to register the new conversation flow.