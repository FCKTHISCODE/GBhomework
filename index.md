# **Git Tutorial**

###### Git is a DevOps tool used for source code management. It is a free and open-source version control system used to handle small to very large projects efficiently. Git is used to tracking changes in the source code, enabling multiple developers to work together on non-linear development.

## Start new repository

This command is used to start a new repository.

> git init

## Add repository

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

