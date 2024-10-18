## Git Commands

There are a number of Git commands that will be commonly used. Take the time to review each command and understand what it will do (you will need to have an idea about these commands going forward). This list is based off https://github.com/joshnh/Git-Commands. You can also get details on Git commands at https://www.atlassian.com/git/glossary.

### Getting & Creating Projects

| Command                                                           | Description                                                                                                                                                          |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git init`                                                        | Initialize a local Git repository. It creates an empty Git repository in the current directory. By default it will have one branch named master.                     |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository from the supplied _url_. This may be over HTTP, SSH, or the Git protocol, or it may be a path to another local repository |

**Both of these operations will create a working copy.**

### Basic Snapshotting

| Command                            | Description                                                        |
| ---------------------------------- | ------------------------------------------------------------------ |
| `git status`                       | Check status. Display the files changed in the index and in the    |
| working tree.                      |
| `git add [file-name.txt]`          | Add a file to the staging area (from working tree into the index). |
| `git add -A`                       | Add all new and changed files to the staging area                  |
| `git commit -m "[commit message]"` | Commit changes out of the current index.                           |
| `git rm -r [file-name.txt]`        | Remove a file (or folder)                                          |

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

### Inspection & Comparison

| Command                                    | Description                                                                                  |
| ------------------------------------------ | -------------------------------------------------------------------------------------------- |
| `git log`                                  | View changes (list the commits on the current branch)                                        |
| `git log --summary`                        | View changes (detailed)                                                                      |
| `git log --oneline`                        | View changes (briefly)                                                                       |
| `git diff [source branch] [target branch]` | Preview changes before merging                                                               |
| `git show [object]`                        | Show an object (e.g. the log information and patch for a commit, or the contents of a file). |

**This material was borrowed from Dr. Scott Fazakerley's COSC 310 lab 1**
