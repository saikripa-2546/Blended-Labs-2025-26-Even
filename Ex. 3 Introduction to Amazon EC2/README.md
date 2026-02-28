# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: SAI KRIPA SK
* **Register Number**: 212224040284
---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow 
1.Launch an EC2 instance (Amazon Linux 2023, t2.micro) with termination protection enabled and configure user data to install a web server.

2.Monitor the instance using Status Checks, CloudWatch Monitoring tab, system logs, and instance screenshot.

3.Update the Security Group to allow HTTP (port 80) inbound traffic and verify web server access via Public IP.

4.Resize the instance by stopping it, changing instance type (t2.micro → t2.small), enabling stop protection, and increasing EBS volume (8 GiB → 10 GiB).

5.Test stop protection & explore limits by checking EC2 service quotas, attempting to stop the instance, disabling stop protection, and stopping the instance successfully.


## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1918" height="1027" alt="image" src="https://github.com/user-attachments/assets/1da12b6d-c710-41ee-80aa-977b33ae9b55" />


### Screenshot 2: SSH Connection to Instance

<img width="1907" height="995" alt="image" src="https://github.com/user-attachments/assets/b5a51296-39be-4eda-a84f-aac4aa9579f2" />
<img width="1916" height="1033" alt="image" src="https://github.com/user-attachments/assets/f37afd2a-3458-4728-add9-a9e511205234" />


### Screenshot 3: Instance Monitoring / Status

<img width="1621" height="911" alt="image" src="https://github.com/user-attachments/assets/3c9d86eb-b8e0-42fd-8023-28e7bf2a9b71" />
<img width="1916" height="1090" alt="image" src="https://github.com/user-attachments/assets/c4b11fdd-2489-4369-9905-c037476a652b" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
