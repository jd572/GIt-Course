# The Full Lifecycle, Start to Finish

| Step | Command | What It Does |
|---|---|---|
| 1 | `git init` | Create the repository (once per project) |
| 2 | `git config` | Tell Git who you are (once per machine) |
| 3 | `git status` | See what's changed - run this constantly |
| 4 | `git add <file>` | Working Directory -> Staging Area |
| 5 | `git diff` / `git diff --staged` | Review changes before / after staging |
| 6 | `git commit -m "..."` | Staging Area -> Repository (permanent) |
| 7 | `git log` | Explore the history you've built |

Once a remote is involved, the loop extends to:

| Step | Command | What It Does |
|---|---|---|
| 8 | `git remote add origin <url>` | Link the repo to a remote (once) |
| 9 | `git push -u origin main` | Upload history, set default upstream |
| 10 | `git pull origin main` | Bring teammates' changes down |
| 11 | `git branch` / `git switch -c` | Work on features in isolation |
| 12 | `git merge <branch>` | Bring finished work back into `main` |

See `command-cheat-sheet.md` for the full quick-reference table.
