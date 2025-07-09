
````markdown
# 🚀 Git Cheat Sheet for Beginners

This cheat sheet helps you learn and revise the most important Git commands step by step. It's perfect for beginners and is written in a clean and simple way.

---

## 📦 1. Initialize Git

```bash
git init                    # Start a new git repo in the current folder
git init [folder-name]     # Create a new folder and initialize a git repo
````

---

## 📥 2. Add Files to Staging Area

```bash
git add index.html         # Add a single file
git add .                  # Add all files to staging
git status                 # Show current status (staged/unstaged/untracked files)
```

---

## ✅ 3. Commit Changes

```bash
git commit -m "Your message here"  # Commit staged changes
```

---

## ⏳ 4. View Commit History

```bash
git log                     # Full commit history
git log --oneline           # One line per commit
git log --all               # Show logs from all branches
git log master              # Show logs of the master branch
git reflog                  # Show all moves HEAD has made (undo history)
git log --graph --oneline --decorate --all  # Visual graph of commits
```

---

## 🧑‍💻 5. Configure Git (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor nano   # Set default editor (nano/vim/code)
```

---

## 🌿 6. Branching

```bash
git branch                     # List all branches
git branch about               # Create a new branch named 'about'
git checkout about             # Switch to 'about' branch
git checkout main              # Switch to 'main' branch
git merge about                # Merge 'about' into current branch
git branch --delete about      # Delete the branch safely (merged only)
git branch -D about            # Force delete a branch (not safe)
```

---

## 🌐 7. Remote Repositories (like GitHub)

```bash
git remote -v                                # View linked remotes
git remote add origin [url]                  # Add a new remote origin
git remote remove origin                     # Remove the remote origin
git remote rename origin newname             # Rename the remote origin
git remote show origin                       # Show remote details
```

---

## ⬆️ 8. Push & Pull

```bash
git push origin main                         # Push changes to remote main branch
git push -u origin main                      # Push first time and track the branch
git pull origin main                         # Pull latest code from GitHub
git clone [repo-url]                         # Clone a GitHub repository
```

---

## ⏪ 9. Reset / Undo

```bash
git reset --soft [commit-hash]      # Keep code and keep staged
git reset --mixed [commit-hash]     # Keep code but unstage
git reset --hard [commit-hash]      # Discard all changes (⚠️ irreversible)
```

---



