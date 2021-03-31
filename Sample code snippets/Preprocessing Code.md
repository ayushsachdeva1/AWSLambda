# Sample Code for Preprocessing data
    import json
    import boto3
    import csv
    import pandas as pd
    import numpy as np
    
    def lambda_handler(event, context):
        
        key = 'file_name.csv'
        directory = 'directory_name'
        bucket = 'bucket_name'
        s3_resource = boto3.resource('s3')
        s3_object = s3_resource.Object(bucket, directory + key)

        data = s3_object.get()
        df = pd.read_csv(data['Body'], sep=';')

        ###Preprocessing of dataframe df

        output_key = "output_file_name.csv"
        obj = s3_resource.Object(bucket, directory + output_key)
        obj.put(Body=df.to_csv())
