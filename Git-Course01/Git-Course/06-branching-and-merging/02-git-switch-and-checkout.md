# git switch / git checkout - Creating & Switching Branches

## What It Does
Moves `HEAD` (and your Working Directory) onto a different branch. With
`-c` / `-b`, it also creates the branch first.

## Use Case
- Starting a new feature in isolation from `main`.
- Moving between in-progress branches.
- Quickly jumping back to whatever branch you were just on.

## Syntax
```
git checkout -b <name>   # classic: create + switch
git switch -c <name>     # modern equivalent
git switch <name>        # switch to an existing branch
git switch -             # jump back to the previous branch
```

## Example - Switching to a Branch That Doesn't Exist
```
$ git checkout feature1
error: pathspec 'feature1' did not match any file(s) known to git
```
"pathspec did not match any file(s)" is Git's way of saying there's nothing
by that name to switch to.

## Example - Create and Switch
```
$ git checkout -b feature1
Switched to a new branch 'feature1'
$ git switch -c feature2
Switched to a new branch 'feature2'
```

## Example - Jumping Back
```
$ git switch -
Switched to branch 'feature1'
```

## Notes
- `git checkout -b <name>` (classic) and `git switch -c <name>` (modern)
  both do two things at once: create the branch and move `HEAD` onto it
  immediately.
- `git switch` was introduced to split "switching branches" out from
  checkout's older, more overloaded job of also restoring files - prefer it
  going forward for branch operations.
- `main` and `feature1` can point at completely different commits at the
  same time; switching branches just changes which commit your Working
  Directory reflects.
