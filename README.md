# aws_cf_cur
Cloudformation template for cur deployment. For payer or member

MUST BE DEPLOYED IN **us-east-1**


Parameters:
DestinationBucket:
    Type: String
    Description: Name of the S3 Bucket to be created to hold data information. This name will be combined with account id
  Compression:
    Type: String
    Default: "Parquet"
  Format:
    Type: String
    Default: "Parquet"
  ReportName:
    Type: String
    Default: "AWS-Cost-and-Usage-Report"
  TimeUnit:
    Type: String
    Default: "HOURLY" 
    AllowedValues:
      - "HOURLY" 
      - "DAILY"
      - "MONTHLY"

For more info on how to utilise your CUR see [here](https://wellarchitectedlabs.com/cost/100_labs/100_1_aws_account_setup/)

Next:
Add events to create athena