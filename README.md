# AWS CloudFormation Stack: Windows EC2 Auto Scaling with S3

This repository contains an AWS CloudFormation template that provisions a scalable infrastructure with Windows EC2 instances and an S3 bucket.

## Stack Resources

- Virtual Private Cloud (VPC)
- Auto Scaling Group with Windows EC2 instances
- Security Group for RDP access
- S3 Bucket for storage

## Prerequisites

Before deploying this stack, ensure you have:

1. An AWS account
2. AWS CLI installed and configured
3. Necessary permissions to create the specified AWS resources

## Deployment Steps

1. Clone this repository:
    ```
        git clone [repository-url]


2. Navigate to the project directory:

3. Deploy the CloudFormation stack:

Replace `[your-stack-name]` with a name for your stack and ensure `template.yaml` is the correct filename if you've named it differently.

4. Monitor the stack creation process:

## Stack Configuration

- VPC: A new VPC is created to host the resources.
- EC2 Instances: 
- Windows Operating System
- Minimum: 1 instance
- Desired: 2 instances
- Maximum: 3 instances
- Security Group: Allows RDP access (port 3389)
- S3 Bucket: Created for storage purposes

## Accessing EC2 Instances

To access the EC2 instances via RDP:

1. Obtain the public IP of an EC2 instance from the AWS Console
2. Use an RDP client to connect to the instance
3. Use the username and password specified in the template (or retrieve the password if using a key pair)

## Customization

You can modify the template to adjust:

- Instance types
- VPC CIDR block
- Subnet configurations
- Auto Scaling group parameters
- S3 bucket properties

## Cleanup

To avoid ongoing charges, delete the stack when no longer needed:

## Support

For issues or questions, please open an issue in this repository.