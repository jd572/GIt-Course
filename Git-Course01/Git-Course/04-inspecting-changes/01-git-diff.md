# git diff

## What It Does
Shows exactly what changed, line by line, before you stage it.

## Use Case
- Reviewing edits before running `git add`.
- Catching accidental changes (whitespace, debug statements) before they're
  staged.

## Syntax
```
git diff
git diff <file>
```

## Example
```
$ git diff
diff --git a/FirstCode.txt b/FirstCode.txt
--- a/FirstCode.txt
+++ b/FirstCode.txt
-Hello world!!!
+Hello world!!!
+Welcome the Git Training session!
```

## Notes
- Lines starting with `-` were removed, lines with `+` were added - plain
  context lines are unchanged.
- This is your last check before running `git add`.
- Once you `git add` the file, plain `git diff` goes quiet - the change is
  no longer "unstaged" (see `02-git-diff-staged.md`).
