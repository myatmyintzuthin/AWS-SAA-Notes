
# Amazon RDS

Amazon RDS supports popular relational database management systems: 
-   **Commercial:** Oracle, SQL Server
-   **Open Source:** MySQL, PostgreSQL, MariaDB
-   **Cloud Native:** Amazon Aurora

RDS is built of compute and storage. Compute portion is called DB instance. Underneath the DB instance is an EC2 instance. 

Use Network ACLs and security groups for dictate flow of traffic. IAM policies to restrict access of action and resources.

Automatic backups  - between 0 to 35 days.
Manual snapshots - automated backups longer than 35days

Amazon RDS Multi-AZ will create a redundant copy of database in another AZ. 
A primary copy in one AZ and standby copy in second AZ.
In an automatic failover, the standby database is promoted to the primary role, and queries are redirected to the new primary database.

## Purpose-Built Databases

Amazon DynamoDB 
Amazon Document DB with MongoDB compatibility
Amazon Neptune graph database
Amazon QLDB ledger database - immutable database 

# Amazon DynamoDB

Serverless NoSQL database with fast and seamless scalability. 
All the data is stored on SSD and is automatically replicated across multiple AZ in an AWS Region.

#### Core components


Standalone tables 