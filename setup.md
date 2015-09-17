# Setting up a basic development environment

A development environment is precisely what it sounds like: a set of tools used to develop computer programs.  In this section, we will install our programming language of choice (Python), our text editor of choice (Atom), our version control of choice (Git), and learn a few Terminal commands for navigating our file system.

The setup documentation and introductory terminal commands in [CS 61A's Lab 0](http://cs61a.org/lab/lab00/) may prove helpful.

A couple additional tools that may be worth setting up: `brew` (a package manager for OS X &mdash; basically, a way to easily install and configure commonly used programs), `pip` (a package manager for the Python programming language), `virtualenv` (a program allowing you to configure separate environments for Python development).

## Setting up Python

### Windows PC

TODO

### OS X

Python, by default, is bundled with OS X installations.  You can confirm this by opening Terminal (in Applications), and typing in `python`.  Something like this should appear:

    Python 2.7.10 (default, Jul 13 2015, 12:05:58)
    [GCC 4.2.1 Compatible Apple LLVM 6.1.0 (clang-602.0.53)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

### Linux

TODO

## Setting up Atom

Follow the directions at [https://atom.io/](https://atom.io/).

## Git

Follow the directions at [https://help.github.com/articles/set-up-git/](https://help.github.com/articles/set-up-git/).  If you chose to install `brew`, you can also install using `brew install git`.

You can learn a little about basic git commands [here](http://rogerdudler.github.io/git-guide/).  You will mostly be using `git add`, `git commit`, and `git push`.  Using git to improve your workflow will be covered later on.

Create a GitHub account, and then make a new repository for this class.  Call it whatever you want, but make sure to put all your code in here (and work on code in here, as well)!  You should have separate folders for `hw1`, `hw2`, `proj1`, etc.

## Some basic Terminal commands

Read [this link](http://mac.appstorm.net/how-to/utilities-how-to/how-to-use-terminal-the-basics/) and test out the commands afterwards.  In particular, `cd` (change directory), `ls` (display contents of current directory), `atom` (open a file or folder in Atom), and `python` (run a Python program) will be the commands you use the most.

In general as you become more proficient and use a wider set of tools, you may be interested in [creating a more intricate development environment](not-currently-available).
