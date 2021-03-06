# 'GIT'ting out of trouble

## Questions
* I messed up the commit message or files committed, how can I edit a commit?
* I realised I introduced a problem, how can I revert a file to an earlier version?
* Something is not right, how can I restore an earlier version of the whole repository?

## Objectives
* Understand how to solve some common problems in arising in git.

## Helping yourself with git
In this lesson we'll cover just a few of the ways you can get yourself out of trouble with git. The key new you commands we'll discuss are:

* `checkout` which will allow us to restore files to previous versions.

There are other great resources on this topic, see:

  * [OhS**tGit](https://ohshitgit.com/)
  * [Getting Unstuck from Git](http://inundata.org/lectures/git/#/)

## Fixing a previous commit
In this scenario you've made a commit and then you realise you missed a file or
made an error with the commit message.

You an call the `git commit` command with the `--amend` flag and any staged
files will be added to the previous commit and you will be given a chance to
rewrite the commit message.

### Your first amendment {.exercise}

Using the 'git_workshop' repository from previous lessons:

1. Open 00_analysis.py in a text editor and insert a new line: "part one"
1. On the terminal, Save, stage, and commit the file with commit messge "added part one"
1. In a text editor, add a new line in 00_analysis.py: "part two"
1. Save and stage the file.
1. Amend the commit as described above.
1. Push the commit.
1. Check the history on GitHub and confirm "part one" and "part two" were added as part of the same commit.

## Restoring a file to an earlier version

Let's say you've identified a problem with a specific file and would like to
restore it to an earlier version. You have two options:

1. You can look through the history, say on GitHub, and find the hash of a
   commit from when things were fine. You restore the file to the version it was
   when that commit was made.
1. You can't find a commit or oh god please there's not much time. You can
   restore the file to the version it was some time ago

After you have restored the file, you can stage, commit, and push it to make it
the current version.

### Restoring to a hash

You don't need the complete hash, just enough letters to ensure a unique match.
6 or so will usually do. The format of the command is

```
$ git checkout <patial hash> <file path>
```

The hashes in your repository are unique so I can't give an example that will
work for you. But this would restore `00_analysis.py` to its a blank
state in my repository:

```
$ git checkout 3ff91b 00_analysis.py
```

### Restoring to a time period ago

Let's say it's Monday morning and you realise you made some bad changes to a
file on Friday afternoon, but you're not sure when, and you just need to fix it in
a hurry before your meeting with your supervisor. You could do:

```
$ git checkout "@{3 days ago}" <file path>
```

To restore the file to as it was on Friday morning. You can use decimal numbers
and any time unit. `@{20 minutes ago}` might be good for those last minute
presentation 'tweaks'.


### Restoring to most recent version

If you decide you would like to return a file you restored with `checkout` to
it's most recent version, remember that HEAD is a reference to the latest
commit. So you can again use `checkout`:

```
$ git checkout HEAD <file path>
```

### Restoration resuce {.exercise}

Using the 'git_workshop' repository:

1. Using `git checkout`, Restore 'analysis.py' to the working directory. This
   is what '00_analysis.py' was called before we changed its name.


## Restoring the entire repository to an earlier version

You have a few options here depending on the outcome you want. Here I assume you want
to temporarily roll back to check an analysis result with an old version, but you do not
want to permanently reset the repository and its history to an earlier time point.

If you call `git checkout` with no `<file path>` argument the entire repository will
be rolled back to the commit hash or time you specified. For example:

```
git checkout "@{1 day ago}"
```

**However be warned** if you make commits in this state, they will work but they
will not be added to the history - You can't just insert stuff into the middle
of history(!). You can add these orphan commits to a branch, but this is
beyond the scope of this lesson.

This state of git purgatory is called 'detached HEAD' as the head reference no
longer points to a commit on the branch's timeline.

We can't use `git checkout HEAD` as before to return to present because HEAD is no longer on any timeline. So we need to put HEAD back on a timeline using:

```
git checkout main
```
Where HEAD will be pointing to the latest commit by default.

Permanently resetting the repository and its history to an earlier time point is
possible but can lead to permanent loss of work. You will need to look into
advanced usage of `git reset --hard`.

## When all else fails

![](https://imgs.xkcd.com/comics/git.png)

This is also called 'burning it down'.

## Summary

You learned git commands that are useful for updating commits, restoring files,
and jumping back to previous repository versions.

* git commit --amend
* git checkout 123abc file.ext
* git checkout 123abc
* git checkout "@{4 days ago}"
