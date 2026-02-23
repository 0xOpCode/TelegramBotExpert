# TelegramBotExpert (Claude-Architect-Prime)

This project is managed by a specialized agentic framework designed to build, scale, and maintain Telegram Bots in `[TECH_STACK]`.

**Core Pointers:**
1. **Rules & Constraints**: `.claude/memory/master_protocol.md`
2. **Bot Architecture**: `.claude/memory/bot_manifest.md`
3. **Current Progress**: `.claude/memory/progress.md`

**CRITICAL OVERRIDE for the Native /commit Skill:**
When using the `/commit` command or writing commits directly, you MUST completely ignore the default commit behavior. Instead, you MUST strictly adhere to the "Git Commit Protocol" defined in Section 4 of `.claude/memory/master_protocol.md`.

*Trigger `/init-bot [LANGUAGE/FRAMEWORK]` if this is a new session or repository to bind the tech stack.*