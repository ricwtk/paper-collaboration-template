# Git workflow for collaborative writing
Adapted from [A Git workflow for writing papers in Latex](https://rvprasad.medium.com/a-git-workflow-for-writing-papers-in-latex-4cfb31be4b06).

## Preparing the document
1. Split the document into different files. Use *main.tex* to combine the files into one document.
2. Create a branch for each collaborator.
   
    `git branch name-of-branch`

## Preparing local machine
1. Clone the repository.
   
    `git clone repository-name`

## Editing 
1. Get latest changes from the server.
   
    `git pull`

2. Switch to your branch (if you are not in your branch) before editing.

    `git checkout name-of-branch`

3. Edit the document and commit the changes to the branch.

    `git add changed-files` - add changes for commit

    `git add -A` - add all files that have been changed

    `git commit -m "message"` - commit changes that have been added with `git add`

    `git commit -a -m "message"` - commit all changes in the currently tracked files

4. Push the changes of the branch to server.

    `git push origin name-of-branch`

5. When you have completed the changes of a section, merge to the master branch by
   1. check out the master branch: `git checkout master`
   2. pull the latest changes from the server: `git pull`
   3. merge your branch into master branch: `git merge name-of-branch`
   4. resolve conflicts if any
   5. push changes to the server: `git push`

6. Then merge the changes from master branch into your branch,
   1. [skip this if you have just done the previous step] check out the master branch: `git checkout master`
   2. [skip this if you have just done the previous step] pull the latest changes from the server: `git pull`
   3. checkout your branch: `git checkout name-of-branch`
   4. merge the master branch into your branch: `git merge master`
   5. resolve conflicts if any
   6. push changes to the server: `git push`

## Additional recommendation
1. Write each sentence on a separte line - for easier change tracking.

## GUI clients
Refer to https://git-scm.com/downloads/guis/

Visual Studio Code extension for GIT: https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph
