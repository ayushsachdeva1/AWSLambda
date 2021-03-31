# Python Functions on AWS Lambda

Quick Steps to create Lambda function:
1. Click on top right corner button "Create Function".
2. Select "Author from scratch" (or "Use a Blueprint" if there is a blueprint available).
3. Choose name and select runtime as "Python 3.7" and NOT "Python 3.8" (This is because many layers are only available for Python 3.7).
4. Choose appropriate execution role.
5. Ignore advanced settings and click on the "Create Function" button on the bottom right. 
<img width="1311" alt="Screen Shot 2021-03-30 at 9 04 28 PM" src="https://user-images.githubusercontent.com/55956808/113081117-b0616d00-919d-11eb-8e55-f7c7db10070a.png">

Using AWS Lambda Environment for Code Execution
1. Note that there is only function in the code by default i.e. the lambda handler. Do not change the signature of this function but feel free to create other functions.
2. Treat the lambda handler function as main() function in C++/Java. It is responsible for the running all the code. The AWS Lambda processor only runs the lambda_handler so you want to put all your executables in there.
3. Input and output in the lambda_handler is done through JSON or through system output which is, as usual, done through print statements. 
4. Add all the executable code to the lambda_handler and click on "Deploy".
<img width="1278" alt="Screen Shot 2021-03-30 at 9 12 48 PM" src="https://user-images.githubusercontent.com/55956808/113081139-bce5c580-919d-11eb-935c-a2f17a4cddde.png">
5. In order to test/run the code, click on "Test". <br /> 
6. If you don't take any input, then just delete all the JSON content in the testing code as shown. If input is required, edit JSON accordingly. <br /> 
7. Click "Test" and see output in execution pane. 
<img width="818" alt="Screen Shot 2021-03-30 at 9 14 47 PM" src="https://user-images.githubusercontent.com/55956808/113081153-c66f2d80-919d-11eb-878e-5be37c3f7910.png">

Trouble-shooting
1. Run-time issues: If run-time is too short, change it using the "Configuration" pane. 
2. Import issues: Various python modules are not available in AWS Lambda. Check out page on Lambda Layers for ways to work around it.
3. Saving issues: Lambda functions are automatically saved. Make sure you are in the same region as when you created the function, as us-west and us-east might show different functions.

Information sources:
1. https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html
2. https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html
