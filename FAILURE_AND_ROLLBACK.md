# Failure and Rollback

## Scenario 1: Build Failure

If the Maven build fails, Jenkins stops the pipeline. After fixing the build error, the pipeline can be run again.

## Scenario 2: Docker Image Build Failure

If Docker image creation fails, Jenkins should stop the pipeline, and the image should not be pushed. After fixing the error, the pipeline can be run again.

## Scenario 3: Kubernetes Deployment Failure

If the Kubernetes deployment fails, the deployment should not be considered successful. If the new development causes problems,the previous working versions should be restored

## Scenario 4: GitOps Rollback

If a new GitOps deployment causes problems, the previous working version should be restored. The Git repository can be reverted to the last known working configuration, and the deployment can be updated again.
