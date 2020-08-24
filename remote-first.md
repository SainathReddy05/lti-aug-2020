## Remote FIRST approach

- Use Existing remote repository or create a new remote repository

1. Login into GitHub and create new repository
    Please DO SELECT  other option like "readme" or "license" file
2. Open Command prompt and make sure that you are NOT in any git repository.

    ```
    $ cd \repos
    $ git status 
    ## EXPECTED ERROR: Not a git repository
    ```
3. CLONE the remote repository into local

    ```
    $ git clone <REPO-URL>
    ```
    
4. Verify the remote repo URL
    ```
    $ git remote -v
    ```

5.  Add some random file and use following commands:

    ```
    $ git add .
    $ git commit -m "Added a file"
    $ git push
    ```  