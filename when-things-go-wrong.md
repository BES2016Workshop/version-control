## When things go wrong...

One of the powerful functions of git is that it allows you to go back 
to an earlier version of your code if you've made a mistake. We don't 
have time to cover this in the workshop but here are some basic pointers.

## If you broke everything and need to go back to a previous version

First use:

`git reflog`

You will see a list of every thing you've done in git each one has an 
index HEAD@{index}. You just need to find the one before you broke everything
and then use:

`git reset HEAD@{index}`

Also known as the magical time machine function!

You can fix many other problems too, see [oh shit git!](http://ohshitgit.com/)
for more details.

## Escaping from the text editor in terminal!

This might sound stupid but this is often the biggest problem with git
(and it isn't even a git problem really).
If you forget the `-m` on your `git commit` it will open a text editor
in your terminal. It's often hard to know how to then get back to the
normal terminal. In general try:

`Esc` then `:x` 

If that doesn't work, this question has been asked a million times on
stack exchange so Google is your friend.

### Documentation, cheatsheets and tutorials
- `git help <command>`
- [oh shit git!](http://ohshitgit.com/)