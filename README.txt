# Gitflow Practice Repository

## Description: 

A repository to practice and master the Gitflow workflow. This repository includes examples and exercises for creating and managing feature, release, and hotfix branches using Gitflow.
Gitflow is a branching strategy for Git that helps manage source code and versions efficiently. Proposed by Vincent Driessen, it uses multiple branches to systematically handle development, deployment, and bug fixes.
This structure allows team members to work on different tasks simultaneously while minimizing conflicts and maintaining code quality.

## Gitflow consists of the following main branches:

1. Master: The stable branch that can be released to production.
2. Develop: The branch where the next release is developed.
3. Feature: Branches created from develop to work on new features.
4. Release: Branches created to prepare for a new production release, including QA and bug fixes.
5. Hotfix: Branches created to fix urgent bugs in the production release.

## Git Flow command list

git init .
vim README.md
git add README.md
git commit -m "create a local repo"
git remote add origin https://github.com/RoySKwon/gitFlow.git
git remote -v
git checkout -b develop
git checkout master 
git push origin master
git push origin develoop
git checkout develop
git checkout -b feature-F001_some
vim feature-F001.txt
git commit -m "2 feature" 
git push origin feature-F001_some

Compare & pull request
Create Pull Requests
Open-Comment
Merge pull request->Confirm merge
Pull request successfully merged and closed
There aren’t any open pull requests.

git checkout develop
git merge feature-F001_SOME
// git branch -d feature-F001_SOME
git checkout -b feature-F002_some
git pull origin
>git push origin feature-F002_some

Compare & pull request
Create Pull Requests

Close with comment
There aren’t any open pull requests.

git checkout -b feature-F003_some 
git pull origin feature-F002_some
Automatic merge failed; fix conflicts and then commit the result.
vim feature-F003.txt
git add .
git commit -m "3 feature"
git push origin feature-F003_some

Compare & pull request
Create Pull Requests
Open-Comment
Merge pull request-> Confirm merge
There aren’t any open pull requests.
git checkout develop
git merge feature-F003_some
// git branch -d feature-F003_some
git checkout -b release/1.0
git pull develop
vim release_1.0.txt
git add .
git commit -m "4 release1.0"
git push origin release/1.0

Compare & pull request
Create Pull Requests
Open-Comment
Merge pull request-> Confirm merge
There aren’t any open pull requests.
merging-> Merged  merged 1 commit into master from release/1.0

git checkout master
git merge release/1.0
git tag -a 1.0 -m "first release" master
git checkout master
git merge release/1.0

git checkout -b hotfix-some
vim hotfix-B001.txt
git commit -m "5 hotfix-some"
git push origin hotfix-some

Compare & pull request
Create Pull Requests
Open-Comment
Merge pull request-> Confirm merge
There aren’t any open pull requests.
merging-> Merged  merged 1 commit into master from hotfix-some

git merge hotfix-some
git tag -a 1.1 -m "hotfix some" master
git merge hotfix-some
git checkout -b feature-F004_some
git pull origin
