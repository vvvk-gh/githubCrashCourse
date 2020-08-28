# Git Basics Commands

## Clone 
Clone the existing remote repository code to local directory 
   
    ```git
        git clone <git repo url>
    ```

## Init :
Initialize an empty Git repository
    
    ```git
        git init 
    ```

## Add :

adds the modified file/files to the staging 
    
    ```git

        git add <file name>
        git add .

    ```

## Commit : 

commits the changes / staged files into commited stage
    
    ```git
       
        git commit -m "heading"
        git commit -m "heading" -m "Commit description"
   
    ```


## Push :

push all the commited files to the remote repository


   ```git
        
        git push -u origin master
        -u : upstream 

    ```
    
If you use upstream for the first git push, from the next we only use

    ```git

       git push

    ``` 
and you can avoid writing long commands like git push origin master