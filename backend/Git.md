# Git

## Git Flow
There are three main components of a Git project:

- __Working tree__: or working directory, consists of files that you are currently working on. 
- __Index__: staging area, is where commits are prepared. When you make a change in the working tree, the index marks the file as modified before it is committed.
- __Repository__: or repo, is the “container” that tracks the changes to your project files. It holds all the commits—a snapshot of all your files at a point in time—that have been made.

    ![](img/git_workflow_001.png)

## Three states of git file

- __Modified__: You have changed the file but have not committed it.
- __Staged__: You have marked a modified file in its current version to go into your next commit snapshot. Using command ```git add ```
- __Committed__: the data is safely stored in your local database.

    ![](img/git_workflow_002.png)

## Questions

1. What is the difference between git pull and git fetch?

    - ```git fetch``` only downloads new data from a remote repository, but it doesn’t integrate any of the downloaded data into your working files.
    - ```git pull``` downloads as well as merges the data from a remote repository into your local working files. It may also lead to merge conflicts if your local changes are not yet committed.


2. What is a conflict in git and how can it be resolved?
    - A conflict arises when more than one commit that has to be merged has some change in the same place or same line of code. Git will not be able to predict which change should take precedence. This is a git conflict.
    - To resolve the conflict in git, edit the files to fix the conflicting changes and then add the resolved files by running git add. After that, to commit the repaired merge, run git commit. Git remembers that you are in the middle of a merge, so it sets the parents of the commit correctly.

3. What is the difference between the ‘git diff ’and ‘git status’?
    - ```git diff``` is similar to```git status```.
    - ```git diff``` shows the more detail differences between various commits, and also between the working directory and index.

4. What is the function of ```git reset```?
    - ```git reset``` is to reset your index as well as the working directory to the state of a specific commit.