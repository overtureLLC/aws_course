1. You've just started developing an application on your On-premise network. This application will interact with the Simple Storage Service and some DynamoDB tables. How would you as the developer ensure that your SDK can interact with the AWS services on the cloud?
	1. Create an IAM Role with the required permissions and add it to your workstation
	2. Create an IAM Role with the required permissions and make a call to the STS service
	3. Create an IAM User , generate the access keys. Use the Access keys from within your program.
	4. Create an IAM User , generate a security token. Use the Security Token from within your program.

2. You're a developer for a company that is developing a .NET based application. This application will be hosted in AWS. There is a need to encrypt data. Currently the company does not have a key store for managing encryption. Which of the following could the developer use in this code for encrypting data?
	1. Use S3 Server-side encryption to work with encryption keys
	2. Use the AWS KMS service to generate data keys
	3. Use the AWS Config service to generate data keys
	4. Use S3 client-side encryption to work with encryption keys

3. You’ve been hired as a developer to work on an application. This application is hosted on an EC2 Instance and interacts with an SQS queue. It’s been noticed that when messages are being pulled by the application, a lot of empty responses are being returned. What change can you make to ensure that the application uses the SQS queue effectively?
	1. Use long polling
	2. Set a custom visibility timeout
	3. Use short polling
	4. Implement exponential backoff.

4. A Security system monitors 600 cameras, saving image metadata every 1 minute to an Amazon DynamoDB table. Each sample involves 1 kb of data, and the data writes are evenly distributed over time.
How much write throughput is required for the target table?
	1. 10
	2. 60
	3. 600
	4. 3600

5. Which of the following features allow organizations to leverage a commercial federation server as an identity bridge, providing secure single sign-on into the AWS console without storing user keys and without additional passwords or sign-on?
	1. Web Identification Services
	2. Web Identity Federation
	3. Active Directory Authentication Services
	4. SAML federation

6. A developer is writing an application that will run on –premises, but must access AWS services through an AWS SDK. How can the Developer allow the SDK to access the AWS services?
	1. Create an IAM EC2 role with correct permissions and assign it to the on-premises server.
	2. Create an IAM user with correct permissions, generate an access key and store it in aws credentials file
	3. Create an IAM role with correct permissions and request an STS token to assume the role.
	4. Create an IAM user with correct permissions, generate an access key and store it in a Dynamo DB table.

7. A Developer is writing an application that will run on EC2 instances and read messages from an SQS queue. The messages will arrive every 15-60 seconds. How should the Developer efficiently query the queue for new messages?
	1. Use long polling
	2. Set a custom visibility timeout
	3. Use short polling
	4. Implement exponential backoff.

8. A Developer is building an application that needs access to an S3 bucket. An IAM role is created with the required permissions to access the S3 bucket. Which API call should the Developer use in the application so that the code can access to the S3 bucket?
	1. IAM: AccessRole
	2. STS: GetSessionToken
	3. IAM:GetRoleAccess
	4. STS:AssumeRole

9. A Developer is writing several Lambda functions that each access data in a common RDS DB instance. They must share a connection string that contains the database credentials, which are a secret. A company policy requires that all secrets be stored encrypted.
Which solution will minimize the amount of code the Developer must write?
	1. Use common DynamoDB table to store settings
	2. Use AWS Lambda environment variables
	3. Use Systems Manager Parameter Store secure strings
	4. Use a table in a separate RDS database.

10. A developer is using Amazon API Gateway as an HTTP proxy to a backend endpoint. There are three separate environments: Development, Testing, Production and three corresponding stages in the API gateway.
How should traffic be directed to different backend endpoints for each of these stages without creating a separate API for each?
	1. Add a model to the API and add a schema to differentiate different backend endpoints.
	2. Use stage variables and configure the stage variables in the HTTP integration Request of the API
	3. Use API Custom Authorizers to create an authorizer for each of the different stages.
	4. Update the Integration Response of the API to add different backend endpoints.  

11. An organization deployed their static website on Amazon S3. Now, the Developer has a requirement to serve dynamic content using a serverless solution. Which combination of services should be used to implement a serverless application for the dynamic content? Select 2 answers from the options given below
	1. Amazon API Gateway
	2. Amazon EC2
	3. AWS ECS
	4. AWS Lambda
	5. Amazon kinesis

