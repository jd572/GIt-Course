# Default Branch: master -> main

## What It Does
Controls the name of the first branch created by `git init`.

## Use Case
- Historically, `git init` created a first branch called `master`.
- Modern Git (and most teams/hosts like GitHub) now default to `main`
  instead.
- Use `-b main` explicitly if your local Git version still defaults to
  `master` and you want to match current conventions.

## Syntax
```
git init -b main
# or, after the fact, on an existing repo with no risky shared history:
git branch -M main
```

## Example
```
$ git init -b main
Initialized empty Git repository in ~/First_Project/.git/
```

## Notes
- The branch name is cosmetic - everything else about Git works identically
  no matter what you call your default branch.
- Renaming later with `git branch -M main` is safe locally; if the branch
  was already pushed under the old name, you'll need to update the remote
  too (push the new name, then delete the old one on the remote).
- You can set this globally so every future `git init` uses `main`:
  ```
  git config --global init.defaultBranch main
  ```
