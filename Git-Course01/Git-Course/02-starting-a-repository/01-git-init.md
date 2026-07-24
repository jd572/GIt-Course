# git init

## What It Does
Creates a hidden `.git` directory inside your project folder. That hidden
directory is what actually turns a plain folder into a Git repository.

## Use Case
- Starting version control on a brand-new project.
- Converting an existing, un-versioned folder into a Git repo.
- You only run this **once per project**.

## Syntax
```
git init
git init -b <branch-name>   # choose the initial branch name
git init <path>             # initialize a repo at a specific path
```

## Example
```
$ git init
Initialized empty Git repository in ~/First_Project/.git/
```

## Notes
- Nothing is tracked automatically - `init` just prepares the repository and
  gives you an empty starting branch.
- A brand-new repo has no commits yet; the branch name is just a label
  waiting for its first snapshot.
- Running `git init` a second time in the same folder is harmless - it
  re-initializes without deleting existing history.
