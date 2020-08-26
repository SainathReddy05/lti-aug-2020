## Jenkins Job (FreeStyle project) for Building Maven project from GIT

1.  Login into Jenkins, from Dashboard use Link `New Item`

2.  Enter following `Job Details`

```yml
Job-Name:   Job2
Description:    Sample maven project
Source-Code-Management:
    Git:
        Repository-URL: https://github.com/mahendra-shinde/ci-servlet-demo/
Build-Environment:
   - Delete Workspace before build start (Clean Older build artifacts)
   - Abort build if it's stuck:
        TimeOut-strategy: Absolute
        TimeOut-minutes: 3
        TimeOut-action: Abort-the-build
   - Add timestamp to the Console Output

Build:
    Invoke-top-level-maven-target:
        Maven-Version: M2
        Goals:  package

Post-Build:
    archive-the-artifacts:
        Files-to-archive: target/*.war
    delete-workspace-build-is-done:
```