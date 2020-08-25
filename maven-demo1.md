## Maven demo 1

1. Open CMD to run all the commands:

    ```
    $ cd \repos
    $ mvn archetype:generate
    [LIST OF OVER 2000 Templates] Choose: <ENTER>
    [List of Versions] Choose: <ENTER>
    GroupId:  com.lti
    artifactId: app-1
    package: com.lti
    version: 1.0
    Y: Y
    $ cd app-1
    $ mvn validate
    ```

2.  Creating project in Non-Interactive mode

    ```
    $ mvn archetype:generate -DgroupId=com.lti -DartifactId=app-2 -DarchetypeGroupId=org.apache.maven.archetypes -DarchetypeArtifactId=maven-archetype-quickstart
    ```