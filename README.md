# AWS-CLI-Commands
AWS Command Line commands which we use on daily purpose

#### AWS Configure:
- To configure a new AWS account in CLI:
```
aws configure
```
Provide access key, secret key, default region and format as json (in small) and it will make an entry in home directory .aws folder and credentials and config files

**Note:** To create access key, login to AWS Account -> Top right (Drop down) -> Security credentials -> Scroll to Access Key and create access key

- To list the accounts:
```
aws configure list-profiles
```

- To add another account, name it with meaningful account name:
```
aws configure --profile <profile name>
```
give access key, secret key, default region and format as json (in small)

To list all the accounts:
```
aws configure list-profiles
```

- To remove old profile:
delete the unwanted profile -
```
vi ~/.aws/credentials
```
remove config here -
```
vi ~/.aws/config
```
**- Swtich between accounts** [only when you have configured two or more account]

Verify which account it is configured:
```
aws sts get-caller-identity
```

to view list of account:
```
aws configure list-profile
```

Configure to particular account:
```
export AWS_PROFILE=<account name>
```

Verify once again which account it is configured:
```
aws sts get-caller-identity
```

or you can always add --profile <profile name>
```
Example: aws s3 ls --profile herovired
aws s3 ls --profile default
```

## AWS CLI Command Sheet

| S. No | AWS Command | Parameters (if any) | Quick Use |
|------:|------------|---------------------|-----------|
| 1 | `aws configure` | — | Set up AWS CLI credentials |
| 2 | `aws s3 ls` | — | List all S3 buckets |
| 3 | `aws s3 ls s3://<bucket>` | — | List objects in a bucket |
| 4 | `aws s3 cp <src> <dest>` | `--recursive` (optional) | Copy files to/from S3 |
| 5 | `aws s3 sync <src> <dest>` | — | Sync directories with S3 |
| 6 | `aws s3 rm s3://<bucket>/<key>` | — | Delete an S3 object |
| 7 | `aws ec2 describe-instances` | — | List EC2 instances |
| 8 | `aws ec2 start-instances` | `--instance-ids` | Start an EC2 instance |
| 9 | `aws ec2 stop-instances` | `--instance-ids` | Stop an EC2 instance |
| 10 | `aws ec2 reboot-instances` | `--instance-ids` | Reboot an EC2 instance |
| 11 | `aws ec2 terminate-instances` | `--instance-ids` | Terminate an EC2 instance |
| 12 | `aws ec2 describe-security-groups` | — | List all security groups |
| 13 | `aws ec2 describe-volumes` | — | List EBS volumes |
| 14 | `aws ec2 create-snapshot` | `--volume-id` | Create EBS snapshot |
| 15 | `aws ec2 describe-images` | — | List AMIs |
| 16 | `aws iam list-users` | — | List IAM users |
| 17 | `aws iam list-roles` | — | List IAM roles |
| 18 | `aws iam list-policies` | — | List IAM policies |
| 19 | `aws iam create-user` | `--user-name` | Create IAM user |
| 20 | `aws iam delete-user` | `--user-name` | Delete IAM user |
| 21 | `aws iam list-access-keys` | `--user-name` | List IAM user access keys |
| 22 | `aws lambda list-functions` | — | List Lambda functions |
| 23 | `aws lambda invoke` | `--function-name` | Invoke a Lambda function |
| 24 | `aws logs describe-log-groups` | — | List CloudWatch log groups |
| 25 | `aws logs get-log-events` | `--log-group-name` `--log-stream-name` | Fetch log events |
| 26 | `aws cloudformation list-stacks` | — | List CloudFormation stacks |
| 27 | `aws cloudformation describe-stacks` | — | Describe CFN stack details |
| 28 | `aws cloudformation deploy` | `--template-file` `--stack-name` | Deploy CFN stack |
| 29 | `aws dynamodb list-tables` | — | List DynamoDB tables |
| 30 | `aws dynamodb describe-table` | `--table-name` | Describe DynamoDB table |
| 31 | `aws dynamodb scan` | `--table-name` | Scan table items |
| 32 | `aws rds describe-db-instances` | — | List RDS instances |
| 33 | `aws rds start-db-instance` | `--db-instance-identifier` | Start RDS instance |
| 34 | `aws rds stop-db-instance` | `--db-instance-identifier` | Stop RDS instance |
| 35 | `aws ecr describe-repositories` | — | List ECR repositories |
| 36 | `aws ecr get-login-password` | — | Authenticate Docker to ECR |
| 37 | `aws ecs list-clusters` | — | List ECS clusters |
| 38 | `aws ecs list-services` | `--cluster` | List ECS services |
| 39 | `aws sts get-caller-identity` | — | Get IAM user/role identity |
| 40 | `aws cloudtrail describe-trails` | — | List CloudTrail trails |
| 41 | `aws sns list-topics` | — | List SNS topics |
| 42 | `aws sqs list-queues` | — | List SQS queues |

