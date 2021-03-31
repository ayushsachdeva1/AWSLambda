# Sample code for prediction using a model  
    import json
    import boto3
    import pickle
    import pandas as pd
    from sklearn.metrics import mean_absolute_error
    from sklearn.linear_model import LinearRegression

    def lambda_handler(event, context):
    
        key = 'file_name.pkl'
        directory = 'directory_name'
        bucket = 'bucket_name'
        s3_resource = boto3.resource('s3')
        LR = pickle.loads(s3_resource.Bucket(bucket).Object(directory + key).get()['Body'].read())

        key2 = 'test_data.csv'
        s3_object = s3_resource.Object(bucket, directory  + key2)

        data = s3_object.get()
        test_data = pd.read_csv(data['Body'], sep=',')

        x_test = test_data.loc[:,['km_driven']]
        y_test = test_data.loc[:,['selling_price']]

        y_pred = LR.predict(x_test)
       
        print('Mean Absolute Error: ', mean_absolute_error(y_test, y_pred))


