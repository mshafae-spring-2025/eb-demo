# Minimal Flask App for AWS Elastic Beanstalk

Tip: make sure the .ebignore is ignoring the projects venv or env directory.

## Group permissions
1. Create a group, call it WebAppDeployment.
1. Add AdministratorAccess-AWSElasticBeanstalk at a minimum to the group.
   Consider adding (list was hastily assembled, may contain errors)
   * AmazonRDSFullAccess
   * AmazonDynamoDBFullAccess
   * AmazonCloudWatchEvidentlyFullAccess
   * AmazonEC2FullAccess
   * AmazonS3FullAccess
   * AmazonSNSFullAccess
   * AmazonSQSFullAccess
   * AutoScalingFullAccess
   * AWSCloudFormationFullAccess
   * ElasticLoadBalancingFullAccess
1. Create a user through the IAM dashboard
1. Add the user to the newly formed group
1. Generate Access Keys under Security Credentials. Save them somewhere safe.

## EB Command Line Tool
1. Get [EB CLI installed](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)

## EB Commands
Takes about 5 minutes to get everything started.

1. eb init
1. eb create
1. eb open

eb deploy to update the application

More information on the eb command at https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-getting-started.html.

## Logs

Download log files by going to the console, selecting the application's current environment, click on logs, and then request the logs.