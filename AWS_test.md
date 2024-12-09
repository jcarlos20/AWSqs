1. A company wants to automate the process of creating multiple AWS resources for their production web-application environment. 
Which AWS service is capable of automating their infrastructure as code?

A) AWS Elastic Beanstalk
B) AWS CloudFormation
X C) AWS CodeBuild
D) AWS Automate

Codebuild has the hability to compile the code without needing for an infraestructure, so developer can easly adopt this method to be more agile.

2. A company security policy requires that all EBS Volumes are encrypted-at-rest. Which AWS service would help meet this requirement?
	
A) AWS Certificate Manager
B) AWS KMS
X C) Server-Side Encryption AES-256
D) Amazon GuardDuty

Also it is possible to encrypt the volume at the moment of the creation of the resource.

3. An application has multiple EC2 instances within an Auto Scaling Group (ASG). The ASG also has a simple scaling policy to meet the demand for fluctuating traffic. The application is scaling up and down repeatedly within the timeframe of an hour. What configuration changes could be made to reduce the cost and the frequency of scaling?

A) Increase the Cooldown timer
B) Reduce the Max Capacity
C) Increase the alarm period that triggers the scale down policy
D) Reduce the Desired Capacity
x E) Add Scheduled Scaling Actions

You should be able to get the first insight of the scaling cycle and determine in what time is the most common peak of traffic and get the idea on how to reduce or get an higher capacity on resource, this will help you to reduce the time and cost on how the auto scaling is acting on the instance.

4. A Solutions Architect is developing several important long-running applications hosted on Docker.
How should the Solutions Architect design a solution on AWS to meet the scalability and orchestration needs?
	
A) Use Spot Instances to orchestrate and scale containers on existing Amazon EC2 instances.
B) Use Amazon ECS and Service Auto Scaling
X C) Use AWS OpsWorks to launch containers in new Amazon EC2 instances
D) Use Auto Scaling groups to launch containers on existing Amazon EC2 instances

OpsWorks will provide a fast solution to deploy any solution on mind. This will give the oportunity to the Devops team to create this solutions.

5. A web application running on EC2 instances managed by Auto Scaling Group and behind an Application Load Balancer generates thousands of PDFs weekly, which are stored in S3. These PDFs need to be accompanied by additional information in the form of metadata, which is 20 KB in size. This additional data needs to be stored and displayed in a flat list on the web application. Which solutions would be the most performant for displaying this list of metadata?
	
A) Metadata can be applied directly to S3 Objects
B) Store the metadata in a DynamoDB table
C) Store the metadata in RDS
D) Store the metadata in the root EBS volume

6. In a VPC network, access control lists (ACLs) act as a firewall for associated subnets, controlling both inbound and outbound traffic at the __________ level.
	
x A) Private
B) Subnet
C) API Gateway
D) EC2 instance

7. An AWS Lamba function needs to access S3 in order to process photos into thumbnails. How can you securely pass credentials to the AWS Lambda?

A) Pass the Access Key and Secret into environment variables within the AWS Lambda console. This will keep the credentials out of the code and secure.
B) Assign an IAM role to the AWS Lambda with permission to S3
C) Place the Access Key and Secret into Lambda function. It is not possible to assign roles or environment variables to AWS Lambda functions. So you must hard code the credentials
x D) Use AWS Secrets Manager to store the Access Key and Secret

The most secure way to manage enviroment variable is using Secret Manager because on a secure way you can store values and sensitive data to retrieve later with any AWS service.

8. www.exampro.com is a popular photo and video hosting service with millions of users.
Which of the following is the best solution for storing large data objects while lowering costs, scaling to meet demand, and speeding up innovation?

A) Amazon Elastic File System
B) Amazon S3 Standard
x C) Amazon S3 Glacier
D) AWS Redshift

Using Glacier to request images or any type of file without a high demand can help you to reduce cost, because using Glacier the image or the file will be avaible only when you consume it on the frontend or backend.

9. An application is backed by DynamoDB. The DynamoDB table has a provisioned throughput of 100 reads and writes per second. During peak hours the number of writes can reach 500 per second and as a result, the excess writes are being dropped. What cost-effective solution could be architected to handle the non-uniform increase in writes?

A) Use Kinesis Data Streams as a buffer.
B) Use SQS as a buffer.
C) Turn on Auto Scaling write for write capacity
x D) Change Read/write capacity mode to On-demand

