---
layout: post
title: "Blog 12"
---
Useful Git Commands
-------------------------------

Now that my last semester of Senior Design is coming to an end, I thought it would be useful to know many common Git commands that I've used this past year and/or may be useful in the future. :)

#### Git clone

A command for downloading existing source code from a remote repository (like Github, for example). In other words, Git clone basically makes an identical copy of the latest version of a project in a repository and saves it to your computer.

	$ git clone <https://name-of-the-repository-link>

#### Git branch

By using branches, people are able to work in parallel on the same project simultaneously. It can be used for creating, listing, and deleting branches.

	$ git branch <branch-name>

	To view branches:

	$ git branch or git branch --list

	Delete a branch:

	$ git branch -d <branch-name>

#### Git checkout

Git checkout is used mostly for switching from one branch to another.

	$ git checkout <name-of-your-branch>

	To create AND switch to a branch at the same time:

	$ git checkout -b <name-of-your-branch>

#### Git status

The Git status command gives us all the necessary information about the current branch.

	$ git status

	This provides information of the branch being up-to-date, if there's anything to push/pull/commit, if files are staged/unstaged/untracked, and if there are files created/modified/deleted.

#### Git add

When we create, modify or delete a file, these changes will happen in our local and won't be included in the next commit. We need to use the git add command to include the changes of a file(s) into our next commit.

	$ git add <file>

	To add everything at once:

	$ git add -A

#### Git commit

Git commit is like setting a checkpoint in the development process which you can go back to later if needed. We also need to write a short message to explain what we have developed or changed in the source code.

	$ git commit -m "message"

#### Git push

After committing your changes, the next thing you want to do is send your changes to the remote server. Git push uploads your commits to the remote repository.

	$ git push <remote> <branch-name>

#### Git pull

The git pull command is used to get updates from the remote repo. This command is a combination of git fetch and git merge which means that, when we use git pull, it gets the updates from remote repository (git fetch) and immediately applies the latest changes in your local (git merge).

	$ git pull <remote>
