## Task List: Focused on Repository Management, Commits, Branching, and Merging
## Part 1: Creating and Cloning Repositories
### Task 1: Create a Local Git Repository
1. Create a new project folder:
```
mkdir MyProject
cd MyProject
```
- create a folder and navigate into the folder

2. Initialize it as a Git repository:
```
git init
```
Explanation: This creates a .git folder that stores the repository's metadata and history.
- initialize git into a local stystum

3. Verify the repository status:
```
git status
```
- display all the track or untack files or folder
- Example Output:
```
On branch main
No commits yet
nothing to commit (create/copy files and use "git add" to track)
```
###  Task 2: Clone a Remote Repository
1. Clone a GitHub repository:
```
git clone https://github.com/username/repo.git
```
- clone the existing repository into local
- Explanation: This command downloads the repository to your local system.

3. Verify the cloned repository structure:
```
cd repo
ls -a
```
- nagiate into the cloned repostiory and list all the items
- Output: The .git folder should be present.
---
## Part 2: Understanding Commits and Commit Messages
###  Task 3: Commit Changes Locally
1. Create a new file and add content:
```
echo "Welcome to Git" > README.md
```
- create a new file with a specific message

2. Stage the file:
```
git add README.md
```
- add a file for staging area  to commit it
- Explanation: git add moves changes to the staging area.

3. Commit the staged file:
```
git commit -m "Initial commit: Added README.md"
```
- Explanation: Commits save the current state of the repository with a message describing the change.

### Task 4: Write Effective Commit Messages
1. Create a detailed commit message:
```
git commit -m "Added initial version of README.md with project overview"
```
- commit the file with a specific message for record the changes 
- Explanation: Commit messages should follow conventions such as starting with a capital letter, being concise, and using the imperative mood.

2. Commit multiple files with one message:
```
touch file1.txt file2.txt
git add .
git commit -m "Added two new files for feature setup"
```
- create a two files and add them to staging area for commit and then commit them with one specific message 
---
## Part 3: Viewing Commit History with git log
### Task 5: View Detailed Commit History
1. View full commit logs:
```
git log
```
- Explanation: Shows a detailed list of commits with hash, author, date, and message.

2. View commit history in a compact format
```
git log --oneline
```
- Example output:
``` 
e23d8a7 Added initial version of README.md
f7b3c62 Initial commit: Added README.md
```
### Task 6: Customize Log Outputs
1. View logs with a graphical representation
```
git log --oneline --graph --decorate
```
2. Filter logs for a specific file:
```
git log README.md
```
---
### **Part 4: Understanding Branching and Merging**
### Task 7: Understanding Branching
1. List all branches:
```
git branch
```
- Explanation: Displays the current branch and all other branches.

2. Create a new branch:
```
git branch feature-branch
```
- Explanation: Creates a new branch without switching to it

3. Switch to the new branch:
```
git checkout feature-branch
```
- alternative command:
```
git checkout -b feature-branch
```
- Explanation: Creates and switches to the branch in one command.

---
## **Part 5: Creating and Working with Branches**
### Task 8: Make Changes in a Branch
1. Add content to a file in the new branch:
```
echo "Feature in progress" > feature.txt
git add feature.txt
git commit -m "Added feature.txt in feature-branch"
```
- create a new file and add file to staging area to commit it and commit it to record the changes

### Task 9: Merging Branches
1. Switch back to the main branch:
```
git checkout main
```
- switch back to main branch

2. Merge the feature-branch into main:
```
git merge feature-branch
```
- merge branch into main branch
---
### **Part 6: Resolving Merge Conflicts**
### Task 10: Simulate a Merge Conflict
1. Modify the same line in a file on two branches:
```
echo "Main branch content" > conflict.txt
git add conflict.txt
git commit -m "Added conflict.txt in main branch"
```
- create a new file and add a file into staging area and commit for record the change 

2. Switch to the other branch and make conflicting changes:
```
git checkout feature-branch
echo "Feature branch content" > conflict.txt
git add conflict.txt
git commit -m "Modified conflict.txt in feature-branch"
```
- switch to another branch
- create a file o  their switched branch and add and commit the file 

3. Merge feature-branch into main:
```
git checkout main
git merge feature-branch
```
- switch back into the main branch 
- merge this two branch

4. Resolve the conflict by editing the file and choosing the correct version:
- Open conflict.txt and decide which changes to keep.
- Stage the resolved file:
```
git add conflict.txt
```
- Commit the merge:
```
git commit -m "Resolved conflict in conflict.txt"
```
---
### **Part 7: Deleting and Renaming Branches**
### Task 11: Delete a Branch
1. Delete a local branch:
```
git branch -d feature-branch
```
- delete a branch 
- Explanation: This deletes the branch only if it has been fully merged.

2. Force-delete a branch:
```
git branch -D feature-branch
```
- Explanation: Deletes the branch even if it hasn’t been merged.

### Task 12: Rename a Branch
1. Rename the current branch:
```
git branch -m new-branch-name
```
- rename the branch 

2. Rename another branch (not checked out)
```
git branch -m old-branch-name new-branch-name
```
---
### **Consolidated Flow Summary**
1. Start by creating and cloning repositories.
2. Learn to commit changes effectively with clear messages.
3. Explore commit history using various git log commands.
4. Understand branching and practice creating, switching, and merging branches.
5. Dive into resolving merge conflicts.
6. End by managing branches through deletion and renaming.

