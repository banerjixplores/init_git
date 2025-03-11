# 📌 Git & GitHub Cheatsheet

## **🛠️ Version Control with Git**

### 🔹 Check Git Version
```bash
git --version
```

### 🔹 Configure Git (First Time Setup)
```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### 🔹 Initialize a New Repository
```bash
git init
```

### 🔹 Clone an Existing Repository
```bash
git clone https://github.com/user/repo.git
```

### 🔹 Check Repository Status
```bash
git status
```

### 🔹 Add Files to Staging Area
```bash
git add filename.txt  # Add a single file
git add .             # Add all files in the current directory
```

### 🔹 Commit Changes
```bash
git commit -m "Your commit message"
```

### 🔹 View Commit History
```bash
git log
git log --oneline --graph --decorate --all  # Compact and visual log
```

### 🔹 Undo Changes
```bash
git checkout -- filename.txt  # Discard changes in working directory
git reset HEAD filename.txt   # Unstage a file
git reset --soft HEAD~1       # Undo last commit (keeps changes)
git reset --hard HEAD~1       # Undo last commit (deletes changes)
```

---

## **🔗 Connecting Projects to GitHub**

### 🔹 Add Remote Repository
```bash
git remote add origin https://github.com/user/repo.git
```

### 🔹 Check Remote Repository
```bash
git remote -v  # View linked repositories
```

### 🔹 Push Code to GitHub
```bash
git push -u origin main  # First time push
git push origin main     # Subsequent pushes
```

### 🔹 Pull Latest Changes from GitHub
```bash
git pull origin main
```

### 🔹 Fetch and Merge Changes
```bash
git fetch origin
git merge origin/main
```

### 🔹 Changing Remote URL (e.g., from HTTPS to SSH)
```bash
git remote set-url origin git@github.com:user/repo.git
```

---

## **🚀 Branching & Merging**

### 🔹 Create a New Branch
```bash
git branch new-branch
```

### 🔹 Switch to a Branch
```bash
git checkout new-branch
git switch new-branch  # Alternative to checkout
```

### 🔹 Create and Switch to a Branch
```bash
git checkout -b feature-branch
```

### 🔹 Merge a Branch
```bash
git checkout main
git merge feature-branch
```

### 🔹 Delete a Branch
```bash
git branch -d feature-branch  # Delete a local branch
git push origin --delete feature-branch  # Delete a remote branch
```

---

## **🔄 Stashing Changes**
### 🔹 Save Uncommitted Changes
```bash
git stash
```

### 🔹 List Stashes
```bash
git stash list
```

### 🔹 Apply the Latest Stash
```bash
git stash apply
```

### 🔹 Apply & Remove the Latest Stash
```bash
git stash pop
```

### 🔹 Drop a Specific Stash
```bash
git stash drop stash@{0}
```

---

## **🔐 Handling Authentication & Credentials**

### 🔹 Remove Stored Credentials (Windows)
```bash
cmdkey /delete:git:https://github.com
```

### 🔹 Remove Stored Credentials (Mac/Linux)
```bash
git credential reject https://github.com
```

### 🔹 Use SSH Instead of HTTPS
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"  # Generate SSH Key
# Then add the key to GitHub (Settings → SSH and GPG keys)
git remote set-url origin git@github.com:user/repo.git
```

---

## **🎯 Summary of Common Commands**

| Command | Description |
|---------|------------|
| `git init` | Initialize a new repository |
| `git clone <repo-url>` | Clone a GitHub repository |
| `git status` | Check repository status |
| `git add .` | Add all files to staging |
| `git commit -m "msg"` | Commit changes |
| `git push origin main` | Push changes to GitHub |
| `git pull origin main` | Pull latest changes |
| `git branch new-branch` | Create a new branch |
| `git checkout new-branch` | Switch to a branch |
| `git merge branch-name` | Merge a branch |
| `git stash` | Stash changes |
| `git stash pop` | Apply and remove stash |
| `git reset --hard HEAD~1` | Undo last commit (deletes changes) |
| `git remote -v` | View linked repositories |

---

🔹 **Now you’re ready to manage your projects with Git & GitHub! 🚀**
