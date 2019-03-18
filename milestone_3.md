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

16. What is the main advantage of using Amazon SQS? Choose the correct answer from the options below
	1. SQS allows time-critical messages to be sent through a push mechanism eliminating the need to poll for data
	2. SQS is used by distributed applications and can be used to decouple sending and receiving components without requiring each application component to be concurrently available
	3. SQS is the only method available that interacts with workers
	4. None of the above

17. You have developed an application that sends an Amazon SNS message to a topic whenever an order is placed for one of your products on an online store you have just created. Any Amazon SQS queues that are subscribed to that topic would receive identical notifications when a new order is placed. This method of message deliver is called the "fan-out" scenario. Which of the below descriptions is the closest in describing the common attributes of this scenario? Choose the correct answer from the options below
	1. The Amazon SNS message is sent to a topic and then replicated and pushed to multiple Amazon SQS queues, HTTP endpoints, or email addresses, which allows for parallel asynchronous processing.
	2. It enables you to send messages directly to mobile apps, HTTP endpoints, or email addresses, which allows for parallel synchronous processing.
	3. The Amazon SNS message is sent to a topic and then replicated and pushed to multiple Amazon SQS queues, HTTP endpoints, or email addresses, which allows for parallel synchronous processing.
	4. The application and system alerts are notifications, triggered by predefined thresholds, sent to specified users by SMS and/or email.

18. Which of the following is true if long polling is enabled? Choose the correct answer from the options below
	1. If long polling is enabled, then each poll only polls a subset of SQS servers; in order for all messages to be received, polling must continuously occur
	2. Increases costs because each request lasts longer
	3. The reader will listen to the queue until timeout
	4. The reader will listen to the queue until a message is available or until timeout

19. Which of the following statements is true about SQS standard queues? 
Choose the correct answer from the options below.
	1. Messages will be delivered one or more times and messages will be delivered in First in, First out order
	2. Messages will be delivered exactly once and message delivery order is indeterminate
	3. Messages will be delivered one or more times and message delivery order is indeterminate
	4. Messages will be delivered exactly once and messages will be delivered in First in, First out order

20. You have created a mobile application that relies on reading data from DynamoDB. How could you give each mobile device permissions to read from DynamoDB? Choose an answer from the options below
	1. Connect to an EC2 instance which will pull the data from DynamoDB securely
	2. Create an IAM role that can be assumed by an app that allows federated users
	3. Add the username and password into the app code
	4. Create an IAM user

21. Which DynamoDB API call does not consume capacity units? Choose the correct answer from the options below
	1. DeleteItem
	2. UpdateTable
	3. GetItem
	4. UpdateItem

22. Which of the following options cannot be used inside a CloudFormation template? Choose a correct answer from the options below
	1. Ruby statements
	2. Parameters
	3. Intrinsic function
	4. Regular expression

23. Which of the following services could be used alone to host a static web site. Choose an answer from the options below
	1. Amazon DyamoDB
	2. Amazon S3
	3. Amazon SNS
	4. Amazon Cloudfront

24. What options are available to a customer who wants to perform penetration testing of his EC2 web servers? Choose an answer from the options below
	1. Penetration testing is never allowed
	2. AWS automatically performs penetration testing
	3. A customer can perform penetration testing at any time
	4. A customer should request permission from AWS before performing perform penetration testing

25. You attempt to store a new object in the US-East region in Amazon S3 and receive a confirmation that it has been successfully stored. You then immediately make another API call and attempt to read this object. Will you be able to read this object immediately after? Choose the correct answer from the options below
	1. It depends. Objects in Amazon S3 do not become visible until they are replicated to a second region, which can take a few milliseconds or sometimes even a few seconds.
	2. Yes, unless you exceed API call limits.
	3. Yes, US-East has read-after-write consistency which means you will have access to the object immediately after.
	4. US-East imposes a 1 second delay before new objects are readable.

26. You have written an application that uses the Elastic Load Balancing service to spread traffic to several web servers Your users complain that they are sometimes forced to login again in the middle of using your application, after they have already logged in. This is not behavior you have designed. What is a possible solution to prevent this happening? Choose an answer from the options below
	1. Use instance memory to save session state.
	2. Use instance storage to save session state.
	3. Use EBS to save session state
	4. Use ElastiCache to save session state.

27. What HTTP response code indicates that an AWS REST API call resulted in a redirection? Choose an answer from the options below
	1. 300
	2. 200
	3. 404
	4. 502

28. A Developer is building an application that needs access to an S3 bucket. An IAM role is created with the required permissions to access the S3 bucket. Which API call should the Developer use in the application so that the code can access to the S3 bucket?
	1. IAM:AccessRole
	2. STS:GetSessionToken
	3. IAM:GetRoleAccess
	4. STS:AssumeRole

