# git clone

## What It Does
Downloads an entire remote repository - full commit history included, not
just the latest snapshot - into a new folder named after the repo.

## Use Case
- Getting a first-time local copy of an existing project.
- Onboarding onto a team's existing codebase.

## Syntax
```
git clone <url>
git clone <url> <target-folder-name>
```

## Example
```
$ git clone https://github.com/microsoft/vscode.git
Cloning into 'vscode'...
remote: Enumerating objects: 2251514, done.
remote: Counting objects: 100% (1780/1780), done.
Receiving objects:  42% (945636/2251514)
```

## HTTPS vs SSH
Both protocols download the exact same repository - they only differ in how
you authenticate.

| | HTTPS | SSH |
|---|---|---|
| Command | `git clone https://github.com/user/repo.git` | `git clone git@github.com:user/repo.git` |
| Auth | Prompts for credentials every time (unless cached); most hosts now require a Personal Access Token instead of a password | Authenticates silently via your SSH key |

## Notes
- Large, long-lived projects can take a while to clone; progress output
  walks through distinct stages - enumerating, counting, compressing, then
  receiving objects.
- Once cloning finishes, `origin` is registered automatically, pointing back
  at the source URL - ready to pull updates immediately.
- See `06-ssh-key-setup.md` for setting up SSH authentication.
