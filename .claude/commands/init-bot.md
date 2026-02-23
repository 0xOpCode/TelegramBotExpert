# /init-bot [LANGUAGE/FRAMEWORK]
*Example: `/init-bot python/aiogram` or `/init-bot nodejs/telegraf`*

1. Run `rg -l "\[TECH_STACK\]" .claude/ CLAUDE.md` to find all placeholder files.
2. Use the `Edit` tool to replace all instances of `[TECH_STACK]` with the provided framework in:
   - `CLAUDE.md`
   - `.claude/agents/tg-architect.md`
   - `.claude/agents/tg-ux-engineer.md`
   - `.claude/agents/tg-sec-auditor.md`
   - `.claude/skills/tg-api-navigator/SKILL.md`
   - `.claude/memory/master_protocol.md`
   - `.claude/memory/bot_manifest.md`
3. Generate a baseline `.claude/memory/bot_manifest.md` documenting the chosen framework, entry point file, and core dependencies if it doesn't exist or update it.
4. Output: "Bot framework bound to [FRAMEWORK]. TelegramBotExpert is ready to build."