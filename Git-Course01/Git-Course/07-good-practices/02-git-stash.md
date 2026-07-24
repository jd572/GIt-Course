# git stash

## What It Does
Takes uncommitted changes (staged or not) off the Working Directory and
tucks them away, leaving a clean working tree - without creating a commit.

## Use Case
- Switching branches urgently (a hotfix, a demo) but you aren't ready to
  commit half-finished work yet.
- Temporarily clearing your working tree to pull updates cleanly.

## Syntax
```
git stash              # save current changes
git stash pop          # re-apply the most recent stash and remove it
git stash list          # see all stashed entries
git stash apply         # re-apply without removing from the stash list
```

## Example
```
$ git status
modified:   Userdata.txt
$ git stash
Saved working directory and index state WIP on feature1: 5d975d3 added the user1
$ git status
nothing to commit, working tree clean
$ git stash pop
modified:   Userdata.txt
```

## Notes
- `git stash pop` brings the most recent stash back, re-applying it to the
  Working Directory and removing it from the stash list.
- `git stash apply` does the same re-apply but keeps the stash entry around
  in case you need it again.
- Stashes are local only - they are not pushed to a remote.
