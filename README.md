# AWS CloudFormation Template: S3 Bucket and EC2 Instance

This repository contains an AWS CloudFormation template (`s3ec2.yaml`) to provision an Amazon S3 bucket and an EC2 instance.

## Template Overview

**Filename:** `s3ec2.yaml`  
**Format Version:** `2010-09-09`  
**Description:**  
This template provisions the following AWS resources:
- An **Amazon S3 bucket**
- An **Amazon EC2 instance** (with default configuration)

## Resources

### `MyS3Bucket`
- **Type:** `AWS::S3::Bucket`
- **Purpose:** Creates an Amazon S3 bucket for storage purposes.

### `MyEC2Instance`
- **Type:** `AWS::EC2::Instance`
- **Properties (may vary depending on the template):**
  - Instance type (e.g., `t2.micro`)
  - AMI ID (Amazon Machine Image)
  - Key pair name
  - Security groups (optional)
  - User data (optional startup scripts)



## How to Deploy

### Using AWS CLI

sh
aws cloudformation create-stack \
  --stack-name s3-ec2-stack \
  --template-body file://s3ec2.yaml \
  --capabilities CAPABILITY_NAMED_IAM
