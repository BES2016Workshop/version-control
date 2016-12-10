## When things go wrong...

One of the powerful functions of git is that it allows you to go back
to an earlier version of your code if you've made a mistake. We don't
have time to cover this in the workshop but here are some basic pointers.

### If you need to change something in your latest commit

It's easy to forget to make a change or to add a file that you wanted
to include in a commit. Provided you haven't already pushed your
changes you can easily adjust the latest commit. Make the necessary
changes, use `git add` to mark the modified files to be committed,
then run:

```
git commit --amend
```

This will re-run the previous commit with the additional changes that
you've made. You can use this command on its own if you just want to
adjust your commit message.


### Escaping from the text editor!

If you forget the `-m` on your `git commit` it will open your system's
default text editor in your terminal. If you're unfamiliar with the
way the editor works it can be hard to know how to exit from the
editor. If this catches you out, try the following:

`Esc` then `:x`

If that doesn't work, this question has been asked a million times on
stack exchange so Google is your friend.


### If you broke everything and need to go back to a previous version

First use:

`git reflog`

You will see a list of everything you've done in git. Each one has an
index indicated by `HEAD@{index}`. You need to find the one before you
broke everything and then use:

`git reset HEAD@{index}`

Also known as the magical time machine function!

**Warning:** if you've already pushed your changes to the remote
repository then using `git reset` in this way will cause problems when
you try to push. This is because git tries to discourage you to change
a remote's version history since doing so can be problematic if you
are working collaboratively.  There are some tips about how to proceed
in
[this StackOverflow answer](http://stackoverflow.com/questions/5816688/resetting-remote-to-a-certain-commit#5816761).

You can fix many other problems in git. Have a look at
[oh shit git!](http://ohshitgit.com/) for how to fix some other common
problems.

**Next:** [Summary](./summary.md)
