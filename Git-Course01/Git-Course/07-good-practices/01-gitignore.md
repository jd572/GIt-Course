# .gitignore - Keeping Files Out of Git

## What It Does
A plain text file named `.gitignore`, placed at the project root, tells Git
which files or patterns to never show as "Untracked" - so they can't be
added by accident.

## Use Case
- Preventing secrets, credentials, or environment files from ever being
  committed.
- Excluding build output, dependency folders, and OS/editor clutter from
  version control.
- The permanent fix for a `creds.txt`-style mistake: `git rm --cached`
  removes something already committed, while `.gitignore` stops it from
  happening again.

## Syntax
```
# inside .gitignore
creds.txt
.DS_Store
node_modules/
*.log
```

## Example
```
$ cat .gitignore
creds.txt
.DS_Store
node_modules/
*.log
$ git status
On branch main
nothing to commit, working tree clean
(creds.txt and .DS_Store never appear)
```

## Notes
- Common candidates: build output (`dist/`, `node_modules/`), OS clutter
  (`.DS_Store`), secrets and credentials, and editor settings folders
  (`.vscode/`, `.idea/`).
- `.gitignore` only affects files Git isn't already tracking. If a file was
  committed before being added to `.gitignore`, run `git rm --cached
  <file>` first (see `03-the-daily-loop/06-git-rm-cached.md`).
- This project's own `.gitignore` (at the repo root) demonstrates a
  reasonable starting set of patterns.
