# Key Points to Revise Before Exam:

There are only 3 AWS services that are global: IAM, S3 and DNS.

## Support Plans

Be able to identify which support plan is best based on the given test cases.

Example:

a) Whether you need TAM (Technical Account Manager) ?

b) Based on different service level agreements, like if you need response time of 4 hours or 1 hour etc.

## Billing Alarm

How can you get automatic notifications in different test cases example: if your account goes above $1000 ?

## IAM

When to make use of IAM (Identity Access Management) Users, Groups, Roles and Policies.

## S3

* S3 is Object-based meaning allows you to upload files (0 bytes to 5TB).
* The storage is unlimited and Files are stored in Buckets.
* S3 os universal namespace. eg: http://bucket_name.s3.amazonaws.com/filename
* S3 is a key(file name) and value(data) type.
* It has Read after Write consistency for PUTS of new objects.
* Eventual consistency for overwrite PUTS and DELETES.
* 6 different Storage classes: S3 Standard, S3 IA, S3 One Zone IA, S3 Intelligent Tiering, S3 Glacier, S3 Glacier Deep Archive.

## CloudFront

* Its amazon's CDN (Content Delivery Network). IF you turn on cloudFront, you will set up Edge locations to make data available with low latency.
* Know what is TTL ?
* READ and WRITE in Edge Locations.
* Charges for cached data in Edge Location

## EC2

* What is EC2? What are different EC2 pricing models?
* What happens if Spot instance is terminated bu Amazon EC2? You will not be charged for a partial hour of usage.
* What happens if you terminate the instance yourself? You will be charged for any hour in which the instance ran.
* Remember FIGHT DR MCPXZ
* Remember EBS and its different types. There are 4 different types: two SSDs(This can be used for databases.) and two Magnetic (can be used for data warehouse and File servers).
* USe a private key to connect EC2
* Linux server = SSH (port 22), Microsoft = RDP (Port 3389), HTTP(Port 80) = HTTPS (Port 443)
* Security group is virtual firewalls in the cloud. You need to open ports in order to use them. Popular ports are SSH(22), HTTP(80), HTTPS(443), RDP(3389)
* Design for failure meaning, always have EC2 in 2 different AZs.
* Where to save Access and secret keys ??
Instead of saving the security credentials in EC2, create role in IAM and apply it to EC2 instances at any time.

## Load Balancer

* Difference in when to use Application Load Balancer, Network Load balancer and Classic Load Balancer ?

## Databases

* Different types of database services offered by AWS?
* Learn about use cases : RDS (SQL/OLTP), DynamoDB (No SQL), Red Shift (OLAP), ElastiCache
* Redshift: For any BI or data warehousing requirement.
* Elasticache: To speed up performance of existing databases (frequent identical queries)

## Elastic Beanstalk??

* What Elastic Beanstalk is ? You can upload your code and EBS will inspect the code automatically provision the required environment.
* Elastic Beanstalk and Cloudformation are both free services. But the services they provision like EC2 etc are not free.
* Elastic Beanstalk is limited in what it can provision and is not programmable.

## CloudFormation?

* What is a cloudFormation? Cloudformation takes care of provisioning and configuring the resources that your template describes. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances). You don't need to individually create and configure AWS resources and figure out what's dependent on what; AWS cloudFormation handles all of that.
* Cloudformation are both free services. But the services they provision like EC2 etc are not free.
* CloudFormation can provision almost any AWS service and is completely programmable.

# Gloabl AWS Services

1. IAM
2. Route53
3. CloudFront
4. SNS
5. SES

Some services give global view but are not global: S3

# What services can be used on Premises

1. Snowball: A gigantic disk or a briefcase which is shipped to your address, you load all your data and ship it back to Amazon. Size to 80TB.

2. Snowball Edge: Similar to Snowball with CPU. It allows you to deploy lambda function on-premises. You use Snowball edge where there are no connectivity eg. Antarctica

3. Storage Gateway: Its a way of caching your files inside data center, replicates those files to S3.

4. CodeDeploy: A way to deploy code to EC2 instance, we can also deploy on-premise as well. Use it to deploy application/code.

5. Opsworks: Uses Chef (automated work). Use Opswork to deploy code to EC2 and on-premise server.

6. IoT Greengrass: Its an IoT and connects devices to cloud and to on-premises as well.

What AWS service used to deploy applications on-premises ?
    a. CodeDeploy
    b. Opsworks

## CloudWatch

* CloudWatch is used for monitoring performance.
* Cloudwatch can monitor most of AWS as well as your applications that run on AWS.
* CloudWatch with EC2 will monitor events every 5 minutes by default.
* Yoy can have 1 minute intervals by turning on detailed monitoring.
* You can create CloudWatch alarms which trigger notifications.

## AWS Systems Manager

* AWS Systems Manager can be used to manage fleets of EC2 instances and VM. A piece if software is installed on each VM. It can be both inside AWS and on-premise.
* Run command is used to install, patch, uninstall software. You can use CloudWatch to have view of your AWS dashboard.
