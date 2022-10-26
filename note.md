#Github Notes
#Reverting Git Commits


#Add & Commit File Automatically
 $ git commit -am "commit message." 
#Delete branch
 $ git branch -d branch-name
#Pull content changes from a brachline
 $ git pull origin branch-name
#Merge branch with the main branch - you MUST be inside main to perfom merge - alter only one branch at time to avoid merge conflicts
 $ git merge branch-name
#Push changes to branchline - web UI will provide "Compare & pull request" option. -> ensure pull request is made -> merge pull request 
 $ git push -u origin branch-name 
#Compare Changes between branches
 $ git diff 	
 $ git diff main
#Create New Branch
 $ git checkout -b new-branch-name
 #Navigate into Branch
 $ git checkout branch-name
 $ git checkout main
#Display Current Branch of remote repository
 $ git bramch

#What is a Pull Request? -> a request for code from one repository to be put into a bramchline of another repository.

#Git Branching
#Master Branch [main] - naming convention for default branch

#Github Workflow 
	write-code -> commit-changes -> pull-request
#Github workflow - Local
	write-code -> stage-changes -> commit-changes -> push-changes -> pull-request

#SSH Key Administration
#Generating a SSH Key
 $ ssh-keygen -t rsa -b 4096 -C "doemagne@gmail.com"
#Copy to Clip board
 $ pbcopy < ./path/to/file/name
#Start SSH Agent in the background
 $ eval "$(ssh-agent -s)"
#Add Key to the SSH Agent
 $ ssh-add -K ./path/to/git/key.pub


#Basic Concepts
Twitter
Intagram
Github
Youtube

#What is Git?
Git is a Tool for Version Control
	Repository
		Content Changes
		we make further changes to components within our code
			Who What When Where Why - 
			explaining / revealing : 
				what was done by 
					who 
						when no reason 
							why could be found any 
								where and 
									how it was revealed.
		whatever was committed can be reverted
	Revert Back to State
	Track History
	Work Collaborativvely with other people
	Distributed Version Control Systems

	
#Clone - Bring a repository that is hosted somewhere like Github and in to a folder on your local machine.
#Add - track your files and changes in git
#Commit - Save your files in git
#Push - Upload to remote repository
#Pull - Download Changes from remote repository to your local machine
#

##Creating a Remote Repository
 $ echo "# tennis" >> README.md
 $ git init
 $ git add README.md
 $ git commit -m "first commit"
 $ git branch -M main
 $ git remote add origin https://github.com/doemagne/tennis.git
 $ git push -u origin main

#…or push an existing repository from the command line
 $ git remote add origin https://github.com/doemagne/tennis.git
 $ git branch -M main
 $ git push -u origin main

#Push updates to the remote repository -u set the default upstream branch name $ git push - can be used afterwards without specifying branch 
 $ git push -u origin main
#Create stage and commit changes to stage
 $ git commit -m "commited update files."
#Specify and add file to track
 $ git add README.md
#Track All files
 $ git add .
#Status of Remote Repository
 $ git status 
_>
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md
	modified:   note.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.note.md.swp
	index.html

no changes added to commit (use "git add" and/or "git commit -a")
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
#Ignore Files & Directories
___

## Always have a .gitignore file inside your repo directory
## to ignore directories list the directory name/ in the .gitignore file eg:
##Directories
ignore/directory/name/
logs/
keys/
private/
##Files
*.log
main.log


___
**
##
##Restore File to earlier version - without Undoing a Commit - from $ git log --oneline
 $ git restore --source HEAD~1 ./path/to/file/name

##Clean Uncommmited Changes
 $ git clean -fd
##Undo all Local Changes
 $ git restore .
##Rmoving an Added file from repository
 $ git restore --staged addedfilename
##View detailed commits history - all files in a commit
 $ git ls-tree HEAD~1
##Show detailed commit history - from $ git log --oneline
 $ git show d601b
 $ git show HEAD
 $ git show HEAD~1
 $ git show HEAD~1:./path/to/file/name

main is the main branch line in git
##View Commit History
 $ git log
##View Commit History in Short Summary
 $ git log --oneline --reverse
 $ git log --oneline
##Manual Compare with diff tool
 $ git difftool 
##Compare Local Directory
 $ git diff 
##Compare Stages
 $ git diff --staged a/filea b/fileb
##Removed cached directory recirsively
 $ git rm --cached -r directoryname
##Remove Commited Ignore file
 $ git rm --cached filename
#Move / Rename Repo Contents
 $ git mv filename newname
##Remove file in repository
 $ git rm filename
##List all files in the staging area
 $ git ls-files
##Commit all untracked Changes/Files
 $ git commit -a -m " Removed unused code. "
##Check directory for untracked files/changes
 $ git status
##Status Summary
 $ git status -s
##Propose for Next Commit - takes snapshot [state] of contents.
 $ git commit -m " Removed unused code. "
 $ git commit -m " Committed a bug fix. "
 $ git commit -m " Initial repo commit. "
##Nominate files or directory to add to the repository.
 $ git add .
 $ git add filename
##Init Empty Repo
 $ git init
##Configure Git Settings via Terminal
##Windows
 $ git config --global core.autocrlf true 
##Unix
 $ git config --global diff.tool vscode
 $ git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
 $ git config --global core.autocrlf input
 $ git config --global -e
 $ git config --global user.name "doemagne"
 $ git config --global user.email doemagne@gmail.com
 $ git config --global core.editor "code --wait"
##Git Version Currently Installed
 $ git --version

Tool

