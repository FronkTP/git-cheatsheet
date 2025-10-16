# Git Cheatsheet

This is a repo where I put every git commands I've come across for future referencing. This is done so that it only includes the commands I use, not the complex commands I don't understand.

## Get started

Initialise the existing directory as a git repository

```bash
  git init
```

Clone an entire repository from url

```bash
  git clone <url>
```

## First few steps

Add a file

```bash
git add <file-name> <file-name>
```

Add all files

```bash
git add .
```

Make a commit

```bash
git commit -m 'message'
```

Make a commit (and open text editor to write message)

```bash
git commit
```

Connect to a remote repo

```bash
git remote add origin <url>
```

Check if the remote has been added correctly

```bash
git remote -v
```

Push for the first time

```bash
git push -u origin master
```

## Making changes later on

1. Add files
2. Make a commit
3. Push to remote repo

```bash
git push
```

## Collaborate

Create a new local branch and switch to it

```bash
git checkout -b <new-branch-name>
```

Create a new local branch from a remote branch and switch to it

```bash
git checkout -b <new-branch-name> origin/<branch-name>
```

Switch to another branch

```bash
git checkout <branch-name>
```

List all local branches

```bash
git branch
```

List all remote branches

```bash
git branch -r
```

List all branches

```bash
git branch -a
```

Fetch changes (but don't change any of your local branches) to all local branches

```bash
git fetch
```

Fetch changes only to a specific local branch

```bash
git fetch origin <branch-name>
```

Merge changes from the tracking remote branch into your current branch

```bash
git merge
```

Merge from another local branch into your current branch

```bash
git merge <branch-name>
```

Merge from another remote branch into your current branch

```bash
git merge origin <branch-name>
```

Merge the changes from one local branch (branch2) into another local branch (branch1) without leaving your current branch (main).

```bash
git checkout <branch-name-1> && git merge <branch-name-2>
```

Fetch and merge changes from the tracking remote branch into your current branch

```bash
git pull
```

Show line-by-line changes between your current branch and another branch

```bash
git diff <another-branch-name>
```

Show the difference of what is in one branch (branch1) but not in another branch (branch2)

```bash
git diff <branch-name-2>...<branch-name-1>
```

## Edit history

Reset the last commit and keep the staged changes

```bash
git reset --soft HEAD~1
```

Reset the last commit and unstages the changes

```bash
git reset HEAD~1
```

Deletes the last commit and all changes in it

```bash
git reset --hard HEAD~1
```

If the commit was already pushed, you’ll need to force push after resetting (DANGEROUS!)

```bash
git push --force
```

## Temporary commits

Save all changes

```bash
git stash
```

Write the changes from top of stash stack

```bash
git stash pop
```

Discard the changes from top of stash stack

```bash
git stash drop
```

List stack-order of stashed file changes

```bash
git stash list
```
