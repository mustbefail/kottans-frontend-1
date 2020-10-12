![cat-banner-top](./images/markdown-styling/cat-banner-top.png)

# kottans-frontend

## Repository dedicated to participation in [Kottans frontend course](https://github.com/kottans/frontend)

![cat-banner-bottom](./images/markdown-styling/cat-banner-bottom.png)

![box-shadow-top](./images/markdown-styling/box-shadow-top.png)

## My progress :rocket:

 1. **GENERAL**
    - [ ] [Git and Github](#1-git-and-github)
    - [ ] [Linux CLI and Networking](#2-linux-cli-and-networking)
    - [ ] [VCS (hello gitty), GitHub and Collaboration](#3-vcs-hello-gitty-github-and-collaboration)
  
 2. **FRONT-END BASICS**
  
    - [ ] [Intro to HTML & CSS](#4-intro-to-html-css)
    - [ ] [Responsive Web Design](#5-responsive-web-design)
    - [ ] [HTML & CSS Practice](#6-html-css-practice)
    - [ ] [JavaScript Basics](#7-javascript-basics)
    - [ ] [Document Object Model - practice](#8-document-object-model-practice)
  
 3. **ADVANCED TOPICS**

    - [ ] [Building a Tiny JS World (pre-OOP) - practice](#9-building-a-tiny-js-world-pre-oop-practice)
    - [ ] [Object oriented JS - practice](#10-object-oriented-js-practice)
    - [ ] [OOP exercise - practice](#11-oop-exercise-practice)
    - [ ] [Offline Web Applications](#12-offline-web-applications)
    - [ ] [Memory pair game — real project!](#13-memory-pair-game-real-project)
    - [ ] [Website Performance Optimization](#14-website-performance-optimization)
    - [ ] [Friends App - real project!](#15-friends-app-real-project)
  
![box-shadow-bottom](./images/markdown-styling/box-shadow-bottom.png)

![cat-banner-top](./images/markdown-styling/cat-picture-top.png)

## GENERAL

![cat-picture-bottom](./images/markdown-styling/cat-picture-bottom.png)

### 1. Git and GitHub

***

1.1. [Version Control with Git course](https://www.udacity.com/courseversion-control-with-git--ud123)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./images/completion-screenshots/version-control-with-git.png)

![alert-image](./images/markdown-styling/alert.png)

During this course i:

- Used just learned commands while trying to add 'after-commit' changes to the last commit of this review.
- Realized that 'versions' is not only about highly specialized software such as git and version control to varying degree can be found in almost every program.
- Worked with versions of a document (called revisions) in google docs.
- Repeated and clarified the basic concepts of git (working directory, index, repository areas and their workflow). Got acquainted with the contents of the hidden `.git` folder. Learned how to add files into `.gitignore` manually and with using special symbols.
- Updated git version and checked config info.
- Discovered new terminal commands:
  | Command | Usage |
  | --- | --- |
  | `rmdir` | remove directory |
  | `ls -a` | list hidden files |
  | `mkdir -p parent/child` | create nested directories with single command |
- Repeated and used next git commands:
  | Command | Usage |
  | --- | --- |
  | `git log`, `git show` | inspecting commits |
  | `git rm --cached <filename>` | unstaging files |
  | `git diff` | difference between working directory and last commit |
- Installed and first used [HTML linter](https://htmlhint.com/), [CSS linter](https://stylelint.io/), [JS linter](https://eslint.org/). While googling discovered command `npm init -y` for generating empty npm project.
- Worked with git documentation to find neccessary command options.
- Got acquainted with Less command line pager and it's commands for navigating through the history of commits:
  | Key | Usage |
  | --- | --- |
  | `j` or `↓` | scroll :arrow_down: by a line |
  | `d` | scroll :arrow_down: by a half-page |
  | `f` | scroll :arrow_down: by a page |
  | `k` or `↑` | scroll :arrow_up: by a line |
  | `u` | scroll :arrow_up: by a half-page |
  | `b` | scroll :arrow_up: by a page |
- Learned and used commands for commits investigation:
  | Command | Usage |
  | --- | --- |
  | `git log --oneline`, `git log --stat`, `git log --patch/-p`, `git log --stat -patch` | display all commits i  certain form |
  | `git log --oneline <commit-ref>`, `git log --stat <commit-ref>`, `git log -p <commit-ref>` | display commit  from the point where specific commit placed |
  | `git show <commit-ref>`, `git show --stat <commit-ref>`, `git show --stat --patch <commit-ref>` | ge  specific commit |
- Realized that each commit should make a change to just **ONE** aspect of the project. **Single-unit change** principle.

  > Work on one change first, commit that, and then change the second one.  
  >  
  > The best way that I've found to think about what should be in a commit is to think, "What if all chang  introduced in this commit were erased?". If a commit were erased, it should only remove one thing.
- Learned about commit naming:
  | Do :white_check_mark: | Don't :x: |
  |----|----|
  | make it *short* | don't use *and* |
  | response *what* was done | don't tell *how* and *why* it was done |
  
  > The best way that I've found to come up with a commit message is to finish this phrase, "This commit will...". However, you finish that phrase, use that as your commit message.
- Learned about entities used for organizing commits structure:
  | Entity | Description |
  | --- | --- |
  | tags  | static commit pointers  |
  | branches | dynamic commit pointers |
  | `HEAD` | dynamic branch/commit pointer |
- Practiced in creating and deleting tags/branches and switching between branches. Practiced in linking tags and branches with specific commits. Practiced working with multiple feature branches.
- Learned useful commands for work with branches:
  | Command | Usage |
  | --- | --- |
  | `git checkout -b <new-branch-name>` | create branch and switch to it |
  | `git checkout -b <new-branch-name> <existing-branch-name>` | create branch pointing on another  branch's las  commit and switch to it |
  | `git checkout -b <new-branch-name> <SHA>` | create branch pointing on specific commit and  switch to it |
  | `git log --oneline/--patch/--stat --all --graph` | log commits for all branches using graph |
- Executed fast-forward and regular merges using `git merge <other-branch>` command. If we merge 2 branches commits will be added to the one which under `HEAD` pointer (current branch). `Branch we merge into === current branch`.
  > When we merge, we're merging *some other branch* ***into the current (checked-out) branch***.
  >
  > Fast-forward merge – the branch being 'merged in' must be ahead of the current branch. Current branch'    pointer will just be moved forward to point to the same commit as the other branch.
  >
  > Regular merge - two divergent branches are combined, merge commit is created.
- Forced and resolved merge conflict. Realized thay Git tracks lines in files and merge conflict happens when the same lines are changed in separate branches.
- Learned how to undo changes using commands:
  - **git amend** - replace last commit with new one (new one created by changing last commit's index).
    | Command | Usage |
    | --- | --- |
    | `git commit --ammend -m='...'` | update recent commit message if index is empty since last   commit |
    | `git add <updated-file>` -> `git commit --amend -m='...'` | add changes made after commit to index -  update recent commit content and message |
    | `git add <updated-file>` -> `git commit --amend --no-edit` | add changes made after commit to index -  update recent commit content |
  - **git revert** - create new commit with removed last/specific commit's changes. If 'a' character is added i  commit A, if Git reverts commit A, then Git will make a new commit where 'a' character is deleted.
    | Command | Usage |
    | --- | --- |
    | `git revert <commit-ref> -m='...'` | create new commit with removed/reversed changes made within define  commi |  
  - **git reset** :warning: - erase commit from memory by moving HEAD and current branch pointer to anothe  commit. Erased commit's fate defined by `--mixed` (default), `--soft` and `--hard` options. It is better t  create backup branch for using this command.
    | Command | Usage |
    | --- | --- |
    | `git reset <commit-ref>` | move HEAD and current branch pointer to defined commit, place erased commit i  working directory |
    | `git reset <commit-ref> --soft` | move HEAD and current branch pointer to defined commit, place erase  commit in index |
    | `git reset <commit-ref> --hard` | move HEAD and current branch pointer to defined commit, place erased i  trash area |
- Learned that to reference commits we can use not only SHA/tags/branches/HEAD, but also relative path. All types of references can be integrated in commands where indicator of specific commit needed.
  
**Most of all in the course I liked presence of simple analogies  and visualizations of how git workflow works.**

1.2 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

***

### 2. Linux CLI and Networking

***

2.1 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

2.2 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

***

### 3. VCS (hello gitty), GitHub and Collaboration

***

3.1 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

3.2 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

***

![cat-picture-top](./images/markdown-styling/cat-picture-top.png)

## FRONT-END BASICS

![cat-picture-bottom](./images/markdown-styling/cat-picture-bottom.png)

### 4. Intro to HTML & CSS

***

4.1 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

4.2 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

***

### 5. Responsive Web Design

***

4.1 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

4.2 [text placeholder](link)

[![Screenchot-image-link](./images/markdown-styling/screenshot-image-link.png)](./)

- **What was new**
  text placeholder
- **What surprised**
  text placeholder
- **What will be used in practice**
  text placeholder
- **General overview**
  text placeholder

***

### 6. HTML & CSS Practice

### 7. JavaScript Basics

### 8. Document Object Model - practice

![cat-picture-top](./images/markdown-styling/cat-picture-top.png)

## ADVANCED TOPICS

![cat-picture-bottom](./images/markdown-styling/cat-picture-bottom.png)

### 9. Building a Tiny JS World (pre-OOP) - practice

### 10. Object oriented JS - practice

### 11. OOP exercise - practice

### 12. Offline Web Applications

### 13. Memory pair game — real project

### 14. Website Performance Optimization

### 15. Friends App - real project