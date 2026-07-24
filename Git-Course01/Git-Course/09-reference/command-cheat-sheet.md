# Command Cheat Sheet

## Core Workflow
| Command | Purpose |
|---|---|
| `git --version` | Check installed Git version |
| `git config --global user.name/email` | Set your commit identity |
| `git init [-b main]` | Create a repo, set branch name |
| `git status` | Show the state of the working tree |
| `git add <file> / .` | Stage specific file(s) / everything |
| `git commit -m "msg"` | Save the staged snapshot |
| `git commit -a -m "msg"` | Auto-stage tracked, then commit |
| `git diff` / `--staged` | Review unstaged / staged changes |
| `git log` / `--pretty=oneline` | View history, full or compact |
| `git rm --cached <file>` | Untrack a file, keep it on disk |

## Remotes & Tags
| Command | Purpose |
|---|---|
| `git clone <url>` | Download an existing repository |
| `git remote -v` | List configured remotes |
| `git remote add origin <url>` | Link this repo to a remote |
| `git remote set-url origin <url>` | Change a remote's URL |
| `git push -u origin main` | Upload + set default upstream |
| `git push origin <branch>` | Upload a branch, first time |
| `git pull origin main` | Fetch + merge remote changes |
| `git tag [-a] v1.0 -m "msg"` | Lightweight / annotated tag |
| `git push origin <tag>` | Upload one tag by name |
| `git push origin --delete <name>` | Remove a branch/tag from remote |

## Branching & Merging
| Command | Purpose |
|---|---|
| `git branch [--all]` | List local / all branches |
| `git switch -c <name>` | Create branch and switch to it |
| `git switch <name> / -` | Switch branches / go back |
| `git branch -d / -D <name>` | Delete a branch (safe / forced) |
| `git merge <branch>` | Bring a branch into the current one |

## Good Practices & Advanced
| Command | Purpose |
|---|---|
| `.gitignore` | Keep specified files out of Git entirely |
| `git stash` / `git stash pop` | Set work aside temporarily, then restore it |
| `git revert <commit>` | Undo a commit safely on shared history |
| `git reset` | Move HEAD backward (rewrites local history) |
| `git cherry-pick <commit>` | Copy one commit onto the current branch |
| `git rebase <branch>` | Replay commits for a linear history |
| `git blame <file>` | See who last touched each line |
| `git show <commit>` | View one commit's full diff in isolation |
