# /commit
*Analyze staged changes and commit using the advanced framework protocol.*

1. Run `git status` and `git diff --cached` to understand the changes.
2. If no files are staged, ask the user what to stage (e.g., `git add .`).
3. Invoke the `commit` skill to format the message according to `master_protocol.md`.
4. Run the git commit command using a heredoc.
