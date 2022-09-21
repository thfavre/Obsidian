# Git
## Commit : 
```shell
git clone URL choseFolderNam
copy paste all needed folder inside choseFolderNam
cd choseFolderNam
git add ex*  # ex to not put .DS_Store
git commit -m "it is the comment section"
git push 
```
### Download files
```shell
git pull
```

### See all files 
```shell
git ls-files
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


## Other solution :
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