10. A cloud engineer needs to use CloudFront to distribute the content they need to create a distribution. They are required to specify the configuration settings.
Which of the following configuration settings should be specified?

A) You configure the environment variables.
B) You specify your origin Amazon S3 bucket or HTTP server.
x C) You specify the number of objects you can serve per distribution.
D) You specify if you want everyone to have access to the files or a select number of users.

11. A company has an application running in us-east-1a. In the case of Availability Zone failure, the company needs to recover the volume and launch another instance in another Availability Zone such as us-east-1b. The company is not concerned with downtime and trying to save costs by running in a single AZ. How can the company ensure that it can recover from such a failure?
	
x A) Continuously create Snapshots and copy Snapshots to another AZ
B) Continuously create Snapshots and copy Snapshots to another Region
C) Continuously create Snapshots
D) Backup the contents of the EBS volumes to S3 with Sync command
E) Use EFS since it is already highly available

Using AV can ensure that if one of the AV fail they can still on. Using another AV to create a backup of the faling one

12. As a Solution Architect, you need to build a CloudFormation template that will provision a highly available architecture. After the stack has been created you need to a convenient way to return the DNS hostname of the load balancer. Which template section would provide the DNS hostname after stack creation?

A) Resources
x B) Parameters
C) Outputs
D) Mappings
E) Variables

13. A company has an application running on EC2 instance which needs to store multiple documents which are uploaded via users. User's frequently uploads changes to their documents but with the same name. The company wants to allows users to roll back to previous documents. Which storage solution would best meet their needs?

A) EBS
x B) S3
C) EFS
D) AWS Elastic Beanstalk

Using S3 gives you the change to activate the copy of the previous file when you upload a new version, also is possible to retrieve this changes in any app or webapp

14. A company has a requirement that does not allow them to use DocumentDB and so they must provision an EC2 instance with MongoDB. Their current requirements are they need at most 10,000 IOPS Which storage solution would meet their needs?

A) EBS Throughput Optimized HDD
B) EBS General Purpose SSD
C) EBS Provisioned IOPS SSD
D) EBS Cold HDD

15. A developer is building an automated transcription service in which "Amazon EC2 worker" instances process an audio file and convert it to a text file. They need to store both of these files in the same secure storage until the text file is retrieved, but they don't know how much space they'll need.
Which of the following storage options is both cost-efficient and scalable?
	
x A) A single Amazon Glacier Vault
B) A single Amazon S3 bucket
C) Multiple instance stores
D) Multiple Amazon EBS volume with snapshots

As a low-cost solution for store files with a low-demand and also can ensure that the file has a unknow

16. A Solution Architect needs to investigate which database solution would be the best fit for a new web application. The data being stored must remain highly available by default. Access to this data should have a guarantee of reads at any scale and the data being stored JSON like data. Which database solution would meet their needs?
	
x A) DocumentDB
B) Amazon Redshift
C) DynamoDB
D) RDS
E) Aurora

Using DocumentDB you can use the same schema as a Postgres DB and retrieve each value stored inside the DB

17. Which of the following should be referred to if you want to map Amazon Elastic Block Store to an Amazon EC2 instance for AWS CloudFormation resources?

x A) The logical IDs of the instance
B) Reference the logical IDs of both the block stores and the instance
C) Reference the physical IDs of the instance
D) Reference the physical IDs of both the block stores and the instance



18. A company wants to back up their on-premise storage volumes to AWS. What solution would meet their needs?

x A) Connect your on-premise with Direct Connect. Create EBS Snapshots
B) Connect your on-premise with AWS VPN. Create EBS Snapshots
C) Use Storage Volume Gateway
D) Use S3
E) Connect your on-premise with AWS VPN. Use EFS

Using Direct connect is a perfect solution for on-premise migration, you can create a secure tunnel to connect to your on-premise machines and bring any data o connect any AWS service.

19. A Solution Architect is designing an application with a relational database that runs on an EC2 instance. This database will be used infrequently once or twice a day. The database is also 100 GB in size. Which Amazon EBS volume type is the most cost-effective option?

	
A) EBS Provisioned IOPS SSD
B) EBS Cold HDD
C) EBS Throughput Optimized HDD
D) EBS General Purpose SSD

20. A Solution Architect needs to choose a database which can perform joins between multiple tables and utilize an open-source service. Which database solution would be best suited for this use case?

A) DynamoDB
B) RDS
x C) Aurora
D) Redshift