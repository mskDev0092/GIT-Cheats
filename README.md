# GIT-Cheats
list of most important git commands &amp; common Git commands to consider memorizing

#1. Init: Create a new repository on your local machine 

>If you’re starting a project on your own from scratch, one of the first things you need to do is create and initialize your local repo.

>You won’t be able to run the other commands until you use git init, so start here. This command creates a .git subdirectory locally, which will have all the necessary metadata for your local repo moving forward.

Command:
```shell
git init 
```
Or transform a current directory into a Git repo with:
```shell
git init <directory>
```
#2. Config: Configure your local and global values 

>git config is a convenient way to configure personal info, settings, and preferences globally, locally, and system-wide. The most common use case for git config is to set your contact info and name. This ensures other developers know who submits what code.

Command:
```shell
git config --global user.email <your-email> or git config --global user.name "your name".
```

#3. Clone: Get source code from your remote repo 

>If you’re contributing to an existing project, the clone command creates a copy of your remote rep (generally via GitHub, GitLab, or Bitbucket) that you can make changes to without overwriting the master version.

>This command gives you access to a copy of the source code on your local machine that can be changed without compromising the master.

>To download your project, use this in your terminal:
```shell
git clone <repo URL> 
```
#4. Branch: Create a local work environment 

>When you’re working with other developers on the same project, branches allow you to both modify and reference copies of the same sections of source code and merge the differences later on.

>This avoids the errors and broken code/features that would happen if you were both making changes to the same code at the same time.

>Create a new local branch with:
```shell
git branch <branch-name>
```

>Push this local branch to the remote repo with:
```shell
git push -u <remote> <branch name> 
```
>View existing branches on the remote repo with:
```shell
git branch or git branch—list 
```
>And delete a branch with:
```shell
git branch -d <branch-name> 
```

