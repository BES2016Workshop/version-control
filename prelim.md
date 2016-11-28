## Preliminaries

Step through the instructions below to make sure that you have
everything you need to get started.

### Install git
You can download git here:
[https://git-scm.com/downloads](https://git-scm.com/downloads)

<!-- TODO: check this -->
If prompted, select the option to add the installation location to system path.

<!-- On Windows, you may need to select an option about "Adjusting your PATH environment". -->
<!-- The option "Run Git from the Windows Command Prompt" will help RStudio find git. -->

Open a terminal or command prompt and type `git version` to check that
the installation worked.

#### Configure git [](#configure)

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
