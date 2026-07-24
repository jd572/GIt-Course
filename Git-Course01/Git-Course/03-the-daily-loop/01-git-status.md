# git status

## What It Does
Reports the current state of your Working Directory and Staging Area. It is
your dashboard - it never changes anything, it only reports.

## Use Case
- Run it constantly, before and after almost every other Git command.
- Checking whether a file is untracked, modified, or staged.
- Confirming a clean working tree before switching branches or pulling.

## Syntax
```
git status
git status -s   # short format
```

## Example - Untracked File
```
$ git status
On branch main
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        FirstCode.txt

nothing added to commit but untracked files present (use "git add" to track)
```

## Example - After Staging
```
$ git status
On branch main
No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   FirstCode.txt
```

## Example - Clean Working Tree
```
$ git status
On branch main
nothing to commit, working tree clean
```

## Notes
- "No commits yet" confirms the repo is brand new.
- "Untracked" means Git sees the file but isn't watching it for changes yet
  - it lives only in the Working Directory.
- "nothing to commit, working tree clean" is the goal state before switching
  branches, pulling updates, or ending a session.
