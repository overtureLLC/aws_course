1. You’ve written an application that uploads objects onto an S3 bucket. The size of the object varies between 200 – 500 MB. You’ve seen that the application sometimes takes a longer than expected time to upload the object. You want to improve the performance of the application. Which of the following would you consider?
	1. Create multiple threads and upload the objects in the multiple threads
	2. Write the items in batches for better performance
	3. Use the Multipart upload API
	4. Enable versioning on the Bucket

2. An application running on Amazon EC2 must store objects in an S3 bucket.
Which option follows best practices for granting the application access to the S3 bucket?
	1. Use the userdata script to store an access key on the EC2 instance
	2. Use an AWS IAM role with permissions to write to the S3 bucket
	3. Store an access key encrypted with AWS KMS in Amazon S3
	4. Embed an access key in the application code

3. An application is publishing a custom CloudWatch metric any time an HTTP 504 error appears in the application error logs. These errors are being received intermittently. There is a CloudWatch Alarm for this metric and the Developer would like the alarm to trigger only if it breaches two evaluation periods or more.
What should be done to meet these requirements?
	1. Update the CloudWatch Alarm to send a custom notification depending on results
	2. Publish the value zero whenever there are no “HTTP 504” errors
	3. Use high – resolution metrics to get data pushed to CloudWatch more frequently
	4. Aggregate the data before pushing to CloudWatch by using statistic sets. 

4. An organization’s application needs to monitor application specific events with a standard AWS service. The service should capture the number of logged in users and trigger events accordingly. During peak times, monitoring frequency will occur every 10 seconds.
What should be done to meet these requirements?
	1. Create an Amazon SNS notification
	2. Create a standard resolution custom Amazon CloudWatch log
	3. Create a high-resolution custom Amazon CloudWatch metric
	4. Create a custom Amazon CloudTrail log.

5. A developer has written an application that will be deployed by a company. The application is used to read and write objects to an S3 bucket. It is expected that the number of reads could exceed 400 requests per second. What should the developer do to ensure that the requests are handled accordingly.
	1. Enable versioning for the underlying bucket
	2. Ensure that the application uses a hash prefix when writing the data to the bucket 
	3. S3 can support these request rates and nothing needs to be done.
	4. Enable Cross region replication for the bucket

6. You’re developing an application that will be hosted on an EC2 Instance. This will be part of an Autoscaling Group. The application needs to get the private IP of the instance so that it can send it across to a controller-based application. Which of the following can be done to achieve this?
	1. Query the Instance Meta Data
	2. Query the Instance User Data
	3. Have an Admin get the IP address from the console
	4. Make the application run IFConfig

7. You’ve been asked to develop an application on the AWS Cloud. The application will involve picking up videos from users and placing them in an ideal and durable data store. Which of the following would be an ideal data store, ensuring that components are properly decoupled?
	1. AWS DynamoDB
	2. EBS Volumes
	3. AWS Simple Storage Service
	4. AWS Glacier

8. You’ve been asked to develop an application on the AWS Cloud. The application will be used to store confidential documents in an S3 bucket. You need to ensure that the bucket is defined in such a way that it does not accept objects that are not encrypted?
	1. Ensure a condition is set in the bucket policy.
	2. Ensure that a condition is set in an IAM policy.
	3. Enable MFA for the underlying bucket
	4. Enable CORS for the underlying bucket

9. You are in charge of deploying an application that will be hosted on an EC2 Instance and sit behind an Elastic Load balancer. You have been requested to monitor the incoming connections to the Elastic Load Balancer. Which of the below options can suffice this requirement?
	1. Use AWS CloudTrail with your load balancer
	2. Enable access logs on the load balancer
	3. Use a CloudWatch Logs Agent
	4. Create a custom metric CloudWatch filter on your load balancer

10. You’ve developed an application script that needs to be bootstrapped into instances that are launched via an Autoscaling Group. How would you achieve this in the easy way possible?
	1. Place a scheduled task on the instance that starts as soon as the Instance is launched.
	2. Place the script in the metadata for the instance
	3. Place the script in the Userdata for the instance
	4. Create a Lambda function to install the script

