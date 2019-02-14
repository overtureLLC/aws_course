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


32233
13143
33112
23212