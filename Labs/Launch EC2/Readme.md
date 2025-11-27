#  💾 Lab: Launching an EC2 Instance

## Overview
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This lab shows an overview of launching, resizing, managing, and monitoring an Amazon EC2 instance.

Amazon EC2 makes it easy to set up and manage the computing power  needed with very little friction. It gives full control over resources, all running on Amazon’s reliable infrastructure. It cuts the time it takes to launch new server instances down to just a few minutes, which makes scaling up or down simple as your requirements change.

Amazon EC2 shifts the way computing costs are handled by letting customers pay only for the capacity they actually use. It also gives developers the tools they need to build applications that can handle failures and stay isolated from common issues, making systems more resilient overall.

## Architecture Diagrams
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/a18ad36cd5c1532a6bf7faede79f39d3721b4dc7/Cloud%20Foundations/Launch%20EC2/Launch%20EC2%202%20image.png)

##Steps taken to Achieve this:
 ### **TASK 1: Launching an instance**
In this task, an EC2 instance was launched, with termination protection to avoid accidentally terminating the EC2 instance.
In management console &rarr; services &rarr; EC2 &rarr; name instance &rarr; choose an AMI &rarr; choose instance type &rarr; configure key pair &rarr; configure network settings &rarr; add storage &rarr; configure advanced details &rarr; launch
 
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/4a3dac6396edbe3451e9b4c4e02ba6aec9afa6dd/Cloud%20Foundations/Launch%20EC2/LAUNCH%20EC2%205.png)

### **TASK 2: Mornitor the instance**
Monitoring is important in the maintainance of the reliability, availability and performance of an EC2 instance.
select instance (check box next to instance) &rarr; navigate to status check tab (bootom of the page) &rarr; !NOTE: systems and instance reachability should pass &rarr; monitoring tab &rarr; Actions menu &rarr; monitor and troubleshoot &rarr; Get screenshot

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/632bcb19885ff8ce83eedfa213738a28f4c57030/Cloud%20Foundations/Launch%20EC2/LAUNCH%20EC2%206.png)

### **TASK3: Update security group and access webserver**
In this task, content was accessed from webserver.
1. Select instance (check box) &rarr; select detals tab &rarr;copy public IP address to clipboard &rarr; in new tab, paste IP and enter.
!NOTE: cannot access server because security group is not allowing inbound traffic on port 80
2. In management console &rarr; Network & security (left pane) &rarr; security groups &rarr; webserver security group (check box) &rarr; select inbound rules &rarr; add rule &rarr; configure type and source &rarr; save rules

   <img width="1910" height="715" alt="image" src="https://github.com/user-attachments/assets/01537b1d-ba5e-486a-9381-dfcc0e58e0a7" />

### **TASK 4: Resize instance** 
changing an instance in case its too small (over-utilised) or too large (under-utilised).

**Stop instance**
On management console &rarr; select instances (left pane) &rarr; selec webserver (checkbox) &rarr; select instant state &rarr; stop instance.

**Change instant type**
In Actions menu &rarr; selectect instance settings &rarr; instance type &rarr; configure to new instance size &rarr; change instance type.

**Resize EBS Volume
Under Elastic Block Store (left pane) &rarr; volumes &rarr; check box &rarr; go to Actions &rarr; modify volume. 

**Start resized instance**
Go back to instance &rarr; select webserver (check box) &rarr; instance state &rarr; start instance.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dcdd3d43c209d35c9d7dc94b8f23d27c75ec3ddd/Cloud%20Foundations/Launch%20EC2/CHANGE%20INSTANCE%20TYPE.png)

### TASK 5: Test termination protection
When an instance is no longer needed, it can be deleted AKA terminated. once terminated, cannot be restarted or connected.

In instances &rarr; select webserver (check box) &rarr; actions menu &rarr; instance settings &rarr; change termination protection &rarr; uncheck enable &rarr; save

Select webserver (check box) &rarr;instance state &rarr; terminate (delete) instance. 

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8b405596b6effb96731ad0e4a9cec098b8a98f6e/Cloud%20Foundations/Launch%20EC2/Launch%20EC2%2011.png)

## Overall learnign experience
**Challenges**
- Confusion with security groups- struggling with the understanding and difference between inbound and outbound rules, identifying ports and why port 22 is needed.
- instance failure- instance refusing to connect or connection being "timed out".

**Wins**
- practical application of cloud computing- understanding instance types and what instances are.
- Successful launch of the first server- choosing an instance type, choosing an AMI, configuring networking and launching a running instance.

## Conclusion
By the end of this lab, solid knowledge and hands on understanding of how to work with EC2 instances was gained. with key benefits being launching an instance, monitor its health, update security groups for appropriate traffic, working with termination protection management and resizing both an instance type and its storage. overall, the lab demonstrates the power and flexibility of an EC2 instance- providing full control over computr resources while keeping it easy to scale, secure and manage instances effectively.


