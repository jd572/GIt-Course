# Setting Up an SSH Key

## What It Does
`ssh-keygen` generates a cryptographic key pair, stored in `~/.ssh` - a
private key and a matching public key - used to authenticate with Git
hosts without a password prompt.

## Use Case
- Avoiding repeated username/Personal Access Token prompts on every push or
  pull.
- Setting up a new machine to work with GitHub, GitLab, or Bitbucket over
  SSH.

## Syntax
```
ssh-keygen -t ed25519 -C "you@example.com"
cat ~/.ssh/id_ed25519.pub
```

## Example
```
$ cd ~/.ssh
$ ls
agent  id_ed25519  id_ed25519.pub
$ cat id_ed25519.pub
ssh-ed25519 AAAAC3Nza...WHxF/ StudioMac@Macmini
```

## Notes
- `id_ed25519` is the **private key** - it never leaves your machine.
- `id_ed25519.pub` is the **public key** - safe to share.
- Paste the `.pub` contents into GitHub/GitLab/Bitbucket -> SSH Keys, once
  per machine, and SSH remotes just work from then on.
- After adding the key, switch a remote to SSH with `git remote set-url`
  (see `02-git-remote-add-and-set-url.md`).
