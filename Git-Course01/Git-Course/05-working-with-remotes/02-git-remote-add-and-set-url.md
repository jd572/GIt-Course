# git remote add / git remote set-url

## What It Does
`git remote add origin <url>` links a local repo to a remote named "origin".
`git remote set-url origin <url>` changes the URL an existing remote points
to, without losing history or the nickname.

## Use Case
- Connecting a freshly-initialized local repo to a new, empty GitHub repo.
- Switching an existing remote from HTTPS to SSH (or vice versa).

## Syntax
```
git remote add origin <url>
git remote set-url origin <url>
```

## Example - Connecting a Local Repo to GitHub
```
$ git branch -M main
$ git remote add origin https://github.com/user/Git-Course.git
$ git push -u origin main
...
* [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

## Example - Switching HTTPS to SSH
```
$ git remote add origin git@github.com:user/Git-Course.git
error: remote origin already exists.
$ git remote set-url origin git@github.com:user/Git-Course.git
$ git push -u origin main
branch 'main' set up to track 'origin/main'.
```

## Notes
- `git branch -M main` renames your current branch to "main" - handy if an
  older Git left you on "master".
- `git remote add origin` only works the first time - Git refuses with
  "remote origin already exists" if that name is already registered. Use
  `set-url` to change the URL in place instead of removing and re-adding.
- Once the URL points at an SSH address, every future push or pull
  authenticates with your SSH key automatically - no more username or token
  prompts.
