tags:  #Git #CS 
# Git `fas:GitAlt`
Author: Dhruv Jha

---
## Basic command cheats:
### Configuring user information
- `git config --global user.name "<firstname lastname>"`
- `git config --global user.email "<email>"`

### Master to main `fas:Procedures`
You ==really want to== do this step.
- `git branch -m master main`
For a more permanent change
- `git config --global init.defaultBranch main`

### Initialisation `fas:InfoCircle`
- Initialize a git repository
	`git init`
- Clone a repo from a specific URL
	`git clone`
	sometimes there might be a few git sub-modules which you need to import as well
	`git cline --recursive <url>`
- 
### Stage & Snapshot `ris:CameraLens`
- Show modified files in working directory
	`git status`
- Add a file as it looks like now for your next commit (staging it)
 	`git add <file>`
- Un-stage a file while retaining the changes in working directory
	`git reset <file>`
- See differences in files
	`git diff` (files not on stage)
	`git diff --staged` (files on stage)
- Committing staged changes
	`git commit -m "<descriptive message>"`
	
### Branch and Merge `ris:GitBranch`
- list all your branches
	`git branch` 
- Create a new branch at the current commit
	`git branch <branch_name>`
- Delete a branch
	`git branch -d <branch_name>`
- Checkout another branch in the directory
	`git checkout <branch_name` or `git switch <branch_name>`
- Merge some branch into currently selected branch
	`git merge <branch_name>`
- See all commits in the current branch's history
	`git log`

### Moving around `ris:DragMove`
- Move to another branch in the directory
	`git checkout <branch_name>` or `git switch <branch_name>`
- Move to another commit
	`Note: This will lead to a detached Head state`
	`git checkout <commit_hash_id>`

### Remote repo stuff `fas:Github`
- Adding a remote repo 
	`git remote add <alias usually origin> <url of the repo>`
- Verifying if the remote works
	`git remote -v`
	Expected output:
	`> origin  https://github.com/user/repo.git (fetch)`
	`> origin  https://github.com/user/repo.git (pull)`
- Rename remote (Convention calls it origin)
	`git remote rename <old-name> <new-name>`
- Removing a remote repo
	`git remote rm`
- Pushing Changes
	`git push <alias> <branch-name>`
- Getting changes from the remote
	`git pull `
