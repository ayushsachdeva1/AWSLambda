# AWS Lambda

![image](https://user-images.githubusercontent.com/55956808/110737873-e2f9f480-81f3-11eb-8371-e1fb5c36fd98.png)

AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code as a ZIP file or container image, and Lambda automatically and precisely allocates compute execution power and runs your code based on the incoming request or event, for any scale of traffic. 

## Advantages of AWS Lambda
* Quick and efficient deployment of resources
* No idle server time 
* Charges per Millisecond i.e. you only pay for as much time you use the server for
* Low operational complexity
* Easy to scale functions
* Rich ecosystem of AWS services that can be used as triggers for function

## When to use Lambda over EC2?
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment. 

Note that Lambda is classified as a function-as-a-service (FaaS) and EC2 is classified as an infrastructure-as-a-service (IaaS). 

Hence, with Lambda, you don't have to worry about operational and administrative activities that you would perform on an EC2 instance. You can simply run your application/function without being concerned about the underlying infrastructure. Furthermore, Lambda provides easy scaling and high availability to your code without additional effort on your part. Lambda is also better to use if your EC2 instance has a lot of idle time.

On the other hand, if your applications are high-performance, long-running, or are applications must not have a delay at the start time, you should be using EC2. Also, EC2 should be used if you need the option to customize the operating system or network and security settings, or the underlying architecture.

## Available Languages: 
* Java
* Go
* PowerShell
* Node.js
* C#
* Python
* Ruby code

For the purposes of this repository, we will be focusing on using Python with AWS Lambda in order to facilitate data pre-processing and machine learning modeling.

Information sources:
1. https://aws.amazon.com/lambda/
2. https://docs.aws.amazon.com/whitepapers/latest/security-overview-aws-lambda/benefits-of-lambda.html
3. https://aws.amazon.com/lambda/faqs/#:~:text=AWS%20Lambda%20natively%20supports%20Java,%2C%20C%23%2C%20Go%20and%20PowerShell.
4. https://www.thesunflowerlab.com/blog/benefits-aws-lambda-serverless-computing/#:~:text=AWS%20Lambda%20is%20offered%20as,thousands%20of%20requests%20per%20second.
5. https://www.nakivo.com/blog/aws-lambda-vs-amazon-ec2-which-one-to-choose/
