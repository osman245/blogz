---
title: "Alb Review"
date: 2024-06-14T16:24:28-04:00
draft: false

categories: []
tags: []
toc: false
author: ""
---
### Elastic Load Balancing and ASG 

We use elastic load balancing to control and direct traffic to targets. To ensure targets are healthy.We use it as a security mechanism. We can limit the traffic to only come from a certain source in ELB.NLB has a fixed static IP while ALB doesnt. 

Here are some practice questions related to AWS Elastic Load Balancing (ELB) and Auto Scaling Groups (ASG) to help prepare for the AWS Certified Developer Associate exam:

1. You have an application deployed across multiple Availability Zones (AZs) using an Auto Scaling group behind an Application Load Balancer. If one of the AZs becomes unavailable, what will happen?[1][3]

A) The instances in the remaining AZs will continue to receive traffic from the load balancer
B) The load balancer will stop routing traffic until the instances are rebalanced across AZs  
C) The Auto Scaling group will automatically launch new instances in the available AZs
D) The application will experience downtime until you manually launch new instances

2. You need to configure an Elastic Load Balancing health check for your web servers. Which of the following is a valid configuration?[2][3]

A) HTTP health check on port 22 (SSH port)
B) HTTPS health check on port 443 using the website's SSL certificate
C) TCP health check on port 80 
D) HTTP health check on /login using HTTP basic authentication

3. You have an Auto Scaling group configured with a scale-out policy based on CPU utilization. However, you notice that instances are being launched and terminated too frequently. How can you stabilize the scaling process?[2][4]

A) Increase the CPU utilization threshold for scaling out
B) Configure a scale-in policy based on CPU utilization 
C) Use step scaling policies instead of simple scaling policies
D) Increase the Auto Scaling group cooldown period

4. You are running a batch processing job on EC2 instances launched by an Auto Scaling group. The job completes in 2 hours. How can you schedule the Auto Scaling group to scale out before the job starts and scale in after completion?[2][3]

A) Use scheduled scaling actions
B) Use a target tracking scaling policy
C) Use step scaling policies based on a metric
D) Use simple scaling policies based on instance metrics

The correct answers with explanations:

1. A) The instances in the remaining AZs will continue to receive traffic from the load balancer[1][3]
2. B) HTTPS health check on port 443 using the website's SSL certificate[2][3]
3. D) Increase the Auto Scaling group cooldown period[2][4]
4. A) Use scheduled scaling actions[2][3]

For ELBs, traffic is automatically distributed across AZs, so remaining instances continue serving traffic if one AZ becomes unavailable.

For health checks, you can configure HTTP/HTTPS checks using the application's listening ports and paths.

To stabilize scaling, increase the cooldown period to allow metrics to stabilize before scaling again.

For predictable scaling needs like batch jobs, use scheduled scaling actions to scale out/in at specific times.

Citations:
[1] https://digitalcloud.training/aws-developer-associate-free-practice-exam-questions/
[2] https://www.udemy.com/course/aws-certified-developer-associate-practice-tests-dva-c01/
[3] https://www.whizlabs.com/blog/aws-developer-associate-exam-questions/
[4] https://www.whizlabs.com/blog/aws-solutions-architect-associate-exam-questions/
[5] https://www.knowledgehut.com/practice-tests/aws-certified-developer-associate



