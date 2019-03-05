# Git

These are a list of commands you MUST know

* git add [files]: Tell git to add the specified new or changed files to the stage (staged files are ready to commit)
	* git add \* or git add .: Dhorthand to add all new/changed files in the current directory
* git commit: Make a new snapshot of the repository (based on the changes you 'git add'ed)
	* git commit -m <message>: git commit with the given message
	* git commit -a: runs 'git add <known-files>' (where known-files are files you've already added at some point, i.e. not new)
* git push: Get any changes that have been 'git commit'ed and put them on Github (or any remote repository)
	* You can only push if you have 'git pull'ed recently
* git pull: Get any changes that were made to the remote repository and add them to your local repo
* git status: Print the status of your local repository, including files you have yet to add, files you have added but not commited, the number of commits you have made but not pushed, and the current working branch

These are some other commands you SHOULD know, but are not needed as often as those above

* git clone <repo>: Gets an existing repo on Github and makes a copy of the repo to use locally
* git init: Turn a directory on your computer into a tracked git repo
	* It is usually easier to make a repo on Github and clone when starting a project fmro scratch
* git remote: Allows you to check or configure what Github repository you are connected to
	* git remote -v: See the remote repo
* git checkout <branch>: Switch between git branches
	* git checkout -b <branch>: Create a new branch with the given name AND move any un-committed changes onto this branch as well AND checkout this branch
* git branch: list all branches, and show which one you're on
	* git branch <branch>: make a new branch with the given name BUT don't checkout that branch
* git merge <branch>: get changes made on another branch and move them into your current branch
	* This can cause merge conflict if the same line in the same file was changed in both branches. You must go into that file and choose which parts of each branch to keep

