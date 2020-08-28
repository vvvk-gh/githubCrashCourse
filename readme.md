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
    git add .
```

## Commit : 

commits the changes / staged files into commited stage
    
```cmd
    git commit -m "heading"
    git commit -m "heading" -m "Commit description"   
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
```

## Checkout

creates a new branch / switches to a new branch 

```cmd
    git checkout -b <branch name>  //new branch
    git checkout <branch name> // switch branch
```

## Branch

Shows the current branch you are on in / shows all the branches

```cmd
    git branch
    git branch -a //for all branches
```
## Diff

```cmd
    git diff <branchname>
```

## Pull 

Pulls all the commited code from the mentioned branch to your current repository
``cmd
    git pull <branchname>
``