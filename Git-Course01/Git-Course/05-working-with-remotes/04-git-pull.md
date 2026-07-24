# git pull

## What It Does
Fetches the latest commits from the remote and merges them into your
current local branch, in one combined step.

## Use Case
- Syncing your local `main` with a teammate's pushed changes before starting
  new work.
- Updating right before merging a feature branch, so you're comparing
  against the most up-to-date main.

## Syntax
```
git pull origin main
git pull            # once upstream tracking is set, just "git pull"
```

## Example
```
$ git switch main
Switched to branch 'main'
$ git pull origin main
$ git status
On branch main
Your branch is up to date with 'origin/main'.
```

## Notes
- Under the hood, `pull` is really two commands in sequence: `git fetch`
  (download) followed by `git merge` (combine) - useful to know when
  troubleshooting.
- `git fetch` alone downloads remote changes without merging them, if you
  want to inspect before integrating.
- Run this before starting new work, and especially right before merging a
  feature branch.
