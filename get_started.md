## Getting started with git

This section of the tutorial focuses on using git on the command line.

### How does git work?

You tell git to manage the files in your project by setting up and
working within a **git repository**. This is simply a directory which
contains some hidden files used by git for bookkeeping.

Once your repository is set up, you need to tell git which files to
manage. Git will keep track of any modifications to the files that it
has been asked to manage. When you have made changes to your project,
you can record those changes as a **commit**. Each commit creates a
snapshot of the project directory, allowing you to make a record of
the state of your project through time.

### Setting up a git repository

To set up a local git repository, create a directory, move into it and
tell git to initialise the repository:

```
mkdir myproj
cd myproj
git init
```

This creates the hidden structure that git needs to start tracking
your files.

### Tell git which files you want to track

You need to tell git which files you want it to manage within the
working directory. To do this you `add` files:

```
echo "# My project" > README.md
git add README.md
```

The first line here creates a file called README.md containing the
specified string.

`git add` tells git to include the new file in the next commit
snapshot. This is called staging a file. `git add` is also used when
you want to tell git to stage files which are already under version
control.

You can use `git status` to produce a report about the current state
of the working directory. This will list files which contain changes
to be committed, those which contain changes that have not been
staged, and files which are not yet tracked.

**Next:** [Getting your project under version control](./version_control.md)
