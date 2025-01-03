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

Command for checking lists for files that are present in **Staging Area**:

    git ls-files

![git-ls-files-command](https://github.com/user-attachments/assets/564ac0b8-ed3e-4162-9f17-0c643290b945)

**When we add file is staging area it means that file is tracked, when any change happen in that file we see by using git status command:**

    git status

![git-status-for-check-staging](https://github.com/user-attachments/assets/6981e6a2-7435-472c-a229-838d116cf579)

## git commit command:
git commit command is use for taking snapshot/backup of specific file with message.

    git commit <File_Name> -m "This is commit message"

![image](https://github.com/user-attachments/assets/aeef8adb-bad3-4c81-9087-3de5060dbe58)

## Git commit ID:
Whenever we commit file that file give commit Id 

**git show command show latest commit & all changes in files during commit.& here HEAD means latest commit.** 

    git show

![Git-show-command](https://github.com/user-attachments/assets/9d193379-fa9a-4fdd-a490-3d502742296a)

**git log command show all the commits with commit Id's & commit message also show. HEAD: We can commit multiple times So, that file has multiple versions/commit ID but, Git automatically give latest commited 
file nickname as "HEAD-Master"**

    git log 

![image](https://github.com/user-attachments/assets/bed83304-696b-4576-8fc7-ea3592624177)

**git log --oneline command show short info of commit ID's.**

    git log --oneline

![image](https://github.com/user-attachments/assets/3559e8ad-7ad8-40ff-ae75-504190ca2619)

## How to remove or restore a file from Staging Area to Working Area:
This command is used to remove the staged file & stop tracking on that file.

    git restore --staged <File_Name>

![git-restore-staged-cmd](https://github.com/user-attachments/assets/fc37b81a-0056-4bb4-a46c-037e920c32a3)

We want remove file from staging area use command:

    git rm --cached <File_Name> 

![git-rm-cached-cmd](https://github.com/user-attachments/assets/c629ad3a-cbc1-4f8c-b171-bc1b3e68dbfc)


## git diff command:
This command use to check the two versions/commit id's difference.

    git diff <commit_id>  <commit_id>

![git-diff-cmd](https://github.com/user-attachments/assets/3570c00c-ca64-4e8d-a3f8-94e698d5b08d)


## Set Git Config global file:
In real Industry on a single project different uses works, So we set "config" settings for our laptop as Auther name & Email. This info shown in commit history.

**Set user name for git:**

    git config --global user.name "PratikShinde"

![git-config-set](https://github.com/user-attachments/assets/121feb0a-3e82-4335-8fc9-50c6f67a9e02)

**Set user email for git:**

    git config --global user.email "pratikshinde@abc.com"

![git-useremail](https://github.com/user-attachments/assets/f1b53eff-a5de-49e6-9938-c7bb8d27fb5a)


**Show all set on configs file:**

    git config --global -l

![Git-config-global-show](https://github.com/user-attachments/assets/02b89a0a-1490-4685-b4ad-def1a722453d)

**Also we can save login information of GitHub Account:**

Set user.email means our GitHub account email id:
  
    git config --global user.email "______"  

Set user.name means our GitHub account password:

    git config --global user.name "______"  


## Alias: [Nickname for Git command]
Git Alias is use to give nickname to any Git command, That Nickname only save in Local laptop,This is only for Local laptop settings.

    git config --global alias.pns "log --oneline"

![Git-Alias-cmd](https://github.com/user-attachments/assets/b8edb55f-abe7-461e-b23e-c063284fa6d0)


## .gitignore file:
For some project also need other files only commit need means not need for taking versions/commit id of that files.

That file only need to push to GitHub(SCM) as it is not need of taking any commit id. So that other files we can put in .gitignore file.

    vim .gitignore 

![gitihnore-cmd](https://github.com/user-attachments/assets/56e687e5-c692-4286-96db-4b163ca699df)

Now all remaining files i put in the .gitignore file
![cat-for-.gitignore-cmd](https://github.com/user-attachments/assets/6939f5ff-6851-44f0-876c-3e0849337616)

**Now add .gitignore file in staging area:**

    git add .gitignore

![gitignore-file-add](https://github.com/user-attachments/assets/1f243fde-e860-4a34-9952-a768125289ca)

**Now commit .gitignorefile**

     git commit .gitignore -m "gitignore file is commited"

![commit-gitignore-file](https://github.com/user-attachments/assets/175b9d95-f92a-42d9-bad3-fed6e93df5e9)

All remaing files are present in working area but that are commited through .gitignore file, So now our workspace is very Clean.

![git-status-cmd](https://github.com/user-attachments/assets/991c15ea-5899-4097-bcd2-085fc567ff36)


## Git Command for multiple files add & commit:

**To add all files in working area to Staging area then use command:(. means current location)**

     git add .

![Git-add-all](https://github.com/user-attachments/assets/bb338d6c-0f7a-49d2-a5dd-ad36c199a35b)

**To commit all files in "Staging Area" use command:**

     git commit . -m "all files are commited"

![Git-commit-all](https://github.com/user-attachments/assets/d90bc06c-719a-4295-8e31-7cf2f2c49ff4)

**To Remove/delete all files from commit, Staging area, working area use command:**

     git rm -r .

![git-rm-r-all-cmd](https://github.com/user-attachments/assets/867dfe8d-6346-4550-9036-77c471c749d0)
     


## Git Branch:
The Branch also known as timeline.

There are two braches in Git & GitHub:
1. Master/Main Branch
2. Feature Branch

Main/Master Branch which is connected to production/QA env for deployment.

Feature Branch which developer update code/build code/test code & also updating version of code.

**git branch is command for show all lists of branches:**

     git branch

![Git-Branch-list](https://github.com/user-attachments/assets/e59b0038-3105-4ad9-b3fd-eddbc48b12ad)

**Create Feature branch in Git:**

     git branch <Branch_Name>

![Git-Branch-create](https://github.com/user-attachments/assets/dd628276-ba85-44c5-abce-e277263c498e)

**Switch to other Branch in Git use this command:**

     git checkout <Branch_Name>

![Git-Checkout-cmd](https://github.com/user-attachments/assets/7e5ca740-bc58-456a-a4ee-17bdf597ba1b)

- When we create a Feature Branch then all data/commit id's in Master Branch come to Feature branch:

![image](https://github.com/user-attachments/assets/46fc1776-c139-4c56-a716-bba47b413c2d)

     
