# Information of Git the Version Control tool:

Snapshot = BackUp

- Note:
  Git commit always read data from "Staging Area" not from Working Area.

There three types of Areas in Git:
1. Working Area/Workspace
2. Staging Area/ Tracking Area
3. Commit Area

![workspace-show](https://github.com/user-attachments/assets/c39ffb55-8d81-4b0e-806c-1cc3c6503778)

In Workspace 1st we need to Initialize Repository(git init) means directory, & then we "add"(Staging Area) any file that we want to commit. Without Initialize repo & without add file we unable to commit.

## Initialize Repository: [git init command]
This command for initialize repo

    git init
    
![git-init-command](https://github.com/user-attachments/assets/6fbc6e9b-66b7-41c5-ba14-2475c33f8321)

To check Status of update we use git status command

    git status

## Adding file to Staging Area: [git add command]
git add command is command used to add file in "Staging Area" & that file is tracking

    git add <File_Name>

![git-add-command](https://github.com/user-attachments/assets/c432c50d-5a35-47da-b1b6-c2cf6e784d1c)

Command for checking lists for files that are present in Staging Area:

    git ls-files

![git-ls-files-command](https://github.com/user-attachments/assets/564ac0b8-ed3e-4162-9f17-0c643290b945)

- When we add file is staging area it means that file is tracked, when any change happen in that file we see by using git status command

       git status

![git-status-for-tracking-show](https://github.com/user-attachments/assets/0a97fd2e-17c3-40f0-828c-a2566e26f8f5)


## git commit command:
git commit command is used for taking snapshot/backup of specific file with message.

    git commit <File_Name> -m "This is commit message"


## Git commit ID:
Whenever we commit file that file give commit Id 

   git show

   git log 

   git log --oneline
