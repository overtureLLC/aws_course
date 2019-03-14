1. You’ve been asked to migrate a static web site onto AWS. You have been told that the solution should be COST effective. Which of the following solutions would you consider?
	1. Create an EC2 Instance and deploy the web site
	2. Deploy the web site using S3 static web site hosting
	3. Create an Elastic Beanstalk environment and deploy the web site
	4. Create an Opswork stack and deploy the web site

2. You’ve been given the requirement to customize the content which is distributed to users via a Cloudfront Distribution. The content origin is an S3 bucket. How could you achieve this?
	1. Add an event to the S3 bucket. Make the event invoke a Lambda function which would customize the content.
	2. Add a Step Function. Add a step with a Lambda function just before the content gets delivered to the users.
	3. Consider using Lambda@Edge
	4. Consider using a separate application on an EC2 Instance for this purpose.

3. Your current log analysis application takes more than four hours to generate a report of the top 10 users of your web application. You have been asked to implement a system that can report this information in real time, ensure that the report is always up to date, and handle increases in the number of requests to your web application. Choose the option that is cost-effective and can fulfill the requirements.
	1. Publish your data to CloudWatch Logs, and configure your application to Autoscale to handle the load on demand.
	2. Publish your log data to an Amazon S3 bucket.  Use AWS CloudFormation to create an Auto Scaling group to scale your post-processing application which is configured to pull down your log files stored an Amazon S3.
	3. Post your log data to an Amazon Kinesis data stream, and subscribe your log-processing application so that is configured to process your logging data.
	4. Create a multi-AZ Amazon RDS MySQL cluster, post the logging data to MySQL, and run a map reduce job to retrieve the required information on user counts.

4. Your company is planning on creating new development environments in AWS. They want to make use of their existing Chef recipes which they use for their on-premise configuration for servers in AWS. Which of the following service would be ideal to use in this regard?
	1. AWS Elastic Beanstalk
	2. AWS OpsWork
	3. AWS Cloudformation
	4. AWS SQS

5. Your company has developed a web application and is hosting it in an Amazon S3 bucket configured for static website hosting. The users can log in to this app using their Google/Facebook login accounts. The application is using the AWS SDK for JavaScript in the browser to access data stored in an Amazon DynamoDB table. How can you ensure that API keys for access to your data in DynamoDB are kept secure?
	1. Create an Amazon S3 role in IAM with access to the specific DynamoDB tables, and assign it to the bucket hosting your website.
	2. Configure S3 bucket tags with your AWS access keys for your bucket hosing your website so that the application can query them for access.
	3. Configure a web identity federation role within IAM to enable access to the correct DynamoDB resources and retrieve temporary credentials.
	4. Store AWS keys in global variables within your application and configure the application to use these credentials when making requests

6. Which of the following is the right sequence of hooks that get called in AWS CodeDeploy?
	1. Application Stop->BeforeInstall->After Install->Application Start
	2. BeforeInstall->After Install-> Application Stop-> Application Start
	3. BeforeInstall->After Install->Validate Service-> Application Start
	4. BeforeInstall->Application Stop-> Validate Service-> Application Start

7. Your team has a Code Commit repository in your account. You need to give access to a set of developer’s in another account access to your Code Commit repository. Which of the following is the most effective way to grant access?
	1. Create IAM users for each developer and provide access to the repository
	2. Create an IAM Group , add the IAM users and then provide access to the repository
	3. Create a cross account role , give the role the privileges. Provide the role ARN to the developers.
	4. Enable public access for the repository.

8. You are planning to use AWS Kinesis streams for an application being developed for a company. The company policy mandates that all data is encrypted at rest. How can you accomplish this in the easiest way possible for Kinesis streams?
	1. Use the SDK for Kinesis to encrypt the data before being stored at rest
	2. Enable server-side encryption for Kinesis streams
	3. Enable client-side encryption for Kinesis streams
	4. Use the AWS CLI to encrypt the data

9. Your company has a large set of data sets that need to be streamed directly into Amazon S3. Which of the following would be perfect for such a requirement?
	1. Kinesis Streams
	2. Kinesis Data Firehose
	3. AWS Redshift
	4. AWS DynamoDB

10. You just developed code in AWS Lambda that makes use of recursive functions. After several invocations, you are beginning to see throttling errors in the metrics. Which of the following should be done to resolve this issue?
	1. Place the recursive function in a separate package
	2. Use versioning for the recursive function
	3. Avoid using recursive code altogether
	4. Use the API gateway to call the recursive code.

11. Your team has developed an application that makes use of AWS resources. In order to provide frequent releases to the customer, you are required to automate the CI/CD process. Which of the following can be used for this purpose?
	1. Create a Pipeline using AWS CodePipeline. Configure a stage for Unit testing as well in the Pipeline.
	2. Use AWS CodeCommit to host your code repository. Use the build tool in AWS CodeCommit to build your pipeline
	3. Create a Pipeline in the AWS CodeBuild Service
	4. Create a Pipeline in the AWS CodeStar service

12. Your company is planning on storing documents in an S3 bucket. The documents are sensitive, and employees should use Multi Factor authentication when trying to access documents. Which of the following must be done to fulfil this requirement?
	1. Ensure that Encryption is enabled the bucket AWS server-side encryption
	2. Ensure that Encryption is enabled the bucket using KMS keys
	3. Ensure that the a bucket policy is in place with a condition of "aws:MultiFactorAuthPresent":"false" with a Deny policy
	4. Ensure that the a bucket policy is in place with a condition of "aws:MultiFactorAuthPresent":"true" with a Deny policy

13. You are developing an application that is going to make use of Docker containers. You need to use an orchestration service on the AWS Cloud for managing the application. Which of the following service would you use for this purpose?
	1. AWS Code Deploy
	2. AWS ECS
	3. AWS SQS
	
	4. AWS Cloudfront

14. Your team lead has finished creating a build project in the console. You have access to run the build but not to access the project. You want to specify a different source location for the build. How can you achieve this?
	1. Issue the update project command and specify the new location of the build
	2. Specify the new location of the build in the buildspec.yml file and issue the update-project command
	3. Specify the new location of the build in the buildspec.yml file and use the start-build command
	4. Specify the new location of the build in the buildspec.yml file and use the update-build command

15. Your company has a set of EC2 Instances and On-premise. They now want to automate the deployment of their applications using the AWS Code Deploy tool in AWS. Which of the following is not a TRUE complete requirement that needs to be fulfilled for preparation of the servers?
	1. Ensure both EC2 Instances and On-premise servers have the Code Deploy agent installed
	2. Ensure both EC2 Instances and On-premise servers can connect to the Code Deploy service
	3. Ensure both EC2 Instances and On-premise servers are tagged
	4. Ensure both EC2 Instances and On-premise servers have instance profile attached to them
