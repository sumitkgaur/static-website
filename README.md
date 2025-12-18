## Creating website 
export AWS_ACCESS_KEY_ID="..."
export AWS_SECRET_ACCESS_KEY="..."
export AWS_REGION="ap-southeast-2"

use aws configure to verify

## Terraform code execution 

cd 00-backend
terraform init
terraform apply   -var="state_bucket_name=sumit-website-bucket" -var="aws_region=ap-southeast-2"

cd ../01-website
terraform init
terraform apply

## Static website access
cloudfront_url = "https://d26yqisan524er.cloudfront.net"
s3_bucket_name = "static-site-site-20251218115959126900000001"