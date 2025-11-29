# Classic Load Balancer Setup and Configuration on AWS
## Introduction
This project demonstrates the deployment and configuration of a Classic Load Balancer (CLB) in AWS. A Classic Load Balancer is designed to automatically distribute incoming traffic across multiple EC2 instances, ensuring improved availability, fault tolerance, and scalability of applications. The Classic Load Balancer operates at both the transport layer (Layer 4) and the application layer (Layer 7), giving it the ability to balance traffic based on both network connections and application requests. It continuously performs health checks to route traffic only to healthy instances, further enhancing fault tolerance.

## Prerequisites
Before setting up the Classic Load Balancer, ensure the following requirements are met:
- AWS Account – with access to EC2 and Load Balancer services
- Running EC2 Instances – at least two instances in the same VPC and region
- Security Groups configured to allow:
    - Inbound HTTP (port 80) and/or HTTPS (port 443) traffic
    - Inbound SSH (port 22) access for administration (optional)
- Web Server Installed (e.g., Apache or Nginx) on each EC2 instance, serving a sample page

## Steps to Setup Classic Load Balancer
### Step 1: Launch 3 EC2 Instances with User Data Script
1. Launch 3 Instance.
![alt](images/1.png)

2. Write user script while launching instance.
![alt](images/3.png)

3. Rename the 3 instance with different names(server-1, server-2, server-3)
![alt](images/4.png)

### Step 2: Create a Classic Load Balancer
1. Go to Load Balancer.
![alt](images/5.png)

2. Choose Classic Load Balancer.
![alt](images/6.png)

3. Name the Load Balancer 
![alt](images/7.png)

4. Select all Availability Zones.
![alt](images/8.png)

5. Manage Security Group
![alt](images/9.png)

6. Add instances to Load Balancer
![alt](images/10.png)

    ![alt](images/11.png)

    ![alt](images/12.png)

7. Copy DNS command and paste it in any browser.
![alt](images/13.png)

### Step 3: Testing the Deployment.
1. Output for Server-1
![alt](images/14.png)

2. Output for Server-2
![alt](images/15.png)

3. Output for Server-3
![alt](images/16.png)

## Summary
This project demonstrates the deployment and configuration of a Classic Load Balancer (CLB) in AWS to distribute incoming traffic across multiple EC2 instances. By launching three instances with a user-data script, the setup ensures that each instance runs a web server and serves unique content, allowing you to verify traffic distribution.