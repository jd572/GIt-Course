# git remote -v

## What It Does
Lists every remote Git knows about, with the URL used for fetching and the
URL used for pushing.

## Use Case
- Checking whether a repo is wired to HTTPS or SSH.
- Troubleshooting a push/pull authentication problem.
- Confirming which remote name ("origin", "upstream", etc.) points where.

## Syntax
```
git remote -v
```

## Example
```
$ git remote -v
origin  git@github.com:user/Git-Course.git (fetch)
origin  git@github.com:user/Git-Course.git (push)
```

## Notes
- Fetch and push URLs are usually identical, but they can differ (e.g. a
  read-only fetch mirror with a different push target).
- "origin" is just a naming convention Git assigns automatically on clone -
  you're free to add more remotes under other names, like "upstream" (a
  common pattern when contributing to a fork).
