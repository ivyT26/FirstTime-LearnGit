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

## **Step 5.1**: Merging branches into master

Used git merge to merge a branch to master or merge a branch to the branch it was created from.
-git merge branchName
-use this command while you are in the chosen branch that you want to merge into
    -if branch1 wants to merge into master, use git merge while in master (git merge branch1)

## **Step 5.2**: Pushing local repository into remote repository on Github and creating a PR to merge into master

Used git push to move changes in local repo to remote repo, then make a pull request.

What is a pull request?
-it is a request/extra step to allow other developers to check on the change before merging the branch into master

If it is a new branch created locally, need to create an upstream branch in the remote repository before pushing.
-git push --set-upstream origin branchName
-shorthand of --set-upstream is -u

### Optional stuff: 

.gitignore file is used to ignore certain files and folders and not save them into remote repository
-when a file written in the .gitignore file, doing git add . will add all the modified and newly created files but will not stage the files that are written in the .gitignore file