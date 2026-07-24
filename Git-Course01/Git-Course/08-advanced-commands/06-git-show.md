# git show

## What It Does
Displays one commit's full diff and metadata in isolation, without wading
through the whole log.

## Use Case
- Inspecting exactly what a single commit changed.
- Reviewing a tag's associated commit and message (see
  `05-working-with-remotes/07-git-tag.md`).

## Syntax
```
git show <commit-hash>
git show <tag-name>
```

## Example
```
$ git show b0e0e83
commit b0e0e83b836d66dcbd16fe18...
Author: Your Name <you@example.com>
Date:   Tue Jul 21 12:01:49 2026 +0530

    My first commit

diff --git a/FirstCode.txt b/FirstCode.txt
new file mode 100644
--- /dev/null
+++ b/FirstCode.txt
+Hello world!!!
```

## Notes
- Combines the metadata of `git log` with the line-by-line detail of
  `git diff`, but scoped to a single commit.
- Works on tags too - `git show v1.0` shows the tagged commit (lightweight)
  or the tag object itself plus the commit (annotated).