11. Your company currently stores its objects in S3.  The current request rate is around 11000 GET requests per second. There is now a mandate for objects to be encrypted at rest. So you enable encryption using KMS. There are now performance issues being encountered. What could be the main reason behind this?
	1. Amazon S3 will now throttle the requests since they are now being encrypted using KMS
	2. You need to also enable versioning to ensure optimal performance
	3. You are now exceeding the throttle limits for KMS API calls
	4. You need to also enable CORS to ensure optimal performance

12. Your company is planning on using the Simple Storage service to host objects that will be accessed by users. There is a speculation that there would be roughly 6000 GET requests per second. Which of the following is the right way to use object keys for optimal performance?
	1. exampleawsbucket/2019-14-03-15-00-00/photo1.jpg
	2. exampleawsbucket/sample/232a-2019-14-03-15-00-00photo1.jpg
	3. exampleawsbucket/232a-2019-14-03-15-00-00/photo1.jpg
	4. exampleawsbucket/sample/photo1.jpg

13. Your company is hosting a static web site in S3. The code has recently been changed wherein Javascript calls are being made to the web pages in the same bucket via the FQDN. But the browser is blocking the requests. What should be done to alleviate the issue?
	1. Enable CORS on the bucket
	2. Enable versioning on the bucket
	3. Enable CRR on the bucket
	4. Enable encryption the bucket

14. A company is storing sensitive data in their S3 bucket. The company policy states that all objects in the S3 bucket need to be encrypted at rest. Which of the following help ensure this policy is met?
	1. Deny permission to upload an object if the header does not include x-amz-server-side-encryption
	2. Deny permission to upload an object if the header includes x-amz-server-side-encryption
	3. Deny permission to upload an object if the header does not include x-allow-encryption
	4. Deny permission to upload an object if the header includes x-allow-encryption

15. A company has a cloudformation template that is used to create a huge list of resources. It creates a VPC, subnets , EC2 Instances , Autoscaling Groups , Load Balancers etc. Which of the following should be considered when designing such Cloudformation templates?
	1. Ensure to create one entire stack from the template
	2. Look towards breaking the templates into smaller manageable templates
	3. Package the templates together and use the cloudformation deploy command
	4. Package the templates together and use the cloudformation package command

16. Your team developed and deployed an application on an EC2 Instance. To test the application, you were given access credentials which also included the rights to write to an S3 bucket. Once the testing was confirmed , an IAM Role was assigned to the Instance. This role only has permissions to read from the bucket. But you notice that the application still has access to write to the S3 bucket. Why is this the case?
	1. You need to restart the instance for the Role settings to take effect
	2. The Environment variables which were set for CLI access are taking priority
	3. The CLI is corrupted , hence the credentials are not being revoked
 	4. The EBS Volume needs to be reattached again for the Instance profile to take effect
		
17. You have been told to make use of Cloudformation templates for deploying applications on EC2 Instances. These Instances need to be preconfigured with the NGINX web server to host the application. How could you accomplish this with Cloudformation?
	1. Use the cfn-init helper script in Cloudformation
	2. Use the Output resource type in Cloudformation
	3. Use the Parameter resource type in Cloudformation
	4. Use SAML to deploy the template

18. You are a developer for your company. You are working on creating Cloudformation templates for different environments. You want to be able to base the creation of the environments on the values passed at runtime to the template. How can you achieve this?
	1. Specify an Outputs section
	2. Specify a parameters section
	3. Specify a metadata section
	4. Specify a transform section

19. You are developing an application that is going to make use of Docker containers. Traffic needs to be routed based on demand to the application. Dynamic host port mapping would be used for the docker containers. Which of the following would you use for distribution of traffic to the docker containers?
	1. AWS Application Load Balancer
	2. AWS Network Load Balancer
	3. AWS Route 53
	4. AWS Classic Load Balancer

