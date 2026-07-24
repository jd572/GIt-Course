# git --version

## What It Does
Prints the installed Git version so you can confirm Git is available on your
machine before doing anything else.

## Use Case
- First thing to run on a new machine or a fresh terminal.
- Confirming a minimum required Git version for a project or CI pipeline.
- Version matters: newer Git versions default new repositories to the
  `main` branch name instead of the older `master` default.

## Syntax
```
git --version
```

## Example
```
$ git --version
git version 2.43.0
```

## Notes
- If this command fails ("command not found"), install Git first:
  - macOS: Xcode Command Line Tools (`xcode-select --install`) or Homebrew (`brew install git`)
  - Windows/Linux: package manager or https://git-scm.com
- No flags are required; `--version` is a standalone check, not something you
  combine with other options.
