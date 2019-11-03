---
layout: post
title: "Blog 8"
---

  How to push to Github in an existing repository
  -----------------------------------------------

  Step 1: Clone the repository

      $ git clone (.git url for repository)

  Step 2: Initialize to make sure you're on the correct branch

      $ git init

  Step 3: Check to make sure the file added/changed are being recognized to push

      $ git status

  Step 4: Get files ready to push to repository

      $ git add .

  Step 5: Commit to branch

      $ git commit -m "add page"

      If the file getting pushed is an existing file that was modified:

      $ git commit -am "add pages"

  Step 6: Push the files to the repository

      $ git push origin (name of branch)

      If it asks to pull first:

      $ git pull origin (name of branch)
