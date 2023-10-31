# AWS Certified Solutions Architect Associate Practice Exams

![](https://img-c.udemycdn.com/course/480x270/1520628_21fa_4.jpg)

### Metadata

- Title: AWS Certified Solutions Architect Associate Practice Exams
- URL: https://www.udemy.com/course/aws-certified-solutions-architect-associate-amazon-practice-exams-saa-c03/learn/quiz/4394972/result/1100741372
### Highlights & Notes

- In Auto Scaling, the following statements are correct regarding the cooldown period:  It ensures that the Auto Scaling group does not launch or terminate additional EC2 instances before the previous scaling activity takes effect.  Its default value is 300 seconds.  It is a configurable setting for your Auto Scaling group.
- You can use Amazon Data Lifecycle Manager (Amazon DLM) to automate the creation, retention, and deletion of snapshots taken to back up your Amazon EBS volumes. Automating snapshot management helps you to:  - Protect valuable data by enforcing a regular backup schedule.  - Retain backups as required by auditors or internal compliance.  - Reduce storage costs by deleting outdated backups.
- AWS Global Accelerator and Amazon CloudFront are separate services that use the AWS global network and its edge locations around the world. CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery). Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover. Both services integrate with AWS Shield for DDoS protection.
- A Gateway endpoint is a type of VPC endpoint that provides reliable connectivity to Amazon S3 and DynamoDB without requiring an internet gateway or a NAT device for your VPC. Instances in your VPC do not require public IP addresses to communicate with resources in the service.
- AWS DataSync makes it simple and fast to move large amounts of data online between on-premises storage and Amazon S3, Amazon Elastic File System (Amazon EFS), or Amazon FSx for Windows File Server. Manual tasks related to data transfers can slow down migrations and burden IT operations. DataSync eliminates or automatically handles many of these tasks, including scripting copy jobs, scheduling, and monitoring transfers, validating data, and optimizing network utilization. The DataSync software agent connects to your Network File System (NFS), Server Message Block (SMB) storage, and your self-managed object storage, so you don’t have to modify your applications.  DataSync can transfer hundreds of terabytes and millions of files at speeds up to 10 times faster than open-source tools, over the Internet or AWS Direct Connect links. You can use DataSync to migrate active data sets or archives to AWS, transfer data to the cloud for timely analysis and processing, or replicate data to AWS for business continuity. Getting started with DataSync is easy: deploy the DataSync agent, connect it to your file system, select your AWS storage resources, and start moving data between them. You pay only for the data you move.
- Here is a list of important information about EBS Volumes:

    - When you create an EBS volume in an Availability Zone, it is automatically replicated within that zone to prevent data loss due to a failure of any single hardware component.

    - An EBS volume can only be attached to one EC2 instance at a time.

    - After you create a volume, you can attach it to any EC2 instance in the same Availability Zone

    - An EBS volume is off-instance storage that can persist independently from the life of an instance. You can specify not to terminate the EBS volume when you terminate the EC2 instance during instance creation.

    - EBS volumes support live configuration changes while in production which means that you can modify the volume type, volume size, and IOPS capacity without service interruptions.

    - Amazon EBS encryption uses 256-bit Advanced Encryption Standard algorithms (AES-256)

    - EBS Volumes offer 99.999% SLA.


