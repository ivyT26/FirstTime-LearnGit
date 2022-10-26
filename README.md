# First-Time

Practice using git for the first time!

## **Step 1**: Cloning repo or creating local repo

Clone repository to local machine/windows desktop.  
- git clone url of repository on Github  

Create a local repository.  
- git init  

## **Step 2**: Saving new files made locally into git

Created new file index.html.

Used git add to track the file(s) made locally and to track files that have been modified.  
- git add fileName or git add . or git add *.extension

Used git commit to save the changes.
- git commit alone directs you to another page to write the messages, to exit do 'esc :wq'  
- git commit -m "" -m "" allows you to do a commit and create the decriptions for each commit; the first message is the general message while the second one is for the more in depth description  
- git commit -am to add and commit at the same time, only works for modifed files

Saving all files of different statuses, whether it is a new file, a modified file, or a deleted file.
- git add --all
*Note: git add --all will ignore files delared in the .gitignore file.

## **Step 3.1**: Moving updates from local machine into a remote repository in Github

Used git push to move changes in local machine to repository in Github.  
- git push origin <branch_name>, where branch_name is the name of the existing branch in the remote repo you want to push your local branch

Push local branch into a new branch in your remote repo
- git push origin <local_branch>:<remote_name>   

If repository was created locally and there is no remote repository, need to create an empty remote repository on Github.  
Next, copy the link from when you would clone the repository. (link ends with .git)  
Then create a reference to the remote repository.  
- git remote add origin link  

## **Step 3.2**: Moving updates from remote repository online (like Github) into a local repository and updating it

Used git pull to move changes in remote repository on Github to local machine's repository.  
git pull is a combined command of git fetch and git merge.  
- git pull  

git fetch is the 'safer' option of git pull because it only downloads the contents from remote repo into local repo without merging it into the local repo.  
To access the fetched content, need to use git checkout to visit the branch. (will be in the form of something like remote-repo/branchName)  
- git fetch origin <branch_name>, where 'origin' is usually the remote repo if you only have 1

## **Step 4.1**: Adding branches to make edits separate from master/main working project

Used git branch to note which branch/es are in the repository.
- git branch will show the user the local branches, the one that is highlighted and starred is the branch the user is currently in
- git branch -a displays all local and remote branches
- git branch -r displays all remote branches
- git show-branch displays the branches and the commits made to each local branch (use -a and -r for the same reasons in last 2 bullet points)

Used git checkout to change to another branch in the repository.
- git checkout -b branchName to create a new branch and move into the new branch  
- git checkout branchName to move into another exiting branch  
- note: before switching to another branch, commit the changes done so far in the current branch

Delete branch
- git branch -d <branch_name>

## **Step 4.2**: Checking differences between branches or files and statuses of branches or files

Used git diff
- git diff branch1..branch2 for comparing two different branches
- git diff branch1 branch2 ./file for comparing two files from two different branches
- git diff shows any uncommited changes since last commit

Used git status to check current state of repo
- git status

Used git log displays history of commits
- use this website to learn more about how to filter the logs: https://www.atlassian.com/git/tutorials/git-log

## **Step 5.1**: Merging branches into master

Used git merge to merge a branch to master or merge a branch to the branch it was created from.  
- git merge branchName
- use this command while you are in the chosen branch that you want to merge into  
	- if branch1 wants to merge into master, use git merge while in master (git merge branch1)  
	- if you want to merge master into branch1, do git merge master while in branch1 

### **5.1 a)** Merge Conflicts

If there is a merge conflict, git will notify you and ask you which changes you want to keep and/or delete. You can modify this within VS code.

## **Step 5.2**: Pushing local repository into remote repository on Github and creating a PR to merge into master

Used git push to move changes in local repo to remote repo, then make a pull request.

What is a pull request?
- it is a request/extra step to allow other developers to check on the change before merging the branch into master

If it is a new branch created locally, need to create an upstream branch in the remote repository before pushing.
- git push --set-upstream origin branchName
- shorthand of --set-upstream is -u

## Optional stuff: 

.gitignore file is used to ignore certain files and folders and not save them into remote repository
- when a file written in the .gitignore file, doing *git add .* will add all the modified and newly created files but will not stage the files that are written in the .gitignore file

### Undoing a git command:

Used to undo a commit or a unstage the change.
- git reset fileName or git reset (unstage changes)
- git reset HEAD~# (undo a commit; # means you can undo back a certain number of recent commits)
    - git reset HEAD~1 will undo the last two changes (undos commit and staging as an example)
- git reset commitHash (from log)
    - will undo everything past this commit, unsaves changes after commitHash
- git reset --hard commitHash
    - will unsave and unstage the changes past this commit AND delete it

### branches ID (if you accidentally delete a branch):
use git reflog and locate the branch; ID number is the first set of numbers/letters next to the commit comments (this is why comments are soo important)
- git reflog to compare current HEAD to previous HEADs
- git log to see detailed commits
- when doing git reflog or git log, type in 'q' to exit out of the log  
**note: do not use git branch -D  
- if you do somehow use -D, get the branch back by going git checkout -b branchName lastBranchID
