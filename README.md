# First-Time

Practice using git for the first time!

## **Step 1**: Cloning and saving commits locally

Cloned repository to local machine/windows desktop.
Saving these changes locally.
-git clone url of repository on Github

## **Step 2**: Saving new files made locally into git

Created new file index.html.

Used git add to track the file(s) made locally and to track files that have been modified.
-git add fileName or git add . or git add *.extension

Used git commit to save the changes.
-git commit alone directs you to another page to write the messages, to exit do 'esc :wq'
-git commit -m "" -m "" allows you to do a commit and create the decriptions for each commit; the first message is the general message while the second one is for the more in depth description
-git commit -am to add and commit at the same time, only works for modifed files

## **Step 3**: Moving updates from local machine into a remote repository in Github

Used git push to move changes in local machine to repository in Github.

## **Step 4**: Adding branches to make edits separate from master/main working project

Used git branch to note which branch/es are in the repository.
-git branch will show the user the branches, the one that is highlighted and starred is the branch the user is currently in

Used git checkout to change to another branch in the repository.
-git checkout -b branchName to create a new branch and move into the new branch
-git checkout branchName to move into another exiting branch
-note: before switching to another branch, commit the changes done so far in the current branch

## **Step 5.1**: Merging branches into master

Used git merge to merge a branch to master or merge a branch to the branch it was created from.
-git merge branchName
-use this command while you are in the chosen branch that you want to merge into
    -if branch1 wants to merge into master, use git merge while in master (git merge branch1)
    -if you want to merge master into branch1, do git merge master while in branch1 

### **5.1 a)** Merge Conflicts

If there is a merge conflict, git will notify you and ask you which changes you want to keep and/or delete. You can modify this within VS code.

## **Step 5.2**: Pushing local repository into remote repository on Github and creating a PR to merge into master

Used git push to move changes in local repo to remote repo, then make a pull request.

What is a pull request?
-it is a request/extra step to allow other developers to check on the change before merging the branch into master

If it is a new branch created locally, need to create an upstream branch in the remote repository before pushing.
-git push --set-upstream origin branchName
-shorthand of --set-upstream is -u

## Optional stuff: 

.gitignore file is used to ignore certain files and folders and not save them into remote repository
-when a file written in the .gitignore file, doing git add . will add all the modified and newly created files but will not stage the files that are written in the .gitignore file

### Undoing a git command:

Used to undo a commit or a unstage the change.
-git reset fileName or git reset (unstage changes)
-git reset HEAD~# (undo a commit; # means you can undo back a certain number of recent commits)
    -git reset HEAD~1 will undo the last two changes (undos commit and staging as an example)
-git reset commitHash (from log)
    -will undo everything past this commit, unsaves changes after commitHash
-git reset --hard commitHash
    -will unsave and unstage the changes past this commit AND delete it

### branches ID (if you accidentally delete a branch):
use git reflog and locate the branch; ID number is the first set of numbers/letters next to the commit comments (this is why comments are soo important)
-git reflog to compare current HEAD to previous HEADs
-git log to see detailed commits
-when doing git reflog or git log, type in 'q' to exit out of the log
**note: do not use git branch -D
-if you do somehow use -D, get the branch back by going git checkout -b branchName lastBranchID