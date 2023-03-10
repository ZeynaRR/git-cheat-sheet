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

## Advices for PR authors
* Keep the PR small
* Have a clear title with the id of the feature / id to make it identifiable easily
* Keep the description clear: don't hesitate to go into details and explain how / why you did what you did regarging the issue / feature
* Don't take it personnaly if you recieve "harsh" comments 

## Advices for PR Reviewer
* Don't be harsh
* Keep an open mind, your way of solving something can be different than someone else's
* Be clear
* Try to make your comments instructive

## 2 ways to create a PR

### Using the portal:

You can create a PR using the portal:
* From the repo screen
* From the Pull requests menu

### Using the github CLI

```sh
gh pr creare --base main --head nameOfBranchWithCommits --title 'Title for the PR' --body 'Description of the PR'
```

## Branch protection

To prevent people from doing whatever they want to the main branch and to increase the level of security of your repo, you can enable branch protection.

There are many options like 'Require a Pull request before merging' or 'Require linear history'.

## Code Owners

You can manage who should validate the pull requests using patterns in the CODEOWNERS file.

WARNING: this file should be in one of theses repositories:
* / or the root of the repo
* /docs
* /.github


## Git flows

* Trunk based dev : devs work on the main branch
* Git flow : the key branch is develop, features branches are created from this branch and release branches are used for release stabilisation too. 
* GitHub flow: devs work on feature branches than make PR to the main branch
* Open source / Inner source model : Open source is now widely adopted. Inner sourcing, the Open Source practices applied to enterprise, is a fast growing practice. In both cases, the main repository is readonly for almost everyone. Contributors wishing to propose new features or bug fixes use a fork. A fork is a feature introduced by git repository hosting system to create a copy of a repo with a link to the original repo. It the same than branch and remotes but for repos.

## How to integrate your changes 
* Merge: most basic way to execute merge. All commit in your source branch will be visible in history
```sh 
git merge features/feature1
```
* Squash merge: all commit in your feature branch are merged in only one commit to the target branch.
```sh 
git merge --squash features/1234-new-killing-feature
```
* Rebase: allows you to update your feature branch to change the first commit
```sh 
git merge
```
