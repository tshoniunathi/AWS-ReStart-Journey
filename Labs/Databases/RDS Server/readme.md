# 💾 Challenge Lab: Build DB Server and Interact With DB

## Overview
This lab is designed to reinforce the concept of leveraging an AWS-managed database instance for solving relational database needs. Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while managing time-consuming database administration tasks, which allows you to focus on your applications and business. Amazon RDS provides you with six familiar database engines to choose from: Amazon Aurora, Oracle, Microsoft SQL Server, PostgreSQL, MySQL and MariaDB.

After completing this lab, will be able to:
- Create an RDS instance
- Use the Amazon RDS Query Editor to query data.

## Steps taken to overcome challenge
**Task 1: Launch an Amazon RDS DB instance**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%201.png)
 
**Task 2: Creat a security group**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%202.png)

**Task 3: Set up inbound rules**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%203.png)

**Task 4: Create a subnet**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%204.png)

**Task 5: Connect  Linux server**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%20PUTTY.png)

**Task 6: Install MySQL server of choice**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/build%20DB%205.png)

**Task 7: connect to RDS MySQL database**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%206.png)

**Task 8: create table**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/BUILD%20DB%20SCREEN%201.png)

**Task 9: Insert sample rows**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/BUILD%20DB%20SCREEN%202.png)

**Task 10: Select all rows**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/BUILD%20DB%20SCREEN%203.png)

**Task 11: create another table**

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/bUILD%20DB%20SCREEN%204.png)

**Task 12: Insert 5 rows & Perform INNER JOIN****

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/9774017d09d92f848705cb55326f43aa0e8d700b/Labs/Databases/RDS%20Server/Images/Build%20DB%20SCREEN%205.png)

## Overall learning experience
**Challenges**
- Handling SQL syntax errors- At first, MySQL returned syntax errors due to typos like VARCHANT. This caused the MySQL client to exit unexpectedly, requiring reconnection and re-running commands.
- Selecting the correct database- Before running CREATE TABLE, forgetting to run USE <database> caused errors like “table does not exist.”
- Understanding RDS settings- Some options were locked (like Multi-AZ), and knowing which to select; especially avoiding standby instances — required careful reading of the instructions.
- Working within a terminal-only environment- Typing commands manually, copying/pasting SQL and navigating without a GUI required more attention to detail.
  
**Wins**
- Connected to the RDS database from the Linux server- Using SSH and the MySQL client, I established a working connection between the Linux server and the RDS instance, confirming networking and security group settings were correct.
- Installed and used MySQL client tools- I learned how to install MySQL on Linux, navigate the terminal, and use MySQL commands to interact with the database.
- Created multiple tables successfully- I created the RESTART and CLOUD_PRACTITIONER tables with the required schema.
- Inserted data and ran SQL queries- I inserted sample rows, queried the data, and performed an INNER JOIN to combine results from both tables.
- Improved SQL troubleshooting skills- I learned how to fix syntax errors, reconnect to MySQL after accidental exits, and verify selected databases

## Conclusion
Completing the first SQL challenge offered a solid introduction to working with relational databases and using commands like CREATE TABLE, INSERT, and INNER JOIN. Along the way, you built confidence by successfully creating tables, adding data, and producing meaningful results through joins. Although challenges such as syntax errors, typos, and unexpected exits from the MySQL environment slowed progress, they also reinforced the importance of attention to detail and problem-solving skills in database work. Overall, the challenge strengthened your foundational SQL skills and prepared you for more advanced database tasks in the future.
