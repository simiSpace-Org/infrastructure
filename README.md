# Infrastructure

# AWS Cloud Formation cloudformation Profile

aws configure --profile=dev
aws configure --profile=demo

export AWS_PROFILE=dev
export AWS_PROFILE=demo

# Change Regions
export AWS_REGION=us-east-1

# AWS : SSL Command : 
aws acm import-certificate --certificate fileb://yourcerti.crt --certificate-chain fileb://yourbundle.ca-bundle --private-key fileb://yourkey.pem


# AWS : Networking

# AWS CLI stack commands
## create stack
aws cloudformation create-stack --stack-name demo5-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json
aws cloudformation create-stack --stack-name demo5-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json --capabilities CAPABILITY_NAMED_IAM
