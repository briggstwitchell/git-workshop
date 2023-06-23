---
title: .gitignore
layout: default
parent: Remotes and Github
nav_order: 3
---

# Storing Secrets in .gitignore

---

![frodo secrets](../images/gitignore/frodo-secrets.jpg)
{: .text-center}

I'm going to create a file called secrets to store my access token.

If I added and committed to my repository now, the password for my remote repository would be visible to the public. This would be bad.

To keep Git from tracking my secrets file, I need another special file called .gitignore
# What is .gitignore?

---

.gitignore is a special file that tells Git which files to track and which files not to. 

Since we are storing our access token in our local directory, we want to make sure that it doesn't get pushed to the remote tracking branch, where anyone could see it. 

This is why I put "secrets" in my .gitignore file. Now that Git knows not to track secrets, which contains our access token, it will not appear in our repository.

Even if I run `git add .`, which adds all files in the project to the staging area, Git won't add secrets because it's in my .gitignore file.

Some other uses for .gitignore:
* preventing dependencies from being pushed and pulled
    * many projects require other libraries and dependencies
    * pushing and pulling all these files to the remote wastes space and time
    * anybody who wants to build our program can install these dependencies themselves anyway
* storing other environment variables that won't apply on a remote server

---
> ## Exercise
> - [ ] create a file called secrets and paste your access token into it
> - [ ] create a file called .gitignore and make the first line of the file "secrets"
> - [ ] add and commit .gitignore to your repository
{: .exercise}