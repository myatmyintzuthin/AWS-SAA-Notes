Verticle Scaling - increase the size of server (active-passive)
Horizontal Scaling - create more instances (active-active)

EC2 Auto Scaling service can take care of that task by automatically creating and removing EC2 instances based on metrics from Amazon CloudWatch.

ELB first check the health of EC2 instance before routing traffic.

Three main components of EC2 Auto Scaling are as follows:

-   **Launch template or configuration:** What resource should be automatically scaled?
-   **EC2 Auto Scaling Group:** Where should the resources be deployed?
-   **Scaling policies:** When should the resources be added or removed?

## Launch Templates

Parameters to create EC2 instance:
- Amazon Machine Image (AMI) id
- instance type
- security group
- EBS volumes 
All these information are stored in a launch template.

## EC2 Auto Scaling Groups

EC2 Auto Scaling takes care of creating the EC2 instances across the subnets, so select at least two subnets that are across different Availability Zones.

Need to configure three capacity settings for group size
- minimum
- maximum
- desired capacity

Three scaling policies
- simple - scale when it is triggered. When cloudwatch triggered, just add or remove instances as specified capacity. If new alaram comes while setting up an instance, it cannot response.

- step - Step scaling policies respond to additional alarms even while a scaling activity or health check replacement is in progress.

- target tracing scaling - All you need to provide is the target value to track and it automatically creates the required CloudWatch alarms. ( two more instances when CPU utilization is at 85% and four more instances when it’s at 95%.)