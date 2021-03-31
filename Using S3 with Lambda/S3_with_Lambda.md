# Using S3 with AWS Lambda
![image](https://user-images.githubusercontent.com/55956808/113081490-62993480-919e-11eb-952a-8cfdda7b211d.png)

Storing files in and getting files from S3 is very similar in Lambda as with other AWS services. 

We will be using Boto3 library for interacting with S3. Boto3 is a software development kit (SDK) provided by AWS to facilitate the interaction with S3 APIs and other services such as Elastic Compute Cloud (EC2). Using Boto3, we can list all the S3 buckets, create an EC2 instances, or control any number of AWS resources.

Use the following commands for uploading and downloading files from S3.

    def upload_file(file_name, bucket):
        object_name = file_name
        s3_client = boto3.client('s3')
        response = s3_client.upload_file(file_name, bucket, object_name)
        return response 
    
    def download_file(file_name, bucket):
        s3 = boto3.resource('s3')
        output = f"downloads/{file_name}"
        s3.Bucket(bucket).download_file(file_name, output)
        return output


Information sources:
1. https://stackabuse.com/file-management-with-aws-s3-python-and-flask/
2. https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html
