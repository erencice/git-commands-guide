# 🚀 Git Commands Guide

Welcome to **Git Commands Guide**! This repository provides a clean and structured list of essential Git commands, helping you navigate version control with ease.

---

## 📌 Table of Contents

- [Basic Git Commands](#basic-git-commands)
- [Branching & Merging](#branching--merging)
- [Working with Remote Repositories](#working-with-remote-repositories)
- [Advanced Git Commands](#advanced-git-commands)
- [Data Science Git Workflow](#data-science-git-workflow)
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
This command establishes a connection between your local branch and the remote one, so future `git push` commands automatically push to the correct branch without needing to specify it.

### 🔽 Pulling Changes
Pulling retrieves and merges the latest changes from the remote repository into your local branch:
```sh
git pull origin <branch_name>
```
Use `git pull` to ensure your local repository is in sync with the latest remote changes, preventing merge conflicts.

### 🔄 Fetching Changes
Fetching downloads the latest commits from the remote repository **without merging** them into your local branch:
```sh
git fetch origin
```
Use `git fetch` when you want to review updates before integrating them, ensuring controlled version updates.

---

## ⚡ Advanced Git Commands

### 🔙 Reverting & Resetting
Revert changes (creates a new commit that undoes the specified commit):
```sh
git revert <commit_hash>
```
Reset to a previous commit (modifies history, use with caution):
```sh
git reset --hard <commit_hash>
```
`git revert` is safer for shared repositories, while `git reset` is best for local modifications.

### 📌 Stashing Changes
Temporarily save changes without committing:
```sh
git stash
```
Apply the most recent stash:
```sh
git stash pop
```
Use `git stash` when you need to switch branches without losing progress.

---

## 📂 Data Science Git Workflow
This repository includes a **`data_science_project/`** folder where Git commands are applied in a real-world data science scenario. The project follows a structured workflow:

### 📌 Project Structure
```
data_science_project/
│-- data/
│   ├── raw_data.csv
│   ├── cleaned_data.csv
│-- notebooks/
│   ├── data_preprocessing.ipynb
│   ├── model_training.ipynb
│-- scripts/
│   ├── preprocess.py
│   ├── train_model.py
│-- results/
│   ├── model_metrics.txt
│-- README.md
```

### 🔄 Workflow Example
1. **Clone the repository:**
   ```sh
   git clone <repo_url>
   ```
2. **Create a feature branch for preprocessing:**
   ```sh
   git branch feature/data-preprocessing
   git switch feature/data-preprocessing
   ```
3. **Modify the `preprocess.py` script and commit changes:**
   ```sh
   git add scripts/preprocess.py
   git commit -m "Added data cleaning functions"
   ```
4. **Push changes to remote:**
   ```sh
   git push -u origin feature/data-preprocessing
   ```
5. **Merge changes into `main`:**
   ```sh
   git switch main
   git merge feature/data-preprocessing
   ```
6. **Fetch latest changes without merging:** If other team members have made changes to the main branch, you can fetch the latest changes to inspect them before merging:
   ```sh
   git fetch origin
   ```
7. **Pull and update local repository:** To update your local repository with any changes made by other team members on the remote, use git pull:
   ```sh
   git pull origin main
   ```
8. **Temporarily save uncommitted changes before switching branches:** If you are in the middle of working on something but need to switch branches, you can stash your uncommitted changes and apply them later:
   ```sh
   git stash
   ```
9. **Retrieve stashed changes (Apply the stashed changes):** If you previously stashed changes and now want to retrieve them, you can apply the stashed changes:
   ```sh
   git stash pop
   ```
   This command retrieves the most recent stash and removes it from the stash list.
   If you want to keep the stash while applying it, use git stash apply instead of git stash pop.
   Apply stashed changes without removing them from the stash list
   ```sh
   git stash apply stash@{1}
   ```
9. **Revert a commit if needed:** If a commit caused issues in the project and you need to revert it, you can use the git revert command to undo the changes introduced by that commit:
   ```sh
   git revert <commit_hash>
   ```
10. **Reset to a previous state if required (dangerous for shared repos):** If you need to completely discard changes and return to a specific commit, you can use git reset. This is risky when working on shared repositories, so use it carefully:
  ```sh
   git reset --hard <commit_hash>
   ```

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

🚀 **Happy Coding with Git!** 🎉
