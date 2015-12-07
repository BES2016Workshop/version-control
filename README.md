# git-example

This repository showcases some basic git workflow. Assumptions: user has installed git and has access to command line environment.

## Setting up a repository

To set up a local repository, create a directory, move into it and initialise the repository:

```
mkdir myproj
cd myproj
git init
```

This sets up the current directory so that `git` can start tracking your files.

## Tell git which files you want to track

You need to tell `git` which files it should track in the working directory. To do this you need to `add` files:

```
echo "# My project" > README.md
git add README.md
```

(The first line here just writes the specified string into the README.md file.)

This places the specified files into `git`'s staging area, which allows you to assemble a set of changes prior to committing them. `git add` is also used when you can to stage changes to files which are already under version control.

You can use `git status` to produce a report about the current state of the working directory. This will list files known by `git` which contain changes that have been staged, those which contain unstaged changes, and files which are not yet tracked.

## Commit your changes

Any files that have been staged can be checked in using `git commit`:

```
git commit -m "My first commit"
```

Using `git commit` with the `-m` option allows you to specify a commit message directly. You may wish to attach a longer message to explain the changes which you're committing; if so, omit the `-m` option and `git` will open a text editor for you to compose your message. The commit history of a project can be viewed using `git log`. It's good practice to start with a short, one-line summary of the commit, followed by a longer description of your changes.

## Connecting to a remote repository

Likely you'll want to connect your local repository to another repository that will act as a central store for your project, so that you can share your work or access it from another computer. For this, you need to tell `git` the name of the remote repository. For example, using GitHub you would set up a new GitHub repository `myproj`, then add it as a remote to your local repository:

```
git remote add origin git@github.com:ghuser/myproj.git
git remote add origin https://github.com/ghuser/myproj.git
```

(The first command indicates that you'll access the remote using an `ssh` connection, while the second says that you'll be using the `HTTPS` protocol. See the [GitHub help pages](https://help.github.com/articles/which-remote-url-should-i-use/) for more information.)

Now you can perform an initial `push` that will set up your local `master` branch to track the equivalent remote branch:

```
git push -u origin master
```

## Setting up a git project in RStudio

You can create a new project to track from an existing repository.

