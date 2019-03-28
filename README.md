# aws-templates
> AWS CloudFormation templates.

## Requirements
* aws-cli  
    ```
    brew install awscli
    aws configure
    ```

### Validate template
```
aws cloudformation validate-template --template-body file://template.yml
```

### Deployment
```
aws cloudformation deploy \
--template-file <template_file> \
--stack-name <stack_name> \
--capabilities <capabilities> \
--parameter-overrides <parameters>
```
