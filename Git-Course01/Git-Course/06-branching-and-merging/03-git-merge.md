# git merge

## What It Does
Brings one branch's commits into the branch you currently have checked out.

## Use Case
- Bringing a completed feature branch back into `main`.
- Combining parallel lines of work into one history.

## Syntax
```
git merge <branch>
```

## Example - Fast-Forward Merge
```
$ git merge feature1
Updating 643fe6a..a4f83e0
Fast-forward
 .DS_Store        | Bin 0 -> 6148
 UesrService.txt  |  4 +++-
 adminservice.txt |  1 +
 3 files changed, 4 insertions(+), 1 deletion(-)
```
Because `main` hadn't moved since `feature1` branched off, Git performs a
fast-forward - it simply slides `main`'s pointer forward to `feature1`'s
tip; no new merge commit is created.

Before merge: `main` and `feature1` point at different commits.
After merge: `main` now points at the same commit `feature1` already did.

## Example - Merge Conflict
See `07-good-practices/03-merge-conflicts.md` for what happens when both
branches edit the same lines and Git can't automatically pick a winner.

## Notes
- Every fast-forward merge simply moves a pointer - it's the simplest case.
- Run `git pull origin main` (see `05-working-with-remotes/04-git-pull.md`)
  before merging, so you're comparing against the most up-to-date `main`.
- After merging, the feature branch is safe to delete
  (`06-branching-and-merging/01-git-branch.md`).
