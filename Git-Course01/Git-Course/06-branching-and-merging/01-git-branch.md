# git branch - Listing, Creating, Deleting

## What It Does
Manages branch pointers: listing existing branches, and (combined with `-d`
or `-D`) deleting them.

## Use Case
- Seeing which branch you're currently on.
- Viewing all local branches, or including remote-tracking branches.
- Cleaning up branches once their work has been merged.

## Syntax
```
git branch                 # list local branches
git branch --all           # list local + remote-tracking branches
git branch -d <name>       # safe delete (blocks if unmerged)
git branch -D <name>       # force delete regardless of merge status
```

## Example - Listing
```
$ git branch
  feature1
* feature2
  main
$ git branch --all
  ...
  remotes/origin/main
```
The asterisk marks whichever branch `HEAD` currently points at - your
current branch. `--all` also lists remote-tracking branches
(`remotes/origin/main`), so you can see what exists on GitHub without
switching to it.

## Example - Safe Delete
```
$ git branch -d feature2
Deleted branch feature2 (was b9ed097).
```
The confirmation "(was b9ed097)" is Git quietly telling you the last commit
the branch pointed to, in case you need to recover it.

## Example - Blocked Delete and Force Delete
```
$ git branch -d feature2
error: the branch 'feature2' is not fully merged
hint: If you are sure you want to delete it, run 'git branch -D feature2'
$ git branch -D feature2
Deleted branch feature2 (was 5d975d3).
```

## Notes
- `git branch -d` safely refuses if the branch still has commits that
  haven't been merged anywhere.
- Deleting a branch only removes the pointer, not the commits - they stay
  reachable in Git's history through any other branch or tag that still
  references them.
- Force-deleting (`-D`) is genuinely destructive if those commits aren't
  reachable from any other branch or tag - double-check with `git log` or
  `git branch --merged` before reaching for `-D`.
