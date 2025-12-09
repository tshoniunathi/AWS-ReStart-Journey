# 💾 Lab: Introduction to Amazon DynamoDB

## Overview
DynamoDB is a fast and flexible NoSQL database service for applications that need conisistent single digit millisecond latency at any scale. It is a fully managed DB that supports document and key-value data models. It also has a flexible data model and reliable perfomance, making it a great fit for mobile, web, gaming, and Internet of Things (IoT) plus many other applications. In this lab, a table was created, data entered and queried, and the table was deleted. Thus, meeting the objectives of this lab. 

## Steps taken to achieve these:
### **Task 1: Create a new table**
- In the mangement console: I went to services menu &rarr; Databases &rarr; DynamoDB &rarr; and chose create table.
- For table details: i entered the name &rarr; partition key &rarr; sort key &rarr; and created  the table
!NOTICE: when entering key values I had to be mindful of chosen data types: eg string for words, number for numerics

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DyanmoDB%20task%201.png)
 
### **Task 2: Add data**
- I choose the table I just created &rarr; wnet to Actions &rarr; and clicked on create item.
- For: artist value &rarr; Artist name
       song value &rarr; song title
- For more attributes &rarr; I added new attribute &rarr; chose data type &rarr; entered data for chosen attributes &rarr; and created item
- To add more data &rarr; I repeated the steps above in task 2.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/Dynamo%20DB%20Task%202.1.png)
  
### **Task 3: Modify an existing data item**
- This is neccesary if theres an error in existing item
- In the DynamoDB dashboard: I chose explore items &rarr; chose music button &rarr; chose item with error &rarr; and ammended erred attribute &rarr; saved changes and item updated.
  
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%203.png)

### **Task 4: Query the table**
- There are 2 ways to query a table in DynamoDB: Query and scan
- To query: I provided partion and sort key &rarr; and ran. Only tems associated with entered keys showed up in the results.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%204%20QUERY.png)
  
- To scan: I expanded filters &rarr; provided attribute name, type and value &rarr; and ran. Only items associate with the provided attributes showed up in the results.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%204%20SCAN.png)

### **Task 5: Delete the table**
- In DynamoDb dashboard: under tables &rarr; I went to Update settings &rarr; chose table &rarr; then Actions &rarr; and chose delete table.
- On confirmation a panel popped up, I follwed prompt &rarr; and deleted the table

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/b01e12f774f928fdbab0220093a053b7bb3d05d4/Labs/Databases/Intro%20to%20DynamoDB/Images/Intro%20to%20DyanmoDB%2008.png)
 
## Overall learning experience
**Challenges**
- Attribute types- struggle with knowing which data type to use, when and why.
- Table layout- the lack of structure like rows or traditional tables and having items with different atribuutes on the same table
- Understanding Keys- what to use as partitition key and when to add sort key
  
**Wins**
- Hands on experience with another AWS service and getting familiar with the AWS console.
- Gaining confidence in navigating the DynamoDB dashboard,item editor, table metrics and queries.
- Undestanding NoSQL database concepts and familiarity with thhe attributes in creating a DynamoDB table, adding data and deleting table.

## Conclusion
Learning how to create tables, insert data, modify items, query results, and finally delete tables in Amazon DynamoDB provides a solid foundation in working with NoSQL databases. Each step helps you understand how DynamoDB handles data differently from traditional relational systems—focusing on speed, flexibility, and scalability. Although challenges like choosing the right partition key, understanding query limitations, or navigating the console can arise, the process builds strong practical skills. Overall, working with DynamoDB as a beginner boosts your confidence in cloud-native database services and prepares you for more advanced AWS development tasks.
