# git blame

## What It Does
Shows which commit and author last touched each line of a file.

## Use Case
- Tracking down when and why a specific line changed.
- Finding who to ask about a confusing piece of code.
- Investigating when a bug was introduced.

## Syntax
```
git blame <file>
git blame -L <start>,<end> <file>   # limit to a line range
```

## Example
```
$ git blame FirstCode.txt
b0e0e83b (Your Name 2026-07-21 12:01:49 +0530 1) Hello world!!!
6d1a9c1a (Your Name 2026-07-21 13:15:02 +0530 2) Welcome the Git Training session!
```

## Notes
- Each line shows the short commit hash, author, date, and the line itself.
- Useful paired with `git show <commit>` to see the full context of that
  change.
