### **Part 1: Git Basics**

#### **Task 1: Install and Configure Git**
1. Install Git from [git-scm.com](https://git-scm.com/).  
2. Configure your global Git settings:  
   ```bash
   git config --global user.email "your-email@example.com"
   ```
   -> configration username and email globally

3. Verify the configuration:  
   ```bash
   git config --list
   ```
   -> display all configration list

#### **Task 2: Initialize a Repository**
1. Create a directory and initialize it as a Git repository:  
   ```bash
   mkdir MyProject
   cd MyProject
   git init
   ```
   -> crate a folder and navigate into the folder and intialize git in local

   - **Purpose**: Initializes a `.git` folder to track changes.

---

### **Part 2: Basic Workflow**

#### **Task 3: Creating and Committing Files**
1. Create a file:  
   ```bash
   echo "Hello Git" > file1.txt
   ```
   -> create a text file with some text 

2. Stage and commit the file:  
   ```bash
   git add file1.txt
   git commit -m "Initial commit: Added file1.txt"
   ```
   -> add file to stageing area and record the changes on the file

#### **Task 4: Viewing Changes**
1. Modify the file:  
   ```bash
   echo "Git is awesome!" >> file1.txt
   ```
   -> modify or change the file 


2. Check file status and differences:  
   ```bash
   git status
   git diff
   ```
   -> display all track or untrack file and display the changes

#### **Task 5: Undoing Changes**
1. Unstage a staged file:  
   ```bash
   git reset file1.txt
   ```
   -> reset all changes 

2. Discard uncommitted changes:  
   ```bash
   git checkout -- file1.txt
   ```
-> discard the changes to track or untrack files 

---

### **Part 3: Branching and Merging**

#### **Task 6: Branch Management**
1. Create a branch and switch to it:  
   ```bash
   git checkout -b feature-branch
   ```
   -> create a new branch and swith on that created branch

2. List branches:  
   ```bash
   git branch
   ```
   -> display all the branch

3. Rename a branch:  
   ```bash
   git branch -m feature-branch feature-enhanced
   ```
   -> rename the branch


#### **Task 7: Merging Branches**
1. Merge `feature-enhanced` into `main`:  
   ```bash
   git checkout main
   git merge feature-enhanced
   ```
->  merge the branch into the main branch

#### **Task 8: Handling Merge Conflicts**
1. Create two conflicting branches and resolve a conflict manually:  
   ```bash
   git merge <branch-name>
   ```
   ->

2. Use:  
   ```bash
   git add <resolved-file>
   git commit
   ```

---

### **Part 4: Remote Repositories**

#### **Task 9: Remote Setup**
1. Add a remote repository:  
   ```bash
   git remote add origin https://github.com/your-username/repo.git
   ```
   -> set up the local repository to a remote server

2. Verify the remote:  
   ```bash
   git remote -v
   ```
   -> to verify where the local repository connect to a remote server


#### **Task 10: Push and Pull**
1. Push changes to the remote repository:  
   ```bash
   git push -u origin main
   ```
   -> Push sends your local changes to the remote branch.

2. Pull changes from the remote:  
   ```bash
   git pull origin main
   ```
   -> pull sends changes from the remote to local

#### **Task 11: Cloning a Repository**
1. Clone a remote repository:  
   ```bash
   git clone https://github.com/your-username/repo.git
   ```
-> clone the existing repository to a local systum

---

## **Part 5: Advanced Git**

### Task 12: Stashing Changes
1. Task 12: Stashing Changes:
```
git stash
```
-> This command stashes all tracked changes (changes to files that Git is already tracking) and leaves the working directory clean.

2. Apply stashed changes:
```
git stash Apply
```
-> This applies the most recent stash without removing it from the stash stack.

3. Drop the stash:
```
git stash Drop
```
-> this command will delete a stash

### Task 13: Tagging Commits
1. Create and annotate a tag:
```
git tag -a v1.0 -m "Version 1.0 release"
```
2. Push the tag to the remote:
```
git push origin v1.0
```
### Task 14: Rewriting Commit History
1. Use interactive rebase to modify commit messages:
```
git rebase -i HEAD~3
```
- Replace pick with edit or squash as needed.
### Task 15: Cherry-Picking Commits
1. Apply a specific commit to another branch:
```
git cherry-pick <commit-hash>
```
---
## **Part 6: Collaboration**
### Task 16: Forking and Pull Requests
1. Fork a repository and clone it locally:
```
git clone https://github.com/your-username/forked-repo.git
```
-> clone repositoryserver to local systum

2. Make changes and push them:
```
git checkout -b fix-typo
echo "Typo fixed" >> README.md
git commit -m "Fixed a typo"
git push origin fix-typo
```
-> make changes in the cloning repository and commit them to record the chnages ans push all changes local to remote server

3. Open a pull request on GitHub.

### **Task 17: Simulating Team Collaboration**
1. Simulate a conflict by having two users modify the same file.
2. Practice resolving the conflict as a team.
---
## **Part 7: Ignoring Files**
### Task 18: Using .gitignore
1. Create a .gitignore file:
```
echo "node_modules/" > .gitignore
git add .gitignore
git commit -m "Added .gitignore"
```
2. Verify that ignored files are not staged:
```
git status
```
---
## **Part 8: Automation and Cleanup**
### Task 19: Cleaning the Repository
1. Remove untracked files:
```
git clean -f
```
### Task 20: Aliases and Shortcuts
1. Create an alias for frequently used commands:
```
git config --global alias.st status
git config --global alias.cm commit
```
2. Use the alias:
```
git st
git cm -m "Message"
```