29. What is the max size of an item that corresponds to a single write capacity unit? (While creating an index or table in Amazon DynamoDB, it is required to specify the capacity requirements for the read and write activity) Choose an answer from the options below.
	1. 1 KB
	2. 2 KB
	3. 4 KB
	4. 8 KB

30. Your company has asked you to maintain an application using Elastic Beanstalk. At times , you normally hit the application version limit when deploying new versions of the application. Which of the following is the most effective way to manage this issue?
	1. Delete the application versions manually
	2. Create an application lifecycle policy
	3. Create multiple applications and deploy the different versions to different applications
	4. Delete the application versions manually

31. A company is planning on using AWS CodePipeline for their underlying CI/CD process. The code will be picked up from an S3 bucket. The company policy mandates that all data should be encrypted at rest. Which of the following measures would you take to ensure that the CI/CD process conforms to this policy? Choose 2 possible actions from the options given below.
	1. Ensure that server-side encryption is enabled on the S3 Bucket
	2. Ensure that server-side encryption is enabled on the CodePipeline stage
	3. Configure the code pickup stage in CodePipeline to use AWS KMS
	4. Configure AWS KMS with customer managed keys and use it for S3 bucket encryption

32. Your application currently makes use of AWS Cognito for managing user identities. You want to analyze the information that is stored in AWS Cognito for your application. Which of the following features of AWS Cognito should you use for this purpose?
	1. Cognito Data
	2. Cognito Events
	3. Cognito Streams
	4. Cognito Callbacks

33. Your team is planning on deploying an application on an ECS cluster. They need to also ensure that the X-Ray service can be used to trace the application deployed on the cluster. Which of the following are the right set of steps that are needed to accomplish this? Choose 2 answers from the options given below.
	1. Create a Docker image with the X-Ray daemon
	2. Deploy the EC2 Instance to the ECS Cluster
	3. Deploy the X-Ray daemon to the ECS Cluster
	4. Deploy the docker container to the ECS cluster

34. Your company is planning on hosting a central bucket for allowing various branch office locations to upload objects. Which of the following can be used to ensure objects can be placed in the bucket with least latency issues?
	1. Enable versioning on the bucket
	2. Enable Transfer Acceleration on the bucket
	3. Enable static web site hosting
	4. Place the bucket behind an ELB

35. Your team is currently working on source code that’s defined in a Subversion repository. The company has just started using AWS tools for their CI/CD process and has now mandated that source code be migrated to AWS CodeCommit. Which of the following steps would you perform to fulfil this requirement. Choose 2 answers from the options given below.
	1. Migrate the code as it is to the AWS Code Commit Repository
	2. Ensure to clone the current repository before committing it to AWS Code Commit
	3. Migrate the code to a Git Repository first
	4. Migrate Git code to AWS Code Commit

36. Your using the AWS CodeDeploy service to deploy an application onto AWS. The application uses secure parameters which are stored in the AWS Systems Manager Parameter store. Which of the following must be done , so that the deployment can be automated via CodeDeploy? Choose 2 answers from the options given below.
	1. Give permissions to the AWS Code Deploy service via an IAM Role
	2. Give permissions to the AWS Code Deploy service via AWS Access Keys
	3. Use the aws ssm get-parameters with the --with-no-decryption option
	4. Use the aws ssm get-parameters with the --with-decryption option

37. You have an application that needs to encrypt data using the KMS service. The company has already defined the customer master key in AWS for usage in the application. Which of the following steps must be followed in the encryption process? Choose 2 answers from the options given below
	1. Use CustomerMaster Key to encrypt the data
	2. Use the GenerateDataKey to get the data key to encrypt the data
	3. Delete the plaintext data encryption key after the data is encrypted
	4. Delete the Customer Master Key after the data is encrypted

38. Your team is performing a load testing for an application. This application is making use of DynamoDB tables. They need to monitor the throughput for the table to ensure that the Consumed capacity does no go beyond the throughout capacity. Which of the following service would you use for this purpose?
	1. AWS Cloudwatch
	2. AWS Cloudtrail
	3. AWS SQS
	4. AWS SNS

39. Your team is using the AWS CodeBuild service for an application build. As part of Integration testing during the build phase, the application needs to access an RDS instance in a private subnet. How can you ensure this is possible?
	1. Create a VPC Endpoint and ensure the codebuild project configuration is modified with the endpoint information
	2. Provide additional VPC-specific configuration information as part of your AWS CodeBuild project
	3. Mark the subnet as a public subnet during the time of the Integration tests
	4. Use a NAT gateway to relay the requests from AWS CodeBuild to the RDS Instance

40. Your team has just moved from their Jenkins setup to using the AWS Code Pipeline service in AWS. They have a requirement to ensure triggers are in place during various stages in the pipeline so that actions can be taken based on those triggers. Which of the following can help you achieve this?
	1. AWS Cloudwatch Events
	2. AWS Config
	3. AWS Cloudtrail
	4. AWS Trusted Advisor
