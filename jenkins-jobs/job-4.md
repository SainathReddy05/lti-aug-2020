## Build Pipeline (from Git Repository)


1.  Login into Jenkins Dashboard
2.  New Item > Pipeline Project

    Name: Job-4
    Pipeline-SCM:

    Git Repository: https://github.com/mahendra-shinde/ci-demo

    Script path: Jenkins

    

3.  Manually trigger a build

NOTE: The contents of `Jenkins` file are:

```jenkinsfile
node {
   def mvnHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/mahendra-shinde/ci-demo.git'
      // Get the Maven tool.
      // ** NOTE: This 'M2' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'M2'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -f DemoApp/pom.xml -Dmaven.test.failure.ignore clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" -f DemoApp\pom.xml -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      
      archiveArtifacts 'DemoApp/target/*.war'
   }
}
```