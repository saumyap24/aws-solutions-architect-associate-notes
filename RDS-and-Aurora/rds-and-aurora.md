- [RDS](#rds)
- [RDS Proxy](#rds-proxy)
- [Aurora](#aurora)
- [Introduction to Aurora](#introduction-to-aurora)
- [Scaling with Aurora](#scaling-with-aurora)
- [Aurora Availability](#aurora-availability)
- [Fault Tolerance and Durability](#fault-tolerance-and-durability)
- [Aurora Replicas](#aurora-replicas)
- [Aurora Serverless](#aurora-serverless)


---
## RDS
---

---
## RDS Proxy
---

- Fully managed database proxy for RDS
- Allows apps to pool and share DB connections established with the database
- <ins><i>Improving database efficiency by reducing the stress on database resources (e.g CPU, RAM)and minimize open connections (and timeouts)</ins></i>
- Serverless, autoscaling, highly available (multi-AZ)
- Reduced RDS and Aurora failover time by up 66%
- Supports RDS (MySQL,PostgreSQL, MariaDB, MS SQL Server) and Aurora (MySQL, PostgreSQL)
- No code changes required for most apps
- <i>Enforce <ins>IAM authentication </ins> for DB, and securely store credentials in <ins>AWS Secrets Manager</ins></i>
- RDS proxy is <ins>never publicly accessible</ins>

<img src="../images/Aurora/rds-proxy.jpg" width="47%"/>

---
## Aurora
---

- Fully managed Postgres or MySQL compatible database designed by default to scale and fine-tuned to be really fast

---
## Introduction to Aurora
---
- Combines the speed and availability of high-end databases with the simplicity and cost-effectiveness of open source databases
- Aurora can run either MySQL or Postgres compatible engines 
- Aurora  MYSQL is <ins> 5x better performance </ins> than traditional MySQL
- Aurora Postgres is <ins>3x better performance </ins> than traditional Postgres
- 1/10th costs of other solutions offering similar performance and availability

---
## Scaling with Aurora
---
- Start with 10GB of storage, and scale in 10GB increments up to 64TB
- Storage is autoscaling
- Computing resources can scale all the way up to 32 vCPUs and 244GB of memory

---
## Aurora Availability
---
- A minimum of <ins> 3 availability zones </ins> each contain <ins> 2 copies of your data at all times</ins>.
- That means there are <b><i><ins> 6 copies </b></i></ins> 
- If in case you lose up to <ins> 2 copies of your data </ins> without affecting write availability
- If in case you lose up to <ins> 3 copies of your data </ins> without affecting read availability

    <img src="../images/Aurora/aurora-availability.jpg" width="47%"/>

---
## Fault Tolerance and Durability
---
- Aurora Backup and Failover is handled <ins> automatically</ins>
- <ins> Snapshots of data </ins> can be <b> shared </b> with other AWS accounts

     <img src="../images/Aurora/aurora-fault-tolerance.jpg" width="47%"/>

- Storage is <ins> self-healing </ins>, in that data blocks and disks are continuously scanned for errors and repaired automatically

---
## Aurora Replicas
---

|          | Amazon Aurora Replicas | Mysql Read Replicas |
| -------- | ---------------------- | ------------------- |
| Number of Replicas | Up to 15 | Up to 5 |
| Replication Type | Asynchronous(ms) | Asynchronous (s) |
|Performance impact on primary | Low | High |
| Act as failover target | Yes (no data loss) | Yes (potentially minutes of data loss) |
|  Automated failover | Yes |No|
| Support for user-defined replication delay | No | Yes | 
| Support for different data or schema vs primary | No | Yes |

---
## Aurora Serverless
---
- Aurora except the database will automatically start up, shut down, and scale capacity up or down based on your application's needs 
- Apps used a few minutes several times per day or week, eg. low-volume blog site
- pay for database storage and the database capacity and I/O your database consumes while it is active