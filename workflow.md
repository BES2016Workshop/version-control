## Subsequent workflow

Once you've set up the remote repository, subsequent updates follow a
similar pattern:

* Add or make changes to files in your repository
* Stage the new/modified files:  `git add`
* Commit your changes: `git commit`
* Push local changes to the remote: `git push`

At any point you can use `git status` to find out the current state of
your repository. If you have made a local commit that has not yet been
pushed to the remote repository, `git status` will display a message
indicating that your local branch is ahead of `origin/master` (the
remote branch). Use

```
git push
```

to bring the remote branch up-to-date.

**Next:** [Summary](./summary.md)
