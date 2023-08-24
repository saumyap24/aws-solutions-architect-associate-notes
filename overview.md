- [Amazon EBS](#amazon-ebs)
- [Cloudwatch](#cloudwatch)
- [AWS Identity and Access Management](#aws-identity-and-access-management)
- [RDS](#rds)
- [Athena](#athena)
- [Kinesis](#kinesis)
- [Storage Gateway](#storage-gateway)
- [Elastic Load Balancer](#elastic-load-balancer)
- [Security Group](#security-group)
- [Route 53](#route-53)
- [AWS Transit Gateway](#aws-transit-gateway)
- [Amazon EMR](#amazon-emr)
- [Auto Scaling](#auto-scaling)

## Amazon EBS
---

- <b> Amazon EBS </b> provides three volume types to best meet the needs of your workloads: 
    - <b> General Purpose (SSD) </b>
        - General Purpose (SSD) volumes are suitable for a <u>broad range of workloads, including small to medium-sized databases, development and test environments, and boot volumes.</u>
    - <b> Provisioned IOPS (SSD) </b>
        - These volumes offer storage with consistent and low-latency performance and are designed for I/O intensive applications such as <u>large relational or NoSQL databases. </u>
    - <b>Magnetic</b>
        - for workloads where <u>data are accessed infrequently, and applications where the <i>lowest storage cost</i> is important. </u>

## Cloudwatch
---
- Monitoring tool for your AWS resources and applications.
- <u> Display metrics and create alarms </u> that watch the metrics and send notifications or automatically make changes to the resources you are monitoring when a threshold is breached.

## AWS Identity and Access Management
---
- You can use an <i><u>IAM role to specify permissions for users </u></i> whose identity is federated from your organization or a third-party identity provider (IdP).
    - <b>Federating users with SAML 2.0</b>
        - If your organization already uses an identity provider <u>software package that supports SAML 2.0 (Security Assertion Markup Language 2.0)</u>, you can create trust between your organization as an identity provider (IdP) and AWS as the service provider. 
        - You can then use SAML to provide your users with <u>federated single-sign on (SSO) </u>to the AWS Management Console or federated access to call AWS API operations. 
        - <b>For example</b>: if your company uses Microsoft Active Directory and Active Directory Federation Services, then you can federate using SAML 2.0
    - <b>Federating users by creating a custom identity <u>broker application</u></b>
        - If your <u>identity store is not compatible with SAML 2.0,</u> then you can <i>build a custom <b>identity broker application </b> to perform a similar function. </i>
        - The broker application <u>authenticates users, requests temporary credentials for users from AWS,</u> and then provides them to the user to access AWS resources.
        - The application verifies that employees are signed into the existing corporate network's identity and authentication system, which might use LDAP, Active Directory, or another system. The identity broker application then obtains temporary security credentials for the employees.
        - To <i>get temporary security credentials, </i>the identity broker application calls either `AssumeRole` or `GetFederationToken` to obtain temporary security credentials, depending on how you want to manage the policies for users and when the temporary credentials should expire.
        - The <u>call returns temporary security credentials consisting of an AWS access key ID, a secret access key, and a session token.</u> The identity broker application makes these temporary security credentials available to the internal company application. 

            <img src="./images/Overview/broker-application.jpg" width="47%" height="40%"/>
        - This scenario has the following attributes:

            - The identity broker application has permissions to access IAM's token service (STS) API to create temporary security credentials.

            - The identity broker application is able to verify that employees are authenticated within the existing authentication system.

            - Users are able to get a temporary URL that gives them access to the AWS Management Console (which is referred to as single sign-on).

## RDS
---
- Supports <b>Aurora, MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL Server.</b>
- <b>DB Instance </b>
    - For production OLTP use cases, use <b>Multi-AZ deployments </b> for <u>enhanced fault tolerance with Provisioned <i>IOPS</u> </i>storage for fast and predictable performance.
        - You can use PIOPS storage with Read Replicas for MySQL, MariaDB or PostgreSQL.
    - <b> Magnetic </b>
        - Doesn’t allow you to scale storage when using the SQL Server database engine.
            - Doesn’t support elastic volumes.
            - Limited to a maximum size of 3 TiB.
            - Limited to a maximum of 1,000 IOPS.


## Athena
---
- An interactive query service that makes it easy to analyze data directly in Amazon S3 and other data sources using SQL.
- <i>Serverless</i>
- Has a <u>built-in query editor.</u>
- highly available and durable
-  <u>integrates with <b>Amazon QuickSight </b></u> for easy data visualization.
- retains query history for 45 days.
- You pay only for the queries that you run. You are charged based on the amount of data scanned by each query.
- There are 2 types of cost controls:
    - <b> Per-query limit </b> 
        - specifies a threshold for the total amount of data scanned per query. 
        - Any query running in a workgroup is <u>canceled once it exceeds the specified limit</u>. 
        - Only one per-query limit can be created
    - <b>Per-workgroup limit</b> 
        - this limits the total amount of data scanned by all queries running within a specific time frame. 

## Kinesis
---
- A fully managed AWS service that you can use to stream <ins> live video from devices to the AWS Cloud</ins>, or build applications for <strong> real-time video processing or batch-oriented video analytics.</strong>
- Amazon Kinesis Data Streams enables real-time processing of streaming big data. It provides ordering of records, as well as the ability to read and/or replay records in the same order to multiple Amazon Kinesis Applications
- A Kinesis data stream is a set of <ins>shards that has a sequence of data records </ins>, and each data record has a <strong>sequence number </strong>that is assigned by Kinesis Data Streams. 
    - Kinesis <ins>can also easily handle the high volume of messages</ins> being sent to the service.
    - durable
    - no missing of messages

## Storage Gateway
---

- Connects an on-premise software appliance with cloud-based storage to <ins>provide seamless integration with data security features between your <b>on-premises IT environment and the AWS storage infrastructure.</b></ins>
- You can use the service to store data in the AWS cloud for scalable and cost-effective storage that helps maintain
- It stores files as native S3 objects, archives virtual tapes in Amazon Glacier and stores EBS snapshots generated by the Volume Gateway with Amazon EBS.

## Elastic Load Balancer 
---
- Distributes incoming application or network traffic across multiple targets, such as EC2 instances containers (ECS), Lambda functions and IP addresses in multiple Availability zones


## Security Group
---

- A security group acts as a virtual firewall for your instance to control inbound and outbound traffic.
     
     <img src="./images/Overview/security-group.jpg" width="87%"/>

## Route 53
---

- A highly available and scalable Domain Name System (DNS) web service used for domain registration, DNS routing and health checking


## AWS Transit Gateway
---

- A networking service that uses a hub and spoke model to connect the on-premises data centers and Amazon VPCs to a <ins><em>Single Gateway.</em></ins>
- With this service, customers only have to create and manage  <ins><em><strong>a single connection from the central gateway into each on-premises data center</ins></em></strong>
- <strong>Features</strong>:
    - <strong>Inter-region peering </strong>
        - allows customers to route traffic
        - easy and cost-effective way
    - <strong> Multicast </strong>
        - allows customers to have fine-grain control on who can consume and produce multicast traffic
    - <strong>Automated provisioning </strong>
        - customers can automatically identify the Site-to-site VPN connections and on-premises resources with which they are associated using AWS Transit Gateway

## Amazon EMR
---
- EMR (Elastic MapReduce)
- A managed cluster that <ins>simplifies running big data frameworks </ins>like Apache Hadoop and Apache Spark on AWS to process and analyze vast amounts of data.
- You can process data for analytics purposes and business intelligence workloads using EMR together with Apache Hive and Apache Pig
- You can <ins><em>use EMR to move large amounts of data in and out of other AWS data stores </em></ins> and databases like S3 and DynamoDB
    <img src="./images/Overview/emr.jpg" width="87%"/>

## Auto Scaling 
---
- Configure automatic scaling for the AWS resources quickly through a scaling plan that uses <strong> Dynamic Scaling </strong>and <strong>Predictive scaling </strong>.
- <strong><em>Useful for </em></strong>:
    - Cyclical traffic such as high use of resources during regular business hours and low use of resources
    - On and Off traffic such as batch processing, testing and periodic analysis 
    - Variable traffic patterns, such as software for marketing growth with periods of spiky growth