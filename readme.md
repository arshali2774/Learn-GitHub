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
>
> - The name of the remote repository we use is `origin` by default.
> - However, you can change it to any name you like.
> - For instance, I've used `root` here instead of `origin`.

```bash
git remote add root <remote-repository-url>
```

2. If you want to push your local branch to the remote repository, you can run the following command:

```bash
git push -u root <branch-name>
```

### `git pull`

1. If you want to pull the latest changes from the remote repository to your local repository, you can run the following command:

```bash
git pull root <branch-name>
```

2. If there are updates in remote repository, and you have also some commited changes in your local repository. When you will try to push local changes to remote repository, you will get an error like this:

```bash
Your branch and 'root/main' have diverged,
```

3. To resolve this issue, you can run the following command:

```bash
git pull
```

4. This will pull the remote changes however the automatic merge will not be done. You will have to do it manually. After that you can save the file and commit the changes.

```bash
git add .
git commit -m "Merge remote changes"
git push root <branch-name>
```
github changes here
