<img width="1" height="3" alt="image" src="https://github.com/user-attachments/assets/186466a5-9e66-470d-86e1-1fda9bbc5efd" />

# Git Assignment - Advanced Git Operations

## Overview
This repository demonstrates comprehensive Git operations including local repository management, remote operations, branching strategies, merge conflict resolution, and advanced staging techniques.

## Repository Information
- **Repository URL**: https://github.com/harivanshx/GitAssignment1Pgdai.git
- **Author**: Harivansh Bhardwaj
- **Assignment**: Git Operations & Workflow Management

## Assignment Structure

### 1. Local Git Repository Initialization
- Initialized local Git repository
- Created `initial.txt` with initial content and committed to `main` branch
- Demonstrated staging and unstaging operations:
  - Staged `temp.txt` and unstaged using `git restore --staged temp.txt`
  - Modified `temp.txt`, staged again, and unstaged using `git reset HEAD temp.txt`

### 2. Remote Repository Operations
- Created remote repository on GitHub
- Linked local repository to remote
- Pushed initial commit to remote `main` branch
- Modified `initial.txt` via GitHub web interface
- Pulled changes using `git pull origin main`
- Staged multiple files (`file1.txt`, `file2.txt`)
- Unstaged `file2.txt` using `git reset HEAD file2.txt`
- Committed and pushed `file1.txt` to remote
- Documented working directory state using `git status`

### 3. Branching and Pull Request
- Created `g1` branch on remote repository via GitHub
- Fetched and checked out `g1` branch locally:
  ```bash
  git fetch origin
  git checkout g1
  ```
- Added `g1_file.txt` on `g1` branch
- Committed and pushed to remote
- Raised pull request from `g1` to `main`
- Successfully merged PR without conflicts

**Pull Request Links:**
- PR #1: [g1 to main merge]

### 4. Local Git Operations

#### Get Updated Files
- Executed `git fetch origin` and `git merge origin/main`
- Ensured local `main` branch is synchronized

#### Reset Operations
- Created commit with changes to `initial.txt`
- Performed soft reset: `git reset --soft HEAD~1`
- Used interactive staging: `git add -p`
- Performed hard reset: `git reset --hard HEAD~1`
- Demonstrated change loss using `git status` and `git log`

#### List Changes
- Used `git diff main g1` to show branch differences
- Listed tracked and untracked files with `git ls-files` and `git status`

#### Create Local Branches
- Created branch `b1` from `main`, updated `initial.txt`
- Created branch `b2` from `b1`, added `b2_file.txt`
- Created branch `b3` from `b2`, modified `b2_file.txt`
- On `b3`: staged multiple changes, used `git reset --mixed HEAD` to unstage
- Selectively staged hunks using `git add -p`
- Showed staged differences using `git diff --staged`

### 5. Branch Merging and Cleanup

#### Merge Operations
- Merged `b3` into `b2`
- Merged `b2` into `b1`
- Merged `b1` into `main`

#### Merge Conflict Resolution
- Introduced merge conflict by modifying same line in `initial.txt` on `b3` and `b2`
- Resolved conflict manually during merge
- Documented resolution process with screenshots

#### Branch Cleanup
- Deleted local branches:
  ```bash
  git branch -d b1
  git branch -d b2
  git branch -d b3
  ```
- Deleted remote `g1` branch:
  ```bash
  git push origin --delete g1
  ```

### 6. Fork Operations
- Forked repository to new repository under account
- https://github.com/harivanshx/Oasisinfobyte
- Made changes (added text to `readme.md`)
- Created PR from forked repository to original repository's `main` branch

**Fork PR Links:**
- PR #2: https://github.com/PoojaShashikantPawar/Oasisinfobyte/commit/6799b0d57f939714eef342799664f9ddb41f7553

### 7. Advanced Unstaging Challenge

#### Complex Staging Scenario
- Modified `initial.txt`, `b2_file.txt`, and added `challenge.txt`
- Staged all changes: `git add .`
- Unstaged `challenge.txt`: `git reset HEAD challenge.txt`
- Selectively staged lines in `initial.txt` using `git add -p`
- Committed staged changes
- Saved remaining changes: `git stash`
- Popped stash: `git stash pop`
- Resolved stash application conflict manually
- Committed resolved changes

#### Remove and Revert Operations
- Performed `git rm` operations on files
- Used `git revert` to undo specific commits
- Documented state after each operation using `git status` and `git diff`

## Key Git Commands Used

```bash
# Repository Setup
git init
git remote add origin <url>
git push -u origin main

# Staging Operations
git add <file>
git add .
git add -p
git restore --staged <file>
git reset HEAD <file>
git reset --soft HEAD~1
git reset --mixed HEAD
git reset --hard HEAD~1

# Branch Operations
git branch <branch-name>
git checkout <branch-name>
git checkout -b <branch-name>
git merge <branch-name>
git branch -d <branch-name>

# Remote Operations
git fetch origin
git pull origin <branch>
git push origin <branch>
git push origin --delete <branch>

# Inspection Commands
git status
git log
git diff
git diff --staged
git diff <branch1> <branch2>
git ls-files

# Advanced Operations
git stash
git stash pop
git revert <commit>
git rm <file>
```

## Screenshots
All terminal screenshots demonstrating each major step are included in the `/git github assgnment 1 screenshots` directory:
- `Photo (3).png`
- `Photo (12).png`
- `Photo (23).png`
- `Photo (25).png`
- `Photo (33).png`
- `Photo (37).png`
- `Photo (46).png`

## Repository Contents
```
.
├── README.md
├── initial.txt
├── file1.txt
├── g1_file.txt
├── b2_file.txt
├── forked.txt
├── challenge.txt
└── git github assgnment 1 screenshots/
    └── [terminal screenshots]
```

## Learning Outcomes
- Understanding of Git workflow and version control
- Proficiency in staging and unstaging operations
- Branch management and merge conflict resolution
- Advanced Git operations including stash and revert
- Fork-based contribution workflow
- Remote repository management


---

**Note**: This assignment was completed as part of the PGDAI program to demonstrate comprehensive understanding of Git version control system.
