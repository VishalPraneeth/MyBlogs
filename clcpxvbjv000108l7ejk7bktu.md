# Serverless computing with AWS Lambda

AWS Lambda is a serverless computing platform provided by Amazon Web Services. It allows you to run code without provisioning or managing servers. With Lambda, you can build and run applications and services, in multiple languages, including Node.js, Python, and Java.

AWS Lambda has the ability to automatically scale your application in response to the incoming load of requests it experiences through implementing a Load balancer(Application/Network), this can result in significant cost savings.

The great advantage of Lambda is that you can integrate it with various other services and build end-to-end applications by making use of S3 Buckets, Amazon RDS, Amazon Lex, and many more.

My beginner introduction to AWS Lambda was by deploying a serverless REST API with integrating it with AWS API Gateway and Application Load Balancer. The python packages for request and response were uploaded as a zip file and layered along with Lambda. The simple test case was written to verify the output before deploying.

Later on, I worked on deploying a WordPress application and also a QnA Chatbot where AWS Lambda plays a vital role in being the serverless backend of the project.

When it comes to using the Lambda function, one should have some basic knowledge of the underlying AWS services, as well as the programming language you plan to use to author your functions. Additionally, you should be familiar with the concept of event-driven programming and the use of triggers and callbacks.

You can also monitor and troubleshoot your Lambda function using CloudWatch. There are plenty of tools,libraries that are available for the user to use AWS Lambda efficiently.