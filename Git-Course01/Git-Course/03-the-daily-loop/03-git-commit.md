# git commit

## What It Does
Moves everything in the Staging Area permanently into the Repository as a
new snapshot.

## Use Case
- Saving a checkpoint you can inspect or return to later.
- Recording a logical, reviewable unit of work with a clear message.

## Syntax
```
git commit              # opens your default text editor for a message
git commit -m "message" # supply the message inline
```

## Example
```
$ git commit -m "My first commit"
[main (root-commit) b0e0e83] My first commit
 1 file changed, 1 insertion(+)
 create mode 100644 FirstCode.txt
```

## Common Mistake: Skipping git add
```
$ git commit -m "My second commit"
On branch main
Changes not staged for commit:
        modified:   FirstCode.txt

no changes added to commit (use "git add" and/or "git commit -a")
-> nothing was saved to the repository
```
Committing without staging first does nothing - Git refuses because the
Staging Area is still empty. Commit only ever saves what's in the Staging
Area, never the raw Working Directory.

## The Fix - Stage, Then Commit
```
$ git add FirstCode.txt
$ git commit -m "My second commit"
[main 6d1a9c1] My second commit
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## Notes
- The output confirms the branch, a short commit hash, the message, and
  which files changed.
- This add -> commit pair is the rhythm you'll repeat for every change,
  forever.
