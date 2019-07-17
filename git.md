# *Git cheatsheet*

**Note** : It is taken for granted that all of this commands will always start
by `git ...`

**Note** : All elements within `{...}` are always command variables

**Note** : All elements within `[---(Explanation)]` are always command modifiers

## Getting Started 

#### Init

`git init` : Starts a new **local** repository

#### Clone

`git clone {URL}` : Takes a remote repository and clones it into a local copy

## Local changes management 

#### Status
`git status` : Shows what changed in the local branch since the last commit 

#### Log

`git log`: Shows the localy tracked commit history
    * `[--oneline (less information) ]`
    * `[--graph (ASCII commit/branch representation) ]`
    * `[-p {file} (Commit log of a single file) ]`

#### Blame
`git blame [-p {file} ]` : Shows who changed a file over different commits 

#### Add

`git add ...` : Adds 1 or more files to staging area

#### Commit 

`git commit [-m (to add message)] {Commit message}` : Commits all changes to 
tracked local files

#### Stash

`git stash`: Add changes to stash so is again posible to move between branches 

`git stash list`: Shows a list of all stashed versions 

`git stash apply stash@{n}`: Apply given stash version 

## Branching

#### List
`git brach` : Lists all local branches
    * `[ -d {branchName} ]` : To delete a local branch

#### Checkout
`git checkout [-b (to create a move to branch)] {branchName}`: Moves to another
branch

#### Track

`git checkout [--track ] {remote brach like origin/something}` : Tracks a remote 
branch

## Interacting with remote

#### Download changes

`git pull {branch}` : Downloads changes into the HEAD

`git fetch {branch}` : Downloads changes without adding int to the HEAD

#### Pushing changes :

`git push {branch}` : Pushes all new local commits into remote 

#### Merging

`git merge {brach to be merged}` : Merges a branch into current HEAD

## Undo

#### Reset

`git reset --hard`: Reset all local changes and sets HEAD to last commit 

`git reset --hard {commit}`: Reset all local changes and sets HEAD to given commit 

`git checkout -- {file}`: Reset given file to the HEAD version 

`git revert {commit}`: Creates a new commit with the contrary changes from the 
last commit




