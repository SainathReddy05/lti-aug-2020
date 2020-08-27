## Deploying WebApplication to Apache Tomcat

1. Download my customized tomcat server from [link](./apache-tomcat-9.0.31.zip)

    Click 'Download' button to start downloading.

2.  Extract the contents of this ZIP into your "c:\" drive.

3.  Open directory `C:\apache-tomcat-9.0.31\bin` into CMD or Powershell and use following command to launch apache tomcat server.

    ```
    $ .\startup.bat
    ```

4.  Open web-browser, and visit TWO urls in TWO Tabs / Windows
    
    4.1 http://localhost:8000   ===> You MUST get 404 error
    
    4.2 http://localhost:8000/manager

    Enter User credentials: manager/pass1234

5.  Launch jenkins and visit `job2`
    
    http://localhost:8080/job/Job2/

    Download the last successful Artifacts: `ROOT.war`

6.  Or get it from folder location
    `C:\Users\mahendra\.jenkins\jobs\Job2\builds\5\archive\target`

7.  Go back to tomcat manager portal (step #4.2)
    And, upload `ROOT.war` and deploy

8.  Go back to Tomcat (Step #4.1) and reload the page.

9.  You should get the sample application home page.

