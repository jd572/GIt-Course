# git add

## What It Does
Moves a change from the Working Directory into the Staging Area. It does not
save history yet - it just marks "this is what I want in my next commit."

## Use Case
- Selecting exactly which changes go into the next snapshot.
- Staging a single file, several specific files, or everything at once.
- Preparing new files (untracked) or modified files (already tracked) for a
  commit.

## Syntax
```
git add <file>
git add <file1> <file2>
git add .          # stage everything in the current directory
```

## Example
```
$ git add FirstCode.txt
(no output - success is silent)
```

## Example - Multiple New Files at Once
```
$ git status
Untracked files:
        Readme.md
        creds.txt
$ git add .
$ git commit -m "readme and story 3.2"
[main 9f3f771] readme and story 3.2
 2 files changed, 3 insertions(+)
 create mode 100644 Readme.md
 create mode 100644 creds.txt
```

## Notes
- `git add .` stages every change in the current directory in one shot,
  instead of naming files one by one.
- To undo a stage without deleting the file, use `git rm --cached <file>`.
- Staging is silent on success - no news is good news.
