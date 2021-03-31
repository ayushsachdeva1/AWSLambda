# Sample code for creating a ML model 
    
    
    import json
    import boto3
    import csv
    import pandas as pd
    import numpy as np
    from sklearn.linear_model import LinearRegression
    import pickle

    def lambda_handler(event, context):

        key = 'file_name.csv'
        directory = 'directory_name'
        bucket = 'bucket_name'
        s3_resource = boto3.resource('s3')
        s3_object = s3_resource.Object(bucket, directory + key)

        data = s3_object.get()
        df = pd.read_csv(data['Body'], sep=',')

        x_train = df.loc[:,['km_driven']]

        y_train = a.loc[:,['selling_price']]

        LR=LinearRegression()
        LR.fit(x_train,y_train)

        pickled_model = pickle.dumps(LR)
        output_key = "output_file_name.pkl"
        s3_resource.Bucket(bucket).put_object(Key=directory + output_key, Body=pickled_model)

