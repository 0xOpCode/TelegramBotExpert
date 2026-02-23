---
name: create-db-schema
description: Use this skill when asked to create or update database schemas for the telegram bot.
tools: ["Bash", "Write", "Edit"]
---
## DB Schema Pattern Protocol
When tasked with building or updating a DB schema for the bot:
1. Ensure the DB technology choice aligns with `[TECH_STACK]` and `bot_manifest.md` (e.g., PostgreSQL + Prisma, MongoDB + Mongoose, SQLite).
2. Create models for standard bot entities if not present:
   - `User`: `telegram_id` (Primary Key or Unique), `username`, `first_name`, `language_code`, `created_at`
   - `Session`/`State` (if DB-backed FSM): `telegram_id`, `current_state`, `state_data`
3. Design models specifically for the requested feature.
4. Scaffold the connection and repository/DAO layer to interface with the schema cleanly.
5. Update `bot_manifest.md` to reflect any new DB requirements or structure.