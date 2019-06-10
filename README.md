# Git for Wizards

This repo is about, _yeah you guessed it right_, Git & GitHub. I will be exposing most of the magic spells that I have learned and the magic wands that I use regularly.

**Found this Helpful?**  
Show some support to help improve this repo and expose more magic spells!

[![followers](https://img.shields.io/github/followers/YoussefRaafatNasry.svg?style=social)][gh-profile]
[![endorsements](https://img.shields.io/badge/Git-endrose%20me-green.svg?logo=linkedin&style=social)][in-profile]

[gh-profile]: https://github.com/YoussefRaafatNasry
[in-profile]: https://www.linkedin.com/in/youssefraafatnasry

---

# Table of Contents

<!-- TOC depthFrom:2 -->

- [**1. Magic Wands**](#1-magic-wands)
    - [1.1. Git Command Line Tools](#11-git-command-line-tools)
    - [1.2. GitHub Chrome Extensions](#12-github-chrome-extensions)
    - [1.3. Update Git to Latest Version](#13-update-git-to-latest-version)
- [**2. Avada Kedavra**](#2-avada-kedavra)
    - [2.1. Clean local untracked files](#21-clean-local-untracked-files)
    - [2.2. Delete All Branches Except `master`](#22-delete-all-branches-except-master)
    - [2.3. Delete Remote-tracking Branches](#23-delete-remote-tracking-branches)
- [**3. Expecto Patronum**](#3-expecto-patronum)
    - [3.1. Discover Bugs Using `git bisect`](#31-discover-bugs-using-git-bisect)
- [**4. Obliviate**](#4-obliviate)
    - [4.1. Create Orphan Branch](#41-create-orphan-branch)
- [**5. The THANK YOU Spell :heart:**](#5-the-thank-you-spell-heart)
    - [5.1. References and Acknowledgments](#51-references-and-acknowledgments)
    - [5.2. Contributors](#52-contributors)

<!-- /TOC -->

---

## 1. Magic Wands

Magic Wands are the **tools and the extensions** that you can use to improve your workflow and magic skills.

### 1.1. Git Command Line Tools

1. [**hub**](https://github.com/github/hub): A command-line tool that makes git easier to use with GitHub.
1. [**git-sizer**](https://github.com/github/git-sizer): Compute various size metrics for a Git repository, flagging those that might cause problems.
1. [**git-quick-stats**](https://github.com/arzzen/git-quick-stats): A simple and efficient way to access various statistics in git repository.

### 1.2. GitHub Chrome Extensions

1. [**GitHub-Dark**](https://github.com/StylishThemes/GitHub-Dark): Dark GitHub style.
1. [**octolinker**](https://octolinker.github.io/): Allow navigation through code on GitHub more efficiently.
1. [**github-repo-size**](https://github.com/harshjv/github-repo-size): Display repository size on GitHub.
1. [**git-history-browser-extension**](https://github.com/LuisReinoso/git-history-browser-extension): Add a button to the github file interface to see its history.
1. [**github-file-icon**](https://github.com/xxhomey19/github-file-icon): Gives different filetypes different icons in GitHub.

### 1.3. Update Git to Latest Version

No matter how many wands you use, keeping your _primary wand_ up-to-date is still your duty.

1. First, check your git version

    ```bash
    git --version
    ```

1. Then use only one of the following commands according to your git version

    ```bash
    git update                   # version between 2.14.2 and 2.16.1
    git update-git-for-windows   # version is equal to greater Git 2.16.1(2)
    ```

## 2. Avada Kedavra

Avada Kedavra is your magic spell to **get rid of** all the dead branches and files.

### 2.1. Clean local untracked files

Casting spells for the first time isn't that safe, so you have to see which files will be deleted before you run the actual command.

```bash
git clean -n
```

Then when you are comfortable use the `-f` or `-fd` option.

```bash
git clean -f       # Cleans files only without cleaning directories
git clean -fd      # Cleans files & directories
```

### 2.2. Delete All Branches Except `master`

Your repo is getting messy, a lot of branches that you no longer need. No need to worry, a simple magic spell can get most of the work done for you.

```bash
git branch | grep -v 'master' | xargs git branch -D
```

You can replace `master` with any other branch name that you want to keep, but be careful **this will delete master**.  
Or even use a pattern of **more than one branch** to keep them and delete the rest.

```bash
git branch | grep -v 'master\|gh-pages' | xargs git branch -D
```

### 2.3. Delete Remote-tracking Branches

Deleting local branches doesn't clean the repo 100%, since they were tracking remote branches, so you will need to burn all those references to the ground. _(This will only work if you've already deleted the remote branch from your GitHub repo)_

```bash
git fetch --prune
```

## 3. Expecto Patronum

**Finding bugs** in long git histories isn't that easy, but by summoning a Patronus to help you hunting them, it will be much easier.

### 3.1. Discover Bugs Using `git bisect`

Debug almost all problems that involve a long history of changes, tracked using Git, and discover when you introduced a bug in your code.

1. To start the binary search process, you will need to checkout to your latest commit first, then provide git with 2 commits to search for the bug within, the last good commit and the commit that first introduced the bug

    ```bash
    git checkout <your-branch-name>
    git bisect start
    git bisect good <SHA-for-good-commit>
    git bisect bad <SHA-for-bad-commit>
    ```

1. Git will ask for your feedback on some commits, so you will need to tell it if the commit is good or bad, use one of the following commands to do so:

    ```bash
    git bisect good
    git bisect bad
    ```

1. When done, Git will guide you to bugged commit. You will need to exit the binary search process afterwards by using the following command:

    ```bash
    git bisect reset
    ```

## 4. Obliviate

Obliviate is a spell used to wipe memories, to forget about things, like old git histories, and start fresh.

### 4.1. Create Orphan Branch

Orphan branches aren't based on any other branches.The first commit made on this new orphan branch will have no parents and it will be the **root of a new history** totally disconnected from all the other branches and commits.  
If you are using [GitHub Pages](https://pages.github.com/) this might be helpful as you can create a new branch named `gh-pages`. This branch is “orphaned” and therefore completely separate from your repository’s prior history.

```bash

                                                    |
            i---j---k     <== branch 'feature-1'    |
           /                                        |    a---b---c---d       <== branch 'master'
  a---b---c---d---h---l   <== branch 'master'       |
       \         /                                  |        1---2---3---4   <== branch 'gh-pages' (orphan)
        e---f---g         <== branch 'feature-2'    |
                                                    |
                 [Normal Branches]                  |                    [Orphan Branch]

```

To create a new empty orphan branch, use the following commands

```bash
git checkout --orphan <new-branch-name>
rm .git/index
git clean -fdx
```

## 5. The THANK YOU Spell :heart:

### 5.1. References and Acknowledgments

1. [Orphaned Branches in Git](https://bugfactory.io/2016/02/12/orphaned-brachnes-in-git/)

### 5.2. Contributors

[![People who made it possible!][contrib-img]][contrib]

[contrib]: https://github.com/YoussefRaafatNasry/git-for-wizards/graphs/contributors
[contrib-img]: https://contributors-img.firebaseapp.com/image?repo=YoussefRaafatNasry/git-for-wizards
