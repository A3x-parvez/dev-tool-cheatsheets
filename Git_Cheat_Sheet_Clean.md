# 🧠 Git Commands Cheat Sheet
---

### 👤 Author: Rijwanool Karim  
🔗 Linkdin - [Rijwanool karim](https://www.linkedin.com/in/rijwanool-karim)  
💻 Github - [A3x-parvez](https://github.com/rijwanoolkarim)

---

## Getting Started

- **`git init`**: Start a new Git repository.
- **`git clone <url>`**: Download a repository from remote (like GitHub).

## Checking Repository Status

- **`git status`**: Check current changes and branch status.
- **`git log`**: View commit history.
- **`git log --oneline`**: Condensed view of commits.
- **`git log --stat`**: Show files changed per commit.
- **`git log -p`**: See line-by-line commit changes.
- **`git show <sha_id>`**: View a specific commit's details.
- **`git diff`**: Compare changes between commits or working area.

## Adding & Committing Changes

- **`git add <filename>`**: Stage a specific file for commit.
- **`git add .`**: Stage all files for commit.
- **`git commit -m "msg"`**: Commit staged files with a message.

## .gitignore Usage

- **`.gitignore`**: File listing patterns to ignore (e.g., *.log, node_modules/).

## Branching and Merging

- **`git branch`**: List all branches.
- **`git branch <name>`**: Create a new branch.
- **`git branch <name> <sha_id>`**: Branch from a specific commit.
- **`git checkout <name>`**: Switch to a branch.
- **`git checkout <sha_id>`**: Checkout a commit (detached HEAD).
- **`git checkout master`**: Switch to master branch.
- **`git merge <branch>`**: Merge another branch into current.
- **`git branch -d <name>`**: Delete a merged branch.
- **`git branch -D <name>`**: Force delete a branch.
- **`git log --oneline --all --graph`**: View commit tree across all branches.

## Working with Remote

- **`git remote add origin <url>`**: Link local repo to a remote one.
- **`git push origin master`**: Upload commits to remote master branch.
- **`git push origin main`**: Upload to main branch.
- **`git pull origin master`**: Fetch and merge from remote master.
- **`git pull origin main`**: Fetch and merge from main.
- **`git fetch`**: Download commits from remote without merging.
- **`git remote -v`**: Show remote URLs.

## Tags and Versioning

- **`git tag`**: List all tags.
- **`git tag -a v1.0.0 -m "msg"`**: Create annotated tag.
- **`git tag -a v1.0.0 <sha_id>`**: Tag specific commit.
- **`git tag -d v1.0.0`**: Delete a tag locally.
- **`git push origin v1.0.0`**: Push a tag to remote.
- **`git push origin --tags`**: Push all local tags.

## Undoing Changes

- **`git reset <file>`**: Unstage a file.
- **`git reset --hard`**: Discard all local changes.
- **`git revert <sha_id>`**: Undo changes by new commit.
- **`git checkout -- <file>`**: Restore file from last commit.

## Stashing Changes

- **`git stash`**: Temporarily save changes.
- **`git stash list`**: Show stashed changes.
- **`git stash apply`**: Apply latest stash.
- **`git stash pop`**: Apply and remove stash.
