---
title: "Ec2 Review"
date: 2024-06-13T16:14:07-04:00
draft: true

categories: []
tags: []
toc: false
author: ""
---


EC2 Instances
EC2 is a web service in AWS that lets you run a virtual server in the cloud. EC2 allows you to increase and decrease capacity using the auto-scaling feature. Their are many instance types to select that fit different use cases. Such as if you want to run a database. Then use storage optimized. If you want to run a high performance based video-game on an instance, let that instance be compute-optimized. Their are also different pricing models depending on what your looking for. When it comes to storage, we can attach the storage option of EBS, since the data in the ec2 instance is ephermal. We can attach the filesystem option of EFS. We can assign roles to the EC2 instance giving permissons to use Amazon S3, dynamodb and much more. We implement networking for a granular experience. We have security groups that we use in order to control wha traffic is allowed into or out of our instances. we have different ports to distinguish out different traffic. For instance, if we allow port 22 access, we allow clients to ssh into our ec2 Instance. When it comes to running EC2 in the cloud, we are equipped with many networking features. Security wise we have IAM roles, security groups and network access control lists. Scalability wise, we autoscaling and Load balancers. For monitoring an EC2 instance we have aws cloudwatch.
Networking: Provides various networking features such as Virtual Private Clouds (VPCs), Elastic IP addresses, and Load Balancing.
Security: Includes features like IAM (Identity and Access Management) roles, security groups, and network access control lists.
Scalability: Auto Scaling and Elastic Load Balancing allow your applications to scale up or down based on demand.
Monitoring: AWS CloudWatch provides monitoring for EC2 instances, enabling you to see resource utilization and operational health

Best Practices
Security: Regularly update your security groups and use IAM roles to control access.
Backup and Recovery: Use Amazon EBS snapshots and regular backups.
Cost Management: Monitor usage and utilize cost-saving options like Reserved Instances or Savings Plans.
High Availability: Distribute instances across multiple Availability Zones.
Monitoring: Use CloudWatch for real-time monitoring and set up alerts for unusual activities.

Practice Questions 
Here are some practice EC2 questions to help prepare for the AWS Certified Developer Associate exam:
1. You are deploying a web application on EC2 instances behind an Application Load Balancer (ALB). How can you ensure that only healthy EC2 instances receive traffic from the ALB?[1]
A) Configure the EC2 instances to use an Amazon CloudWatch metric to report their health
B) Enable EC2 Auto Recovery for the instances
C) Configure the ALB health checks
D) Use an AWS Lambda function to check instance health and deregister unhealthy instances
2. You need to launch an EC2 instance and store sensitive data on its instance store volumes. What steps should you take to encrypt the data at rest?[2][3]
A) Enable EBS encryption on the instance's root volume
B) Use AWS KMS to create a customer master key (CMK) and encrypt the instance store volumes
C) Use the AWS CloudHSM service to generate encryption keys for the instance store volumes
D) Instance store volumes cannot be encrypted, use EBS volumes instead
3. You are running a batch processing job on an EC2 instance that generates logs. You need to persist the logs after the instance terminates. What is the best solution?[2]
A) Store the logs on the instance store volumes
B) Use AWS CloudWatch Logs and create a log group 
C) Store the logs in an Amazon S3 bucket
D) Use AWS CloudTrail to capture the logs
4. You need to launch EC2 instances in a private subnet with outbound internet access for software updates. How can you accomplish this?[2][3]
A) Create a NAT Gateway in the public subnet and configure a route table for the private subnet
B) Assign public IP addresses to the instances in the private subnet
C) Create an Internet Gateway and configure a route table for the private subnet
D) Create a VPN connection between the private subnet and your corporate network
The correct answers with explanations:
1. C) Configure the ALB health checks[1]
2. D) Instance store volumes cannot be encrypted, use EBS volumes instead[2][3]
3. C) Store the logs in an Amazon S3 bucket[2] 
4. A) Create a NAT Gateway in the public subnet and configure a route table for the private subnet[2][3]
For ALBs, you configure health checks to test the responsiveness of the registered targets like EC2 instances. Only healthy instances receive traffic.
Instance store volumes are ephemeral and data is lost after termination, so they cannot be encrypted. Use EBS volumes for persistent encrypted storage.
For persisting EC2 instance logs, store them in a durable service like S3 rather than on the local instance.
To allow outbound internet access for EC2 instances in a private subnet, create a NAT Gateway in a public subnet and configure a route table for the private subnet to route traffic through the NAT Gateway.
Citations:
[1] https://www.udemy.com/course/aws-certified-developer-associate-practice-tests-dva-c01/
[2] https://www.whizlabs.com/blog/aws-developer-associate-exam-questions/
[3] https://tutorialsdojo.com/aws-certified-developer-associate-dva-c02-sample-exam-questions/
[4] https://digitalcloud.training/aws-developer-associate-free-practice-exam-questions/
[5] https://www.knowledgehut.com/practice-tests/aws-certified-developer-associate

