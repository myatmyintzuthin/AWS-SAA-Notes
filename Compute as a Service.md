
Compute Options 
- virtual machines (VMs)
- container services
- serverless

## Amazon EC2

VM - Amazon Elastic Compute Cloud, EC2
To create an EC2 instance, define:
- Hardware specifications, like CPU, memory, network and storage
- Logical configurations, like networking location, firewall rules, authentication, and the operation system.

Choose Amazon Machine Image (AMI) - operating system along with installation drivers.
AMI is copied to the root device volume, which contains the image used to boot the volume.
AMI are reuseable. 

## Find AMIs

You can select an AMI from the following categories:

-   Quick Start AMIs, which are created by AWS to help you get started quickly
-   AWS Marketplace AMIs, which provide popular open source and commercial software from third-party vendors
-   My AMIs, which are created from your EC2 instances
-   Community AMIs, which are provided by the AWS user community
-   Build your own custom image with EC2 Image Builder

## EC2 instance family
- General purpose
- Compute optimized
- Memory optimized
- Accelerated computing
- Storage optimized

By default, EC2 instances are placed in a network called default Amazon Virtual Private Cloud (Amazon PVC) which is a public and accessible by the internet.