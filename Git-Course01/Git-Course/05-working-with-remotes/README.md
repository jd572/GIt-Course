# 05 - Working with Remotes

A remote is another copy of your repository, usually hosted online (GitHub,
GitLab, Bitbucket). This section covers connecting a local repo to a remote,
pushing, pulling, cloning, tagging, and SSH authentication.

```
Local Repository  --git push-->   Remote Repository
Local Repository  <--git pull--   Remote Repository
                  --git clone-->  (first-time copy)
```

None of GitHub, GitLab, or Bitbucket are Git itself - they're hosting
platforms that store your remote repository and add collaboration tools
(pull requests, issues, CI/CD) around plain Git. The core commands (clone,
add, commit, push, pull) work identically no matter which one you choose.
