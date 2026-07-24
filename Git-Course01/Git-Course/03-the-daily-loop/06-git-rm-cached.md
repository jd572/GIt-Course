# git rm --cached

## What It Does
Removes a file from Git's tracking without deleting it from disk.

## Use Case
- The fix when something sensitive (like `creds.txt`) gets committed by
  mistake.
- Untracking a file that should never have been added in the first place.

## Syntax
```
git rm --cached <file>
```

## Example
```
$ git rm --cached creds.txt
rm 'creds.txt'
$ git commit -m "removed the creds file"
[main 224a939] removed the creds file
 1 file changed, 2 deletions(-)
 delete mode 100644 creds.txt
```

## Notes
- The file instantly becomes both "deleted" (staged) and "Untracked" again
  - it's back in the Working Directory only, still safely on disk.
- Commit the removal, then add the file to `.gitignore` (see
  `07-good-practices/01-gitignore.md`) so it can't be re-added by accident.
- This does **not** remove the file from earlier commits in history - only
  from the current tracked state going forward.
