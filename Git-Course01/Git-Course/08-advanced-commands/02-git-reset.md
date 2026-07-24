# git reset

## What It Does
Moves `HEAD` (and optionally the staging area / working files) backward to
an earlier commit.

## Use Case
- Undoing local commits that haven't been pushed yet.
- Unstaging files without discarding their edits.

## Syntax
```
git reset --soft <commit>    # move HEAD only, keep staged + working changes
git reset --mixed <commit>   # move HEAD + unstage, keep working changes (default)
git reset --hard <commit>    # move HEAD, unstage, and discard working changes
```

## Example
```
$ git reset --soft HEAD~1
(last commit undone, changes remain staged)
```

## Notes
- Powerful, but rewrites history if used after pushing - avoid `reset` on
  commits others may have already pulled.
- `--hard` is destructive: uncommitted working directory changes are lost.
  Double-check `git status` and `git diff` before using it.
- For shared/pushed history, prefer `git revert` instead.
