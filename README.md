# Uploadfile
//Python JSON Sales upload to bucket

import json
import boto3

s3Client= boto3.client("s3")

json_object='SalesJan.json'

response=s3Client.put_object(
     Body=json.dumps(json_object),
     Bucket='Sales-2021',
     Key='SalesJan.json'
)

print(response)

