---
title: What to do when VSCODE ignores your .gitignore
layout: page
parent: Coding
---

# What to do when VSCODE ignores your .gitignore

When you're working on a project, you may want to ignore certain files from being tracked by git. You can do this by adding a `.gitignore` file to your project. This file tells git which files to ignore. For example, if you're working on a Python project, you may want to ignore the `venv` folder. You can do this by adding the following line to your `.gitignore` file:

    venv/

I tried this, but if you try to ignore a file that's already being tracked by git, it won't work. You'll need to remove the file from git's tracking first. You can do this by running the following command:

    git rm -r --cached .
    git commit -m ".ignore has been fixed"

The first line will remove the files from git's tracking. 
The second line will commit the changes to git.