20. A developer has created a script which access an S3 bucket. The script will run on an EC2 Instance at regular intervals. What is the authentication mechanism that should be employed to ensure that the script works as desired?
	1. Create an IAM user. Ensure the IAM user has access to the S3 bucket via IAM policies. Embed the user name and password in the script.
	2. Create an IAM Role. Ensure the IAM Role has access to the S3 bucket via IAM policies. Attach the role to the instance
	3. Create an IAM user. Ensure the IAM user has access to the S3 bucket via IAM policies. Embed the Access keys to the program.
	4. Create an IAM user. Ensure the IAM user has access to the S3 bucket via IAM policies. Embed the Access keys as environment variables for the Instance.

21. You’ve setup an application on a set of EC2 Instances. It is a web-based application. You’ve also setup a load balancer. During the initial round of testing after deploying, the users complain that they are not able to reach the home page for the web based application. Which of the following must you check? Choose 2 answers from the options given below
	1. Ensure that the load balancer is attached to a private subnet
	2. Ensure that the load balancer is attached to a public subnet
	3. Ensure that the Security Group of the Load balancer allows traffic from the internet
	4. Ensure that the Security Group of the EC2 allows traffic from the internet

22. Your team has developed an application that will be launched on EC2 Instances that are part of the an Autoscaling Group. It needs to be ensured that the application can get the IP address of the Instance. How can you achieve this?
	1. Make the application query the Instance Metadata
	2. Make the application query the Instance Userdata
	4. Make the application query the Autoscaling Group
	5. Make the application query the Launch configuration

23. You’re in charge for creating a cloudformation template. This template needs to create resources for multiple types of environment. The template needs to be flexible so that it can create resources based on the type of environment. How can you achieve this? Choose 2 answers from the options given below.
	1. Create an Input Parameter to take in the type of environment.
	2. Use the Outputs section to define the type of environment
	3. Use the Custom Resources feature to create resources based on the type of environment
	4. Use the Conditions section to create resources based on the type of environment

24. Your company has a development application that needs to interact with an S3 bucket. There is a requirement that all data in the bucket is encrypted at rest. You also need to ensure that the keys are managed by you. Which of the following can you use for this purpose? Choose 2 answers from the options given below
	1. Server-Side Encryption with AWS Managed Keys
	2. Server-Side Encryption with AWS KMS Keys
	3. Server-Side Encryption with Customer-Provided Keys
	4. Client-Side Encryption

25. You are setting out policies for allowing access to users for objects in an S3 bucket. You have configured a policy for testing which currently works as intended. You try to create a more restrictive policy but find out that the changes are not working as intended. What can you do to resolve the issue in the EASIEST way possible?
	1. Delete the current version of the policy and recreate the older one
	2. Revert back to the previous version of the policy
	3. Recreate the IAM users again
	4. Use the recycle bin to get the deleted policies back

26. You are using a custom tool known as POSTMAN to make API requests to resources in AWS. Part of the job of sending requests is to sign the request. Which of the following would you use to sign the API requests made to AWS?
	1. Your user name and password
	2. A private key file
	3. KMS keys
	4. Access Keys

27. An application consists of an Autoscaling Group. It has been determined that the best way to scale the group is based on the number of concurrent users. How can you achieve this?
	1. Create a tag for the Group to contain the number of concurrent users
	2. Create a custom metric for the number of concurrent users
	3. Since concurrent user metrics are not available, base the scaling of the group on CPU percentage
	4. Since concurrent user metrics are not available, base the scaling of the group on Memory percentage

28. As a developer, you need your operations team to monitor a set of metrics for an on-promise application. They also need to be notified in case any of the metrics crosses the threshold. How can you achieve this?
	1. Publish custom metrics for the application that can be monitored via Cloudwatch. Create Alarms for notifications.
	2. Ask the System administrators to monitor the Cloudwatch logs
	3. Ask the System administrators to monitor the Cloudtrail logs
	4. Use the inbuilt metrics for Cloudwatch. Create Alarms for notifications.

29. In regards to their data consistency model, AWS states that "Amazon S3 buckets in all Regions provide read-after-write consistency for PUTS of new objects and eventual consistency for overwrite PUTS and DELETES." What does AWS actually mean when they say Read-after-write consistency for PUTS of new objects? Choose the correct answer from the options below
	1. If you write a new key to S3, you will be able to retrieve any object immediately afterwards. Also, any newly created object or file will be visible immediately, without any delay.
	2. If you write a new key to S3, a subsequent read might return the old data or the updated data. Your applications should be built with this uncertainty in mind.
	3. If you write a new key to S3, it may write corrupted or partial data.
	4. You cannot write a new key to S3 unless there has been a read done prior to the write

