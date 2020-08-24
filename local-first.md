## Local FIRST approach

- Existing local repository TOBE connected with NEW remote repository!

1. Create a local repository and add at least ONE commit
2. Verify that, when using 'git status' command, you should "Working directory clean"
3. Login into remote git server (github.com) and create a new Reposity 
    Please DO NOT use any other option like "readme" or "license" file
4. GITHub would show you, how to ADD this repository to your local repository.
    Out of THREE command snippets, the MIDDLE one (second) should contain something:

    ```
    $ git remote add origin <URL>
    $ git push -u origin master
    ```

5.  Copy the above TWO commands and RUN them inside local repository.
6.  For the FIRST TIME, a small POP-UP Screen should ask you for GITHUB credentials
7.  Try "Adding ReadMe" into Github repository and then try following command in local :

    ```
    $ git pull
    $ git status
    ```

