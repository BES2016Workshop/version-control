## Get your project under version control

In the [previous step](./get_started.md) you initialised a git
repository and added some files that you want git to track.

The next stage is to create your first commit, but before you go any
further, check the current state of your working directory using `git
status` to make sure that you're happy with the list of files to be
committed.

Creating your first commit will set up version control on the files
that you've asked git to manage.

For the first commit you can use `git commit` with the `-m` option,
which allows you to specify a commit message directly:

```
git commit -m "My first commit"
```

This should result in a short report about the commit.

### Working in the version control framework

Now that your project is under version control you can keep track of
any changes that you make.

Open the README.md file and add a few lines describing your
project. Also, change the heading from "My project" to something more
specific. Save and close the file.

Now, use `git status` to check the state of the working directory. It
should report that you've modified README.md.

![](img/git_status_change.png)

You can use `git diff` to review your changes:

![](img/git_diff_cmd.png)

<!-- <pre> -->
<!-- diff --git a/README.md b/README.md -->
<!-- index 9848698..94fee06 100644 -->
<!-- --- a/README.md -->
<!-- +++ b/README.md -->
<!-- @@ -1 +1,6 @@ -->
<!-- -# My project -->
<!-- +# An introduction to version control for research -->
<!-- + -->
<!-- +This tutorial introduces a basic workflow for version control using -->
<!-- +git and the popular online hosting service, GitHub. The aim is to -->
<!-- +provide a starting point for researchers who want to curate and -->
<!-- +distribute their code. -->
<!-- </pre> -->

Lines prefaced with a `-` indicate lines that have been removed, while
lines with a `+` at the start are additions.

If you're happy with the changes that you've made, use `git add` to
stage your file.

### Committing your changes

For this tutorial it's fine to carry on using `git commit -m` with a
short message when you commit your changes.  However, it's a good idea
to get into the habit of writing commit messages which explain the
modifications that you've made in some detail. That way you'll have a
record of the changes that you have made to your code to which you can
refer later. This can be really useful when you want to review the
history of your project.

Using `git commit` without the `-m` option prompts git to open a text
editor in which to compose your message. Note that the text editor
that is used depends on your
[git configuration](./prelim.md#configure). Before going further you
may want to make sure you've set the `core.editor` option to something
sensible.

A good strategy for commit messages is to start with a short, one-line
summary of the commit, followed by a longer description of your
changes. For example:

    Update README file

    Update README file to include the proper title and a description
    of the project aims.

### Reviewing version history

You can view the history of your project using `git log`. This lists
each commit together with its unique SHA1 identifier, date, author,
and commit message. The commit history can be extremely useful for
finding bugs or looking back to how your project looked a few months
ago.

You can use the information in the commit history to extract more
information about changes made in a commit. For example, to see a
detailed report of the changes for a given commit you can use `git
show -p` together with the first part of the SHA1 identification
string for that commit:

```
git show -p f9fae515
```

This will display the changes introduced in the specified commit in a
similar format to the output from `git diff`.

**Next:** [Connecting to a remote repository](./remote.md)
