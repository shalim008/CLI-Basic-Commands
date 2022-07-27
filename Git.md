# Basic Git Command

### Git Status Check -
git status

git init

### Add VS Git Ignore File (.gitignore) - 
bin

obj

appsettings.json

*.db

### Create Repository in your git account
git remote add origin https://github.com/shalim008/scommerce.git

git push -u origin master

### Follow these steps to upload new project to Github
1) git init
2) git add .
3) git commit -m "Add all my files"
4) git remote add origin https://github.com/shalim008/ERP_ARCH.git Upload of project from scratch require git pull origin master.
5) git pull origin master
6) git push origin master
 
 
 
### Follow these steps to commit project changes to Github
   git add -A or git add .

   git commit -m "Comment here.." 

   git pull origin master

   git push origin master
 
### Create a Branch to Github

Git branch yourbranchname = To create new branch

Git branch = to display all available branch

Git checkout yourbranchname = To change our branch. 

### Marge or Pull code from one branch to another (ex-master) branch:
Git checkout master = to select master branch.

Git pull origin master = to pull master branch first

Git branch --merged

Git merge yourbranchname = we are already select master branch so code merge with master branch,

Git push origin marster = push code in master branch

### Push code in specific branch:
git add -A = Add everything from working directory to stage.

git commit -m "Comment here.." = Commit code from Stage to Server.

Git push -u origin yourbranchname

Git pull

Git push
 
### Resolve Conflict to Github
If you dont want to merge the changes and still want to update your local then run: git reset // reset all commit
 

 


### Deleting a Branch:

Git branch -d yourbranchname = this command delete repo locally

Git branch -a

Git push origin --delete yourbranchname = to delete the branch from server also
 
### Others
Git reset = All Stage file are clear and available in working directory. 
git log = To track change history
Git clone servpath.git .= to clone server repository into current directory.
git remote -v = display all repo url
git branch -a = display all branch
git diff = to show code changes





