# Data-Pipeline
Creating a Data Pipeline using AWS
# AWS Data Pipeline: CSV to JSON Conversion

This project demonstrates how to build a scalable and serverless data pipeline using AWS services that automatically converts CSV files into JSON format when uploaded to an S3 bucket.



 Architecture Overview

1. Amazon S3
   - Stores incoming CSV files.
   - Stores output JSON files.

2. AWS Lambda  
   - Triggered when a new CSV file is uploaded to S3.
   - Invokes AWS Glue job.

3. AWS Glue 
   - Reads the CSV file.
   - Converts it into JSON format.
   - Writes the output to another S3 bucket/folder.

4. Amazon CloudWatch 
   - Monitors the pipeline.
   - Logs Lambda and Glue activity for debugging and tracking.

 ##How It Works
1.Upload a .csv file to csv-input-bucket.

2.Lambda is triggered → starts Glue job.

3.Glue reads the CSV → transforms → writes a .json file to json-output-bucket.

4.CloudWatch logs everything for review.


IAM Permissions:
AWSs3Fullaccess
AWSlambdaFullaccess
AWSglueconsoleFullaccess




