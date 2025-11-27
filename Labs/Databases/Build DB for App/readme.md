# 💾Lab: Build DB server and interact with DB using an app

## Overview
This lab was desined to reinforce the concept of leveraging an aws managed database instance for solving relational database needs. The objectives of this lab was to launch an RDS DB instance, configure it to permit connections from web server and open a web application to interact with the database. 

## Steps taken to achieve these objectives
### **Task 1: Create a security group for the RDS instance**
- In console: go to services menu &rarr; Network & content delivery &rarr; choose VPC
- In left pane: click security group &rarr; create security group &rarr; then configure security group name, description and VPC of choice.
- In inbound rules: click add rule &rarr; and configure type and source &rarr; create security group

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%201.png)

### **Task 2: Create a DB subnet group**
- In console: go to service menu &rarr; databases &rarr; RDS &rarr; subnet groups (left pane) &rarr; create DB subnet group &rarr; configure name, description and VPC ID.
- In add subnets section: for availability zone &rarr;click dropdown menu &rarr; select first and second AZ.
- For subnets &rarr;click dropdown menu &rarr; select CIDR blocks for the AZs &rarr; create.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20Server%203.png)

### **Task 3: Create an Amazon RDS DB instance**
- In left navigation pane: click databases &rarr; full configuration (standard create)
- Engine options &rarr; choose type &rarr; engine version (latest) &rarr; templates &rarr; Deve/Test &rarr; availability and durability &rarr; choose DB instance.
- In settings: configure DB instance identifier, master username, password and cofirm password
- Under instance configuration: configure DB instance class &rarr; storage &rarr;configure storage type 9 compatible with instance class.
- Under connectivity: configure VPC &rarr; configure security group
- Under monitoring: disable enhanced monitoring
- Under additional configuration: configure initial database name &rarr; disable automated backups &rarr; create database &rarr; wait ~4 minutes or until status says modifying or available &rarr; connectivity and security &rarr;copy endpoint (save for later)

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%206.png)

### **Task 4: Interact with DB**
- Copy webserver IP address &rarr; open new web browser tab &rarr; paste IP &rarr; enter

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2013.png)

- At the top of the application page: click RDS &rarr; configure endpoint from task 3, database, username and password (configured in settings) &rarr; submit

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2012.png)

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/562553133c7da7be2e606d9ba5f2a0c2c0d76003/Labs/Databases/Build%20DB%20for%20App/Images/DB%20SERVER%2014.png)
- Result will be the database storing information that is editable, deletable and more information can also be added.

## Overall Learning experience
**Challenges**
- Connecting an application to remote database- mispelling in password that resulted in failure to login

**Wins**
- Improved understanding of app-database architechture

## Conclusion
Working with Amazon RDS to interact with an application provides a valuable, real-world introduction to cloud-based databases. Through creating the database, connecting it to an app, and running queries, you learn how modern applications handle data reliably and securely. Despite challenges, each step builds confidence and strength in understanding of how backend systems work. Overall, gaining hands-on experience with RDS prepares you for managing scalable, production-ready databases in real cloud environments.

