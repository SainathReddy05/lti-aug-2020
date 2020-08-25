## Maven demo-2 : Project from GitHub

1.  Open CMD and using `c:\repos` directory clone the sample project

    ```
    $ cd \repos
    $ git clone https://github.com/mahendra-shinde/ci-servlet-demo
    $ cd ci-servlet-demo
    $ git status
    $ dir
    ```


2.  Build & Package application

    ```
    $ mvn package
    ```

3.  List all the project dependencies

    ```
    $ mvn dependency:tree
    ```