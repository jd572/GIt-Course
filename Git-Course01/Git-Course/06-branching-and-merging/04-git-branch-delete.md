# Force-Deleting a Branch: git branch -D

## What It Does
Deletes a branch even if Git's safety check thinks it has unmerged commits.

## Use Case
- Cleaning up an abandoned branch whose work you deliberately don't want.
- Removing a branch after confirming its commits are reachable elsewhere
  (or genuinely disposable).

## Syntax
```
git branch -d <name>   # safe - blocks if not fully merged
git branch -D <name>   # force - deletes regardless
```

## Example
```
$ git branch -d feature2
error: the branch 'feature2' is not fully merged
hint: If you are sure you want to delete it, run 'git branch -D feature2'
$ git branch -D feature2
Deleted branch feature2 (was 5d975d3).
```

## Notes
- Unlike a branch whose work was already merged, this branch still has
  commits that don't exist anywhere else yet - Git's safety check blocks
  the lowercase `-d` with "not fully merged".
- The hint tells you exactly what to do if you're certain: uppercase `-D`
  forces the delete regardless of merge status.
- Force-deleting is genuinely destructive if those commits aren't reachable
  from any other branch or tag - double-check with `git log` or
  `git branch --merged` before reaching for `-D`.
- To also remove a branch from the remote:
  ```
  git push origin --delete <branch-name>
  ```
