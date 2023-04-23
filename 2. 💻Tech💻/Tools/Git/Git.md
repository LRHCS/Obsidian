  #Tools 
## Basics

-   `git help <command>`: get help for a git command
-   `git init`: creates a new git repo, with data stored in the `.git` directory
-   `git status`: tells you what’s going on
-   `git add <filename>`: adds files to staging area
-   `git commit`: creates a new commit
    -   Write [good commit messages](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)!
    -   Even more reasons to write [good commit messages](https://chris.beams.io/posts/git-commit/)!
-   `git log`: shows a flattened log of history
-   `git log --all --graph --decorate`: visualizes history as a DAG
-   `git diff <filename>`: show changes you made relative to the staging area
-   `git diff <revision> <filename>`: shows differences in a file between snapshots
-   `git checkout <revision>`: updates HEAD and current branch

## Branching and merging

-   `git branch`: shows branches
-   `git branch <name>`: creates a branch
-   `git checkout -b <name>`: creates a branch and switches to it
    -   same as `git branch <name>; git checkout <name>`
-   `git merge <revision>`: merges into current branch
-   `git mergetool`: use a fancy tool to help resolve merge conflicts
-   `git rebase`: rebase set of patches onto a new base

## Remotes

-   `git remote`: list remotes
-   `git remote add <name> <url>`: add a remote
-   `git push <remote> <local branch>:<remote branch>`: send objects to remote, and update remote reference
-   `git branch --set-upstream-to=<remote>/<remote branch>`: set up correspondence between local and remote branch
-   `git fetch`: retrieve objects/references from a remote
-   `git pull`: same as `git fetch; git merge`
-   `git clone`: download repository from remote

## Undo

-   `git commit --amend`: edit a commit’s contents/message
-   `git reset HEAD <file>`: unstage a file
-   `git checkout -- <file>`: discard changes

# Advanced Git

-   `git config`: Git is [highly customizable](https://git-scm.com/docs/git-config)
-   `git clone --depth=1`: shallow clone, without entire version history
-   `git add -p`: interactive staging
-   `git rebase -i`: interactive rebasing
-   `git blame`: show who last edited which line
-   `git stash`: temporarily remove modifications to working directory
-   `git bisect`: binary search history (e.g. for regressions)
-   `.gitignore`: [specify](https://git-scm.com/docs/gitignore) intentionally untracked files to ignore