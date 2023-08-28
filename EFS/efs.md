- [Elastic File System (EFS) ](#elastic-file-system-efs)
- [Introduction to ELastic File System (EFS)](#introduction-to-elastic-file-system-efs)

---
## Elastic File System (EFS)
---
- <i><ins>Scalable, elastic, <b> Cloud-Native NFS File System</b></ins></i>
- Attach a single file system to multiple EC2 Instances
- Don't worry about running out or managing disk space

---
## Introduction to Elastic File System (EFS)
---
- EFS is a file storage service for EC2 instances
- Storage capacity grows (upto petabytes) and shrinks automatically based on data stored (elastic) 
- <ins> Multiple EC2 instances </ins> in same VPC can mount a single EFS Volume (Volume must be in same VPC)
- EC2 instances install the NFSv4.1 client and can then mount the EFS volume
- EFS is using Network File System version 4 (NFSv4) protocol
- EFS creates multiple <b><ins> mount targets </ins></b> in all your VPC subnets 
0 You based per space used starting at $0.30 GB / month