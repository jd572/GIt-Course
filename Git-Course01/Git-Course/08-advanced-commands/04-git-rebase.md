# git rebase

## What It Does
Replays your commits on top of another branch instead of merging - produces
a straighter, linear history.

## Use Case
- Keeping a feature branch's history linear before merging into `main`.
- Cleaning up a messy sequence of local commits before sharing them.

## Syntax
```
git rebase <branch>
git rebase -i <branch>   # interactive rebase - reorder, squash, edit commits
```

## Example
```
$ git switch feature1
$ git rebase main
Successfully rebased and updated refs/heads/feature1.
```

## Notes
- Unlike merge, rebase rewrites commit hashes - never rebase commits that
  have already been pushed and shared, unless the whole team agrees
  (force-push required, and it can break teammates' local history).
- Interactive rebase (`-i`) is commonly used to squash multiple small
  commits into one clean commit before opening a pull request.
