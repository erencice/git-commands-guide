# 🚀 Git Commands Guide

Welcome to **Git Commands Guide**! This repository provides a clean and structured list of essential Git commands, helping you navigate version control with ease.

---

## 📌 Table of Contents

- [Basic Git Commands](#basic-git-commands)
- [Branching & Merging](#branching--merging)
- [Working with Remote Repositories](#working-with-remote-repositories)
- [Advanced Git Commands](#advanced-git-commands)
- [License](#license)

---

## 📌 Basic Git Commands

### 🛠️ Repository Setup
Initialize a new Git repository:
```sh
git init
```
Clone an existing repository:
```sh
git clone <repository_url>
```

### 🔍 Status & History
Check repository status:
```sh
git status
```
View commit history:
```sh
git log
```

### 📂 Staging & Committing
Stage files for commit:
```sh
git add <file_name>
```
Commit changes:
```sh
git commit -m "Commit message"
```

---

## 🌿 Branching & Merging

### 📌 Working with Branches
Create a new branch:
```sh
git branch <branch_name>
```
Switch to a branch:
```sh
git switch <branch_name>
```

### 🔗 Merging Changes
Merge branches:
```sh
git merge <branch_name>
```
Delete a branch:
```sh
git branch -d <branch_name>
```

---

## 🔗 Working with Remote Repositories

### 📡 Connecting to a Remote Repository
Add a remote repository:
```sh
git remote add origin <repository_url>
```

### 🔼 Pushing Changes
Pushing uploads your committed changes to a remote repository, making them available to others:
```sh
git push origin <branch_name>
```
To set an upstream tracking branch and push changes, use:
```sh
git push -u origin <branch_name>
```
This command links your local branch with the remote one, so future `git push` commands don’t need to specify the branch name.

### 🔽 Pulling Changes
Pulling retrieves changes from the remote repository and merges them into your local branch:
```sh
git pull origin <branch_name>
```
If conflicts occur, Git will prompt you to resolve them before finalizing the pull.

### 🔄 Fetching Changes
Fetching downloads the latest commits from the remote repository without merging them into your local branch:
```sh
git fetch origin
```
Use `git fetch` when you want to inspect the latest changes before integrating them into your codebase.

---

## ⚡ Advanced Git Commands

### 🔙 Reverting & Resetting
Revert changes:
```sh
git revert <commit_hash>
```
Reset to a previous commit:
```sh
git reset --hard <commit_hash>
```

### 📌 Stashing Changes
Stash current changes:
```sh
git stash
```
Apply stashed changes:
```sh
git stash pop
```

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

🚀 **Happy Coding with Git!** 🎉
