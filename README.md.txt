Rendering a Document from One Language to Another

Services used:- S3 bucket,IAM,Lambda

Step by Step process

Step 1:- Navigate to S3 services in AWS console
	Create Two S3 buckets named as inputbucketklu & outputbucketklu
•	Click on create bucket
•	Give the bucket name 
•	Click on create
Step 2:-  Navigate to IAM 
	Go to roles 
•	Click on create role
•	In use case choose lambda 
•	Then click on next
•	Now add the permissions amazonS3FullAccess, TranslateFullAccess, CloudWatchFullAccess then click on next
•	Give the role name and click on create role
Step 3:- Navigate to Lambda function
	Click on create function
•	Give the Function name as translatelabmda
•	Choose the runtime (ex : python)
•	In Change default execution role choose Use an existing role
•	Existing role “ translate”
•	Click on create function
	Click on add trigger choose s3 “ inputbucketklu”
	Click on add
	Then trigger inputbucketklu was successfully added to function translatelabmda

•	Then go to code – source code 
	Deploy the code
Step 4:- go to s3 bucket upload the text file in inputbucketklu 
Step 5:- In lambda go to monitor- cloudWatch logs 
	In log groups “Log streams”


