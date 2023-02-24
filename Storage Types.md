
- File Storage
- Block Storage
- Object Storage

## Amazon EC2 instance Storage

Temporary block storage for an instance and physically attached to the instance. If EC2 instance goes down, this will also goes down. 

## Amazon Elastic Block Storage (Amazon EBS)

External storage device to EC2 instance. If instance fails, data still remains in EBS.  
One EBS to one EC2 instance.
You can detach an EBS volume from one EC2 instance and attach it to another EC2 instance in the same Availability Zone, to access the data on it.

EBS use cases:
-   **Operating systems:** Boot/root volumes to store an operating system. The root device for an instance launched from an Amazon Machine Image (AMI) is typically an Amazon EBS volume. These are commonly referred to as EBS-backed AMIs.
-   **Databases:** A storage layer for databases running on Amazon EC2 that rely on transactional reads and writes.
-   **Enterprise applications:** Amazon EBS provides reliable block storage to run business-critical applications.
-   **Throughput-intensive applications:** Applications that perform long, continuous reads and writes.

SSD and HDD Types
Amazon EBS snapshots - backup of Amazon instance storage in Amazon EBS. only modified data will be updated to EBS. You can create multiple new volumes from snapshots.

## Amazon S3

object storage and distributed storage. Standalone storage which isn't tied to compute. 

S3 buckets - unlimited object storage.
99.99999999999% durability and 99.99% availability 
Everything in S3 is private by default. 
There are two main access management features - IAM policies and S3 bucket policies.

### IAM policies

You should use IAM policies for private buckets in the following two scenarios:

-   You have many buckets with different permission requirements. Instead of defining many different S3 bucket policies, you can use IAM policies.
-   You want all policies to be in a centralized location. Using IAM policies allows you to manage all policy information in one location.

### S3 bucket policies

The difference in IAM policies is they are attaced to users, groups and roles whereas S3 bucket policies are only attached to S3 buckets. 
Bucket policies can only be placed on buckets not on folders or objects. 

You should use S3 bucket policies in the following scenarios:

-   You need a simple way to do cross-account access to S3, without using IAM roles.
-   Your IAM policies bump up against the defined size limit. S3 bucket policies have a larger size limit.

### Amazon S3 encryption

For data at rest :
- server-side encryption - encrypt data and save in AWS data centers
- client-side encryption - encrypt data client side and upload it to Amazon S3

For data at transit:
Client-side encryption or Secure Socket Layer (SSL)

### Amazon S3 versioning

If you enable versioning for a bucket, Amazon S3 automatically generates a unique version ID for the object. In one bucket, for example, you can have two objects with the same key, but different version IDs, such as employeephoto.gif (version 111111) and employeephoto.gif (version 121212).

### Amazon S3 Storage Classes
- Amazon S3 Standard
- Amazon S3 Intelligent Tiering
- Amazon S3 Standard-Infrequent Access (S3 Standard IA)
- Amazon S3 One Zone Infrequent Access (S3 One Zone-IA)
- Amazon S3 Glacier
- Amazon S3 Glacier Deep Archive

### Life cycle management

- Tansition
- Expiration
![[Screenshot from 2023-02-24 10-41-36.png]]

## Amazon EFS and Amazon FSx

- File storage
- can be mounted onto multiple EC2 instances
- pay for what you use
