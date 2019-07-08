# What is this?
```
no more YAML. use your favorite programming language (JS, python and more) to build :

Build out the Fargate infrastructure for your  spring boot application, 
RDS,
including logging, 
Secret env variable in task definition (RDS Password),
cloudwatch dashboard and 
custom metric autoscaling with target tracking.

```
# Prepwork

Use AWS Cloud9.


## Create a DB password for RDS .. replace it with your own password value
```
aws ssm put-parameter --name "/mysqlpassword" --value "P@ssW%rd#1" --type "SecureString"

```


## Deploy using aws cdk
```bash
export AWS_REGION=ap-southeast-1  # or any region

npm install
npx cdk@0.36.1 bootstrap
npx cdk@0.36.1 deploy  --require-approval never  "*"

```