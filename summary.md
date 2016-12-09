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

### Typical use of git in a workflow

To clarify the above, when using git for a project we follow these steps:

1. [Initialise a local repository](./get_started.md#git-init) (`git
   init`), or
   [clone an existing remote repository from GitHub](./workflow.md#git-clone)
   (`git clone`).
2. Write some code. Save the file to the working directory, e.g. `mycode.R`
3. Use `git status` to see what is ready to add/commit and check file names.
4. Stage the file using `git add mycode.R`
5. Commit the file with a message using `git commit -m "My first commit"`
6. [Connect your repository to a remote GitHub repo](./remote.md) (if
   you didn't start off by cloning a repository) or push the code to
   the remote GitHub repo using `git push`
7. Write some more code. Save.
8. Use `git status` to see what is ready to add/commit and check file names.
9. Stage the file using `git add mycode.R`
10. Commit the file with a message using `git commit -m "Edits to first bit of code"`
11. Push the code to the remote GitHub repo using `git push`
12. Write some more code...etc.

Most of the time you'll just be using four git commands: `add`, `commit`, `push` and `status`

### Going further

Git and GitHub are extremely powerful and flexible systems and there
is a lot more you can learn if you wish. Here are some starting points:

### Documentation, cheatsheets and tutorials
- `git help <command>`
- git -- the simple guide [http://rogerdudler.github.io/git-guide/](http://rogerdudler.github.io/git-guide/)
- Version Control with Git (Software Carpentry tutorial) [http://swcarpentry.github.io/git-novice/](http://swcarpentry.github.io/git-novice/)
- Pro Git book [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
- git reference/cheatsheets [https://git-scm.com/docs](https://git-scm.com/docs)
