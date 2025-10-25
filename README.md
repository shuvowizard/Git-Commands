# 🔄 Git Commands Cheatsheet

## 👨🏻‍💻 What is Git?

**Git** is a free and open-source **distributed version control system** that manages everything GitHub-related on your local computer.  
It’s an essential tool for developers to **track, manage, and collaborate** on code efficiently.  
Version control ensures multiple developers can work on the same project simultaneously without conflicts and with a structured workflow.

---

## 📚 Key Concepts
- **Repository**: A storage space for your project’s files and history.
- **Commit**: A snapshot of changes in your project.
- **Staging Area**: A temporary area to prepare files for a commit.
- **Branch**: A parallel version of your repository for isolated work.

---

## 🛠️ Installation
- **GitHub Desktop:** 🔗 [desktop.github.com](https://desktop.github.com/)
- **Git for All Platforms:** 🔗 [git-scm.com](https://git-scm.com/)
- **Verify Installation:** Run `git --version` to check if Git is installed.

---

## ⚙️ Git Configuration
_Configure user information for all local repositories_

| Command | Description |
| -------- | ------------ |
| `git config --global user.name "[name]"` | Sets the name attached to your commits |
| `git config --global user.email "[email address]"` | Sets the email attached to your commits |
| `git config --list` | Lists all current Git configuration settings |
| `git config --get user.name` | Gets the global username |
| `git config --get user.email` | Gets the global user email |

---

## ⚙️ Getting & Starting Projects
_Initialize or clone repositories_

| Command | Description |
| -------- | ------------ |
| `git init` | Initialize a new local Git repository |
| `git clone [url]` | Create a local copy of a remote repository |

---

## ⚙️ Stage & Snapshot
_Working with snapshots and the Git staging area_

| Command | Description |
| -------- | ------------ |
| `ls` | List all files |
| `ls -a` | List all files, including hidden ones |
| `git status` | Show the current status of your working directory |
| `git status -s` | Check status in short (single-line) format |
| `git add [file-name]` | Add a file to the staging area |
| `git add -A` / `git add --all` | Stage all changes (new, modified, deleted) in the entire repository |
| `git add .` | Stage all changes in the current directory and subdirectories |
| `git add *.txt` | Add only `.txt` files to the staging area |
| `git commit -m "[commit message]"` | Commit staged changes with a message |
| `git commit -a -m "[commit message]"` | Stage and commit all tracked files |
| `git rm [file-name]` | Remove a file from the working directory and staging area |
| `git rm -f [file-name]` | Forcefully remove a file from both working directory and staging area |
| `git rm --cached [file-name]` | Remove a file from version control but keep it locally |
| `git reset` | Unstage all files without changing working directory |
| `git reset --hard` | Discard all local changes and reset to last commit |
| `git reset --hard [commit-id]` | Reset repository to a specific commit |

---

## ⚙️ Branching & Merging
_Isolating work in branches, changing context, and integrating changes_

| Command | Description |
| -------- | ------------ |
| `git branch` | List branches (the `*` marks the current branch) |
| `git branch -a` | List all local and remote branches |
| `git branch [branch-name]` | Create a new branch |
| `git branch -d [branch-name]` | Delete a local branch |
| `git branch -m [new-branch-name]` | Rename the current branch |
| `git switch [branch-name]` | Switch to another branch (recommended, introduced in Git 2.23) |
| `git checkout [branch-name]` | Switch to another branch (older command, still works) |
| `git checkout -b [branch-name]` | Create and switch to a new branch |
| `git merge [branch-name]` | Merge a branch into the current one |
| `git rebase [branch-name]` | Reapply commits on top of another branch |
| `git rebase -i [commit-id]` | Interactive rebase to edit, squash, or reorder commits |

---

## ⚙️ Sharing & Updating Projects
_Retrieving updates and pushing changes_

| Command | Description |
| -------- | ------------ |
| `git fetch origin` | Fetch changes from the remote without merging |
| `git pull` | Fetch and merge changes from the remote repository |
| `git push origin [branch-name]` | Push a branch to your remote repository |
| `git push -u origin [branch-name]` | Push and set upstream (remembers the branch) |
| `git push` | Push commits of the current tracked branch |
| `git push origin --delete [branch-name]` | Delete a remote branch |
| `git remote add origin [url]` | Add a remote repository (SSH or HTTPS) |

---

## ⚙️ Inspection & Comparison
_Examining logs, differences, and commit information_

| Command | Description |
| -------- | ------------ |
| `git log` | View commit history |
| `git log --oneline` | View concise commit history |
| `git reflog` | View all references (including dropped commits) |
| `git log -p -1` | View details of the most recent commit |
| `git diff` | View unstaged changes |
| `git diff --staged` | View staged changes vs. last commit |
| `git blame [file-name]` | Show who last modified each line of a file |
| `git show [commit-id]` | Show details of a specific commit |

---

## ⚙️ Temporary Commits (Stash)
_Temporarily store changes for later use_

| Command | Description |
| -------- | ------------ |
| `git stash` / `git stash push` | Temporarily store modified tracked files |
| `git stash -u` / `git stash --include-untracked` | Stash all changes, including untracked files |
| `git stash -a`| Stash all changes, ncluding tracked, iuntracked, and ignored files |
| `git stash save "stash message"` | Save current changes with a message |
| `git stash list` | List all stashed changes |
| `git stash show -p` | View details of the latest stash |
| `git stash show [stash-id] -p` | View a specific stash |
| `git stash pop` | Apply and remove the latest stash |
| `git stash apply` | Apply the latest stash without removing it |
| `git stash apply [stash-id]` | Apply a specific stash |
| `git stash drop` | Drop the latest stash without applying it |
| `git stash drop [stash-id]` | Drop a specific stash |
| `git stash clear` | Clear all stashes |

---

## 🛡️ Troubleshooting
_Resolve common issues_

| Command | Description |
| -------- | ------------ |
| `git merge --abort` | Abort a merge in case of conflicts |
| `git reset --soft [commit-id]` | Undo a commit but keep changes in staging area |
| `git revert [commit-id]` | Create a new commit that undoes a previous commit |

---

## 🙌 Contributors
- [@shuvowizard](https://www.github.com/shuvowizard)

## 🌐 Connect with Me
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/msshuvo07)  
[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/msshuvo07/)  
[![Facebook](https://img.shields.io/badge/facebook-1DA1F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/shuvowizard/)  
[![Instagram](https://img.shields.io/badge/instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/shuvowizard/)