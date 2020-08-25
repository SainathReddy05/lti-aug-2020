Apache Software Foundation

- Apache Maven
- Apache Tomcat
- ANT
...

## Installation

1. Download apache maven `binary zip` from http://maven.apache.org/download.cgi

2. Extract the downloaded ZIP into your D: drive. (Or C drive )

3. Verify the folder structure after extraction
    d:\apache-maven-3.6.3\bin

    > In case there is a NESTED folder apache-maven-3.6.3-bin\apache-maven-3.6.3\
      Then please MOVE the inner folder outside.

    > Maven MIGHT give you trouble when file path contain "spaces"
    > Maven (and Java) is Case sensitive for filenames and foldernames as well.

4.  Add "Maven Home" to System Environment Variable 

    M2_HOME=d:\apache-maven-3.6.3
    JAVA_HOME=C:\Program Files\Java\jdk1.8.0_231
    Update Path, Add new Entry:
    %M2_HOME%\bin

5.  Open new CMD window and try following command:

    ```
    $ mvn --version
    ```

