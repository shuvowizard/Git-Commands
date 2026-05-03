
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
- **Remote**: A version of your repository hosted on a server (e.g., GitHub).
- **HEAD**: A pointer to the current branch/reference you're on.

---

## 🛠️ Installation
- **GitHub Desktop:** 🔗 [desktop.github.com](https://desktop.github.com/)
- **Git for All Platforms:** 🔗 [git-scm.com](https://git-scm.com/)
- **Verify Installation:** Run `git --version` to check if Git is installed.

---

## ⚙️ Git Configuration
_Configure user information for all local repositories_

| Command                                            | Description                                  |
| -------------------------------------------------- | -------------------------------------------- |
| `git config --global user.name "[name]"`           | Sets the name attached to your commits       |
| `git config --global user.email "[email]"` | Sets the email attached to your commits      |
| `git config --list`                                | Lists all current Git configuration settings |
| `git config --get user.name`                       | Gets the global username                     |
| `git config --get user.email`                      | Gets the global user email                   |
| `git config --unset [key]`                         | Remove a specific config value (local repo)  |
| `git config --unset --global [key]`                | Remove a global config value                 |
| `git config --unset --local [key]`                 | Remove a local repo config value (default)   |
| `git config --unset --global user.email`           | Example: Remove global email setting         |
| `git config --unset --global user.name`            | Example: Remove global username setting      |

---

## 🚀 Getting & Starting Projects

_Initialize or clone repositories_

| Command                           | Description                                |
| --------------------------------- | ------------------------------------------ |
| `git init`                        | Initialize a new local Git repository      |
| `git clone [url]`                 | Create a local copy of a remote repository |
| `git clone [url] --branch [name]` | Clone a specific branch                    |

---

## 📦 Stage & Snapshot

_Working with snapshots and the Git staging area_

### 🔍 File Inspection (Shell Commands)

| Command           | Description                                       |
| ----------------- | ------------------------------------------------- |
| `ls` _(Shell)_    | List all files                                    |
| `ls -a` _(Shell)_ | List all files, including hidden ones             |
| `git status`      | Show the current status of your working directory |
| `git status -s`   | Check status in short (single-line) format        |

### ➕ Adding Files

| Command                        | Description                                                          |
| ------------------------------ | -------------------------------------------------------------------- |
| `git add [file]`               | Add a file to the staging area                                       |
| `git add -A` / `git add --all` | Stage all changes (new, modified, deleted)  in the entire repository |
| `git add .`                    | Stage all changes in current directory & subdirectories              |
| `git add *.txt`                | Add only `.txt` files to staging                                     |

### 💾 Committing Changes

| Command                             | Description                                                |
| ----------------------------------- | ---------------------------------------------------------- |
| `git commit -m "[message]"`         | Commit staged changes with a message                       |
| `git commit -a -m "[message]"`      | Stage & commit all **tracked** files                       |
| `git commit --amend -m "[new msg]"` | Amend/rewrite last commit message                          |
| `git commit --amend`                | Add forgotten files or edit to the last commit.            |

### 🗑️ Removing Files

| Command                  | Description                                             |
| ------------------------ | ------------------------------------------------------- |
| `git rm [file]`          | Remove file from working dir & staging                  |
| `git rm -f [file]`       | Forcefully remove a file                                |
| `git rm --cached [file]` | Remove from version control  (untrack) but keep locally |
| `git rm -r [folder]`     | Remove a directory recursively                          |

### 🔄 Reset & Undo

| Command                         | Description                                            |
| ------------------------------- | ------------------------------------------------------ |
| `git reset`                     | Unstage all files without changing working directory   |
| `git reset [file]`              | Unstage a specific file                                |
| `git reset --soft [commit-id]`  | Undo commit, but keep changes in **staging**           |
| `git reset --mixed [commit-id]` | Undo commit, keep changes in **working dir** (default) |
| `git reset --hard [commit-id]`  | ⚠️ Go back to a commit, discard everything after       |
| `git checkout -- [file]`        | Discard local changes in a file (pre-Git 2.23)         |
| `git restore [file]`            | Restore file to last commit (Git 2.23+)                |

---

## 🌿 Branching & Merging

_Isolating work in branches, changing context, and integrating changes_

### 📋 Branch Management

| Command                    | Description                          |
| -------------------------- | ------------------------------------ |
| `git branch`               | List local branches (`*` = current ) |
| `git branch -a`            | List all local & remote branches     |
| `git branch -r`            | List only remote branches            |
| `git branch [name]`        | Create a new branch                  |
| `git branch -d [name]`     | Delete a local branch (safe)         |
| `git branch -D [name]`     | Force delete a local branch          |
| `git branch -m [new-name]` | Rename current branch                |
| `git branch -v`            | List branches with last commit info  |

### 🔄 Switching Branches

| Command                    | Description                                         |
| -------------------------- | --------------------------------------------------- |
| `git switch [branch]`      | Switch to another branch _(recommended, Git 2.23+)_ |
| `git switch -c [branch]`   | Create & switch to new branch                       |
| `git checkout [branch]`    | Switch to branch _(legacy, still works)_            |
| `git checkout -b [branch]` | Create & switch to new branch _(legacy)_            |

### 🔀 Merging & Rebasing

| Command                             | Description                                       |
| ----------------------------------- | ------------------------------------------------- |
| `git merge [branch]`                | Merge a branch into current branch                |
| `git rebase [branch]`               | Reapply commits on top of another branch          |
| `git rebase -i [commit-id]`         | Interactive rebase: edit, squash, reorder commits |
| `git branch --merged`               | List branches already merged into current         |
| `git branch --no-merged`            | List branches NOT merged yet                      |
| `git push origin --delete [branch]` | Delete a remote branch                            |

---

## 🌐 Remote & Collaboration

_Retrieving updates, managing remotes, and pushing changes_

### 🔗 Remote Connection Management

_Add, rename, or remove remote repository links_

|Command|Description|
|---|---|
|`git remote -v`|View configured remote repositories|
|`git remote add origin [url]`|Add a remote repository (SSH or HTTPS)|
|`git remote rename old new`|Rename a remote connection|
|`git remote remove origin`|Remove a remote connection from local project|

### 📥 Fetching & Pulling

_Get updates from remote without overwriting local work_

|Command|Description|
|---|---|
|`git fetch origin`|Download changes from remote (no merge)|
|`git fetch --all`|Fetch from all configured remotes|
|`git pull`|Fetch + merge changes into current branch|
|`git pull --rebase`|Fetch + rebase (keeps linear history)|
|`git pull origin [branch]:[local-branch]`|Pull remote branch into a specific local branch|

### 📤 Pushing & Upstream

_Send local commits to remote repository_

| Command                       | Description                                                    |
| ----------------------------- | -------------------------------------------------------------- |
| `git push origin [branch]`    | Push a branch to remote                                        |
| `git push -u origin [branch]` | Push & set upstream (remembers tracking for future `git push`) |
| `git push`                    | Push current tracked branch                                    |
| `git push --force`            | ⚠️ Force push (overwrites remote history)                      |
| `git push --force-with-lease` | Safer force push (fails if remote has new commits)            |


---


## 🏷️ Tags & Releases

_Marking a specific version of the project (e.g. `v1.0`, `v2.1.0`)_

| Command                            | Description                                            |
| ---------------------------------- | ------------------------------------------------------ |
| `git tag`                          | List all tags                                           |
| `git tag [name]`                   | Create a lightweight tag                               |
| `git tag -a [name] -m "[message]"` | Create an **annotated tag** (recommended for releases) |
| `git show [name]`                  | Show details of a specific tag                         |
| `git push origin --delete [name]`  | Delete a remote tag                                    |
| `git tag -d [name]`                | Delete a local tag                                     |
| `git push origin [name]`           | Push a specific tag to remote                          |
| `git push origin --tags`           | Push all local tags to remote                          |
| `git checkout [tag]`               | Switch to a tagged version (detached HEAD mode)         |

---

## 🔍 Inspection & Comparison

_Examining logs, differences, and commit information_

### 📜 Commit History

| Command                           | Description                                           |
| --------------------------------- | ----------------------------------------------------- |
| `git log`                         | View full commit history                              |
| `git log --oneline`               | Concise one-line commit history                       |
| `git log --oneline --graph --all` | Visual branch history tree                            |
| `git reflog`                      | View all references (including dropped commits)       |
| `git log -p -1`                   | View details + diff of most recent commit             |
| `git log --author="[name]"`       | Filter commits by author                              |
| `git log -- [file]`               | Show history for a specific file                      |
| `git shortlog -s -n`              | List contributors with commit count **(sorted by #)** |
| `git shortlog -s -n --all`        | Same as above, but includes **all branches**          |
| `git shortlog -s -n [branch]`     | Contributor stats for a specific branch               |


### 🔎 Comparing Changes

| Command                            | Description                        |
| ---------------------------------- | ---------------------------------- |
| `git diff`                         | View unstaged changes              |
| `git diff --staged`                | View staged changes vs last commit |
| `git diff [branch1]..[branch2]`    | Compare two branches               |
| `git diff [commit-id] [commit-id]` | Compare two commits                |
| `git diff HEAD~1 HEAD`             | Compare last two commits           |
| `git show [commit]`                | Show details of a specific commit  |
| `git blame [file]`                 | Show who last modified each line   |

---

## 🛠️ Stash (Temporary Storage)

_Temporarily store changes for later use_

| Command                                | Description                             |
| -------------------------------------- | --------------------------------------- |
| `git stash` / `git stash push`         | Temporarily stash tracked changes       |
| `git stash push -m "message"`          | Stash with a descriptive message        |
| `git stash -u` / `--include-untracked` | Stash all tracked + untracked files     |
| `git stash -a` / `--all`               | Stash all (tracked, untracked, ignored) |
| `git stash list`                       | List all stashed changes                |
| `git stash show`                       | Preview latest stash                    |
| `git stash show -p [stash-id]`         | View full diff of a specific stash      |
| `git stash pop`                        | Apply & remove latest stash             |
| `git stash apply`                      | Apply latest stash without removing it  |
| `git stash apply [stash-id]`           | Apply stash without removing it         |
| `git stash drop [stash-id]`            | Delete a specific stash                 |
| `git stash clear`                      | Remove all stashes ⚠️                   |

---

## 🛡️ Troubleshooting

_Resolve common issues and recover from mistakes_

| Command                                 | Description                                     |
| --------------------------------------- | ----------------------------------------------- |
| `git merge --abort`                     | Abort a merge with conflicts                    |
| `git rebase --abort`                    | Abort an ongoing rebase                         |
| `git rebase --continue`                 | Continue after resolving rebase conflicts       |
| `git revert [commit]`                   | Create new commit that undoes a previous one    |
| `git revert --no-commit [start]..[end]` | Revert multiple commits at once                 |
| `git clean -n`                          | Preview untracked files to be deleted (dry run) |
| `git clean -f`                          | Remove untracked files permanently              |
| `git clean -fd`                         | Remove untracked files + directories            |
| `git fsck`                              | Verify repository integrity                     |
| `git bisect start`                      | Start binary search to find buggy commit        |

---

## 🙌 Contributors
- [@shuvowizard](https://www.github.com/shuvowizard)

## 🌐 Connect with Me
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/msshuvo07)  
[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/msshuvo07/)  
[![Facebook](https://img.shields.io/badge/facebook-1DA1F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/shuvowizard/)  
[![Instagram](https://img.shields.io/badge/instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/shuvowizard/)

<div align="center">

🎉 Happy Coding with Git! 🚀
</div>