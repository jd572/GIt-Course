# git revert

## What It Does
Undoes a commit by adding a new, opposite commit - the original commit
stays in history, and a new one cancels its effect.

## Use Case
- Safely undoing a change on shared/pushed history, since nothing already
  pushed is rewritten.
- Publicly reversing a bad commit without disrupting teammates who already
  pulled it.

## Syntax
```
git revert <commit-hash>
```

## Example
```
$ git revert 6d1a9c1
[main 7f2b3aa] Revert "My second commit"
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## Notes
- Safe on shared history - unlike `git reset`, it never rewrites existing
  commits.
- Git may open an editor to confirm/edit the revert commit message.
- If the revert conflicts with later changes, you'll resolve it the same
  way as a merge conflict (see `07-good-practices/03-merge-conflicts.md`).
