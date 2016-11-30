## Summary

We've introduced the following basic git workflow using git on the command line:

**Local operations**

- Staging files:    `git add <file>`
- Committing changes:    `git commit`
- Inspecting your workspace:    `git status`
- Reviewing history:    `git log`

**Syncing with a remote**

- Pushing local changes:   `git push`
<!-- - Merging remote changes `git pull` -->

## Typical use of git in a workflow

To clarify the above, typically when using git for a project we follow these steps:

1. Go to GitHub, create a new repository, e.g. `new-repo`
2. Clone the repository so it is on your computer using `git clone https://github.com/username/new-repo.git`

3. Write some code. Save the file to the `new-repo` folder, e.g. `mycode.R`
4. Use `git status` to see what is ready to add/commit and check file names.
5. Stage the file using `git add mycode.R`
6. Commit the file with a message using `git commit -m "My first commit"
7. Push the code to the remote GitHub repo using `git push`

8. Write some more code. Save.
9. Use `git status` to see what is ready to add/commit and check file names.
10. Stage the file using `git add mycode.R`
11. Commit the file with a message using `git commit -m "Edits to first bit of code"
12. Push the code to the remote GitHub repo using `git push`
13. Write some more code...etc. 

Most of the time you'll just be using four git commands: `add`, `commit`, `push` and `status`

## Going further

Git and GitHub are extremely powerful and flexible systems and there
is a lot more you can learn if you wish. Here are some starting points:

### Documentation, cheatsheets and tutorials
- `git help <command>`
- [git -- the simple guide](http://rogerdudler.github.io/git-guide/)
- [Version Control with Git (Software Carpentry tutorial)](http://swcarpentry.github.io/git-novice/)
- [Pro Git book](https://git-scm.com/book/en/v2)
- [git reference/cheatsheets](https://git-scm.com/docs)

