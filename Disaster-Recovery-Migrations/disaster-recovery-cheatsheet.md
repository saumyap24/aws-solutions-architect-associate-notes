- Backup 
    - EBS Snapshots, RDS automated backups/ Snapshots etc 
    - Regular pushes to S3/ S3 IA/ Glacier, Lifecycle Policy, Cross Region Replication 
    - From On-Premise:Snowball or Storage Gateway 
- High availability
    - Use Route 53 to migrate DNS over Region to Region 
    - RDS Multi-AZ, Elastic Cache Multi-AZ, EFS, S3 
    - Site to Site VPN as a recovery from Direct Connect
- Replication 
    - RDS Replication (Cross Region),AWS Aurora + Global Databases 
    - Database replication from on-premise to RDS 
    - Storage Gateway
- Automation 
    - CloudFormation / Elastic Beanstalk to re-create a whole new environment 
    - Recover / Reboot Ec2 instances with CloudWatch if alarms fail 
    - AWS Lambda functions for customized automatons 
- Chaos 
    - Netflix has a "simian-army" randomly terminating EC2
