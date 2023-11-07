# Git CLI
- You can create git repositories and commits locally. You can also synchronize your local repository with a remote repository (i.e. on GitHub).

## Connecting to a remote repository
- This enables teams to work on the same remote repository and clone it locally. The remote repository also serves as a backup.

## Connecting your local repository to a new remote repository
- The first thing you need to do is create a new empty remote repository on GitHub. You will then see some hints e.g. "...or push an existing repository from the command line". Copy the commands from GitHub and execute them in your local project folder.

---

Example:

git remote add origin git@github.com:GitHubUsername/repository-name.git
git branch -M main
git push -u origin main

## Resources
---
- Connect with SSH Docs on GitHub
- Git SCM
- Git book
- Git Cheatsheet