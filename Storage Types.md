
- File Storage
- Block Storage
- Object Storage

## Amazon EC2 instance Storage

Temporary block storage for an instance and physically attached to the instance. If EC2 instance goes down, this will also goes down. 

## Amazon Elastic Block Storage (Amazon EBS)

External storage device to EC2 instance. If instance fails, data still remains in EBS.  You can detach an EBS volume from one EC2 instance and attach it to another EC2 instance in the same Availability Zone, to access the data on it.

EBS use cases:
-   **Operating systems:** Boot/root volumes to store an operating system. The root device for an instance launched from an Amazon Machine Image (AMI) is typically an Amazon EBS volume. These are commonly referred to as EBS-backed AMIs.
-   **Databases:** A storage layer for databases running on Amazon EC2 that rely on transactional reads and writes.
-   **Enterprise applications:** Amazon EBS provides reliable block storage to run business-critical applications.
-   **Throughput-intensive applications:** Applications that perform long, continuous reads and writes.

SSD and HDD Types