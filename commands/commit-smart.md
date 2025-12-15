# Smart Commit

Analyze uncommitted changes, group them logically by subsystem or purpose, and create separate well-formatted commits for each group.

## Process

1. **Analyze Changes**
   - Run `git status` and `git diff --stat` to see all uncommitted changes
   - Identify modified, added, and untracked files

2. **Group Logically**
   Group changes by:
   - Subsystem (e.g., auth, database, protocol, world)
   - Purpose (e.g., security, bugfix, feature, refactor, docs)
   - Related functionality (files that work together)

   Present the proposed groupings as a table:
   | Commit | Files | Purpose |
   |--------|-------|---------|
   | 1. ... | ... | ... |

3. **Get Approval**
   Ask: "Proceed with these commits?"

4. **Create Commits**
   For each group:
   - Stage only the relevant files with `git add`
   - Create commit with conventional commit message format:
     ```
     type: short description

     Longer explanation if needed.

     🤖 Generated with [Claude Code](https://claude.com/claude-code)

     Co-Authored-By: Claude <noreply@anthropic.com>
     ```
   - Types: feat, fix, refactor, docs, test, chore

5. **Verify**
   - Run `git log --oneline -N` to show the created commits
   - Report success

6. **Ask About Push**
   Ask: "Push these commits to origin?"
   - If yes: `git push`
   - If no: Done

## Guidelines

- Never commit sensitive files (.env, credentials, etc.)
- Check for untracked files that should be gitignored
- Keep commits atomic - one logical change per commit
- Use descriptive commit messages that explain "why" not just "what"
- Prefer smaller, focused commits over large mixed ones
