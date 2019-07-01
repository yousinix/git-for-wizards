# Git for Wizards

This repo is about, _yeah you guessed it right_, Git & GitHub. I will be exposing most of the magic spells that I have learned and the magic wands that I use regularly.

**Found this Helpful?**  
Show some support to help improve this repo and expose more magic spells!

[![followers](https://img.shields.io/github/followers/YoussefRaafatNasry.svg?style=social)][gh-profile]
[![endorsements](https://img.shields.io/badge/Git-Endrose%20Me-green.svg?logo=linkedin&style=social)][in-profile]

[gh-profile]: https://github.com/YoussefRaafatNasry
[in-profile]: https://linkedin.com/in/YoussefRaafatNasry

---

# Table of Contents

<!-- TOC depthFrom:2 -->

- [**1. Magic Wands**](#1-magic-wands)
    - [1.1. Git Command Line Tools](#11-git-command-line-tools)
    - [1.2. GitHub Chrome Extensions](#12-github-chrome-extensions)
    - [1.3. VS Code Extensions](#13-vs-code-extensions)
    - [1.4. Update Git to Latest Version](#14-update-git-to-latest-version)
- [**2. Avada Kedavra**](#2-avada-kedavra)
    - [2.1. Clean Local Untracked Files](#21-clean-local-untracked-files)
    - [2.2. Delete All Branches Except `master`](#22-delete-all-branches-except-master)
    - [2.3. Delete Remote-tracking Branches](#23-delete-remote-tracking-branches)
- [**3. Reparo**](#3-reparo)
    - [3.1. Rebase Without Changing Dates](#31-rebase-without-changing-dates)
    - [3.2. Set Committer Date to Author Date for Multiple Commits](#32-set-committer-date-to-author-date-for-multiple-commits)
    - [3.3. Set Commit's Date to Custom Date](#33-set-commits-date-to-custom-date)
- [**4. Expecto Patronum**](#4-expecto-patronum)
    - [4.1. Discover Bugs Using `git bisect`](#41-discover-bugs-using-git-bisect)
- [**5. Obliviate**](#5-obliviate)
    - [5.1. Create Orphan Branch](#51-create-orphan-branch)
- [**6. Riddikulus**](#6-riddikulus)
    - [6.1. Count Occurrence of Pattern](#61-count-occurrence-of-pattern)
    - [6.2. Count Number of Commits](#62-count-number-of-commits)
    - [6.3. Count Lines of Code](#63-count-lines-of-code)
    - [6.4. Count Lines Changed](#64-count-lines-changed)
    - [6.5. Export Full Log to File](#65-export-full-log-to-file)
    - [6.6. List Ignored Files](#66-list-ignored-files)
    - [6.7. List Large Files](#67-list-large-files)
- [**7. Markdown Beautifio**](#7-markdown-beautifio)
    - [7.1. Keyboard Key Strokes](#71-keyboard-key-strokes)
    - [7.2. Mathematics Equations](#72-mathematics-equations)
    - [7.3. Icons](#73-icons)
    - [7.4. Contributors Image](#74-contributors-image)
    - [7.5. Dropdowns](#75-dropdowns)
    - [7.6. Badges](#76-badges)
    - [7.7. Captions](#77-captions)
    - [7.8. README Headers](#78-readme-headers)
- [**8. The THANK YOU Spell :heart:**](#8-the-thank-you-spell-heart)
    - [8.1. References and Acknowledgments](#81-references-and-acknowledgments)
    - [8.2. Contributors](#82-contributors)

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

### 1.3. VS Code Extensions

1. [**GitLens**](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens): Supercharges the Git capabilities built into Visual Studio Code.
1. [**Git Blame**](https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame): See git blame information in the status bar.
1. [**Git History**](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory): View git log, file history, compare branches or commits.
1. [**Code Spell Checker**](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): A basic spell checker that works well with camelCase code. No more _"Fix Typo"_ commits.
1. [**Markdown Preview Github Styling**](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles): Changes VS Code's built-in markdown preview to match Github's style.
1. [**Markdown TOC**](https://marketplace.visualstudio.com/items?itemName=AlanWalk.markdown-toc): Markdown TOC _(Table Of Contents)_ Plugin for Visual Studio Code.
1. [**markdownlint**](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Markdown linting and style checking for Visual Studio Code.

### 1.4. Update Git to Latest Version

No matter how many wands you use, keeping your _primary wand_ up-to-date is still your duty.

1. First, check your git version

    ```bash
    git --version
    ```

1. Then use only one of the following commands according to your git version

    ```bash
    git update                    # version between 2.14.2 and 2.16.1
    git update-git-for-windows    # version is equal to greater Git 2.16.1(2)
    ```

---

## 2. Avada Kedavra

Avada Kedavra is your magic spell to **get rid of** all the dead branches and files.

### 2.1. Clean Local Untracked Files

Casting spells for the first time isn't that safe, so you have to see which files will be deleted before you run the actual command.

```bash
git clean -n
```

Then when you are comfortable use the `-f` or `-fd` option.

```bash
git clean -f     # Cleans files only without cleaning directories
git clean -fd    # Cleans files & directories
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

---

## 3. Reparo

Reapro is a spell that help you **fixing** your repository history.

> **CAUTION!:** Remember that those spells rewrite history, every commit included in the range will be rewritten. Don’t include any commit you’ve already pushed to a central server — doing so will confuse other developers by providing an alternate version of the same change

### 3.1. Rebase Without Changing Dates

Whenever you use `git rebase`, the `CommitDate` and `SHA` are updated to current date.

```bash
                    [Before rebase]                    |                     [After rebase]
                                                       |
    commit e7ee3464aa3c133df6f5ee622be863bc855dc8fd    |    commit eda7945c8d944e78d226b13a5c7280977f65a8c6
    Author:     Youssef Raafat <...>                   |    Author:     Youssef Raafat <...>
    AuthorDate: Sun Jun 30 02:05:07 2019 +0200         |    AuthorDate: Sun Jun 30 02:05:07 2019 +0200
    Commit:     Youssef Raafat <...>                   |    Commit:     Youssef Raafat <...>
    CommitDate: Sun Jun 30 02:05:07 2019 +0200         |    CommitDate: Mon Jul 1 02:06:20 2019 +0200
                                                       |
        Added New Feature                              |        Added New Feature
                                                       |
```

To avoid this from happening, use the `--committer-date-is-author-date`. But be careful that this option **doesn't work** with both `-i` and `--root`.

```bash
git rebase --committer-date-is-author-date
```

### 3.2. Set Committer Date to Author Date for Multiple Commits

Let's say we have about 10 commits that the `CommitDate` is not the same as the `AuthorDate` and we want them to be the same.

```bash
git rebase <first-bad-commit-SHA>^ --committer-date-is-author-date
```

> Tip: Use `git log --format=fuller` to see both `CommitDate` & `AuthorDate`.

### 3.3. Set Commit's Date to Custom Date

You made a commit 2 days ago, and God knows for whatever reason you want to **change that date** to be today's or another date. Don't freak out, this is possible!

1. Rebase to before said commit and stop for amendment.

    ```bash
    git rebase -i <commit-SHA>^
    ```

1. Replace `pick` with `edit` on the line with that required commit _(the first line usually)_.

1. Use one of the following commands depending on your needs.

    ```bash
    # [1] Use today's date:
    GIT_COMMITTER_DATE="$(date)"
    git commit --amend --no-edit --date "$(date)"

    # [2] Use custom date:
    GIT_COMMITTER_DATE="Mon Jul 1 02:06:20 2019 +0200"
    git commit --amend --no-edit --date "Mon Jul 1 02:06:20 2019 +0200"
    ```

---

## 4. Expecto Patronum

**Finding bugs** in long git histories isn't that easy, but by summoning a Patronus to help you hunting them, it will be much easier.

### 4.1. Discover Bugs Using `git bisect`

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

---

## 5. Obliviate

Obliviate is a spell used to **wipe memories**, to forget about things, like old git histories, and **start fresh**.

### 5.1. Create Orphan Branch

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

---

## 6. Riddikulus

Riddikulus is used to **transforms nasty git repositories** from something scary as complicated long histories **into something silly** as numbers, lists, insights and statistics.

### 6.1. Count Occurrence of Pattern

Let's say you want to count how many lambda expressions (`->`) you've used in all `.java` files, a quick spell can count it for you in the blink of an eye.

```bash
git grep '\->' '*.java' | wc -l
```

### 6.2. Count Number of Commits

You've been committing for so long now, maybe it's time to know how many commits are out there now.

```bash
git rev-list --count <branch-name>    # One branch
git rev-list --count --all            # All branches
```

### 6.3. Count Lines of Code

Curiosity is an enough reason to know loc.

```bash
git ls-files | xargs wc -l          # Detailed
git ls-files | xargs cat | wc -l    # Total
```

### 6.4. Count Lines Changed

You have been working on multiple features, and now you wanna know how many lines you have touched. It's fine spells got your back.
_**Note:** Add `--staged` if your changes were staged._

```bash
git diff --stat         # Detailed
git diff --shortstat    # Total
```

### 6.5. Export Full Log to File

Exporting your repository log to a file might be helpful sometimes, just learn this spell until the time comes and you need it.

1. **Text File**

    ```bash
    git log > log.txt
    ```

1. **JSON File** _(refer to [pretty-formats](https://git-scm.com/docs/pretty-formats) for more placeholders)_

    ```bash
    git log --pretty=format:'{
        "commit": "%H",
        "subject": "%s",
        "body": "%b",
        "author": {
            "name": "%aN",
            "email": "%aE",
            "date": "%aD"
        }
    },' > log.json
    ```

### 6.6. List Ignored Files

You wanna make sure that your `.gitignore` is working fine and that all files that you want to ignore are really ignored. Here's a quick spell for you.

```bash
git ls-files --others --ignored --exclude-standard
```

### 6.7. List Large Files

Keeping track of your repository size is something that you need to learn, this spell might be helpful if you managed to do so.

```bash
git rev-list --objects --all \
| git cat-file --batch-check='%(objecttype) %(objectname) %(objectsize) %(rest)' \
| sed -n 's/^blob //p' \
| sort --numeric-sort --key=2 \
| cut -c 1-12,41- \
| $(command -v gnumfmt || echo numfmt) --field=2 --to=iec-i --suffix=B --padding=7 --round=nearest
```

---

## 7. Markdown Beautifio

Some spells that you can use on GitHub to add a bit of _"beautifulness"_ to your **markdown files**.

### 7.1. Keyboard Key Strokes

Writing key strokes as plain text is the unforgivable sin that we are trying to void here using this spell.

```html
Press the following to save: <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>s</kbd>
```

Press the following to save: <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>s</kbd>

### 7.2. Mathematics Equations

Mathematicians are somehow wizards too, they need to write their equations and formulas.  
**CodeCogs** provides a good solution for embedding mathematics equations as images in markdown files, like the following equation.

![My Awesome Equation](https://latex.codecogs.com/png.latex?%5Cinline%20%5Cdpi%7B200%7D%20%5Csmall%20%5Cint%20u%20%5Cfrac%7Bdv%7D%7Bdx%7D%5C%2Cdx%3Duv-%5Cint%20%5Cfrac%7Bdu%7D%7Bdx%7Dv%5C%2Cdx)

1. Write your equation in the [Equation Editor](https://www.codecogs.com/latex/eqneditor.php).
1. Edit Image type, font, and size.
1. Choose **URL (encoded)** from the combobox at the end of the page.
1. Use the copied URL in a markdown **image** as follows:

```markdown
![My Awesome Equation](Endoded_URL_Here)
```


### 7.3. Icons

Adding icons to markdown files isn't that hard, you can use any of those two providers to help you:

1. [**ImgPlaceholder**](https://imgplaceholder.com)

    - Supports Font Awesome, Ionicons & Glyphicons.
    - Customizable size, foreground color & background color.
    - Can be written in markdown or HTML syntax.
    - Lower quality.
    <br/><br/>

    ```markdown
    ![imgplaceholder](https://imgplaceholder.com/80x80/transparent/000000/fa-github?font-size=92)
    ```

    ![imgplaceholder](https://imgplaceholder.com/80x80/transparent/000000/fa-github?font-size=92)

2. [**Simple Icons**](https://simpleicons.org/)

    - Supports [SVG icons](https://github.com/simple-icons/simple-icons/tree/develop/icons) for popular brands only.
    - Black color only.
    - HTML syntax only.
    - Higher quality.
    <br/><br/>

    ```html
    <img alt="simple-icons" width="80" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/github.svg" />
    ```

    <img alt="simple-icons" width="80" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/github.svg" />

### 7.4. Contributors Image

[contributors-img](https://contributors-img.firebaseapp.com/) provides a good way for adding a good looking image of your contributors in your markdown file.

```markdown
[![Contributors][contributors-img]][contributors]

[contributors]: https://github.com/USERNAME/REPONAME/graphs/contributors
[contributors-img]: https://contributors-img.firebaseapp.com/image?repo=USERNAME/REPONAME
```

[![Angular Contributors][contributors-img]][contributors]

[contributors]: https://github.com/angular/angular-ja/graphs/contributors
[contributors-img]: https://contributors-img.firebaseapp.com/image?repo=angular/angular-ja

### 7.5. Dropdowns

Keep the less useful content collapsed, no one needs to see it!

```markdown
<details>

<summary><b>Example</b></summary>
<br/>

1. Remove the `<b>` & `<br/>` tags if you want, it's fine.
1. Don't forget to surround the body with blank lines.
1. Supports **Markdown** _Syntax_. Including Images.

![git-for-wizards](https://imgplaceholder.com/1000x200/992c2c/ffffff?text=Git+for+Wizards&font-family=OpenSans_Bold)

</details>
```

<details>

<summary><b>Example</b></summary>
<br/>

1. Remove the `<b>` & `<br/>` tags if you want, it's fine.
1. Don't forget to surround the body with blank lines.
1. Supports **Markdown** _Syntax_. Including Images.

![git-for-wizards](https://imgplaceholder.com/1000x200/992c2c/ffffff?text=Git+for+Wizards&font-family=OpenSans_Bold)

</details>

### 7.6. Badges

A wise wizard once said _"Just add more badges!"_.  
Maybe that's why they created [**shields.io**](https://shields.io/).

```markdown
![GitHub last commit](https://img.shields.io/github/last-commit/YoussefRaafatNasry/git-for-wizards.svg)
![GitHub repo size](https://img.shields.io/github/repo-size/YoussefRaafatNasry/git-for-wizards.svg)
```

![GitHub last commit](https://img.shields.io/github/last-commit/YoussefRaafatNasry/git-for-wizards.svg)
![GitHub repo size](https://img.shields.io/github/repo-size/YoussefRaafatNasry/git-for-wizards.svg)

### 7.7. Captions

Some photos are meaningless without captions, but wizards know how to handle that!

```html
<div align="center">
    <img src="https://imgplaceholder.com/480x200/992c2c/ffffff?text=Git+for+Wizards&font-family=OpenSans_Bold" />
    <br/>
    <sub><sup>© 2019, licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.</sup></sub>
</div>
```

<div align="center">
    <img src="https://imgplaceholder.com/1000x200/992c2c/ffffff?text=Git+for+Wizards&font-family=OpenSans_Bold" />
    <br/>
    <sub><sup>© 2019, licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.</sup></sub>
</div>

### 7.8. README Headers

This will be enough as a start to add a cool header for your README file, but try to be more creative.

```html
<div align="center">
    <img src="https://imgplaceholder.com/100x100/transparent/323232/ion-ios-color-wand?font-size=100" />
    <h3>Git for Wizards</h3>
    <strong>Some magic spells and wands for Git & GitHub</strong>
</div>
```

<div align="center">
    <img src="https://imgplaceholder.com/100x100/transparent/000000/ion-ios-color-wand?font-size=100" />
    <h3>Git for Wizards</h3>
    <strong>Some magic spells and wands for Git & GitHub</strong>
</div>

---

## 8. The THANK YOU Spell :heart:

### 8.1. References and Acknowledgments

1. [Change the date of a git commit](https://codewithhugo.com/change-the-date-of-a-git-commit/)
1. [How to discover a bug using git bisect?](https://flaviocopes.com/git-bisect/)
1. [How to find/identify large commits in git history?](https://stackoverflow.com/a/42544963/10194811)
1. [Orphaned Branches in Git](https://bugfactory.io/2016/02/12/orphaned-brachnes-in-git/)

### 8.2. Contributors

[![contributors][contrib-img]][contrib]

[contrib]: https://github.com/YoussefRaafatNasry/git-for-wizards/graphs/contributors
[contrib-img]: https://contributors-img.firebaseapp.com/image?repo=YoussefRaafatNasry/git-for-wizards

---

<!-- Footer -->

<div align="center">
    <h3>Congratulations!</h3>
    <small>
    You have finally reached the end!<br/>
    You've done it all. You are FREE now!<br/>
    <sub><i>* Please don't forget to turn off the lights on your way out.</i></sub><br/>
    </small>
    <br/>
    <img src="https://user-images.githubusercontent.com/41103290/59287218-8742b600-8c71-11e9-8104-f31f8a612ff6.gif">
    <br/>
    <sub><sup><b>© 2019 git-for-wizards, licensed under the <a href="./LICENSE.md">MIT License</a>.</b></sup></sub>
</div>
