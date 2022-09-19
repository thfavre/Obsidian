# Git
## Comit

## Creer un git en local
transformer son répertoir en répertoir git  :  -> creation du .git :
```shell
git init
```

Savoir ou on en est en ce moment :
```shell
git status
```

to commit :
```shell
touch itemName  # creation of the file we want to commit
git add itemName
git commit -m "commit description"

# folder 
git add *
# ...
```

to modify a document :
```Shell
vim itemName
git status  # modified : itemName
git diff  # voir les changements qui ont été fait 
git add fileName  # to commit  (git restore fileName to discard changes in working directory)
```
```shell
git rm --cached */.DS_Store  # useful stuff
```
```shell
git reset  # remove added files
```

## .gitignore
create this file inside a git repertory and write the file you don't want
### Creation :
```shell
vim .gitignore
```
```.gitignore
.DS_Store
```

## Put on 42
```shell
git add *  # first commit all the needed files
git commit -m "decription..."

git remote add origin {insert intra repo here}
git push origin master

# to test the code :
git clone {insert intra repo here}
```
### When it don't works :
1) delete .git
2) git init
3) git remote add origin {insert intra repo here}
4) git push origin master
#### Or : 
```shell
git clone URL choseFolderNam
copy paste all needed folder inside choseFolderNam
cd choseFolderNam
git add ex*  # ex to not put .DS_Store
git commit -m "it is the comment section"
git push 
```
#### Download files
```shell
git pull
```
#### See all files 
```shell
git ls-files
```