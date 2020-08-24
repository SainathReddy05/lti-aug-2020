## Branching

1. Always create branch when repository status is `nothing to commit, working tree clean`
2. Command to create a branch   
    git checkout -b BRANCHNAME
3. Switch to parent Branch
    git checkout PARENT-BRANCHNAME

========================

Create a new repository "myrepo03"
$ cd \repos\
$ git init myrepo03
$ cd myrepo03

Check if contains any COMMIT (No Commits)
$ git status

Create few HTML files 
- index.html        
    <h2>Home Page</h2>

- aboutus.html
    <h2>About Us</h2>

Save the files and ADD them to repository.
$ git add .
$ git commit -m "Project created"
$ git log

Create a new BRANCH called "css-style"
$ git checkout -b "css-style"
$ git status

Create a CSS files
- style.css
    h2 { color: red; }

Modify `index.html` and `aboutus.html`
Add this line in beginning
<link rel=stylesheet type="text/css" href="style.css" />

Save all the changes and add to index
$ git add .
$ git commit -m "Formatting 1"

Check the git log
$ git log
$ git log --oneline --all --graph

Switch to Master branch
$ git checkout master
$ dir
Add one more line at the end of `index.html`
<p>The quick brown fox jumps over the lazy dog.</p>

Save changes and add to INDEX
$ git add .

Make a new COMMIT 
$ git commit -m "Modified index.html"

Now, view the LOG
$ git log --oneline --all --graph

### Merge Conflict

# When both branches tries to modify same file!!
# To Resolve Merge Conflict, edit the files, save changes, add to index and then COMMIT

$ git checkout master
$ git merge css-style

At this point, you SHOULD get MERGE CONFLICT error
You need to EDIT all files which have merge conflicts

$ git add .
$ git commit -m "Fixed Merged"
$ git log --oneline --all --graph
