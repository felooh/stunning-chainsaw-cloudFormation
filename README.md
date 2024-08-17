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


## Deployment Steps (AWS Management Console)

1. Sign in to the AWS Management Console.

2. Navigate to the CloudFormation service:
   - Click on "Services" at the top of the page
   - Type "CloudFormation" in the search bar
   - Select "CloudFormation" from the results

3. Create a new stack:
   - Click on "Create stack" (with new resources)
   - Under "Prerequisite - Prepare template", choose "Template is ready"
   - Under "Specify template", select "Upload a template file"
   - Click "Choose file" and select your CloudFormation template file
   - Click "Next"

4. Specify stack details:
   - Enter a Stack name (e.g., "WindowsEC2AutoScalingStack")
   - Fill in any parameters required by your template
   - Click "Next"

5. Configure stack options:
   - Add any tags if desired
   - Set up any advanced options if needed
   - Click "Next"

6. Review:
   - Review all the details of your stack
   - At the bottom of the page, check the box acknowledging that AWS CloudFormation might create IAM resources
   - Click "Create stack"

7. Monitor the stack creation:
   - On the stack details page, you can view the progress of resource creation
   - Wait until the status changes to "CREATE_COMPLETE"

8. Access your resources:
   - Once the stack is created, go to the "Outputs" tab to find important information like VPC ID, S3 bucket name, etc.
   - You can now use these resources as needed

Remember to delete the stack when you no longer need these resources to avoid unnecessary charges.


## Stack Configuration

- VPC: A new VPC is created to host the resources.
- EC2 Instances: 
- Windows Operating System
- Minimum: 1 instance
- Desired: 2 instances
- Maximum: 3 instances
- Security Group: Allows RDP access (port 3389)
- S3 Bucket: Created for storage purposes

## Screenshots
   - Overview Stack status
   ![Alt text](/screenshots/overview.png?raw=true "Optional Title")

   - Resources Status
   ![Alt text](/screenshots/resources.png?raw=true "Optional Title")

   - You may also use the cloud formation composer to visualize your stack before deployment
   ![Alt text](/screenshots/cf_composer.png?raw=true "Optional Title")



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

