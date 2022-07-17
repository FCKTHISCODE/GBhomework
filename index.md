# **Introduction** 
## Why a Version Control System like Git is needed
Real life projects generally have multiple developers working in parallel. So a version control system like Git is needed to ensure there are no code conflicts between the developers.
Additionally, the requirements in such projects change often. So a version control system allows developers to revert and go back to an older version of the code.
Finally, sometimes several projects which are being run in parallel involve the same codebase. In such a case, the concept of branching in Git is very important.

# Git Commands Tutorial

## Start new repository

This command is used to start a new repository.

> git init

## Adding repository

This command adds one or more to the staging area.

> git add [file name]

## Commit

If you need to make any further adjustments, do so now, and then add any newly modified content to the index. Finally, commit your changes with:

>git commit

This will again prompt you for a message describing the change, and then record a new version of the project.
Alternatively, instead of running git add beforehand, you can use

>git commit -a

Which will automatically notice any modified (but not new) files, add them to the index, and commit, all in one step.

## Differences 
This command shows the file differences which are not yet staged.

>git diff

## Git status
This command lists all the files that have to be committed.

>git status

## Viewing project history

At any point you can view the history of your changes using

>git log

If you also want to see complete diffs at each step, use

>git log -p

Often the overview of the change is useful to get a feel of each step

>git log --stat --summary

## Understanding history: History diagrams
We will sometimes represent Git history using diagrams like the one below. Commits are shown as "o", and the links between them with lines drawn with - / and \. Time goes left to right:

         o--o--o <-- Branch A
        /
 o--o--o <-- master
        \
         o--o--o <-- Branch B

If we need to talk about a particular commit, the character "o" may be replaced with another letter or number.

## Understanding history: What is a branch?

When we need to be precise, we will use the word "branch" to mean a line of development, and "branch head" (or just "head") to mean a reference to the most recent commit on a branch. In the example above, the branch head named "A" is a pointer to one particular commit, but we refer to the line of three commits leading up to that point as all being part of "branch A".

## Git push

Create Changes
To create new changes for review, simply push to the project’s magical refs/for/'branch' ref using any Git client tool:

>git push ssh://sshusername@hostname:29418/projectname HEAD:refs/for/branch

E.g. john.doe can use git push to upload new changes for the experimental branch of project kernel/common, hosted at the git.example.com Gerrit server:

>git push ssh://john.doe@git.example.com:29418/kernel/common HEAD:refs/for/experimental

Each new commit uploaded by the git push client will be converted into a change record on the server. The remote ref refs/for/experimental is not actually created by Gerrit, even though the client’s status messages may say otherwise.

Other users (e.g. project owners) who have configured Gerrit to notify them of new changes will be automatically sent an email message when the push is completed.