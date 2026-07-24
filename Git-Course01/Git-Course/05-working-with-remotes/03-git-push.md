# git push

## What It Does
Uploads your local commits to the remote repository.

## Use Case
- Sharing your committed work with teammates.
- Backing up local history to a hosted remote.
- Publishing a new branch so others can see and review it.

## Syntax
```
git push -u origin main       # first push, sets upstream tracking
git push                      # subsequent pushes, once upstream is set
git push origin main          # explicit form
git push origin <branch>      # push a branch that doesn't exist remotely yet
```

## Example - Staying in Sync
```
$ git status
Your branch is up to date with 'origin/main'.
$ git add .
$ git commit -m "added the service file"
$ git push origin main
   eb79962..643fe6a  main -> main
```

## Example - Pushing a New Branch
```
$ git push origin feature1
...
remote: Create a pull request for 'feature1' on GitHub by visiting:
remote:   https://github.com/user/Git-Course/pull/new/feature1
To https://github.com/user/Git-Course.git
 * [new branch]      feature1 -> feature1
```

## Notes
- `-u` (or `--set-upstream`) is only needed the first time you push a
  branch - it remembers "origin main" as the default target for future
  pushes.
- `git status` compares against the remote too: "up to date with
  origin/main" means nothing is waiting to be pushed.
- Pushing a branch doesn't merge anything by itself; it just makes the
  branch visible, and pushable/pullable, for teammates.
- GitHub (and similar hosts) print a direct link to open a pull request
  right after a new branch is pushed.
