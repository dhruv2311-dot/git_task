### **Task 1: Install and Configure Git**
 1. Configure Git with your username and email:
```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```
-> set username and email globally

2. View your Git configuration:
```
git config --list
```
-> this command is used for list all configration 

### **Task 2: Initialize a Repository**
1. Create a new project folder and navigate to it:
```
mkdir myproject
```
-> create a folder name myproject

```
cd myproject
```
-> navigate into the created folder

2. Initialize it as a Git repository:
```
git init
```
-> intialize git in your local systum or code
### **Task 3: Create a file and make multiple commits**
1. Create a new file and add content:
```
echo "My first project" >> README.md
```
Create a readme file with a specific message

2. stage the file:
```
git add README.md
```
-> git add command is used for stage the file for commit

3. Commit the file:
```
git commit -m "Initial commit: Added README.md"
```
->it is use for rocord the changes into the repository

4. Make changes to the file
```
echo "Added a description" >> README.md
```
-> changes in file

5. Stage and commit the changes:
```
git add README.md
git commit -m "Updated README with a description"
```
-> stage the file for commit and record the changes
### **Task 4: Check Status and Log**

1. Check the repository’s current status:
```
git status
```
-> display the working directory and the statging area

2. View commit history in detail:
```
git log --oneline --graph --decorate
```
-> check the all history of commits

Example Output:
```
* 2f8d6a2 (HEAD -> main) Updated README with a description
* d3c4b21 Initial commit: Added README.md
```
### **Task 5: Create and Clone a Repository**
1. Create a repository on GitHub named example-repo
2. Clone it locally:
```
git clone http://codinggita.com/example-repo
```
-> clone the repository global to local
### **Task 6: Understanding the Git Workflow**
* Example Workflow:

i.Make changes to a file in the working directory:
```
echo "Workflow example" > workflow.md
```
-> change in the file

ii. stage the file:
```
git add workflow.md
```
-> add file to stage for commit

iii. Commit the file to the repository:
```
git commit -m "Added workflow example"
```
-> record the change in the file

## **Part 2: Working with Repositories**

### **Task 7: Branching and Merging**
1. Create a new branch for a feature:
```
git branch feature-login
git checkout feature-login
```
-> Create a branch 

Or use:
```
git checkout -b feature-login
```
2. Add a new file and commit changes:

```
echo "Login Page" > login.html
git add login.html
git commit -m "Added login page"
```
-> add a file and staging to commit and record the changes

3. Merge the feature branch into main:

```
git checkout main
git merge feature-login
```
-> merge branch into the main branch

### **Task 8: Handling Merge Conflicts**
1. Create two branches:
```
git branch branch-A
git branch branch-B
```
-> create a branch 

2. Modify the same line in README.md in both branches.

3. Merge branch-A into main:
```
git checkout main
git merge branch-A
```
-> merge into the main branch

4. Attempt to merge branch-B into main (this will cause a conflict):
```
git merge branch-B
```
-> merge the branch into main branch

5. Resolve the conflict manually in README.md, then:
```
git add README.md
git commit -m "Resolved merge conflict between branch-A and branch-B"
```
-> add file to the staging area and record the changes

### **Task 9: Renaming and Deleting Branches**

1. Rename a branch:
```
git branch -m old-branch-name new-branch-name
```
-> rename the branch

2. Delete a branch:
```
git branch -d feature-login
```
-> delete the branch


