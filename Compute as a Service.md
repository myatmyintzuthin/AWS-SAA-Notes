
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

When architecting any application for high availability, consider using at least two EC2 instances in two separate availability zones.

## EC2 instance lifecycle

![[Screenshot from 2023-02-23 14-30-22.png]]

## Pricing

### On-Demand Instances
Pay as you go. Billing starts whenever the instance is running and stops when the instance is in a stopped or terminated state. The price per second on running instance is fixed.

### Reserved Instances 

Provide a discounted hourly rate. Need to commit to 1 year or 3 year.
- All Upfront - offers a higher discount than Partial upfront instances
- Partial Upfront - offer a higher discount than No Upfront
- No Upfront - offers a higher discount than On-Demand

### Spot Instances

Spot instances available at up to 90% discount compared to On-Demand prices. You can set a limit on how much you would like to pay for the instance hour. If the amount you pay is mor e than current spot price, you will receive an instance. 
Spot instances can be interrupted. If AWS determines that capacity is no longer available for a particular spot instance or if the spot price exceeds how much you are willing to pay, AWS will give 2 min warning before it interrupts your instance.

## **Containers**

A container is a standardized unit that packages your code and its dependencies. This package is designed to run reliably on any platform because the container creates its own independent environment. 
Container share the same operating system and kernal as the host they exist on. whereas virtual machines contain their own operating system. 

### Orchestrate containers
In AWS, containers run on EC2 instances. People run many containers on many instances across AZs. To manage many containers, AWS provide container orchestration services.
Containers can run in Amazon EC2 mode or AWS Fargate mode.

### Amazon Elastic Container Service (Amazon ECS)

Amazon ECS is an end-to-end container orchestration service that helps you spin up new containers and manage them across a cluster of EC2 instances. 

First Install Amazon ECS container agent on EC2 instances. This agent is open source and responsible for communicating to the Amazon ECS servie about cluster management details.
Both Windows and Linux AMI support. 
An instance with the container agent installed is often called a container instance.

![[Screenshot from 2023-02-23 15-45-13.png]]

### Amazon Elastic Kubernets Service (Amazon EKS)

Kubernets is a portable, extensible open source platform for managing containerized workloads and services. If you have containers running on Kubernetes, use Amazon EKS.

Amazon EKS is conceptually similar to Amazon ECS but with some differences.

-   An EC2 instance with the ECS agent installed and configured is called a container instance. In Amazon EKS, it is called a worker node.
-   An ECS container is called a task. In Amazon EKS, it is called a pod.
-   While Amazon ECS runs on AWS native technology, Amazon EKS runs on top of Kubernetes.

## Serverless

Underline implementation and infrastructure are taken care from AWS. 
AWS Fargate - serverless compute platform which can run with Amazon ECS or Amazon EKS.
AWS Lambda 
![[Screenshot from 2023-02-23 15-57-41 1.png]]

## AWS Lambda

