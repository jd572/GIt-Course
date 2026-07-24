# git cherry-pick

## What It Does
Copies one specific commit from another branch onto your current branch,
without merging everything else from that branch.

## Use Case
- Pulling a single bug fix from a feature branch into `main` without
  bringing in unfinished work.
- Applying a hotfix commit to multiple release branches.

## Syntax
```
git cherry-pick <commit-hash>
```

## Example
```
$ git cherry-pick 5d975d3
[main 8a1c2f0] Fix header bug
 1 file changed, 2 insertions(+)
```

## Notes
- Creates a new commit with the same changes and message, but a new hash
  (since it now has a different parent commit).
- Conflicts can occur if the target branch has diverged - resolve the same
  way as a merge conflict.
