Absolutely! Here's a **complete, detailed, beginner-to-FAANG-level Git Command Guide**, with **clear explanations** so you can understand everything in **one read**, **memorize easily**, and **practice confidently**.

---

# 🧠 **GIT COMMANDS – Explained Like Never Before (For FAANG + Practice)**

---

## 🚀 1. **Git Version and Initialization**

```bash
git -v
```

🟢 Shows the installed version of Git.
✅ Use this to confirm if Git is installed properly.

---

```bash
git init
```

🟢 Initializes a **new Git repository** in the current directory.
✅ It creates a hidden `.git` folder to start tracking changes.

---

```bash
git init [folder-name]
```

🟢 Creates a new folder with the given name and initializes a Git repo inside it.

---

## 📁 2. **Staging Files (Preparing for Commit)**

```bash
git add index.html
```

🟢 Adds `index.html` file to the **staging area**, which means Git is now tracking this file and it's ready to be committed.

---

```bash
git add .
```

🟢 Adds **all new or modified files** in the current directory to the staging area.

---

```bash
git status
```

🟢 Shows the current state of the working directory and staging area:

* Modified files (but not staged)
* Files added to staging
* Untracked files

---

```bash
git status -s
```

🟢 Gives a **short and cleaner version** of `git status`.
Example:

* `M file.txt` → Modified
* `A file.txt` → Added
* `?? file.txt` → Untracked

---

```bash
git rm index.html
```

🟢 Removes `index.html` from your directory and stages the deletion.

---

## 📦 3. **Committing and Viewing History**

```bash
git commit -m "first commit"
```

🟢 Creates a **snapshot of your project** at the current stage with a message describing the changes.

---

```bash
git log --all
```

🟢 Shows the complete commit history across all branches.

---

```bash
git log --all --oneline
```

🟢 Shows the full commit history in a **single-line format** (great for a quick look).

---

```bash
git log [commit-id]
```

🟢 Shows detailed information about a specific commit using its commit hash (ID).

---

```bash
git log master
```

🟢 Shows commits on the `master` branch only.

---

```bash
git reflog
```

🟢 Shows **all movements** (HEAD pointer changes), even if they’re not part of the commit history.
✅ Useful for undoing mistakes.

---

```bash
git log --graph --oneline --decorate --all
```

🟢 Beautiful graphical visualization of your commit history.

---

## 👤 4. **Git Configuration (Set Identity & Editor)**

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

🟢 Sets your name and email globally (used for all Git repos).

---

```bash
git config --global core.editor nano
```

🟢 Sets the default text editor to Nano (can also be `code`, `vim`, etc.).

---

## 🌱 5. **Branches – Creation, Switch, Rename, Delete**

```bash
git branch
```

🟢 Lists all available branches.

---

```bash
git branch about
```

🟢 Creates a new branch named `about`.

---

```bash
git branch [branch-name]
```

🟢 Creates a new branch with the given name.

---

```bash
git branch -c [branch-name]
```

🟢 **Creates and switches** to a new branch (short for checkout + branch).

---

```bash
git branch -m oldName newName
```

🟢 Renames a branch.

---

```bash
git switch [branch-name]
```

🟢 Switches to the specified branch (modern alternative to checkout).

---

```bash
git checkout about
```

🟢 Also switches to the `about` branch (older syntax).

---

```bash
git branch --delete [branch-name]
```

🟢 Deletes the branch **safely** (only if it's merged).

---

```bash
git branch -D [branch-name]
```

🟢 Force-deletes a branch **even if it’s not merged**.

---

```bash
git merge [branch-name]
```

🟢 Merges the specified branch **into the current branch**.

---

## 🌍 6. **Remote Repositories**

```bash
git remote show origin
```

🟢 Shows detailed information about the remote repository.

---

```bash
git remote add origin [url]
```

🟢 Connects your local Git repo to a **remote GitHub repo**.

---

```bash
git remote remove origin
```

🟢 Removes the connection to the remote origin.

---

```bash
git remote rename origin [new-name]
```

🟢 Renames the remote from `origin` to a new name.

---

```bash
git remote -v
```

🟢 Lists the URLs of the connected remote repositories (for fetch & push).

---

## ☁️ 7. **Push & Pull Commands**

```bash
git push origin [branch-name]
```

🟢 Push your local branch to the remote repo.

---

```bash
git push origin main
```

🟢 Push current code to `main` branch on GitHub.

---

```bash
git push -u origin [branch-name]
```

🟢 Set **upstream tracking** so you can later just type `git push`.

---

```bash
git pull origin main
```

🟢 Pulls the latest changes from the remote `main` branch.

---

## 🔄 8. **Cloning and Fetching**

```bash
git clone [url]
```

🟢 Clone the remote repo to your local machine.

---

```bash
git clone [url] [folder-name]
```

🟢 Clone into a folder with a specific name.

---

```bash
git fetch
```

🟢 Download changes from remote **without merging** them into your local branch.

---

## ⏪ 9. **Undoing Changes – Reset, Revert, Restore**

```bash
git reset --hard [commit-hash]
```

🛑 Removes all commits and changes after the given commit.
❗ WARNING: Deletes everything after that commit.

---

```bash
git reset --soft [commit-hash]
```

🟢 Moves HEAD to the commit, but **keeps all changes staged**.

---

```bash
git reset --mixed [commit-hash]
```

🟢 Moves HEAD to commit, **unstages files**, keeps code intact.

---

```bash
git reset --hard HEAD~1
```

🛑 Deletes the **last commit** entirely.

---

```bash
git reset HEAD~1
```

🟢 Removes last commit but keeps changes in working directory.

---

```bash
git revert [commit-hash]
```

🟢 Creates a new commit that **reverses** the changes of the selected commit.
✅ Safe for team collaboration.

---

```bash
git restore --staged style.css
```

🟢 Unstages the file (removes it from commit) but **keeps the file**.

---

## 💾 10. **Stashing (Temporarily Save Work)**

```bash
git stash
```

🟢 Temporarily saves your uncommitted changes.

---

```bash
git stash drop 1
```

🟢 Delete a specific stash (use `git stash list` to find ID).

---

```bash
git stash clear
```

🟢 Delete **all** saved stashes.

---

```bash
git stash pop
```

🟢 Restore the most recent stash and **remove it** from stash list.

---

## 🍒 11. **Cherry-Pick**

```bash
git cherry-pick [commit-hash]
```

🟢 Apply the **changes of one commit** from one branch to another.

---

## 🚫 12. **.gitignore**

Create a file named `.gitignore` and add files/folders to ignore:

```
node_modules/
style.css
```

```bash
git commit -m "add style.css file in .gitignore"
```

🟢 This will ensure Git no longer tracks ignored files.

---

## 🔁 13. **One-Liner Commit and Push**

```bash
git commit -m "message" && git push
```

🟢 Combine commit and push in a single line.

---

## 🔄 14. **Daily Workflow for Practice & Real Projects**

```bash
git init
git add .
git commit -m "Initial Commit"
git branch feature
git switch feature
git push -u origin feature
```

---

### ✅ Pro Tip for Memorization:

🔤 Think of Git like **writing a story**:

* `init` → Start notebook
* `add` → Select what to write
* `commit` → Save the page
* `push` → Share it to the world
* `branch` → Start a side story
* `merge` → Join the stories
* `reset/revert` → Erase or fix mistakes

---


