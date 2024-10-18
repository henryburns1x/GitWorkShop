# Git/Github Workshop

## Your Activites

Firstly, fork this repository into your account on github. Then clone your fork to your local machine. Then open the project in VS code.

**NOTE: you can only clone to an empty directory**<br>
**using HTTPS protocol is the simplest way to clone**

### Basic git commands

1. First let's look at the existing branches in the repository. Use `git branch` command to view the existing branches. Now notice that one of these branches is marked with an asterisk **(\*)**, that branch is your current branch.

2. Create a new branch and call it `my-branch`. Then in the src directory, create a new text file `introduction.txt` and in it write down your name. **(Use git checkout -b [branch-name] to create a new branch and switch to it)**

3. Run the `git status` command. This will show you the current status of the files you're working on.

4. Add the file you created to the staging area. Now commit the changes to git, and run `git status` again. This time you should get the message indicating a clean working tree. \*\*(use `git commit -m "commit message goes here"` to make your commits)

5. Now switch back to the `main` branch. Merge the changes made in the new branch to the main

6. Still in the main, make some changes in the `introduction.txt` file. Add whatever you wish. Then add the changes to the staging area and commit.

7. run the `git log` command. Here you can notice your commit history. Each commit that you have created has an associated SHA-1 hash that references it. These hashes are important and can be used when you want to rollback changes/commits. **(press q on your keyboard to return back to terminal)**

### Remote repository

#### Pushing changes

8. Now that you have made all the changes that you want, let's push these commits onto github.

9. run the git branch command with r flag `git branch -r` to view all of the remote branches.

10. We want to push to the main branch of the remote repository. Use `git push [remote] [remote-branch]` command to push to your changes to your remote repository. Next go on github and confirm that your changes have correctly appeared on the remote repository

#### Pulling changes

11. Still on github, go into the `src` directory and use the add file button to create a new text file `anotherFile` and add some text to it. Once you are done, commit the changes.

12. Go back to your local workspace. Now let's bring that file we created in the remote repository onto our local machine. First run the git status command to check for any changes that are yet to be commited. Commit those changes if there are any. Next use the `git pull` command to bring the latest snapshot of your project that is stored on the remote repository.

#### making a pull request

Pull requests are very useful when working in teams.
In practice, you would create a pull request for every issue that you work on and wish to merge into your main codebase. Each pull request will contain all the commits that need to be pulled into main codebase and a description of the work that you have done. Then once a pull request in created, it will be reviewed by other members of your team. If the reviewers find any errors/mistakes, they will request changes that you can then work on. Otherwise they can approve and pull your changes.

13. Go into your remote repository and create a pull request from your fork to the original repository.

### Misc.

#### Merge conflicts

Merge conflicts commonly occur when trying to merge two branches that have changed the same line in a document but with different values.

scenario:

main/master branch:
department.txt; this file only contains the word sofware

git checkout -b change-dept

here department.txt is changed to only contain the word electrical

git add .
git commit -m "changed dept to electrical"
git checkout main

here in the main, change the word in the file to mechanical

git add .
git commit -m "changed dept to mechanical"
git merge change-dept <- this will create merge conflict
