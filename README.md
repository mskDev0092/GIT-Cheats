# GIT-Cheatsheet
>list of most important git commands &amp; common Git commands to consider memorizing

# 1. Init: Create a new repository on your local machine 

> If you’re starting a project on your own from scratch, one of the first things you need to do is create and initialize your local repo.

> You won’t be able to run the other commands until you use git init, so start here. This command creates a .git subdirectory locally, which will have all the necessary metadata for your local repo moving forward.

> Command:
```shell
git init 
```
Or transform a current directory into a Git repo with:
```shell
git init <directory>
```
# 2. Config: Configure your local and global values 

>git config is a convenient way to configure personal info, settings, and preferences globally, locally, and system-wide. The most common use case for git config is to set your contact info and name. This ensures other developers know who submits what code.

> Command:
```shell
git config --global user.email <your-email> or git config --global user.name "your name".
```

# 3. Clone: Get source code from your remote repo 

> If you’re contributing to an existing project, the clone command creates a copy of your remote rep (generally via GitHub, GitLab, or Bitbucket) that you can make changes to without overwriting the master version.

> This command gives you access to a copy of the source code on your local machine that can be changed without compromising the master.

> To download your project, use this in your terminal:
```shell
git clone <repo URL> 
```
# 4. Branch: Create a local work environment 

> When you’re working with other developers on the same project, branches allow you to both modify and reference copies of the same sections of source code and merge the differences later on.

> This avoids the errors and broken code/features that would happen if you were both making changes to the same code at the same time.

> Create a new local branch with:
```shell
git branch <branch-name>
```

> Push this local branch to the remote repo with:
```shell
git push -u <remote> <branch name> 
```
> View existing branches on the remote repo with:
```shell
git branch or git branch—list 
```
> And delete a branch with:
```shell
git branch -d <branch-name> 
```

# 5. Checkout: Switch branches and inspect files, commits 

> git checkout lets you move between the master branch and your copies locally and can be used to inspect file and commit history.

> By default, the local clone of your master branch is the one that you’ll start out in. To make changes to a different local branch, you’ll need to run the command to switch between them. Note: Before you switch, make sure that you commit or stash any in-progress changes; otherwise, you may run into errors when pushing changes to the remote repo.

> Command:
```shell
git checkout <name of your branch> 
```
> Or create a use this to create a new branch and switch to it with one command:
```shell
 git checkout -b <name-of-your-branch>
```
# 6. Add: Include local changes in your next commit 

> git add ensures that changes across your branch, or singular files changes, are staged for the next commit. While the verbiage is a little confusing, a commit actually includes two steps: stage and commit.

> The git add command essentially queues your changes to be included when you commit at the local level.

> Command:

> For single file changes use:
```shell
git add <file>  
```
Or use the below to stage all changes if you’ve made a bunch of them:
```shell
git add -A
```
# 7. Diff: Quickly compare unstaged files before committing 

> Has it been a minute since you last made changes to your project? Have you been flying through code and everything is > blurring together? You’re in luck: The git diff command lets you quickly compare files that aren’t staged yet and see > where the differences lie.

> Command:

> For all local files:
```shell
git diff  
```
> Or, for changes to specific files:
```shell
 git diff <file> 
```
# 8. Status: Check the information in the branch 

> git status is a quick way to see the status of your local repo and staging area. This command shows a quick picture of 
> any changes that haven’t been staged and any files that are being overlooked by Git.

> Command:
```shell
git status 
```
> And if you want to remove a change from your next commit, you can do so with
```shell
git reset HEAD <file>....
```
# 9. Commit: Save changes at a checkpoint 

> Commit essentially acts as your local save point for changes made to a local branch or repo.

> After you’ve made your changes, staged them for commit using git add, and checked to make sure no changes to the >remote repo will conflict with your local changes, use git commit to create a checkpoint you can refer back to.

> Additionally, make sure to replace the “commit message” below with a succinct but descriptive summary of the changes >you made.

> Command:
```shell
git commit -m “commit message” 
```
> And if you want to see the information about a previous commit, use this to display metadata and content changes:
```shell
 git show 
```
# 10. Pull: Get updates from your remote repo 

> git pull is a combination of the git fetch (which downloads all the changes everyone else has been working on from the remote repo) and the git merge (which integrates those changes into your local code) commands.

> Before you push changes to your remote repo, you need to make sure that the updates you’ve made don’t conflict with > > the code changes that may have been added by other developers since you first ran the clone command.

>Command:
```shell
git pull <remote>
```
# 11. Merge: Combine your local branch with the master version 

> Congratulations! If you’ve made it to this step, it means you’ve completed the development in your branch, and everything is working smoothly. Now, you can use git merge to combine your local branch with your local parent branch (dev or master).

> Note: Before you do this step, make sure you’ve compared your local branch with the remote repo with git pull one    > last time.

> Command:
```shell
git merge 
```
> You can specify what branch you want to merge to with:
```shell
git checkout dev 
```
> Update your local dev branch with:
```shell
git fetch 
```
> Or merge your feature branch into another specific branch with:
```shell
git merge <branch name>
```
# 12. Push: Send updated code to your team 

> git push delivers your commits to the remote repo, so the rest of your team can review and test them. This command   > only uploads changes that were staged (via git add) and committed.

> Once you’ve committed your source code changes, you can send your updated project to your team’s remote server repo. > The point of doing this is to prompt your team to do a QA check on your work and merge it on your behalf.

> Command:
```shell
git push <remote> <branch-name> 
```
> Or (for newly created branches):
```shell
git push —set-upstream <remote> <name-of-your-branch> 
```
> Or:
```shell
git push -u origin <branch_name>
```
# 13. Revert: Undo changes locally or remotely 

> What happens if you made a mistake in your code, or you need to undo a change that’s causing error or conflict?       > First, don’t panic. Second, use git revert. This command will undo a previous commit without erasing the commit       > history, making it easy for you and your team to see the complete code timeline.

> git revert makes it easy to undo a change. You can do this in a number of ways in Git, but revert is the safest,     > especially if you’re modifying your remote repo and want to make sure you’re not deleting code your teammates may  need.

> Command:
```shell
git revert 
```
> First, review the master branch commit history with
```shell
 git log—oneline 
```
> Then specify the commit’s hash code with
```shell
git revert <hash>
```




