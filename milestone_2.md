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
Which of the following should be chosen as the partition key to ensure the MOST effective distribution of keys?
	1. Product ID
	2. Review ID
	3. Product Name
	4. Production Description

Attribute Name | Type | Description
-------------- | ---- | -----------
Product ID | Number | ID of product
Review ID | Number | Automatically generated GUID
Product Name | String | Name of the product
Product Description | String | Description of the product

21. A company is planning on using DynamoDB as their data store. The tables in DynamoDB will be receiving millions of requests. Which of the following can be used to ensure the latency of requests to the DynamoDB table is kept at a minimal?
	1. Createa read replica of the DynamoDB table
	2. Enable Multi-AZ for the DynamoDB table
	3. Enable DynamoDB Accelerator
	4. Enable Encryption for the DynamoDB table

22. You’ve developed a Lambda function and are now in the process of debugging it. You add the necessary print statements in the code to assist in the debugging. You go to Cloudwatch logs , but you see no logs for the lambda function. Which of the following could be the underlying issue for this?
	1. You’ve not enabled versioning for the Lambda function
	2. The IAM Role assigned to the Lambda function does not have the necessary permission to create Logs
	3. There is not enough memory assigned to the function
	4. There is not enough time assigned to the function

23. Your team is developing a solution that will make use of DynamoDB tables. Due to the nature of the application, the data is needed across a couple of regions across the world. Which of the following would help reduce the latency of requests to DynamoDB from different regions?
	1. Enable Multi-AZ for the DynamoDB table
	2. Enable global tables for DynamoDB
	3. Enable Indexes for the table
	4. Increase the read and write throughput for the table

24. Your application is developed to pick up metrics from several servers and push them off to Cloudwatch. At times , the application gets client 429 errors. Which of the following can be done from the programming side to resolve such errors?
	1. Use the AWS CLI instead of the SDK to push the metrics
	2. Ensure that all metrics have a timestamp before sending them across
	3. Use exponential backoff in your requests
	4. Enable encryption for the requests

25. As a developer you have been told to create an API gateway stage that will directly interact with DynamoDB tables. Which of the following feature of the API Gateway must be used to fulfill this requirement?
	1. Ensure to create an Integration request
	2. Ensure to enable CORS
	3. Ensure to enable DAX
	4. Enable Binary payloads

26. You have recently developed an AWS Lambda function to be used as a backend technology for API gateway. You need to give the API gateway URL to a set of users for testing. What must be done before the users can test the API?
	1. Ensure that a deployment is created in the API gateway
	2. Ensure that CORS is enabled for the API gateway
	3. Generate the SDK for the API
	4. Enable support for binary payloads

27. An application is making a request to AWS STS for temporary access credentials. Below is the response being received
Which of the following is TRUE with regards to the above response?
	1. The  SecretAccessKey can be used like Access keys to make request to resources
	2. The user will assume the role of arn:aws:sts::123456789012:assumed-role/demo/lambda
	3. The session token will be valid for the lifetime of the application
	4. The Request ID can be used to make requests to access other AWS resources

```xml
<AssumeRoleResponse xmlns="https://sts.amazonaws.com/doc/2011-06-15/">
	<AssumeRoleResult>
		<Credentials>
  			<SessionToken>
   				AQoDYXdzEPT//////////wEXAMPLEtc764bNrC9SAPBSM22wDOk4x4HIZ8j4FZTwdQW
   				LWsKWHGBuFqwAeMicRXmxfpSPfIeoIYRqTflfKD8YUuwthAx7mSEI/qkPpKPi/kMcGd
   				QrmGdeehM4IC1NtBmUpp2wUE8phUZampKsburEDy0KPkyQDYwT7WZ0wq5VSXDvp75YU
   				9HFvlRd8Tx6q6fE8YQcHNVXAkiY9q6d+xo0rKwT38xVqr7ZD0u0iPPkUL64lIZbqBAz
   				+scqKmlzm8FDrypNC9Yjc8fPOLn9FX9KSYvKTr4rvx3iSIlTJabIQwj2ICCR/oLxBA==
  			</SessionToken>
  			<SecretAccessKey>
   				wJalrXUtnFEMI/K7MDENG/bPxRfiCYzEXAMPLEKEY
  			</SecretAccessKey>
  			<Expiration>
  				2011-07-15T23:28:33.359Z
  			</Expiration>
  			<AccessKeyId>
  				AKIAIOSFODNN7EXAMPLE
  			</AccessKeyId>
		</Credentials>
		<AssumedRoleUser>
  			<Arn>
  				arn:aws:sts::123456789012:assumed-role/demo/lambda
  			</Arn>
  			<AssumedRoleId>
  				ARO123EXAMPLE123:lambda
  			</AssumedRoleId>
		</AssumedRoleUser>
		<PackedPolicySize>
			6
		</PackedPolicySize>
	</AssumeRoleResult>
	<ResponseMetadata>
		<RequestId>
			c6104cbe-af31-11e0-8154-cbc7ccf896c7
		</RequestId>
	</ResponseMetadata>
</AssumeRoleResponse>
```

28. You have an application that is hosted on an EC2 Instance. This application is part of a custom domain (www.demo.com). The application has been changed to make calls to the API gateway. But the browser is not rendering the responses and Javascript errors are being seen in the developer console. What must be done to ensure that this issue can be resolved?
	1. Make the application call a Lambda function instead.
	2. There is an issue with the stage defined on the API gateway, hence define a new stage
	3. Make use of Cognito user pools
	4. Enable CORS for the API gateway

