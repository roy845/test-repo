# 🧠 Git Essentials: Senior-Level Cheat Sheet

> A concise yet powerful reference of Git commands every developer should know — from initializing a repository to rewriting history. Perfect for personal use or team onboarding.

---

## 🗂️ Table of Contents

- [📦 Initialization & Configuration](#-initialization--configuration)
- [🌿 Branching Workflow](#-branching-workflow)
- [📥 Staging & Committing](#-staging--committing)
- [🔄 Undoing Changes](#-undoing-changes)
- [📤 Syncing with Remote](#-syncing-with-remote)
- [👁️ Viewing History](#-viewing-history)
- [🧹 Cleaning Up](#-cleaning-up)
- [🛑 Remove Git Tracking](#-remove-git-tracking)
- [📚 References](#-references)

---

## 📦 Initialization & Configuration

```bash
git init                            # Initialize new Git repo
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

## 🌿 Branching Workflow

```bash
git checkout -b feature/login      # Create and switch to new branch
git checkout main                  # Switch to existing branch
git merge feature/login            # Merge another branch into current
git branch -d feature/login        # Delete branch after merging
```

```bash
git push -u origin feature/forgot-password # pushing the branch to github
```

---

## 📥 Staging & Committing

```bash
git status                         # Show file changes
git add .                          # Stage all modified/new files
git add index.html                 # Stage specific file
git restore --staged file.js       # Unstage a file
git commit -m "Add login feature"  # Commit staged changes
```

---

## 🔄 Undoing Changes

### Undo last commit (but keep changes):

```bash
git reset --soft HEAD~1
```

### Undo last commit (keep changes unstaged):

```bash
git reset --mixed HEAD~1
# or simply:
git reset HEAD~1
```

### Undo last commit (discard changes completely):

```bash
git reset --hard HEAD~1
```

> 🔥 Use with caution — deletes your work permanently.

### Undo the first and only commit:

```bash
git update-ref -d HEAD
```

> Removes commit history while keeping changes staged.

### Revert a pushed commit safely:

```bash
git revert <commit_hash>
```

> Creates a new commit that undoes a previous one (safe for shared branches).

---

## 📤 Syncing with Remote

```bash
git remote add origin https://github.com/user/repo.git
git push -u origin main            # Push initial branch
git pull                           # Fetch and merge remote changes
git fetch                          # Fetch only (no merge)
git clone <repo_url>               # Clone a remote repository
```

---

## 👁️ Viewing History

```bash
git log                            # Full commit history
git log --oneline --graph          # Compact tree-style view
git diff                           # View unstaged changes
git diff --staged                  # View staged changes
```

---

## 🧹 Cleaning Up

```bash
git clean -fd                      # Remove untracked files and folders
git stash                          # Save changes temporarily
git stash pop                      # Re-apply last stash
```

---

## 🛑 Remove Git Tracking

### Stop tracking a project:

```bash
rmdir /s /q .git                   # Windows (PowerShell/CMD)
rm -rf .git                        # macOS/Linux
```

### Reinitialize clean Git project:

```bash
git init
git add .
git commit -m "Initial clean commit"
```

---

## 📚 References

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Documentation](https://git-scm.com/docs)
- [GitHub Git Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

> ✨ Mastering Git is a journey. Use version control not just for saving work, but for crafting software like a true professional.
