# git commit -a -m

## What It Does
The `-a` flag auto-stages every already-tracked file that changed, skipping
a separate `git add` step, then commits in the same call.

## Use Case
- Quick edits to files Git is already tracking.
- Skipping the extra `git add` step when you know you want everything
  tracked staged as-is.

## Syntax
```
git commit -a -m "message"
```

## Example
```
$ git commit -a -m "My third commit"
[main 862e5e7] My third commit
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## Notes
- Important limit: `-a` only catches **modified or deleted tracked files**.
  Brand-new, untracked files still need an explicit `git add`.
- Handy for quick edits; many teams still prefer explicit `git add` for
  clarity and to review exactly what's being staged.
