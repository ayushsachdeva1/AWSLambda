# Lambda Layers

![image](https://user-images.githubusercontent.com/55956808/111727794-96d53280-8839-11eb-9a6e-02b2d58bc9a7.png)

Lambda Layers are a new type of artifact that can contain arbitrary code and data, and may be referenced by zero, one, or more functions at the same time. Lambda functions in a serverless application typically share common dependencies such as SDKs, frameworks, and now runtimes. With layers, you can centrally manage common components across multiple functions enabling better code reuse. You can configure your Lambda function to pull in additional code and content in the form of these layers. A layer is a .zip file archive that contains libraries, a custom runtime, or other dependencies. 

The easiest way to add python packages that are extensively used is through [this](https://github.com/mthenw/awesome-layers) repository which is a list of ARN/Links to pre-configured Lambda layers containing the required packages. Note that if you get a region error, you might need to change the region while using AWS Lambda or you can try changing the region in the ARN. For example to change the region from us-east-1 to us-west-2 in "arn:aws:lambda:us-east-1:251566558623:layer:python37-layer-pandas-gbq:1", you would change it to "arn:aws:lambda:us-west-2:251566558623:layer:python37-layer-pandas-gbq:1".ARNs for commonly used packages are as follows:
1. pandas: arn:aws:lambda:us-east-1:251566558623:layer:python37-layer-pandas-gbq:1
2. scikit-learn: arn:aws:lambda:us-east-1:446751924810:layer:python-3-7-scikit-learn-0-23-1:2


Step by step guide to adding Lambda Layers:
1. Create your lambda function.
2. Locate the function overview on the function dashboard and click on "Layers".
<img width="863" alt="Screen Shot 2021-03-18 at 10 56 07 PM" src="https://user-images.githubusercontent.com/55956808/111729511-3e079900-883d-11eb-830a-00cd5f9acd1e.png">
3. Click on "Add a Layer". 

4. Choose "Specify an ARN", enter the ARN and click on "Add".
<img width="839" alt="Screen Shot 2021-03-18 at 10 58 39 PM" src="https://user-images.githubusercontent.com/55956808/111729632-7c04bd00-883d-11eb-8a91-33c3491a51af.png">

Information sources:
1. https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html
2. https://aws.amazon.com/blogs/compute/working-with-aws-lambda-and-lambda-layers-in-aws-sam/
3. https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html#configuration-layers-create
