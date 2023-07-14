# Amoria-Tea-BackendTemplate
Backend Template

## AWS Terraform (Automated) 
This option uses terraform and will set up the required cloud infrastructure (Lambda, IAM user, and API Gateway) for you. Also, if you wanted to delete resources, you won't have to individually delete resources manually; you can simply remove resources with terraform in one go. 

## Required
-------------------------------------------------------------------------------------------------------
## AWS Console

1. Create AWS Account
2. Create IAM user with correct permissions for using Lambda and API Gateway
3. Login with that new user credentials
4. Create Rest API with API Gateway
5. Create Lambda Function

### Rest API with API Gateway

1. Create two API resources (API endpoints) one representing client orders to business and the other representing conformation email for client
2. Create a **method** via "Actions" button
3. Enable cors on API endpoint, and only allow request from AmoriaTea domain (i.e. www.domain.com)
4. Deploy API, this will ask you to stage your API **The url given after deploy is not correct**
   (i.e. https://something/**stage name**/**your endpoint**)


### Lambda Function

* In the lambda function you need add a lambda environment variable, indicating the APIKEY that you 
got from sendgrid

1. Create two different Lambda Functions for both API endpoints (choose the latest version of python)
2. Use the zip files that from the github repo
3. **Optional** You can upload via s3 or from your system
4. Go to runtime settings to change handler name to "lambda_function.lambda_handler"
