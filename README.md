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

## **Step 3**: Moving updates from local machine into a remote repository in Github

Used git push to move changes in local machine to repository in Github.

## **Step 4**: Adding branches to make edits separate from master/main working project

Used git branch to note which branch/es are in the repository.
-git branch will show the user the branches, the one that is highlighted and starred is the branch the user is currently in

Used git checkout to change to another branch in the repository.
-git checkout -b branchName to create a new branch and move into the new branch
-git checkout branchName to move into another exiting branch

### Optional stuff: 

.gitignore file is used to ignore certain files and folders and not save them into remote repository
-when a file written in the .gitignore file, doing git add . will add all the modified and newly created files but will not stage the files that are written in the .gitignore file