# git config --global user.name / user.email

## What It Does
Git stamps every commit with an author name and email. `git config` sets
these values in a config file so Git doesn't have to ask each time.

## Use Case
- Required before your very first commit - Git will complain if identity is
  unset.
- Setting up a brand-new machine or a fresh Git install.
- Distinguishing personal vs. work identities across different projects
  (by omitting `--global` inside a specific repo).

## Syntax
```
git config --global user.name "<Your Name>"
git config --global user.email "<you@example.com>"
```

## Example
```
$ git config --global user.name "Your Name"
$ git config --global user.email "you@example.com"
```
(no output - success is silent)

## Notes
- `--global` applies the setting to every repository for your user account
  on this machine.
- Omit `--global` to configure just the current project - useful when you
  need a different email for work vs. personal repos.
- Config is layered: **system -> global -> local (per repo)** - each level
  can override the one before it.
- This is a one-time setup step per machine, not something you repeat per
  project (unless you need a local override).
