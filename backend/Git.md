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

