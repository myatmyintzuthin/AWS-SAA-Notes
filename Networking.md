## Amazon Virtual Private Cloud

Amazon VPC is an isolated network that you create in the AWS cloud. When creating a VPC, you must choose three main factors.
- name of VPC
- Region where the VPC will live. Each VPC spans multiple AZ within the selected region.
- IP range for the VPC in CODR notation. 10.0.0.0/16

After VPC creation is done, create subnets for public and private.

When you create a subnet, you must specify the following:

-   VPC you want your subnet to live in. In this case: VPC (10.0.0.0/16)
-   Availability Zone you want your subnet to live in. In this case: AZ1
-   CIDR block for your subnet, which must be a subset of the VPC CIDR block. In this case: 10.0.0.0/24

![[Screenshot from 2023-02-23 16-59-48.png]]

AWS reserved 5 IP addresses in each subnet for routing, DNS, network management, future use and network broadcast address.

**Internet gateway** - to enable internet connectivity for VPC. 
**virtual private gateway** - connect AWS VPC to another private network. On the other side, you need to connect with customer gateway. Once the connection is done, establish an encrypted VPN connection between the two sides.

### Main route table

AWS creates a main route table when you create a VPC which contains a set of rules to determine where network traffic is directed.

For explicit routing to separate subnet, use custom route table. 

![[Screenshot from 2023-02-24 08-09-26.png]]

## Amazon VPC Security

Network access control list - network ACL
A firewall at the subnet level. Network ACL enables you to control what kind of traffic is allowed to enter or leave your subnet. 
Everything is allowed in and out. You need to define inbound and outbound rules for allow or denied.

Security Groups 
A security layer of EC2 instances. The default configuration blocks all inbound traffic and allow all outbound traffic.