12. An organization has an Amazon Aurora RDS instance that handles all of its AWS-based e-commerce activity. The application accessing the database needs to create large sales reports on an hourly basis, running 15 minutes after the hour. This reporting activity is slowing down the e-commerce application.
Which combination of actions should be taken to reduce the impact on the main e-commerce application? Select 2 answers from the options given below
	1. Point the reporting application to the read replica
	2. Migrate the data to a set of highly available Amazon EC2 instances
	3. Use SQS Buffering to retrieve data for reports
	4. Create a read replica of the database
	5. Create an SQS queue to implement SQS Buffering

13. An application hosted in AWS has been configured to use a DynamoDB table. A number of items are written to the DynamoDB table. These items are only accessed in a particular time frame, after which they can be deleted. Which of the following is an ideal way to manage the deletion of the stale items?
	1. Perform a scan on the table for the stale items and issue the Delete operation.
	2. Create an additional column to store the date. Perform a query for the stale objects and then perform the Delete operation.
	3. Enable versioning for the items in DynamoDB and delete the last accessed version.
	4. Enable TTL for the items in DynamoDB

14. Your architect has drawn out the details for a mobile based application. Below are the key requirements when it comes to authentication. Users should have the ability to sign-in using external identities such as Facebook or Google. There should be a facility to manage user profiles
Which of the following would you consider as part of the development process for the application?
	1. Consider using IAM Roles which can be mapped to the individual users
	2. Consider using User pools in AWS Cognito
	3. Consider building the logic into the application
	4. Consider using SAML federation identities

15. Your mobile application includes a photo-sharing service that is expecting tens of thousands of users at launch. You will leverage Amazon Simple Storage Service (S3) for storage of the user Images, and you must decide how to authenticate and authorize your users for access to these images. You also need to manage the storage of these images. Which two of the following approaches should you use? Choose two answers from the options below
	1. Create an Amazon S3 bucket per user, and use your application to generate the S3 URL for the appropriate content.
	2. Use AWS Identity and Access Management (IAM) user accounts as your application-level user database, and offload the burden of authentication from your application code.
	3. Authenticate your users at the application level, and use AWS Security Token Service (STS)to grant token-based authorization to S3 objects.
	4. Authenticate your users at the application level, and send an SMS token message to the user. Create an Amazon S3 bucket with the same name as the SMS message token, and move the user’s objects to that bucket.
	5. Use a key-based naming scheme comprised from the user IDs for all user objects in a single Amazon S3 bucket.

16. An application has been making use of AWS DynamoDB for its back-end data store. The size of the table has now grown to 20 GB , and the scans on the table are causing throttling errors. Which of the following should now be implemented to avoid such errors?
	1. Large Page size
	2. Reduced page size
	3. Parallel Scans
	4. Sequential scans

17. You are planning on deploying a built application onto an EC2 Instance. There will be a number of tests conducted on this Instance. You want to have the ability to capture the logs from the web server so that it can help diagnose any issues if they occur? How can you achieve this?
	1. Enable Cloudtrail for the region
	2. Install the Cloudwatch agent on the Instance
	3. Use the VPC Flow logs to get the logs from the Instance
	4. Create a dashboard for the key Cloudwatch metrics

18. You are developing a mobile based application that needs to make use of an authentication service. There are a set of videos files which need to be accessed via unauthenticated identities. How can you BEST achieve this using AWS?
	1. Create an IAM user with public access
	2. Create an IAM group with public access
	3. Use AWS Cognito with unauthenticated identities enabled.
	4. Use AWS STS with SAML

19. An application needs to make use of a messaging system. The messages need to be processed in the order they are received and also no duplicates should be allowed. Which of the following would you use for this purpose?
	1. Use the standard SQS Queues
	2. Use the FIFO SQS Queues 
	3. Use SNS
	4. None above

20. A company is planning on developing an application that is going to make use of a DynamoDB table. The structure of the table is given below

Attribute Name | Type | Description
-------------- | ---- | -----------
Product ID | Number | ID of product
Review ID | Number | Automatically generated GUID
Product Name | String | Name of the product
Product Description | String | Description of the product

Which of the following should be chosen as the partition key to ensure the MOST effective distribution of keys?
	1. Product ID
	2. Review ID
	3. Product Name
	4. Production Description

