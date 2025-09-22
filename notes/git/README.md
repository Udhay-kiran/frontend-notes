# Git notes

**##Git workflow basics**

Git- Version control system- to track changes in files over time.
GitHub to store git repos online remotely, share them and collaborate.
Workflow= edits files locally, save with git and push them to github. 

## **Git workflow (add-commit-push)**

### **Git add:**

Adding changes/files and preparing them for the next commit.

Example:

git add README.md
git add notes/css/README.md

To add all changes at once:

git add .


### **Git Commit:**

It saves a copy of the staged files (in the add part of the workflow) into git's history.
-m signifies a message that describes the changes made

Example:

git commit -m ":docs: Added new information on customer data to README"

Commit messages must always be wrapped in quotes (" ") - otherwise git thinks its a filename.


### **Git Push:**

Send the commits from local repo to remote repo (Github).

First push -                        git push -u origin main  

(-u helps git remember that the local branch 'main' should always push to this remote branch 'origin/main)

Later pushes ( after -u is set):    git push  (Since the upstream branch is already set)