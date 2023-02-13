# git-workshop

## Objectives

- Learn how to use git
- Learn how to rebase
- Learn how to use git-flow
- Learn how to resolve conflicts

## First exercise (How to make a pull request)

- Create a new branch from main
- Create a new file with your name, for example `my-name.txt`
- Commit your changes with the message `feat: add my name`
- Push your branch to the remote (origin)
- Create a pull request
- Merge your branch to main
- Delete your branch

## Second exercise (How to rebase non-conflicting changes)

- Create two new branches from main (branch1 and branch2)
- Create a new file with your name in branch1, for example `my-name.txt`
- Commit your changes with the message `feat: add my name`
- Push your branches to the remote (origin)
- Create a pull request from branch1 to main

- On branch2, rebase interactive your branch with main using `git rebase -i main` (You need to run this command to get the changes from main)
- Find the commit that you want to rebase (Comment the commits that you don't want to rebase, left your own commit uncommented)
- Push your branch to the remote with `git push --force-with-lease origin branch2` (This is because you are rewriting the history of your branch) (Make sure that you are not rewriting the history of a branch that is being used by other people)
- Create a pull request from branch2 to main (You will see that the commits from branch1 are not in this pull request, because you rebased them)

## Third exercise (How to rebase conflicting changes)

- Create two new branches from main (branch1 and branch2)
- Create a new file with your name in branch1, for example `my-name.txt`
- Commit your changes with the message `feat: add my name`
- Create a new file with your name in branch2, for example `my-name.txt`
- Commit your changes with the message `feat: add my name`
- Push your branches to the remote (origin)
- Create a pull request from branch1 to main

- On branch2, rebase interactive your branch with main using `git rebase -i main` (You need to run this command to get the changes from main)
- Find the commit that you want to rebase (Comment the commits that you don't want to rebase, left your own commit uncommented)
- Push your branch to the remote with `git push --force-with-lease origin branch2` (This is because you are rewriting the history of your branch) (Make sure that you are not rewriting the history of a branch that is being used by other people)
- Create a pull request from branch2 to main (You will see that the commits from branch1 are not in this pull request, because you rebased them)

- On branch2, rebase your branch with main using `git rebase main` (You need to run this command to get the changes from main)
- Fix the conflicts
- Add the files that you fixed
- Commit your changes with the message `fix: fix conflicts`
- Push your branch to the remote with `git push --force-with-lease origin branch2` (This is because you are rewriting the history of your branch) (Make sure that you are not rewriting the history of a branch that is being used by other people)
- Create a pull request from branch2 to main (You will see that the commits from branch1 are not in this pull request, because you rebased them)
