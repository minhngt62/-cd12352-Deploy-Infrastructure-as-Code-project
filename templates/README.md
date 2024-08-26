# CD12352 - Infrastructure as Code Project Solution

## Infrastructure diagram
![alt](https://github.com/minhngt62/-cd12352-Deploy-Infrastructure-as-Code-project/blob/main/infrastructure_diagram.png)

## Spin up instructions
```
  setup.bat deploy MessagingNetwork network.yml network-parameters.json us-east-2 default
  setup.bat deploy Udagram udagram.yml udagram-parameters.json us-east-2 default
```

## Tear down instructions
```
  setup.bat delete Udagram us-east-2 default
  setup.bat delete MessagingNetwork us-east-2 default
```

## Other considerations
1. `emptyS3`: Empty an S3 bucket.
  
    Usage: `setup.bat emptyS3 <S3BUCKET> <REGION> <PROFILE>`
  
    - `S3BUCKET`: The name of the S3 bucket to be emptied.
    - `REGION`: The AWS region where the S3 bucket is located.
    - `PROFILE`: The AWS CLI profile to be used.

2. `uploadS3`: Upload a file to an S3 bucket.
    
    Usage: `setup.bat uploadS3 <S3BUCKET> <REGION> <PROFILE> <FILE>`
    
    - `S3BUCKET`: The name of the S3 bucket to upload the file to.
    - `REGION`: The AWS region where the S3 bucket is located.
    - `PROFILE`: The AWS CLI profile to be used.
    - `FILE`: The path to the file to be uploaded.

3. `deploy`: Deploy a CloudFormation stack.
    
    Usage: `setup.bat deploy <STACK_NAME> <TEMPLATE_NAME> <PARMS_NAME> <REGION> <PROFILE>`
    
    - `STACK_NAME`: The name of the CloudFormation stack to be deployed.
    - `TEMPLATE_NAME`: The path to the CloudFormation template file.
    - `PARMS_NAME`: The path to the parameter file for the CloudFormation stack.
    - `REGION`: The AWS region where the CloudFormation stack will be deployed.
    - `PROFILE`: The AWS CLI profile to be used.

4. `delete`: Delete a CloudFormation stack.
    
    Usage: `setup.bat delete <STACK_NAME> <REGION> <PROFILE>`
    
    - `STACK_NAME`: The name of the CloudFormation stack to be deleted.
    - `REGION`: The AWS region where the CloudFormation stack is located.
    - `PROFILE`: The AWS CLI profile to be used.

5. `preview`: Preview changes for a CloudFormation stack.
    
    Usage:   `setup.bat preview <STACK_NAME> <TEMPLATE_NAME> <PARMS_NAME> <REGION> <PROFILE>` 
    
    - `STACK_NAME`: The name of the CloudFormation stack to preview changes for.
    - `TEMPLATE_NAME`: The path to the CloudFormation template file.
    - `PARMS_NAME`: The path to the parameter file for the CloudFormation stack.
    - `REGION`: The AWS region where the CloudFormation stack is located.
    - `PROFILE`: The AWS CLI profile to be used.
