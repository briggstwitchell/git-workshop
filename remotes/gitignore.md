---
title: .gitignore
layout: default
parent: Remotes and Github
nav_order: 2
---

# Storing Secrets in .gitignore

---

Create a file called secrets in your repository, and paste your access token into it.

Now create a file called .gitignore
* this file's name must begin with a '.'
* it must be named .gitignore

Make the first line of .gitignore "secrets"

# What is .gitignore?

---

.gitignore is a special file that tells git which files to track and which files not to. 

Since we are storing our access token in our repo, we want to make sure that it doesn't get pushed to the remote tracking branch, where anyone could see it. 

This is why we put "secrets" in our .gitignore file. Now that git knows not to track secrets, which contains our access token, it will not appear in our repository.

Some other uses for .gitignore:
* preventing dependencies from pushed and pulled
* storing other environment variables that won't apply on a remote server

Add .gitignore using ```git add``` and commit your changes.