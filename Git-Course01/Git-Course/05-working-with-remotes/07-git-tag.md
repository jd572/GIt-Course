# git tag - Lightweight vs Annotated

## What It Does
A tag is a permanent name pointing at one specific commit - most often used
to mark release points like `v1.0`.

## Use Case
- Marking a release version.
- Creating a stable reference point you can check out or share, separate
  from a moving branch pointer.

## Syntax
```
git tag <name>                       # lightweight tag
git tag -a <name> -m "message"        # annotated tag
git tag                              # list all tags
git show <tag-name>                  # inspect a tag
git push origin <tag>                # push one tag
git push --tags                      # push all tags
git push origin --delete <tag-name>  # remove a tag from the remote
```

## Example - Lightweight
```
$ git tag v1.0
$ git show v1.0
commit b0e0e83b83...
Author: Your Name <you@example.com>
Date:   Tue Jul 21 2026 +0530

    My first commit
```
Just a bookmark - no metadata of its own.

## Example - Annotated
```
$ git tag -a v1.0.1 -m "First stable release"
$ git show v1.0.1
tag v1.0.1
Tagger: Your Name <you@example.com>

    First stable release
```
Stores a message + tagger - like a mini commit.

## Example - Uniqueness and Pushing
```
$ git tag v1.0 -m "22nd July 2026"
fatal: tag 'v1.0' already exists
$ git tag
v1.0
$ git push origin v1.0
...
 * [new tag]         v1.0 -> v1.0
```

## Example - Deleting a Tag from the Remote
```
$ git push origin --delete v1.1
To https://github.com/user/Git-Course.git
 - [deleted]         v1.1
```

## Notes
- **Lightweight tags** are just a pointer with no extra data attached -
  quick to create, but carry no record of who tagged it or why.
- **Annotated tags** are full Git objects: they store a tagger name/email,
  date, and message - the recommended choice for anything you'll actually
  release or share.
- Tag names must be unique - reusing a name fails with "tag already exists".
  To intentionally replace one, add `--force` (or `-f`), but be cautious:
  this moves what the tag points to and can confuse anyone who already
  fetched the old one.
- Tags aren't pushed automatically - share them with `git push origin <tag>`
  or `git push --tags`.
