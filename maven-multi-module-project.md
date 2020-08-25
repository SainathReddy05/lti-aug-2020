## Multi Module project

* A Parent project without the usual `src/main` and `src/test` directories
* Project `packaging` should be set to `pom`
* Inside project directory, there could be maven projects (Modules)
* Modules (child projects) would inherit all the dependencies from Parent project


## Folder Structure

ProjectDirectory/
   - pom.xml
   - module-1/
        - pom.xml
        - src/
   - module-2/
        - pom.xml
        - src/
    
## Start with Normal maven project

1. Create a parent-project at C:\repos directory

    ```
    $ cd repos\
    ## -B is batch mode, uses DEFAULT template
    $ mvn archetype:generate -DgroupId=com.lti -DartifactId=parent-project -B
    $ cd parent-project
    $ start notepad pom.xml
    Replace default "packaging" to "pom"
    save and close the file
    $ rmdir /S /Q src
    $ mvn validate
    ```

2.  Create the "modules" inside parent project

    ```
    $ cd \repos\parent-project\
    $ mvn archetype:generate -DgroupId=com.lti -DartifactId=module-1 -B
    $ mvn archetype:generate -DgroupId=com.lti -DartifactId=module-2 -B
    $ mvn validate
    ```
3.  Remove the dependencies from `module-1` 
    Open `module-1\pom.xml` delete everything between `<dependencies>` and `</dependencies>`

4.  Remove the dependencies from `module-2` 
    Open `module-2\pom.xml` delete everything between `<dependencies>` and `</dependencies>`

5.  Try building entire parent project.

    ```
    $ cd \repos\parent-project
    $ mvn package
    ```

6.  Build only selected module(s)

    ```
    $ mvn -pl module-1 package
    ```


    