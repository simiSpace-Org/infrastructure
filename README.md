# Infrastructure

# Check if valid yaml file 
http://www.yamllint.com/

# AWS Cloud Formation cloudformation Profile

aws configure --profile=dev
aws configure --profile=demo

export AWS_PROFILE=dev
export AWS_PROFILE=demo

# Change Regions
export AWS_REGION=us-east-1

# AWS : Networking

# AWS CLI stack commands
## create stack
aws cloudformation create-stack --stack-name demo5-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json
aws cloudformation create-stack --stack-name demo5-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json --capabilities CAPABILITY_NAMED_IAM

aws cloudformation create-stack --stack-name demo5-vpc7 --template-body file://demo.yml --parameters file://parameter.json

## update stack 
aws cloudformation update-stack --stack-name demo5-vpc9 --template-body file://csye6225-infra.yml --parameters file://parameter.json

## delete-stack
aws cloudformation delete-stack --stack-name demo1-vpc737 

# To go into EC2 
ssh -i "simis_cloud.pem" ec2-user@ec2-44-199-234-165.compute-1.amazonaws.com


/Users/seeminvasaikar/Desktop/demo4/infrastructure-main/csye6225-infra.yml

      


/Users/seeminvasaikar/Desktop/demo4/infrastructure-main/parameter.json      