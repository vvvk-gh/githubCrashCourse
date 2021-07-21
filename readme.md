# Git Basics Commands

## Clone 

Clone the existing remote repository code to local directory 

```cmd
    git clone <remote-repo-url
    git clone -b <branchname> <remote-repo-url>  #clones the specific branch code from the remote.
 ```

## Init 

Initialize an empty Git repository
    
```cmd
    git init
```

## Add

adds the modified file/files to the staging 
    
```cmd
    git add <file name>
    git add .   # all the untracked + modified files.
    git add -u  # all the modified files
```

## Commit

commits the changes / staged files into commited stage
    
```cmd
    git commit -m "heading"
    git commit -m "heading" -m "Commit description"
    git commit -am "heading" // addes the modified files and commit them   
```

## Push 

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
    git log --online --graph -all # shows the commits of all the branches in a graph.
    
```

## Branching

### Branches

Shows the current branch you are on in / shows all the branches

```cmd
    git branch     # return current branch
    git branch -v  # shows the current branch along with latest commit id and msg.
    
    git branch -a  # show all branches
    
    git branch -d <branchname> # deletes that branch #only deltes if there is a merged branch
    git brancg -D <branchname> # force deletes the branch even though its not merged.
    
```

### Changing Branching

Creates a new branch / switches to a new branch 

```cmd
    git checkout -b <branch name>  //new branch
    git checkout <branch name> // switch branch
```


## Diff

```cmd
    git diff <filename>  # only to the specified file
    git diff # gives the diff btw the modified and the commited and once staged this cmd doesn't work.
    git diff --staged   # gives the biff btw the staged and the last commit.
```

## Pull 

Pulls all the commited code from the mentioned branch to your current repository

```cmd
    git pull <branchname>
```

## Merge

Merges the one branch committed code into an other branch
 

```cmd
    git merge <branchname>
```
merges can be of 2 types.

 - Fast forwarding : The head pointer will be moved from the master to the latest commits of the b1 its not have no extra commits and the only 1 step behind common ancestor.
 
    - <img width="412" alt="bbm" src="https://user-images.githubusercontent.com/22676852/126391376-2ca1a597-ec75-4dc5-a558-da4f78ba75c0.PNG">
      
    - <img width="412" alt="abm" src="https://user-images.githubusercontent.com/22676852/126391386-d25fad14-f462-44b1-8fd8-134f046be3ff.PNG">

 - Recursive Merging : This happens when they have more code changes/versions/commits from the common ancestor in the masster and these forms a new merge commit.
 
    - intial stage
        
        - <img width="412" alt="arm-1" src="https://user-images.githubusercontent.com/22676852/126392507-d9f88201-c742-42c3-b1bb-60e8572a6bea.PNG">

        
    - finding common ancestor 
    
        - <img width="412" alt="arm" src="https://user-images.githubusercontent.com/22676852/126392505-5ec7d50c-5afa-42e4-8b07-8ac64cfe5f43.PNG">

        
    -after merge
    
      - <img width="412" alt="arm_final" src="https://user-images.githubusercontent.com/22676852/126392514-8eddccca-cc70-4dbc-a672-b95a90424342.PNG">


## Move and Remove files 
```cmd
    mv <source_file> <dest_file> # git tracks it but we have to stage those changes again (2-step).
    git mv <source_file> <dest_file> # git adds the changes to the staging automatically (1-step).
    rm <filename>   #git tracks it but we have to stage those changes again (2-step).
    git rm <filename> # git adds the changes to the staging automatically (1-step).

```
## Unstaging
```cmd
    git restore --staged <filename>
```
## Unmodifying 

```cmd
    git checkout --filename.txt  # takes you to the last commit.
```

## Stages of a flie
- untracked : New file is created (U in VS code)
- unmodified : Already present in the local repo but no changes were made.
- modified : When we made some changes to the file.
- commited : Once the changes are working we will create a new version.

<img width="470" alt="stages of file" src="https://user-images.githubusercontent.com/22676852/126295806-d72cc46b-9ea0-436d-b600-aa7a3c471681.PNG">
