># Github Basics Workshop

## Things we will go over:
-  Making a Repo
- Cloning a Repo
-  Basic Git Commands
- For DEV Team Members Only (Dev- Specific Commands)

## Making a Repo
**STEP 1** 
![](/images/RepoCreate.png)
Click on the New button on the left-hand side

**STEP 2**
![](/images/createNew.png)
Fill in desired info! And your repo has been created! 

## Cloning a Repo
**STEP 1** 
![](/images/cloneRepo.png)
Click on the code button and copy the link. Once the link is copied, go to the terminal of your choice and cd into the directory in which you wish to clone your repo. 


**STEP 2**
In your terminal type in the following command:

``` git clone https://github.com/seemavora/githubWorkshop.git ```   
Replace the link with the link you copied in Step 1. (For this workshop simply copy paste this command.) 

## Basic Git Commands
### **The Best Git Command to Exist**
```git status``` : When in doubt use this command, will give you hints on what you should do next.

### **Pushing To Github**
**Step 1** Adding Your Changes

```git add .``` : Stages all your files for commit

``` git add <file>``` Stages a particular file for commit


![](/images/gitAdd.png)

**Step 2** Commiting Your Changes

```git commit -m 'message'``` : Commiting your changes with a specific message.

``` git commit --amend --no-edit``` Commiting changes without changing your previous commit message.

*In the case that you enter VIM while trying to commit:*
- MAC USERS: press esc follwed by :wq

**Step 3** Pushing Your Changes

```git push origin <branch>'``` : Pushes the changes you made on your branch. 

``` git push --force origin <branch>``` Force pushes the changes.


*In the case that you enter VIM while trying to commit:*
- MAC USERS: press esc follwed by :wq








