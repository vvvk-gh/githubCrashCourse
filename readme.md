# Git Basics Commands

## Clone 
Clone the existing remote repository code to local directory 
   
    ```git
        git clone <git repo url>
    ```

## Init :
Initialize an empty Git repository
    
    ```cmd

        git init

    ```

    ```javascript
        if (isAwesome){
        return true
    }
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