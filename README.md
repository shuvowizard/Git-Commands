
# 🔄 Git Commands

## 👨🏻‍💻 Git?
Git is the free and open-source distributed version control system that's responsible for everything GitHub-related that happens locally on your computer. Git is an essential tool for version control in software development. Version control is the practice of tracking and managing changes to code, allowing multiple developers to seamlessly collaborate on a project and a structured workflow for developers. Here are some Git commands that all developers need to know.

## 🛠️ Install
### GitHub Desktop
🔗 [desktop.github.com](https://desktop.github.com/)
### Git for All Platforms
🔗 [git-scm.com](https://git-scm.com/)



## ⚙️ Git Configuration
_Configure user information for all local repositories_
| Command | Description |
| ------- | ----------- |
| `git config --global user.name "[name]"` | Sets the name you want attached to your commit transactions |
| `git config --global user.email "[email address]"`  | Sets the email you want attached to your commit transactions |
| `git config --list` | List all the git configuration |


## ⚙️ Getting & Starting Projects
_Configuring user information, initializing and cloning repositories_
| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone [url]` | Create a local copy of a remote repository that already exists on GitHub |


## ⚙️ Stage & Snapshot
_Working with snapshots and the Git staging area_
| Command | Description |
| ------- | ----------- |
| `ls` | List all files |
| `ls -a` | List all files including hidden files |
| `git status` | Check status |
| `git status -s` | Check status on a single line |
| `git add [file-name]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git add --all` | Add all new and changed files to the staging area |
| `git add .` | Add all changes in the directory to the staging area |
| `git add *.txt` | Add only all .txt files to the staging area |
| `git commit -m "[commit message]"` | Commit your staged content as a new commit snapshot |
| `git commit -a -m "[commit message]"` | Add all new and changed files to the staging area with Commit the staged content |
| `git rm [file-name]` | Remove a file |
| `git rm -f [file-name]` | Forcefully remove a file |
| `git rm --cached [file-name]` | Removed from the local repository (tracking system) but remain in the working directory |
| `git reset` | Reset staging area to most recent commit, but working directory unchanged |
| `git reset --hard` | Reset staging area and working directory to most recent commit and overwrite all changes in the working directory |
| `git reset --hard [commit-id]` | Reset the staging area to the specified commit ID|


## ⚙️ Branching & Merging
_Isolating work in branches, changing context, and integrating changes_
| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch --list` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch-name]` | Create a new branch |
| `git branch -d [branch-name]` | Delete a local branch |
| `git branch -m [new-branch-name]` | Rename the current local branch |
| `git switch [branch-name]` | Switch to another branch |
| `git checkout [branch-name]` | Switch to another branch |
| `git checkout -b [branch-name]` | Create a new branch and switch to this branch |
| `git merge [branch-name]` | Merge a branch into the active branch |


## ⚙️ Sharing & Updating Projects
_Retrieving updates from another repository and updating local repos_
| Command | Description |
| ------- | ----------- |
| `git push origin [branch-name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to the remote repository (and remember the branch) |
| `git push` | Uploads all local branch commits to GitHub (remembered branch) |
| `git push origin --delete [branch-name]` | Delete a remote branch |
| `git pull	` | Updates current local working branch with all new commits from the corresponding remote branch on GitHub. |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git` | Check |


## ⚙️ Inspection & Comparison
_Examining logs, diffs and object information_
| Command | Description |
| ------- | ----------- |
| `git log` | View commit history |
| `git log --oneline ` | View commit history in briefly |
| `git reflog` | View commit history include all reference |
| `git log -p -1` | View the recent 1 commit and also view changes |
| `git diff` | View the difference between local and stage |
| `git diff --staged` | View the difference between stage and recent commit |


## ⚙️ Temporary commits
_Temporarily store modified, tracked files in order to change branches_
| Command | Description |
| ------- | ----------- |
| `git stash` | Temporary store modified tracked files |
| `git stash list` | List all stashed changes |
| `git stash show -p` | View changing stash |
| `git stash pop` | Restore the latest stashed files |
| `git stash apply [stash-id]` | Restore particular stashed files |


## 💻 Contributors

- [@shuvowizard](https://www.github.com/shuvowizard)

## 🌐 Where To Find Me

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/shuvo_wizard)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shuvowizard/)

[![facebook](https://img.shields.io/badge/facebook-1DA1F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/shuvowizard/)

[![instagram](https://img.shields.io/badge/instagram-0A66C2?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/shuvowizard/)
