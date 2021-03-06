# Creating a GitHub Repository


## Questions
* How can I create a git repository on GitHub for my work?
* How can I keep my work private if need be?
* How can I get a copy of the repository I can modify on my computer?

## Objectives
* Understand options for creating a repository on GitHub.
* Understand how to clone a local copy repository from GitHub.

## Git vs GitHub

Git is called a 'distributed version control system'. The contrast to this is a
Centralised Version Constrol System (CVS) e.g. Google Docs. Git is distributed
in the sense that although it can be used to syncronise changes to a repository,
it does not require a 'single source of truth' to do that. File changes can be
shared in networks of peers with any topology.

Git was developed for the Linux Kernel project which has a structure reminiscent
of a military. A supreme commander accepts code changes from a few trusted
generals, who in turn accept code changes from a few trusted lieutenants and so
on. This would not be possible with a centralised model.

Torvalds sarcastically quipped about the name git (which means "unpleasant person" in British English slang): "I'm an egotistical bastard, and I name all my projects after myself. First 'Linux', now 'git'." The man page describes Git as "the stupid content tracker". The read-me file of the source code elaborates further:

"git" can mean anything, depending on your mood.

* random three-letter combination that is pronounceable, and not actually used by any common UNIX command. The fact that it is a mispronunciation of "get" may or may not be relevant.
* stupid. contemptible and despicable. simple. Take your pick from the dictionary of slang.
* "global information tracker": you're in a good mood, and it actually works for you. Angels sing, and a light suddenly fills the room.

GitHub hosts git repositories, that act as central repositories that users
synchronise with. But even this mode is more flexible than a traditional
centralised approach. Users can use git locally to manage committed changes
before 'pushing' them to GitHub. E.g. remove or amend commits.

GitHub also introduces the concept of 'forking' whereby users can create a fork
of another user's GitHub repository, sync changes with the fork, and eventually propose
changes be pulled from the fork by the original repository. Forks can themselves
be forked, which allows for a complex topologies within repositories hosted on
GitHub.

In summary git is the program that creates repositories and powers the version
control, and GitHub provides cloud hosting for git repositories with additional
website features that facilitate collaboration.

## Creating a hosted repository on GitHub

There are a number of ways to set up a local repository that is syncronised with
GitHub. In this lesson we will use the 'GitHub first' approach described by
[@Bryan2018-le]. At a high level the workflow for this approach looks like:

1. Create repository on https://www.github.com
1. Clone the GitHub repository to your PC, making a 'local copy'.
1. Commit changes to local copy and push to GitHub.

### Creating a repository on github.com

The two key things we'll need to decide when creating a repository are what the
repository shall be called, and whether it shall be public or private.

#### On naming
As suggested by GitHub, the name should be short and memorable. However, you
want to balance this with searchable as your repository count grows. For example
when creating repositories associated with an event or group you might include a
reference to it in the name eg. 'ABS_ML_workshop'. You get to 'pin' 6 repositories
to your profile page ensuring they will always be easy to find.

#### On public vs private
Public in the GitHub sense means the repository and all its history are able to
be viewed (and copied) by all GitHub users. Only nominated collaborators can
modify the repository.

Private repositories can only be seen and interacted with by the owner and
nominated collaborators.

GitHub has social network type features that allow users to follow eachother and
see when someone they follow creates or 'stars' a public repository. Starring is
similar to 'liking' on other platforms. It is possible to take advantage of
these features to get your work noticed, but this depends on your work being
public.

A repository's public/private status can be changed at any time. If you are open
to collaborations or feedback arising from your work you probably want to make
it public as early as possible. Many people (author included) take a 'public by
default' approach to creating repositories. This is also probably driven by the
fact that users only get 1 private repository with a free tier GitHub account.

#### Follow some people {.exercise}
In a minute we'll create a repository but before that you should follow some
people so you can see what the GitHub activity stream looks like.

1. Exchange GitHub usernames with a couple of your neighbours.
1. With each username:
    1. Type the username into the search box at the top left of the menu
    1. In the results, click the 'Users' link of the left of screen.
    1. Click the 'Follow' button associated with the username you searched for.

#### Create a repository {.exercise}

1. Navigate to github.com and login.
1. Click the '+' icon on the top right on the menu bar and select 'New Repository'.
1. Choose 'git_workshop' as the repository name.
1. Choose 'Public'.
1. Check 'Initialize this repository with a README' <-- **IMPORTANT**
1. Check 'Choose a license' <-- **IMPORTANT**
1. Click 'Create repository'

#### On the README
It is good practice for every repository to have a README.md file. GitHub will
use this file as the 'front page' of the respository, so it is the place to
communicate what your work is about. Even in private repositories you'll want
to put some notes here that will help future you remember what the project was
or where it was up to.

It is especially important to initialise the repository with a README in this
workflow as this will allow you to clone the repository to a local copy
immediately. Empty repositories cannot be cloned.

## Summary

* Creating a repository using the GitHub GUI
  - private vs public
  - naming
  - README
