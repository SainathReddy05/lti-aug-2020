## Maven with Selenium test cases

1. Clone the sample project (Multi-Module Maven project)

    ```
    $ cd /repos/
    $ git clone https://github.com/mahendra-shinde/selenium-samples-java
    $ cd selenium-samples-java
    $ mvn validate
    ## Compile all the TEST cases (Also download all selenium dependencies)
    $ mvn test-compile
    ## Run the Test cases for project `cucumber-parallel`
    $ mvn -pl cucumber-parallel clean test
    ```

2.  Get test reports