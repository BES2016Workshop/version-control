## Subsequent workflow

Once you've set up the remote repository, subsequent updates follow a
similar pattern:

* Add or make changes to files in your project
* Stage the new/modified files:  `git add`
* Commit your changes: `git commit`
* Push your local changes to the remote repository: `git push`

### Making sure your repository is up-to-date

At any point you can use `git status` to find out the current state of
your repository. If you have made a local commit that has not yet been
pushed to the remote repository, `git status` will display a message
indicating that your local branch is ahead of `origin/master` (the
remote branch). Use

```
git push
```

to bring the remote branch up-to-date.

## Other ways to get started: cloning a repository [](#git-clone)

Rather than initialising a local repository, you can start your
project by *cloning* a remote repository from GitHub.

Cloning a remote repository creates a new copy of the repository on
your computer. For example, if you have created a repository on GitHub
called `new-repo` you can set up a local copy by entering:

```
git clone https://github.com/username/new-repo.git
```

This will create a local repository in a directory called `new-repo`
and populate it with the contents of the remote repository.

If you've only just created the repository on GitHub, running `git
clone` will generate a warning that you've cloned an empty
repository. This is just to remind you that you'll need to add files
and [create an initial commit](./get_started.md#initial-commit) before
you have a version controlled project.

**Next:** [Summary](./summary.md)
