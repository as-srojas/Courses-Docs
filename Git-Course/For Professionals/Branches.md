# Branches in Git

Git branches are pointers to snapshots of your changes. They allow you to work on different tasks simultaneously without interfering with the main project.

## Mainline Development

Mainline development refers to the primary branch where the main work is done, usually called main or master.

Create and switch to a new branch

`git checkout -b new-feature`

Work on new-feature branch
Merge new-feature branch into main

`git checkout main`

`git merge new-feature`

## State

A branch's state refers to its status compared to the main branch, such as ahead, behind, or up-to-date.

Check branch status

`git status`

Compare branches

`git diff main new-feature`

## Release

A release branch is used to prepare a new production release. It allows for minor bug fixes and preparing the release.

Create a release branch
`git checkout -b release-v1.0`

Prepare the release
Merge back to main and tag the release

`git checkout main`

`git merge release-v1.0`

`git tag -a v1.0 -m "Release version 1.0"`

## Feature Branches

Feature branches are used to develop new features for the upcoming or a distant future release. They exist as long as the feature is in development.

Create a feature branch

`git checkout -b feature-login`

Work on the feature
Merge the feature branch into main when done

`git checkout main`

`git merge feature-login`

## Long Running & Short Lived Branches

Long Running Branches: These branches exist for a long time, often used for major ongoing features or projects.

Example of a long-running branch

`git checkout -b refactor-architecture`

### Short Lived Branches: These branches are quickly created and merged, often used for hotfixes or small features

Example of a short-lived branch

`git checkout -b hotfix-login-bug`

Fix the bug and merge

`git checkout main`

`git merge hotfix-login-bug`

These concepts help manage the development process, keeping code organized and changes trackable.