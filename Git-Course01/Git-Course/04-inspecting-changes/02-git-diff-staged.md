# git diff --staged

## What It Does
Shows what's sitting in the Staging Area, ready for the next commit.

## Use Case
- Double-checking exactly what will be committed, after running `git add`.
- Reviewing a batch of staged changes across multiple files before
  finalizing a commit message.

## Syntax
```
git diff --staged
git diff --cached   # equivalent alias
```

## Example
```
$ git add FirstCode.txt
$ git diff
(nothing - no unstaged changes left)
$ git diff --staged
-Hello world!!!
+Hello world!!!
+Welcome the Git Training session!
```

## Notes
- `--staged` and `--cached` are interchangeable flags for the same thing.
- Together, `git diff` and `git diff --staged` let you review changes at
  every stage before committing: unstaged first, then staged.
