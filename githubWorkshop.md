## Git vs GitHub:
   - Git: version control system that keeps track of your source code
   - Can be executed through CLI
   - GitHub: hosting service that manages Git repositories
   - There are many hosting services such as GitHub, Bitbucket, internal services at many companies
   - But they all support Git
## Things we will go over:
   - Fork a repo
   - Clone a repo
   - Branches
   - ADD, COMMIT, PUSH, PULL
   - Merge
   - Rebase
   - Some tips
 
 ## Clone a repo
 
![](/images/cloneRepo.png)
   - Copy the git repo address
   - Use the command: git clone *git_repo*. This will make a copy of a repo to your local machine
 ## Local repo vs remote repo
   -  Local repo: git repo on your local machine
   -  Remote repo: repo hosted on cloud server
   -  One of the goal of learning git: make sure that your local repo and remote repo in sync with each other
   -  Also to collaborate with others
## Basic Git Commands
### **The Best Git Command to Exist**
- ```git status``` : When in doubt use this command, will give you hints on what you should do next.

### **Github Branches**

- ```git branch``` : Checks what branch you are on and the history of branches you have checked out in the past. The main branch is by default named master.

*For Dev Team Members: The root branch for Core-V4 is dev, NEVER EVER WORK ON THIS BRANCH!!!*


- ``` git checkout -b <branch> ``` Creates new branch.

- ``` git checkout <branch> ``` Switch to that branch, it exists, allows you to work on this branch

- ``` git fetch origin <branch>``` Updates branch of all recent commits. 


### **ADD, COMMIT, PUSH, PULL**
**Step 1** Adding Your Changes

- ``` git add [file] ```: Add files to commit
- ```git add .``` : Stages all your files for commit

![](/images/gitAdd.png)

**Step 2** Commiting Your Changes

- ```git commit -m 'message'``` : Commiting your changes with a specific message.

- ``` git commit --amend --no-edit``` Commiting changes without changing your previous commit message.

*In the case that you enter VIM while trying to commit:*
- MAC USERS: press esc follwed by :wq

**Step 3** Pushing Your Changes

- ```git push origin <branch>'``` : Pushes the changes you made on your branch. 

- ``` git push --force origin <branch>``` Force pushes the changes.
- ``` git push origin <branch>``` Pulls the changes you just made. 
- ``` git push origin ``` Push everything to the online repo

*Once your branch has been merged into the main repository, make sure to start a new project with  NEW BRANCH!*

** Update your local repo
- ``` git pull ``` Will pull everything from online repo to your local one
Should do this if you need to rebase or switch to another branch by your friends
### **Resetting Branch to Github Branch**

- ``` git pull origin <branch>``` Pulls the changes you just made. 
- ``` git reset --hard origin/<branch>``` Resets branch to what was last committed to Github.  
### 

### Merge
- Once you push code, you should be able to merge into the default branch if you are the owner

### Git rebase
- We use git rebase when master repo has new changes that your branch doesn't have => hard to merge once you push your branch
- Git rebase to get new updates from master repo while still working on your branch
- git checkout master
- git pull origin master
- git checkout *rebase_branch*
- git rebase master
- git push origin *rebase_branch* --force
- We need to checkout and pull master in order to have the lastest changes of these repo and rebase master will use local master repo.

### Some tips
- Commit whenever you feels like you've done something substantial
- Whenever there's bugs that you cannot find out, git stash to revert to the nearest commit
- Or you vscode to revert those changes