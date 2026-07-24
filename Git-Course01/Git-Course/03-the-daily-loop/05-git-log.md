# git log

## What It Does
Lists commits newest-first: hash, author, date, and message.

## Use Case
- Reviewing project history.
- Finding a specific commit hash to reference, revert, or cherry-pick.
- Confirming where `HEAD` currently points.

## Syntax
```
git log
git log --pretty=oneline   # compact, one line per commit
git log --oneline          # also abbreviates the hash
```

## Example
```
$ git log
commit b0e0e83b836d66dcbd16fe18... (HEAD -> main)
Author: Your Name <you@example.com>
Date:   Tue Jul 21 12:01:49 2026 +0530

    My first commit
```

## Example - Compact Form
```
$ git log --pretty=oneline
b9ed097bdd... (HEAD -> feature1) New updates
643fe6a5a1... (origin/main, main) added the service file
```

## Notes
- The full hash (`b0e0e83b83...`) is the commit's permanent ID; you'll
  usually refer to it by its first 7 characters.
- `(HEAD -> main)` marks where you are right now - the tip of the main
  branch.
- `--pretty=oneline` compresses each commit to a single line - full hash
  plus message - perfect for scanning history quickly. Branch and HEAD
  labels still appear inline.
