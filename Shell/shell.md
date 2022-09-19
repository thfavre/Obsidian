# Shell

## Basic manipulation :
```bash
ctrl-a  # clear screen
pwd  # le path de ou on est
cd  # change directory (cd .. pour aller en arriere)
```

## Commands
### man :
```shell
man name  # manuel of name
```
write /blabla to search blabla in the man

### ls : 
```bash
ls  # see file / folder
ls -a  # see hidden files
ls -al  # fileName	to have infos on the file
```
#### ls -l
voir infos / droits du fichier
```bash
ls -l  # example -rwxr-x--x 1 thfavre 2022_lausanne 9 Aug 29 11:53 testShell00.txt 
``` 
Explication :
1) - : - for file, d for directory, l for links
2) thfavre can read, write and execute
3) 2022_lausanne can read not write and execute
4) the rest of the worldcan execute

### chmod : modifier les droits d'un fichier
```shell
chmod u+r fileName
# option 1 : u : user, g : group, o : other, a : all 
# option 2 : + to add, - to remove
# option 3: add the right of : r : read, w : write, x : execute

# to have rwx rw- r-- :  4+2+1 4+2+0 4+0+0 = 764 : donc 764 est pareil : 
chmod 764 fileName

chmod -h XXX  # to change the rights of the symbolic link itself rather than the file that the link point to
```



### tar : archive file 
#### Create
```shell
tar -cf fileName.tar fileName
tar -cf fileName.tar * 
```
#### Unarchive
```shell
tar -xvf fileName.tar
```

### file / folder management
```shell
mkdir folderName  # make directory (folder)
rmdir folderName # remove directory (should be empty)
rm -rf folderName  # also delete every file inside 

cat  fileName  # liste le contenu d'un ficher
cat -e  # affiche les character invisible

touch fileName  # create a file 
touch -t   201307150842 fileName  # modifie le temps
touch -ht 201307150842 linkName  # modifie le temps du link sans changer l'original 
rm filename  # remove filename

#### Links
##### hard links : ou cans think a hard link as an additional name for an existing file.
```

#### ln : Symbolic Links
##### Hard links
It is an additional name for an existing file.
```shell
ln folder1 folderName2  # cree une copie link to the original (modifier )
```
##### Soft links
It is something like a shortcut in Windows. It is an indirect pointer to a file or directory.
```shell
ln -s folder1 linkFolderName  # linked file from folder 1 to linkFolderName 
```

#### Size of a file 
```shell
dd if=/dev/zero of=fileName bs=size count=1  # create a file of size size
# or write some character inside
```

### echo
affiche 
```shell
echo HEHEHE  # output HEHEHE
```

### cat
affiche un document 
```shell
cat fileName  # -e to display invisib le character
```

### cp : copy
```bash
cp a b  # copy the a file to the b file
cp -R folderA dest
```

### find :
faire recherceh dans l
```
find startRepository
find startRepository -name text # find the file that contain text
# -type f  # f for file, d for directory
# -maxdepth Nb

```

### grep :
Search any line that contains the word in filename
```shell
grep 'word' filename  # -i : case insensitive, -R : looks also in all subdirectory, -c : display the number of time the word appears
```

### tr :transliterate
Is meant to transliterate one character with another.
Made to transform one character to an other, work strangly with the strings
```shell

```
```shell:ex
echo "test" | tr "t" "o"  # oeso
cat linux.txt | tr [a-z] [A-Z]  # show the text file with upper case 
cat domains.txt | tr -d 'text'  # delete text from the domains.txt
tr -d ' '  # remove all the ' ' from the input
```
ATTENTION :
```shell:ex
echo "test" | tr -d "te"  # ATTENTION : Ca effacera le "t" puis regarde si la prochaine lettre est un "e" et efface 
```

### sed : replace string
```shell
echo "string1" | sed s/str2/str3/  # replace all the str2 of string1 with str3
```
Usefull case : remove some character and replace it with nothing

### | : pipe
the pipe will take the outcome from the left and give it to the right
```
f1 | f2 
```
```shell:ex
ls | grep txt  # comme ls mais montre que les fichiers ayants txt
ls -l | sed -n 'n;p' # ls -l the odd lines
```

### > : redirection
change the standard output
```shell
command > fileName  # the output will be in fileName
```
```shell:ex
ls > res.txt
```

