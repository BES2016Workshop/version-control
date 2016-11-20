# Introduction to version control for research

This tutorial introduces a basic workflow for version control using
git and the popular online hosting service, GitHub, providing a
starting point for curating and distributing code for research.

## Preliminaries

In this tutorial the focus is on using git with the command line. Step
through the instructions below to make sure that you have everything
you need to get started.

### Install git
You can download git here:
[https://git-scm.com/downloads](https://git-scm.com/downloads)

<!-- TODO: check this -->
If prompted, select the option to add the installation location to system path.

<!-- On Windows, you may need to select an option about "Adjusting your PATH environment". -->
<!-- The option "Run Git from the Windows Command Prompt" will help RStudio find git. -->

Open a terminal or command prompt and type `git version` to check that
the installation worked.

#### Configure git

After installing git, you need to tell it who you are. Open a terminal
window or command prompt and type the following:

```
git config --global user.email "you@youremail.com"
git config --global user.name "Your Name"
```

You can also configure git to use your preferred editor for commit
messages:

```
git config --global core.editor nano
```

### Sign up for an account on GitHub

GitHub is a popular online hosting service for git repositories. It
provides a useful interface for collaboration and code sharing.

Create a free account on GitHub:

[https://github.com/join](https://github.com/join)

***If you have an academic email account you should use it here.***
GitHub users can create an unlimited number of free, public
repositories but only a limited number of private
repositories. However, academic users can request access to an
unlimited number of free private repositories.

**Optional**

If you are an academic user, sign up for free private repositories here:

[https://education.github.com/discount_requests/new](https://education.github.com/discount_requests/new)

***This requires your account to be associated with an academic email
address.***

It may take a while to receive the verification email for
this step. Don't worry, we won't need this for the tutorial.


## How does git work?

You can use git to manage the files in a specified directory.  You do
this by setting up a git repository, which is simply a directory with
some hidden files for bookkeeping.

Once your repository is set up, you need to tell git which files to
manage. Git will keep track of any modifications to those files. When
you have done some work on your project, you can record specific
changes as a *commit*, which creates a snapshot in time of the project
directory.

<!-- There are three representations of file state in git: -->

<!-- * modified files -->
<!-- * staged files -->
<!-- * committed files -->


## Setting up a repository

To set up a local repository, create a directory, move into it and
initialise the repository:

```
mkdir myproj
cd myproj
git init
```

This creates the hidden structure that git needs to start tracking
your files.

## Tell git which files you want to track

You need to tell git which files it should track in the working
directory. To do this you `add` files:

```
echo "# My project" > README.md
git add README.md
```

(The first line here creates a file called README.md containing the
specified string.)

This tells git to include the new file in the next commit snapshot.
`git add` is also used when you want to include files which are
already under version control in the next commit (this is called
staging files).

You can use `git status` to produce a report about the current state
of the working directory. This will list files which contain changes
to be committed, those which contain changes that have not been
staged, and files which are not yet tracked.

## Get your project under version control

Creating your first commit will set up version control on the files
that you've asked git to track.

For the first commit you can use `git commit` with the `-m` option,
which allows you to specify a commit message directly:

```
git commit -m "My first commit"
```

## Making changes

Now that your project is under version control you can keep track of
the changes that you make.

Open the README.md file and add a few lines describing your
project. Also, change the heading from "My project" to something more
specific. Save and close the file.

Now, use `git status` to check the state of the working directory. It
should report that you've modified README.md. You can use `git diff`
to review your changes:

![](img/git_diff.png)

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

If you're happy with the changes you've made, use `git add` to stage
your file.

For most commits it's a good idea to attach a commit message which
explains the modifications that you've made in some detail.

```
git commit
```

prompts git to open a text editor for you to compose your message.
Start with a short, one-line summary of the commit, followed by a
longer description of your changes. For example:

    Update README file

    Update README file to include the proper title and a description
    of the project aims.

## Reviewing version history

You can view the commit history of your project using `git log`. Each
commit is listed together with its unique SHA1 identifier, date,
author, and commit message. This can be extremely useful for finding
bugs or looking back to how your project looked a few months ago. To
see a detailed report of the changes for a particular commit, use `git
show -p` together with the first part of the SHA1 identification
string for that commit:

```
git show -p f9fae515
```

This will give you a diff of the changes introduced in the commit.


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

You can create a new project to track from an existing repository. If you've got git installed!
