# Git Basics

## Git Config

1. If you want to set default branch name to `main` instead of `master`, you can run the following command:

```bash
git config --global init.defaultBranch main
```

2. Convert line endings to LF when commiting and back to CRLF on checkout.

```bash
git config --global core.autocrlf true
```

## Git Commands

### `git push`

1. Setup a remote repository

> [!NOTE]
> The name of the remote repository we use is `origin` by default. However, you can change it to any name you like. For instance, I've used `root` here instead of `origin`.

```bash
git remote add root <remote-repository-url>
```

1. If you want to push your local branch to the remote repository, you can run the following command:

```bash
git push -u root <branch-name>
```
