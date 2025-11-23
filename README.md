git init
git branch -m main #rename the current branch



git status
git log
git log --oneline
git commit -m "msg to commit"
git push origin <branch-name>



some file present that you don't want to commit or push like .env file
Add a file named ".gitignore" and untracked file names to that file
git didn't track empty folders, so we have to add a file named ".gitkeep" in that empty folder so that git can track.

You chnaged something and checked the changes by using 
git status
git add <file-name>
git restore <file-name> ==> to discard the changes
git restore --staged <file-name> ==> remove file from staged area to modified area
git rm --cached <file-name>   ==> cached the file
git add <file-name> ==> to add the file to staging area
git commit -m "updated the first story"
git add . ==> stage all the changes


Musketeers of git
- Commit Object
- Tree Object
- Blob Object

HEAd :: HEAD is the pointer to the current branch that you are working on it. It points to the fastest commit in the current branch. When you create a branch it is automatically set as the HEAD of that branch.

git branch <new-branch-name>  ==> It will create a new branch but still the HEAD is with previous branch
git switch <new-branch-name>  ==> HEAD will point to new branch
git branch ==> list all the branch
git switch -c <bracnh-name>  ==> create and change to new branch
git checkout <branch-name>   ==> change to the given branch name, the branch must be present before


To merge work of side branch to main branch
1- First go to main branch  ==> git checkout main
2- Merge side branch to main  ==> git merge <branch-to-merge>

**Conflict manage**
git merge --abort
resolve manually


Rename branch ::: git branch -m <old-name> <new-name>
Delete branch ::: git branch -d <branch-name>

**Git diff**
git diff is an informative command that shows the different between two commits

git diff --staged
git diff
git diff <one-branch> <branch-to-compare>
git diff <commit-id> <commit-id-to-compare>


**Git stash**
git stash
git stash save "work in progress on X feature"
git stash list
git stash apply stash@{0}  ==> applying specific stash  
git stash pop  ==> applying and dropping the stash
git stash drop
git stash apply stash@{0} <branch-name>  ==> apply stash to a specific branch


**Git tag**
git tag ==> List all the tag
git tag <tag-name> ==> create new tag name
git tag -a chai -m "Releasem 1.0"  ==> add tag with a specifc message
git tag <tag-name> <commit-id>  ==> add tag to a specific commit
git push origin xxxx:tag-name  ==> add while pushing


**Git rebase**
git rebase is a powerful feature used to change the base of a branch. It effectively allows you to move a branch to a new static point, usually different commit. 


git switch -c pinkmode
ensure you are on the branch you want to rebase, here you must be present in pinkmode to rebase master branch.
git rebase <branch-name>
git log --oneline ==> you wont get any extra commit msg in logs after rebase

**Git reflog**
It is a simple informative command to see the history of commits

git log --oneline
git log --name-only
git log <branch-name>  ==> to see commit history of a perticular branch
git reflog
git reflog <commit-hash>
git reset --hard HEAD@{1}
git reset --hard <commit-id>

**Github push** 
git remote -v
git remote add origin https://github.com/satyasiba001/LearnGit.git
git remote add upstream https://github.com/satyasiba001/LearnGit.git
git add .
git commit -m "added"
git push --set-upstream origin main ==> set default branch to push
git push  or  git push origin <branch-name>

**Git fork**
Click “Fork” → choose your account → GitHub creates your own copy.
git clone https://github.com/YOUR_USERNAME/PROJECT_NAME.git
cd PROJECT_NAME
git remote add upstream https://github.com/ORIGINAL_OWNER/PROJECT_NAME.git
git remote -v
git checkout -b feature/my-change
git add .
git commit -m "Describe your change"
git push origin feature/my-change
On GitHub → “Compare & Pull Request” → send it to the original repo.


