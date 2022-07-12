# Git Commands Tutorial**

## Init new reposit

This command is used to start a new repository.

> git init

## Adding repository

This command adds one or more to the staging area.

> git add [file name]

## Commit

This command commits any files you’ve added with the git add command and also commits any files you’ve changed since then.

> git commit -a

## Differences 
This command shows the file differences which are not yet staged.

>git diff

## Git status
This command lists all the files that have to be committed.

>git status

## Log
This command is used to list the version history for the current branch.
>git log

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