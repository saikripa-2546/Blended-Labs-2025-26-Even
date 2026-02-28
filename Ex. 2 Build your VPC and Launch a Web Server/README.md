# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: SAI KRIPA SK
* **Register Number**: 212224040284

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow 

1.Create a VPC using the VPC wizard with public & private subnets, Internet Gateway, NAT Gateway, and route tables.

2.Add additional subnets in a second Availability Zone and associate them with the appropriate route tables.

3.Create a Security Group allowing HTTP (port 80) access from Anywhere (IPv4).

4.Launch an EC2 instance in the public subnet, attach the security group, enable auto-assign public IP, and add user data to install Apache.

5.Verify the deployment by accessing the instance’s Public DNS in a browser and confirming the web page loads successfully.

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1918" height="1032" alt="image" src="https://github.com/user-attachments/assets/70ac05f8-d1c7-406d-86f1-f1b09a796df6" />

### Screenshot 2: EC2 Instance Running

<img width="1918" height="986" alt="image" src="https://github.com/user-attachments/assets/3b3ab4a1-8bc3-42bf-bbe6-9523280105ff" />
<img width="1912" height="1031" alt="image" src="https://github.com/user-attachments/assets/ec201aab-5a23-4043-8ea2-c16f9cbcb50e" />


### Screenshot 3: Web Server Output in Browser
<img width="1907" height="1007" alt="image" src="https://github.com/user-attachments/assets/4f22626d-e9fc-4266-80a9-9f01340d67f9" />


## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
