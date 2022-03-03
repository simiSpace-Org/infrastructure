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
aws cloudformation create-stack --stack-name demo1-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json

## update stack 
aws cloudformation update-stack --stack-name demo1-vpc737 --template-body file://csye6225-infra.yml --parameters file://parameter.json

## delete-stack
aws cloudformation delete-stack --stack-name demo1-vpc737 

# Packer Commands

export PACKER_LOG=1

```
//go to folder location of packer and run the following commands
cd Desktop/demoadd3/infrastructure/packer 
packer build -var-file='dev_vars.json' ami.json

# Validate packer
    ./packer validate ami.json

```
# To go into EC2 
ssh -i "simis_cloud.pem" ec2-user@ec2-44-199-234-165.compute-1.amazonaws.com


