# git config --global --list

## What It Does
Displays every configuration value Git currently has saved, so you can
confirm what was actually written.

## Use Case
- Verifying `user.name` and `user.email` are set correctly before your first
  commit on a new machine.
- Debugging unexpected Git behavior that might come from a stray config
  value (e.g. a wrong email, a misconfigured alias).
- Auditing which config layer (system, global, or local) is providing a
  given value.

## Syntax
```
git config --global --list
git config --list            # includes system + global + local, merged
git config --local --list    # only the current repository's settings
```

## Example
```
$ git config --global --list
user.name=Your Name
user.email=you@example.com
```

## Notes
- Good habit: run this before your very first commit on any new machine.
- Use `git config --get user.email` to check a single key without listing
  everything.
- Config values live in plain text files: `~/.gitconfig` (global) and
  `.git/config` (local, inside a repository).