30. How much data can be stored in S3? Choose the correct answer from the options below
	1. 500 TB
	2. 500 GB
	3. 5GB
	4. No limits to the amount of data

31. EC2 instances are launched from Amazon Machine Images (AMIs). Which of the below options are true for a given public AMI.
	1. can only be used to launch EC2 instances in the same AWS availability zone as the AMI is stored
	2. can only be used to launch EC2 instances in the same country as the AMI is stored
	3. can be used to launch EC2 instances in any AWS region
	4. can only be used to launch EC2 instances in the same AWS region as the AMI is stored

32. After having created a new Linux instance on Amazon EC2, and downloaded the .pem file (called file.pem) you try and SSH into your IP address (52.2.222.22) using the following command.
	ssh -i file.pem ec2-user@52.2.222.22
However you receive the following error.
WARNING: UNPROTECTED PRIVATE KEY FILE!
What is the most probable reason for this and how can you fix it?
	1. You do not have root access on your terminal and need to use the sudo option for this to work as follows. "sudo ssh -i LAfile.pem ec2-user@52.2.222.22"
	2. Your key file must not be publicly viewable for SSH to work. You need to modify your pem file as follows "chmod 400 LAfile.pem"
	3. Your key file is not encrypted. You need to use the -u option for unencypted not the -i option as follows. "ssh -u LAfile.pem ec2-user@52.2.222.22"
	4. Your key file does not have the correct permissions for you to run the command. You need to modify your pem file as follows "chmod 644 LAfile.pem"

33. Which of the following request headers, when specified in an API call, will cause an object to be SSE-S3? Choose the correct answer from the options below
	1. AES256
	2. amz-server-side-encryption
	3. x-amz-server-side-encryption
	4. server-side-encryption

34. What result would you expect from the Fn::Join function in the following line in a CloudFormation template? Choose an answer from the options below
	"Fn::Join" : [ "/", [ "list-a","list-b","list-c"] ]
	1. lista-listb-listc
	2. list-c/list-b/list-a
	3. list-a:list-b:list-c
	4. list-a/list-b/list-c

35. Fn:GetAtt is used on a CloudFormation template to: Choose an answer from the options below
	1. Conditionally create stack resources
	2. Return the value of an attribute from a resource on the template
	3. Appends a set of values into a single value which can include resources on the template
	4. Returns the value corresponding to keys into a two-level map declared in the mappings section

36. By default, what event occurs if your CloudFormation receives an error during creation? Choose a correct answer from the options below
	1. DELETE_IN_PROGRESS
	2. ROLLBACK_IN_PROGRESS
	3. DELETE_COMPLETE
	4. CREATION_IN_PROGRESS

37. Which of the following AWS services can be used to record logs of all AWS API calls. Choose an answer from the options below
	1. AWS IAM
	2. Amazon Cloudwatch
	3. Amazon EC2
	4. AWS CloudTrail

38. Which of the following items are required to allow an application deployed on an EC2 instance to publish metrics to CloudWatch? Assume that no security Keys are allowed to be stored on the EC2 instance. Choose an answer from options below:
	1. Create an IAM user that allows write access to CloudWatch
	2. Launch an EC2 instance with the IAM user included in the launch configuration.
	3. Create an IAM role that allows write access to CloudWatch and attach to the instance.
	4. Create an IAM user and allow programmatic access.

39. Which of the following are the responsibility of AWS. Choose 2 answers from the options below
	1. Virtualization Infrastructure
	2. Managing security groups
	3. Physical security of AWS data centers
	4. Patching the OS on the running EC2 instance

40. What is required for a subnet to control the flow of traffic in a subnet? Choose one answer from the options below
	1. Route table
	2. Subnet table
	3. VPC table
	4. Route53


32233
13143
33112
23212
(23)1(14)(34)2
42114
42342
243(13)1