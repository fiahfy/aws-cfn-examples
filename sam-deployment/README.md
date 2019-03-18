# sam-deployment
> Template for SAM deployment.


## Application Deployment Flow

### Development
1. push `develop` branch on CodeCommit
2. build artifacts on CodeBuild
3. deploy stack for `testing`

### Production
1. push `master` branch on CodeCommit
2. build artifacts on CodeBuild
3. deploy stack for `staging`
4. needs manual approval
5. deploy stack for `production`


## Parameters
* `ServiceName`  
Your service name, used in the code repository, Lambda function, and pipeline names.


## Deployment
```
aws cloudformation deploy --template-file template.yml --stack-name <stack_name> --capabilities CAPABILITY_IAM --parameter-overrides ServiceName=<service_name>
```