29. You’re developing an application that is going to be hosted in AWS Lambda. The function will make calls to a database. The security mandate is that all connection strings should be kept secure. Which of the following is the MOST secure way to implement this?
	1. Use Lambda Environment variables
	2. Put the database connection string in the app.json file
	3. Put the database connection string in AWS Systems Manager Parameter Store
	4. Place the database connection string in the AWS Lambda function itself since all lambda functions are encrypted at rest

30. Your team needs to create a custom Elastic Beanstalk environment. The application requires an instance that needs a lot of custom software installed. Which of the following is the ideal way to prepare this environment?
	1. Ensure that you choose a Web server environment
	2. Ensure that you choose a Worker environment
	3. Create multiple environments
	4. Create a custom AMI

31. You’re developing an application that will need to do the following: Upload images via a front end from users, store the images in S3, add the location of the images to a DynamoDB table, Which of the following two options would be part of the implementation process?
	1. Add a Lambda function which would respond to events in S3
	2. Add a message to an SQS queue after the object is inserted into the bucket.
	3. Ensure that the Lambda function has access to the DynamoDB table
	4. Ensure that the SQS service has access to the DynamoDB table

32. You are planning on using the Serverless Application Model to deploy a Lambda function. Below is a normal construct for the template to be used.
Where would the code base for the CodeUri normally point to?
	1. The code as a zip package in Amazon Glacier
	2. The code as a zip package in Amazon EBS Volumes
	3. The code as a zip package in Amazon S3
	4. The code as a zip package in Amazon Config

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Transform: AWS::Serverless-2016-10-31
Resources:
  PutFunction:
  Type: AWS::Serverless::Function
        Properties:
           Handler: index.handler
           Runtime: nodejs6.10
           CodeUri:
```

33. Your development team is planning on using AWS ElastiCache – Redis for their caching implementation. It needs to be ensured that data is only filled in the cache when it is required. Which of the following cache strategy can be used for this purpose?
	1. Lazy loading
	2. Write through
	3. Adding a TTL
	4. Use Redis AOF

34. Your team has an application deployed using the Elastic Beanstalk service. A Web environment has been configured for the production environment. There is now a requirement to perform a Blue Green deployment for a new version of the application. How can you achieve this?
	1. Create a new application and swap the application environments.
	2. Create a new application version and upload the new application version
	3. Create a new environment in the application with the updated application version and perform a swap
	4. Create a new environment in the application and Load the configuration of an existing environment

35. Your team has an application deployed on the AWS platform. This application is making requests to an S3 bucket. There is a surge of increased number of GET requests. After monitoring using Cloudwatch metrics you can see the rate of GET requests going close to 5000 requests per second. Which of the following can be used to ensure the performance and cost are optimized?
	1. Add an Elasticache in front of the S3 bucket
	2. Use DynamoDB instead of using S3
	3. Place a Cloudfront distribution in front of the S3 bucket
	4. Place an Elastic Load balancer in front of the S3 bucket

36. Your team is working on an application that will connect to a MySQL RDS Instance.  The security mandate is that the connection to the database from the application should be encrypted.  How can you accomplish this?
	1. By using Access Keys assigned to an IAM user
	2. By using Private Key pairs
	3. By using SSL
	4. By using KMS Keys

37. You are planning on developing and deploying a Node.js Lambda function. The code has a dependency on a lot of third-party libraries. Which of the following needs to be done to ensure the code can be executed in the AWS Lambda service?
	1. Install the third-party libraries in the Lambda service
	2. Create a deployment package with your code and the third-party libraries
	3. Use Cloudformation templates to deploy the third-party libraries
	4. Use an IAM Role with the required permissions on those libraries

38. A company has an application that is making use of a DynamoDB table. There is now a requirement to ensure that all changes to the items in the table are recorded and stored in a MySQL database. Which of the following would ideally be one of the implementation steps?
	1. Enable DynamoDB Accelerator
	2. Enable DynamoDB global tables
	3. Enable DynamoDB streams
	4. Enable DynamoDB triggers

39. You have developed a Lambda function. This function needs to run on a scheduled basis. Which of the following can be done to accomplish this requirement in an ideal manner?
	1. Use the schedule service in AWS Lambda
	2. Use an EC2 Instance to schedule the Lambda invocation
	3. Use Cloudwatch events to schedule the Lambda function
	4. Use Cloudtrail to schedule the Lambda function

40. Which of the descriptions below best describes what the following bucket policy does?
Choose the correct answer from the options below
	1. It allows read and write access to bucket 'mybucket'.
	2. It allows read access to bucket 'mybucket' but only if it is accessed from www.example.com or www.demo.com.
	3. It allows read access to bucket 'mybucket' for all requests.
	4. It allows read or write access to bucket 'mybucket' but only if it is accessed from www.example.com or www.demo.com.

```json
{
   "Version":"2012-10-17",
   "Id":"Statement1",
   "Statement":[
    {
       "Sid":" Statement2",
       "Effect":"Allow",
       "Principal":"*",
       "Action":"s3:GetObject",
       "Resource":"arn:AWS:s3:::mybucket/*",
       "Condition":{
             "StringLike":{"AWS:Referer":["http://www.example.com/*","http://www.demo.com/*"]}
        }
   }
  ]
}
``` 
