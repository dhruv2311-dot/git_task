### **Task List: Focused on Advanced Git Operations**
### **Part 1: Understanding and Using git stash**
### Task 1: Save Changes Temporarily with git stash
1. Make changes to a file without committing:
```
echo "Temporary changes" >> temp-file.txt
```
- create a file to for temporary change

2. View the status of changes:
```
git status
```
- display the changes
- output
 - Explanation: This command saves changes to a stash and restores the working directory to the last commit state.

 4. View the stashed changes:
 ```
 git stash list
 ```
 - output
 ```
 stash@{0}: WIP on main: 27e5f23 Added temporary changes
 ```
 ### Task 2: Apply and Drop Stashed Changes
1. Apply the most recent stash:
```
git stash apply
```
- This applies the most recent stash without removing it from the stash stack.( it means it aplly the most recent commit message)

2. Drop the most recent stash after applying it:
```
git stash drop
```
- this command will delete the most recent stash

3. Alternatively, to apply a specific stash:
```
git stash apply stash@{1}
```
- it will deleted a specific stash 

### Task 3: Stash Untracked Files
1. Stash changes, including untracked files:
```
git stash -u
```
- by default git stash does not include untracked file it will use for stash untracked file

2. Apply stashed changes including untracked files:
```
git stash apply
```
- this applies the most recent stash without removing it from stash stack
---
### **Part 2: Rewriting History with git rebase**
### Task 4: Rebase Commits to a New Base
1. Rebase the current branch onto main:
```
git rebase main
```
- Explanation: This command applies the commits from your current branch on top of the latest commit from main.

2. Resolve any conflicts that may arise during rebase, and continue:
```
git rebase --continue
```
### Task 5: Canceling a Rebase
1. if a rebase goes wrong, abort it
```
git rebase --abort
```
---
### **Part 3: Interactive Rebase (git rebase -i)**
### Task 6: Use Interactive Rebase to Modify Commit History
1. View the last few commits:
```
git log --oneline
```
- display last few commit history

2. Start an interactive rebase for the last 3 commits:
```
git rebase -i HEAD~3
```
- Explanation: This opens an editor with the list of commits in the last 3 commits.

3. Modify the commits by changing pick to one of the following:
- squash (combine commits)
- reword (edit commit message)
- edit (edit commit content)
- drop (remove commit)

4. Example of squashing two commits:
- Change the second commit from pick to squash and save.
- Git will combine the commit messages for the squashed commit.
### Task 7: Complete Interactive Rebase
1. After modifying the commits, save and close the editor.
2. Resolve any conflicts if prompted, then continue the rebase:
```
git rebase --continue
```
---
### **Part 4: Cherry-Picking Commits (git cherry-pick)**
### Task 8: Pick a Specific Commit
1. View the commit history to find the commit hash you want to cherry-pick:
```
git log --oneline
```

2. Cherry-pick a specific commit by its hash:
```
git cherry-pick <commit-hash>
```
- Example:
```
git cherry-pick e23d8a7
```
3. Resolve conflicts if any, then commit the changes:
```
git add .
git cherry-pick --continue
```
---
### **Part 5: Tagging Commits (git tag)**
### Task 9: Tag a Commit
1. Tag the current commit with a version number:
```
git tag -a v1.0 -m "Initial release"
```
2. List all tags:
```
git tag
```
- display all tags

### Task 10: Tag a Specific Commit
1. Tag a specific commit by its hash:
```
git tag -a v1.1 <commit-hash> -m "Bug fix"
```
### Task 11: Push Tags to Remote
1. Push a specific tag to the remote repository:
```
git push origin v1.0
```
2. Push all tags to the remote repository:
```
git push --tags
```
### **Part 6: Working with Remote Repositories**
### Task 12: Add a Remote Repository
1. Add a remote repository URL to the project:
```
git remote add origin https://github.com/username/repo.git
```
- connect repository to remote server
### Task 13: Fetch Changes from Remote
1. Fetch changes from the remote repository without merging them:
```
git fetch origin
```
This fetches updates from the main branch of the origin remote.

2. View fetched branches:
```
git branch -r
```
- After running git fetch, Git updates the remote-tracking branches (e.g., origin/main), which represent the state of branches on the remote.
### Task 14: Pull Changes from Remote
1. Pull the latest changes from the remote repository and merge them into the local branch:
```
git pull origin main
```
- This pulls updates from the branch currently being tracked from origin.

### Task 15: Push Changes to Remote
1. Push local changes to the remote repository:
```
git push origin main
```
- Pushes the commits of the current branch to its remote counterpart.

2. Push a new branch to the remote repository:
```
git push origin feature-branch
```
- This command pushes the commits from your local feature-branch to the feature-branch on the remote repository named origin.

### Task 16: Delete Remote Branch
1. Delete a remote branch:
```
git push origin --delete feature-branch
```
- This command deletes the feature-branch from the remote repository named origin.

---
### **Part 7: Forking and Contributing to Open-Source Projects**
### Task 17: Fork a Repository on GitHub
1. Go to a repository on GitHub and click Fork in the top right corner to create your own copy of the repository.

2. Clone the forked repository to your local machine:
```
git clone https://github.com/your-username/repo.git
```
- clone the remote repository on a local stystum

### Task 18: Make Changes and Commit
1. Create a new branch for your changes:
```
git checkout -b fix-typo
```
- create a new branch and switch on the branch

2. Make changes to the code (e.g., fix a typo in README.md), stage, and commit them:
```
git add README.md
git commit -m "Fixed typo in README.md"
```
- stage the file for commit and record the changes with commit them

### Task 19: Push Changes to Your Fork
1. Push the changes to your remote fork:
```
git push origin fix-typo
```
- push changes local to remote server
### Task 20: Create a Pull Request
1. Go to your forked repository on GitHub, click on Compare & Pull Request.
2. Write a description of your changes and submit the pull request to the original repository.
### Task 21: Sync Your Fork with the Original Repository
1. Add the original repository as a remote source:
```
git remote add upstream https://github.com/original-owner/repo.git
```
- This command adds a new remote repository named upstream to your local Git project and points it to the specified URL

2. Fetch changes from the original repository:
```
git fetch upstream
```
The command git fetch upstream retrieves the latest changes from the remote repository named upstream without modifying your working directory.

3. Merge changes from the original repository into your local branch:
```
git checkout main
git merge upstream/main
```
- switch into main branch after that merge two branches

4. Push the changes to your fork:
```
git push origin main
```
- push the changes into main branch
---
### **Consolidated Summary**
1. Stashing: Saving and applying uncommitted changes temporarily.
2. Rewriting History: Using git rebase and interactive rebase to modify and clean up commit history.
3. Cherry-Picking: Selecting specific commits from another branch.
4. Tagging: Labeling commits for versioning.
5. Working with Remote Repositories: Managing remotes, pushing, pulling, and fetching changes.
6. Forking & Contributing: Forking repositories, contributing to open-source projects, and syncing your fork.


