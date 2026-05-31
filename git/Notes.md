# Setting Names and Emails 

git config user.name
git config --global user.name "<User Name>"

git config --global user.email "<email id>"

# Basic of git 

|Command|Comment|
|:------|:------|
|git log|Check git history Logs| 

git status 
git init 


# Staging Changes with git add

Working Directory --> git add --> Staging Area --> git commit --> Repository 

## Commands 

git add <file/Directory>
git rm --cached <file/Directory> --> To unstaged the file/Directory 
git commit -m <Comment for commiting the message>

## git Documents 

https://git-scm.com/docs

## Atomic Commits 

Add files on commit which are changed instead of committing eveything. 

### Use vs code instead of default vim editor during commits 
Configure VS code or any other code instead of default git editor in git 

git config --global core.editor "code --wait"

or 

git config --global core.editor "vim"

## Git Logs 
git log
git log --oneline 

## Ammending Commits 
git commit -m "Comment Message"
git add <forgotten file>
git commit --amend

## Ignoring files 
Create a file .gitignore and add content in it 

1. .DS_STORE --> Give exact file name 
2. foldername/ --> Give folder name 
3. *.log --> Ignore files with the .log extension

# Working with branchaes 

Master is the primary branch in git. 

(HEAD -> master) --> Head is the pointer refers to current location in your repository. 

## Working and switching in branches  

git branch 
git branch <branch Name> 
git switch <branch name> ** Switch to already created branch **
git switch -c <branch name> ** Create and switch to newely created branch ** 
git checkout <branch Name> ** Old way of switching branches. It will do many things - switch branches, restore files, checkout commits **
git branch -D <branch name> ** Delete Branch **
git branch -m <new branch name> # Rename current branch to new name 

# Merging in git 

Merging is about to merging multiple branches into one or master. 

git merge <Branch Name> # It will merge content of branch name into existing branch

** Below message would be happen if merge will conflicts appear ** 

<<<<<<< HEAD
test merge  
=======
git merge <Branch Name> # It will merge content of branch name into existing branch 
 
>>>>>>> merging

# Comparing changes with git diff

git diff
git diff HEAD 
git diff --staged [file name]
git diff --cached [file name]
git diff [branch name]

# The ins and Out of stashing 

git stash --> Temporarly save uncommited changes 
git stash pop -->  Restoring the saved changes  
git stash list --> List stashed 
git stash apply --> Restore without removing 
git stash push -m [Messages]
git stash --include-untracked 
git stash clear 
