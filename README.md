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
- [**2. Avada Kedavra**](#2-avada-kedavra)
  - [2.1. Remove local untracked files](#21-remove-local-untracked-files)
  - [2.2. Delete All Branches Except `master`](#22-delete-all-branches-except-master)
  - [2.3. Delete Remote-tracking Branches](#23-delete-remote-tracking-branches)

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

---

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