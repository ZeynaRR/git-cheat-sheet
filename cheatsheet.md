# My git cheatsheet

## check history of commits on the branch you're working on

```sh 
git log 
```
## git branch

Branching allows you to keep modification in a separate space. After some time on your feature branch.

So when you create or delete a branch, you just create or delete a pointer to a commit.

When you commit on a branch, the pointer is updated to this newly created commit.

To be persisted, this "pointer like" reference is stored into a file (remember: git, linux, file)

## Command to list your branches

```sh 
git branch
```
## Command to create a branch

create a new branch then checkout:
```sh 
git checkout -b nameOfTheBranch
```

create a new branch:
```sh 
git branch nameOfTheBranch 
```

## Command to delete a branch

to delete a branch:

```sh 
git branch -d nameOfTheBranch
```

