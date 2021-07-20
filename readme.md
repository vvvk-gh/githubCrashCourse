# Git Basics Commands

## Clone 
Clone the existing remote repository code to local directory 

```cmd
    git clone <git repo url>
 ```

## Init :
Initialize an empty Git repository
    
```cmd
    git init
```

## Add :

adds the modified file/files to the staging 
    
```cmd
    git add <file name>
    git add .   # all the untracked + modified files.
    git add -u  # all the modified files
```

## Commit : 

commits the changes / staged files into commited stage
    
```cmd
    git commit -m "heading"
    git commit -m "heading" -m "Commit description"
    git commit -am "heading" // addes the modified files and commit them   
```

## Push :

push all the commited files to the remote repository

```cmd
     git push -u origin master
     -u : upstream 
```
    
If you use upstream for the first git push, from the next we only use

```cmd
     git push
``` 
and you can avoid writing long commands like git push origin master
where origin : remote name , master : branch name

## Status
status shows/tracks the status of the file

```cmd
    git status
```

## Log 
Shows the history of commits

```cmd
    git log
    git log --online 
```

## Branching

### Branches

Shows the current branch you are on in / shows all the branches

```cmd
    git branch //return current branch
    git branch -a //for all branches
    git branch -d <branchname> //deletes that branch
```

### Changing Branching

creates a new branch / switches to a new branch 

```cmd
    git checkout -b <branch name>  //new branch
    git checkout <branch name> // switch branch
```


## Diff

```cmd
    git diff # gives the diff btw the modified and the commited and once staged this cmd doesn't work
    git diff --staged   # gives the biff btw the staged and the last commit.
    git diff <filename>  # only to the specified file
```

## Pull 

Pulls all the commited code from the mentioned branch to your current repository

```cmd
    git pull <branchname>
```

## Merge

Merges the one branch committed code into an other branche 
 

```cmd
    git merge <branchname>
```

## Stages of a flie
- untracked : New file is created (U in VS code)
- unmodified : Already present in the local repo but no changes were made.
- modified : When we made some changes to the file.
- commited : Once the changes are working we will create a new version.

<img width="470" alt="stages of file" src="https://user-images.githubusercontent.com/22676852/126295806-d72cc46b-9ea0-436d-b600-aa7a3c471681.PNG">
