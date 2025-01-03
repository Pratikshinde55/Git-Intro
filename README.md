# Information of Git the Version Control tool:

Snapshot = BackUp

- Note:
  Git commit always read data from "Staging Area" not from Working Area.

There three types of Areas in Git:
1. Working Area/Workspace
2. Staging Area/ Tracking Area
3. Commit Area

In Workspace 1st we need to Initialize Repository(git init) means directory, & then we "add"(Staging Area) any file that we want to commit. Without Initialize repo & without add file we unable to commit.

## Initialize Repository: [git init command]
This command for initialize repo

    git init

To check Status of update we use git status command

    git status

## Adding file to Staging Area: [git add command]
git add command is command used to add file in "Staging Area" & that file is tracking

    git add <File_Name>

Command for checking lists for files that are present in Staging Area:

    git ls-files

## git commit command:
git commit command is used for taking snapshot/backup of specific file with message.

    git commit <File_Name> -m "This is commit message"

## Git commit ID:
Whenever we commit file that file give commit Id 

   git show

   git log 

   git log --oneline
