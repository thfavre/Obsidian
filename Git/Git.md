# Learn Git :
- https://learngitbranching.js.org/

# Info :
- *master* is getting rename in *main*

# Commands :
## Commits : 
Save all staged changes, along with a brief description from the user.
`git commit`

## Branching
They are simply pointers to a specific commit -- nothing more.
A branch essentially says "I want to include the work of this commit and all parent commits."
`git branch <branchName>`
### Checkout
This will put us on the new branch (before committing our changes).
`git checkout <branchName>`
(Replaced with the `git switch` command)

## Merging
To combine the work from two different branches together. This will allow us to branch off, develop a new feature, and then combine it back in.
1. `git merge branchName` It will merge branchName in the current branch (ex. main) (It create a commit containing branchName and main).
## Rebase
It takes a set of commits, "copies" them, and plops them down somewhere else.
It is cleaner than merging (make a linear tree).
`(from branchName) git rebase main`
# Work :
1. Create a new branch to work on : `git branch <name>`
2. Go on the new branch (checkout) `git checkout <name>`
3. 


___
# .gitignore
create this file inside a git repertory and write the file you don't want
### Creation :
```shell
vim .gitignore
```
```.gitignore
.DS_Store
```

