# Git notes

## **Git workflow basics**

Git- Version control system- to track changes in files over time.
GitHub to store git repos online remotely, share them and collaborate.
Workflow= edits files locally, save with git and push them to github. 

## **Git workflow (add-commit-push)**

### **Git add:**

Adding changes/files and preparing them for the next commit.

Example:

<pre> git add README.md
      git add notes/css/README.md </pre>

To add all changes at once:

<pre> git add . </pre>


### **Git Commit:**

It saves a copy of the staged files (in the add part of the workflow) into git's history.

-m signifies a message that describes the changes made

Example:

<pre> git commit -m ":docs: Added new information on customer data to README" </pre>

Commit messages must always be wrapped in quotes (" ") - otherwise git thinks its a filename.


### **Git Push:**

Send the commits from local repo to remote repo (Github).

First push -                       <pre> git push -u origin main  </pre>

(-u helps git remember that the local branch 'main' should always push to this remote branch 'origin/main)

Later pushes ( after -u is set):    <pre> git push </pre>  (Since the upstream branch is already set)


## **Repo Setup**

### 1. To create a repo on Github

A local repo is in the computer whereas a remote repo lives on Github.

Ex of remote url : https://github.com/USERNAME/repo-name.git

Ex of SSH URL:  git@github.com:USERNAME/repo-name.git

### 2. Initialize repo locally 

```bash
mkdir repo-name 
 #makes a folder

cd repo-name #moves into the folder
 
git init  # tells git to track the folder (with a hidden .git folder inside)

```

### 3. Connect local- Remote

git remote add origin git@github.com:USERNAME/repo-name.git

where,

git remote add - tells git about a remote repo.

origin -  the default nickname the "the main remote repo.

git@github.com:USERNAME/repo-name.git - the SSH url of the github repo

To check if it's set correctly - git remote -v 



### 4. First commit (Local snapshot)

Add files to the repo (See below- adding files) and run:

git add .  #stages all new/changed files.
git commit -m "message -saves a snapshot locally.

### 5. First push (from local to github)

git push -u origin main  #git push -    uploads commits.

                         #origin-       the remote repo you set earlier

                         #main -        the branch you're pushing

                         #-u (upstream)- tells git 'next time, just git push without any args. 


### 6. Everyday workflow after setup.

1. Edit files in vs code and save them
   
2. Stage them
   
3. Commit them
   
4. Push them


## Add files to your repo (before first commit)

Inside the repo folder:

echo "# Customer Information" > README.md

This creates a file called README.md with the one line in double quotes.

ALternatively, create a new file in vs code and save changes before you stage, commit and push them. 

An example of full final flow:

mkdir repo-name

cd repo-name

git init

echo "# Customer Information" > README.md     # ← add a file
git add README.md
git commit -m "chore: add initial README"
git branch -M main
git remote add origin git@github.com:USERNAME/repo-name.git
git push -u origin main
