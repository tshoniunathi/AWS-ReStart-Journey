# 💾Lab: Build DB server and interact with DB using an app

## Overview
This lab was desined to reinforce the concept of leveraging an aws managed database instance for solving relational database needs. The objectives of this lab was to launch an RDS DB instance, configure it to permit connections from web server and open a web application to interact with the database. 

## Steps taken to achieve these objectives
### **Task 1: Created a security group for the RDS instance**
- In console: I went to services menu &rarr; Network & content delivery &rarr; and chose VPC
- In left pane: I clicked on security group &rarr; created security group &rarr; then configured a security group name, description and chose VPC of choice.
- In inbound rules: I added a new rule &rarr; and configured type and source &rarr; and then created a security group

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%201.png)

### **Task 2: Created a DB subnet group**
- In console: I went to service menu &rarr; chose databases &rarr; RDS &rarr; then subnet groups (left pane) &rarr; and create DB subnet group &rarr; configured name, description and VPC ID.
- In add subnets section: for availability zone &rarr;I clicked the dropdown menu &rarr; and selected the first and second AZ.
- For subnets &rarr; I clicked dropdown menu &rarr; and selected CIDR blocks for the AZs &rarr; and pressed create.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20Server%203.png)

### **Task 3: Create an Amazon RDS DB instance**
- In left navigation pane: I clicked on databases &rarr; and chose full configuration (standard create)
- In Engine options &rarr; I chose type &rarr; engine version (latest) &rarr; templates &rarr; Deve/Test &rarr; availability and durability &rarr; choose DB instance.
- In settings: I configured DB instance identifier, master username, password and cofirmed password
- Under instance configuration: i configured DB instance class &rarr; storage &rarr;configure storage type 9 compatible with instance class.
- Under connectivity: I configured VPC &rarr; and security group
- Under monitoring: I disabled enhanced monitoring
- Under additional configuration: I configured initial database name &rarr; disable automated backups &rarr; and create database &rarr; this resulted in a wationg time of ~4 minutes before it was available &rarr; I wnet connectivity and security &rarr; and copied endpoint (saved for later)

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%206.png)

### **Task 4: Interact with DB**
- in this task, I Copied the webserver IP address &rarr; opened a new web browser tab &rarr; pasted IP.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2013.png)

- At the top of the application page: I click RDS &rarr; configured the endpoint I saved from task 3, database, username and password (configured in settings) &rarr; and submited

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2012.png)

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2014.png)
- the result were the database storing information that is editable, deletable and more information could be added.

## Overall Learning experience
**Challenges**
- Connecting an application to remote database- mispelling in password that resulted in failure to login

**Wins**
- Improved understanding of app-database architechture

## Conclusion
Working with Amazon RDS to interact with an application provides a valuable, real-world introduction to cloud-based databases. Through creating the database, connecting it to an app, and running queries, you learn how modern applications handle data reliably and securely. Despite challenges, each step builds confidence and strength in understanding of how backend systems work. Overall, gaining hands-on experience with RDS prepares you for managing scalable, production-ready databases in real cloud environments.

