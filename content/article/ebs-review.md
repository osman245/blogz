---
title: "EBS Review"
date: 2024-06-13T19:36:04-04:00
draft: false

categories: []
tags: []
toc: false
author: ""
---
Amazon Elastic Block Store

Amazon Elastic Block Store is a high-performance block storage. We attach this into our EC2 instances, in order to provide it with persistent storage that is available and reliable. We can use it for a plethora of different applications. EBS can be attached prior or after runtime on a EC2 instance. by default we terminate on deletion of EC2 instance. EBS volumes can scale from gigabytes to terabytes, you can increase capacity at anytime to match application requirements. EBS volumes replicated within availability zone to protect against hardware failure, high availability and durability. Snapshots for backups of EBS volumes to Amazon S3, to ensure data durability and disaster recovery. EBS supports encryption at rest and in transit.
#### Best Practices
- **Snapshot Management**: Regularly create snapshots of your EBS volumes to ensure data backup and enable quick recovery.
- **Performance Tuning**: Choose the appropriate EBS volume type based on your application's performance requirements. For high IOPS needs, use Provisioned IOPS SSD volumes.
- **Monitoring and Optimization**: Utilize CloudWatch metrics to monitor EBS performance and set alarms for key metrics such as latency, throughput, and IOPS.
- **Security**: Enable encryption for EBS volumes containing sensitive data to ensure compliance with security policies and regulations.

AMIs are built for a specific AWS Region, they're unique for each AWS Region. You can't launch an EC2 instance using an AMI in another AWS Region, but you can copy the AMI to the target AWS Region and then use it to create your EC2 instances.

Practice questions for EBS

Here are some practice questions related to Amazon Elastic Block Store (EBS) to help prepare for the AWS Certified Developer Associate exam:
You are running a database workload on an EC2 instance with an EBS volume attached. The database frequently writes large amounts of data. Which EBS volume type should you choose to optimize performance for this use case?
A) General Purpose SSD (gp2)
B) Provisioned IOPS SSD (io1)
C) Throughput Optimized HDD (st1)
D) Cold HDD (sc1)
You need to take a point-in-time snapshot of your EBS volume for backup purposes. How can you ensure that the data is consistent when the snapshot is created?
A) Stop the EC2 instance before taking the snapshot
B) Create the snapshot directly from the EBS volume
C) Use EBS multi-volume snapshots
D) Use Amazon Data Lifecycle Manager to create snapshots
You have an application that requires high IOPS performance. How can you increase the IOPS provisioned for your EBS volume?
A) Modify the volume type from gp2 to io1
B) Take a snapshot of the volume and restore it as an io1 volume
C) Enable EBS volume modification to change the IOPS
D) Increase the size of the EBS volume
You need to encrypt an existing unencrypted EBS volume. What is the recommended approach?
A) Enable encryption on the existing volume
B) Create a snapshot of the unencrypted volume and copy it as an encrypted volume
C) Detach the volume, enable encryption, and re-attach it
D) It is not possible to encrypt an existing unencrypted EBS volume
The correct answers with explanations:
B) Provisioned IOPS SSD (io1)
A) Stop the EC2 instance before taking the snapshot
B) Take a snapshot of the volume and restore it as an io1 volume
B) Create a snapshot of the unencrypted volume and copy it as an encrypted volume
For database workloads with large writes, use Provisioned IOPS SSD volumes to get consistent high performance.
To ensure data consistency when creating EBS snapshots, stop the EC2 instance first to flush all data from memory to disk.
You cannot modify the IOPS of an existing volume. To increase IOPS, take a snapshot and restore it as an io1 volume with the desired IOPS.
You cannot enable encryption on an existing unencrypted volume. Create a snapshot and copy it as a new encrypted volume.



