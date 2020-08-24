### Initial Git Setup

* Git is `Distributed Version control`
* Git is ideal source control for Smaller repositories 
* Git is ideal source control for `Source code files`, but not so for `binary files`
* Git (default settings) DO NOT ALLOW files bigger than 100 MB
* For files bigger than 100 MB, use git-lfs (Large file support)


1. Install GIT for Windows using https://git-scm.com/download/win

2. Signup on https://github.com / Use existing account

3. One time Git setup for Local system. type following commands on "CMD" or "Powershell" or "Git Bash"

    ```
    ## GitHub Account name as Username
    $ git config --global user.name "Mahendra Shinde"
    ## GitHub Login ID as Email
    $ git config --global user.email "MahendraShinde@synergetics-india.com"
    $ git config --global -l
    ```

4.  Test create local GIT repository (Using CMD)

    ```
    $ cd \
    $ mkdir repos
    $ cd repos
    $ git init myrepo01
    $ cd myrepos01
    $ explorer .
    ```

5.  Add first ROOT-COMMIT 

    ```
    $ cd \repos\myrepo01\
    $ start notepad file1.txt
    ## Once notepad opens, press "Yes" or "OK" to create new file
    ## Save the changes and close notepad
    $ git status
    ### Start TRACKING the changes to files
    $ git add file1.txt
    $ git status
    ### After adding several files/changes using GIT ADD
    $ git commit -m "First Commit"
    $ git status
    $ git log
    ```

> git add <FILENAME>   Add single file to INDEX
> git add *            Add all files from CURRENT PATH to INDEX
> git add .            Add all files from THIS DIRECTORY and ALL SUB-DIRECTORIES to INDEX  

### Time travel (Go back to previous COMMIT and come back to present)

1.  Create new set of files in `myrepo01`

    ```
    $ cd \repos\myrepo01
    $ start notepad .gitignore
    Add following lines
    #### Ignore all CSS files
    *.css
    Save and close notepad
    $ start notepad style.css
    Add following lines:
    ---    
    h1 {
    color: red;
    }
    ---
    Save and close notepad
    $ start notepad index.html
    Add following lines
    ---
    <html>

    <body>
    <h1>Hello World</h1>
    </body>
    </html>
    ---
    Save and close notepad
    $ git add .
    $ git status
    $ git commit -m "Added a webpage"
    $ git log 
    Copy the FIRST FOUR digits of First commit-ID
    $ git checkout <PASTE-COMMIT-ID>
    $ dir 
    $ git checkout master 
    ```