git init
git branch -m main #rename the current branch

git config --global user.name "sibu"
git config --global user.email "thetripples530@gmail.com"
git config --global core.editor "code --wait"

git status
git log
git log --oneline
git commit -m "msg to commit"
git push origin <branch-name>



some file present that you don't want to commit or push like .env file
Add a file named ".gitignore" and untracked file names to that file
git didn't track empty folders, so we have to add a file named ".gitkeep" in that empty folder so that git can track

