# sam-deployment
> Template for SAM deployment with CodePipeline.
* Source: CodeCommit
* Build: CodeBuild
* Deploy: CloudFormation


## Deployment Flow

### Development
1. Push `develop` branch on CodeCommit
2. Build artifacts on CodeBuild
3. Deploy stack for `testing` environment

### Production
1. Push `master` branch on CodeCommit
2. Build artifacts on CodeBuild
3. Deploy stack for `staging` environment
4. Needs manual approval
5. Deploy stack for `production` environment


## Parameters
* `ServiceName`  
Your service name, used in the code repository, Lambda function, and pipeline names.


## References
* https://gist.github.com/SAPessi/246b278b6b7502b157a9fbaf3981d103
* https://qiita.com/is_ryo/items/0382d183f514e0d06f4d
