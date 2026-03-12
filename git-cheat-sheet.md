# Git Cheat Sheet

## Repository Setup (using GitHub website)
Initialize a new Git repository:
```git init```

Clone an existing repository:
```git clone <repo-url>```

Check the status of files in the repository:
```git status```

## Repository Setup (using GitHub CLI)
```
git init
git add .
git commit -m "Initial commit"
gh repo create git-demo --public --source=. --push
```

## Basic Workflow
Stage files for commit:
```git add <file-name>```

Stage all changes:
```git add .```

Commit changes with a message:
```git commit -m "Description of changes"```

Push commits to a remote repositiory:
```git push```

Pull latest changes from a remote repository:
```pit pull```

## Branching
Create a new branch:
```git branch <branch-name>```

Switch to a branch:
```git checkout <branch-name>```

Create and switch to a new branch:
```git checkout -b <branch-name>```

List all branches:
```git branch```

## Merging
Merge another branch into the current branch:
```git merge <branch-name>```

Example workflow:
```
git checkout main
git merge feature-branch
```

## Resolving Merge Conflicts
When Git cannot automatically merge changes, conflict markers appear:
```
<<<<<<< HEAD
Current branch changes
=======
Incoming branch changes
>>>>>>> branch-name
```

Steps to resolve:
1. Edit the file to keep the correct code
2. Remove the conflict markers
3. Stage the file

```
git add <file-name>
git commit -m "Resolve merge conflict"
```

## Viewing History
View commit history:
```git log```

Compact commit history:
```git log --oneline```

Graph view of commit history:
```git log --oneline --graph --all```

## Remote Repositories
Add a remote repository:
```git remote add origin <repo-url>```

Push branch to remote:
```git push -u origin main```

View remote repositories:
```git remote -v```

## Undoing Changes
Unstage a file:
```git restore --staged <file-name>```

Discard changes in a file:
```git restore <file-name>```

Reset to previous commit:
```git reset --hard <commit-id>```

## How to Use ```.gitignore```
Create a file in root of repo:
```.gitignore```

List files or patterns for Git to ignore

Example ```.gitignore```:
```
# OS files
.DS_Store
Thumbs.db

# Python cache
__pycache__/
*.pyc

# Environment variables
.env

# Logs
*.log

# Build folders
dist/
build/

# Node modules
node_modules/

# IDE files
.vscode/
.idea/
```