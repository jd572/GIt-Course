# Git & Version Control - From Zero to First Commits

A hands-on reference course covering Git fundamentals: configuration, the
three-tree model, staging, committing, inspecting history, remotes, and
branching/merging.

This repository is organized as a set of self-contained lessons. Each command
has its own file with:

- **What it does** - a plain-English explanation
- **Use case** - when and why you'd reach for this command
- **Syntax** - the general command form
- **Example** - a real terminal session with sample output
- **Notes** - gotchas, related commands, and good practices

## How to Use This Repo

Work through the folders in numeric order. Each one builds on the last, the
same way the original training session did.

## Session Roadmap

| # | Folder | Topic |
|---|--------|-------|
| 01 | `01-getting-started` | Checking your install and configuring your identity |
| 02 | `02-starting-a-repository` | `git init`, and the master -> main branch story |
| 03 | `03-the-daily-loop` | `git status`, `git add`, `git commit` - over and over |
| 04 | `04-inspecting-changes` | `git diff` to inspect changes before and after staging |
| 05 | `05-working-with-remotes` | Connecting to GitHub/GitLab/Bitbucket, push, pull, clone, tags |
| 06 | `06-branching-and-merging` | Creating, switching, merging, and deleting branches |
| 07 | `07-good-practices` | `.gitignore`, `git stash`, resolving merge conflicts |
| 08 | `08-advanced-commands` | `revert`, `reset`, `cherry-pick`, `rebase`, `blame`, `show` |
| 09 | `09-reference` | Full lifecycle recap and command cheat sheet |

## The Three Trees of Git

Every file in a Git project always lives in one (or more) of three places:

1. **Working Directory** - files you're editing on disk
2. **Staging Area** (the "index") - changes marked for the next commit
3. **Repository** (the `.git` database) - permanent, committed history

```
Working Directory  --git add-->  Staging Area  --git commit-->  Repository
```

## The Everyday Git Loop

```
edit a file -> git status -> git add <file> -> git commit -m "..." -> git log
```

This edit -> add -> commit cycle repeats for the life of a project.

## Prerequisites

- Git installed (`git --version` to check)
- A terminal / shell
- Optional: a GitHub, GitLab, or Bitbucket account for the remotes section

## License

See [LICENSE](LICENSE). Training material - free to reuse and adapt.
