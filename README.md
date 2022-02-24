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

aws cloudformation create-stack --stack-name demo1-vpc --template-body file://csye6225-infra.yml

# AWS CLI stack commands
#create vpc using dynamic vpccidrblock
aws cloudformation create-stack --stack-name demo1-vpc1 --template-body file://csye6225-infra.yml --parameters file://parameter.json

#update stack 
aws cloudformation update-stack --stack-name demo1-vpc1 --template-body file://csye6225-infra.yml --parameters file://parameter.json

#delete-stack
aws cloudformation delete-stack --stack-name demo1-vpc1 

