## Jenkins pipeline (Inline pipeline)

1. Login into Jenkins dashboard

2. New Item > Pipeline Project
    

    Name: job-3
    Build Trigger: Build Periodically, H/2 * * * *
    Pipeline-Inline

    ```
    pipeline {
    agent any

    stages {
        stage('init') {
            steps {
                bat script: 'echo "Init Stage %BUILD_NUMBER%"'
            }
        }
        stage('first') {
            steps {
                bat script: 'echo "First stage %BUILD_NUMBER%"'
            }
        }
        stage('after') {
            steps {
                bat script: 'echo "After stage %BUILD_NUMBER%"'
            }
        }
    }
    }
    ```

3.  Check the build log after every 2 minutes.