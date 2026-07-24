# When Merges Aren't Fast-Forward: Conflicts

## What It Does
Happens when both branches being merged have edited the same lines. Git
can't automatically choose a winner, so it pauses the merge and asks you to
decide.

## Use Case
- Understanding what to do when `git merge` (or `git pull`) reports a
  conflict instead of completing cleanly.

## Syntax
```
git merge <branch>
# ... resolve conflict markers in affected files ...
git add <file>
git commit
```

## Example
```
$ git merge feature1
Auto-merging Userdata.txt
CONFLICT (content): Merge conflict in Userdata.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Inside `Userdata.txt`:
```
<<<<<<< HEAD
Thanks for the update!
=======
Thank you for the update!
>>>>>>> feature1
```

## Notes
- Every merge in a simple demo is often a fast-forward because `main` never
  changed while a feature branch was being built. Real projects will hit
  real conflicts once multiple people edit the same files.
- Git marks the file with conflict markers - `<<<<<<<`, `=======`,
  `>>>>>>>` - showing both versions side by side, right inside the file.
- To resolve: edit the file to keep the correct content, remove the marker
  lines, then `git add` and `git commit` as normal to complete the merge.
- After resolving, `git status` will show the file as staged for the merge
  commit.
