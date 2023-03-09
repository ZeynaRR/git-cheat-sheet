# My git cheatsheet

## git branch

Last but not least of the git basic commands: git branch

## Reminder about branches

Let's take a moment to remember what a branch is and some principles associated with it.

A branch is a way to isolate a set of modifications. We talk about feature branch. Why do we isolate a feature ?

Branching allows you to keep modification in a separate space. After some time on your feature branch, you have many possibilities:

    your branch is good enough and completes with feature goals, you decide to integrate it within the rest of the project
    you need more time to develop the feature (this is more complicated than expected, you are blocked by a dependency, ...). It allows you to switch to another branch and come back later to this feature.
    your development is not ok from a quality point of view, becomes obsolete or what so ever and you decide to abandon this feature. You can then keep this branch, maybe someday it can be useful, or simply delete it and go on with something else.

Imagine you were developing in the same unique branch, the 2 last scenarios would be hard to manage.
What is a branch, I mean, how does git handle branches ?

Good question. In fact, this is quite simple. A branch is some kind of a pointer (remember: git, linux, C). A branch is a pointer to a commit.

So when you create or delete a branch, you just create or delete a pointer to a commit.

When you commit on a branch, the pointer is updated to this newly created commit.

To be persisted, this "pointer like" reference is stored into a file (remember: git, linux, file)

## List your branches

Let's start to manipulate branches. First things first, let's list those branches:

&nbsp; git branch

*master

## Create your own branch

When you start working on a feature or just want to test something without impacting the whole repo, create a branch

The simplest way is using git checkout this way:

&nbsp; git checkout -b features/1234-new-killing-feature

Switched to a new branch 'features/1234-new-killing-feature'

&nbsp; git status

On branch features/1234-new-killing-feature

## Delete a branch
A branch is not expected to live forever. Once a feature is complete or abandoned, you should delete the associated branch to keep your repo clear.

You achieve it using the delete switch:

&nbsp; git branch -d features/1234-new-killing-feature

Deleted branch features/1234-new-killing-feature (was 3e60269).

