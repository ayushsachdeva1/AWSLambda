# AWS Lambda

![image](https://user-images.githubusercontent.com/55956808/110737873-e2f9f480-81f3-11eb-8371-e1fb5c36fd98.png)

AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code as a ZIP file or container image, and Lambda automatically and precisely allocates compute execution power and runs your code based on the incoming request or event, for any scale of traffic. 

## When to use Lambda over EC2?
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment. 

Note that Lambda is classified as a function-as-a-service (FaaS) and EC2 is classified as an infrastructure-as-a-service (IaaS). 

Hence, with Lambda,you don't have to worry about operational and administrative activities that you would perform on an EC2 instance. You can simply run your application/function without being concerned about the underlying infrastructure. Furthermore, Lambda provides easy scaling and high availability to your code without additional effort on your part. Lambda is also better to use if your EC2 instance has a lot of idle time.

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
