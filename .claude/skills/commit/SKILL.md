---
name: commit
description: Use this skill to craft high-quality, structured, and informative git commits according to the master protocol.
tools: ["Bash"]
---
## Git Commit Protocol Executer
When tasked with writing a git commit, always enforce the structured protocol from `master_protocol.md`.

**Format Pattern:**
```
[Module/Feature Name] Summary of the core change (Capitalized)

Changes:
• Detail 1: What changed and the specific file/function affected.
• Detail 2: How this impacts the bot's behavior.
• Detail 3: Edge cases handled or API limits respected.

Reasoning/Context:
Brief explanation of WHY this approach was taken.

Next Steps (if applicable):
What needs to be done immediately following this commit.
```

1. Use `git diff --cached` and `git status` to analyze the staged changes.
2. If nothing is staged, remind the user to stage files or ask to stage them automatically.
3. Generate the commit message strictly following the format above.
4. Execute the commit using a heredoc:
   ```bash
   git commit -m "$(cat <<'EOF'
   [Module] Summary
   
   Changes:
   • ...
   EOF
   )"
   ```
