## Git vs GitHub:
   - Git: version control system that keeps track of your source code
   - GitHub: hosting service that manages Git repositories
## Things we will go over:
   - Fork a repo
   - Clone a repo
   - Branches
   - ADD, COMMIT, PUSH, PULL
   - Merge
   - Rebase
 
 ## Clone a repo
 
![](/images/cloneRepo.png)
   - Copy the git repo address
   - Use the command: git clone *git_repo*
 ## Local repo vs remote repo
   -  Local repo: git repo on your computer
   -  Remote repo: repo hosted on cloud server
   -  Goal of learning git: make sure that your local repo and remote repo in sync with each other
 ## Branches
  
## Basic Git Commands
### **The Best Git Command to Exist**
- ```git status``` : When in doubt use this command, will give you hints on what you should do next.

### **Github Branches**

- ```git branch``` : Checks what branch you are on and the history of branches you have checked out in the past. The main branch is by default named master. 

*For Dev Team Members: The roote branch for Core-V4 is dev, NEVER EVER WORK ON THIS BRANCH!!!*

- ``` git checkout -b <branch> ``` Creates new branch.

- ``` git checkout <branch> ``` Allows you to work on this branch

- ``` git fetch origin <branch>``` Updates branch of all recent commits. 


### **ADD, COMMIT, PUSH, PULL**
**Step 1** Adding Your Changes

- ```git add .``` : Stages all your files for commit

- ``` git add <file>``` Stages a particular file for commit


![](/images/gitAdd.png)

**Step 2** Commiting Your Changes

- ```git commit -m 'message'``` : Commiting your changes with a specific message.

- ``` git commit --amend --no-edit``` Commiting changes without changing your previous commit message.

*In the case that you enter VIM while trying to commit:*
- MAC USERS: press esc follwed by :wq

**Step 3** Pushing Your Changes

- ```git push origin <branch>'``` : Pushes the changes you made on your branch. 

- ``` git push --force origin <branch>``` Force pushes the changes.
- ``` git pull origin <branch>``` Pulls the changes you just made. 

*Once your branch has been merged into the repository, make sure to start a new project with  NEW BRANCH!*

### **Resetting Branch to Github Branch**

- ``` git pull origin <branch>``` Pulls the changes you just made. 
- ``` git reset --hard origin/<branch>``` Resets branch to what was last committed to Github.  

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
