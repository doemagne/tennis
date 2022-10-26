#Github Notes
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
			what was done by who when no reason why could be found any where.
		whatever was committed can be reverted
	Revert Back to State
	Track History
	Work Collaborativvely with other people
	Distrobuted Version Control Systems

	
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


#
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

