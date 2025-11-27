# 💾 Lab: Introduction to Amazon DynamoDB

## Overview
DynamoDB is a fast and flexible NoSQL database service for applications that need conisistent single digit millisecond latency at any scale. It is a fully managed DB that supports document and key-value data models. It also has a flexible data model and reliable perfomance, making it a great fit for mobile, web, gaming, and Internet of Things (IoT) plus many other applications. In this lab, a table was created, data entered and queried, and the table was deleted. Thus, meeting the objectives of this lab. 

## Steps taken to achieve these:
### **Task 1: Create a new table**
- In mangement console: go to services menu &rarr; Databases &rarr; DynamoDB &rarr; choose create table.
- For table details: enter name &rarr; partition key &rarr; sort key &rarr; create table
- Give table a minute or so to create. Once created go to task 2.
!NOTICE: when entering key values be mindful of chosen data types: eg string for words, number for numerics

 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DyanmoDB%20task%201.png)
 
### **Task 2: Add data**
- Choose table &rarr; Actions &rarr; create item.
- For: artist value &rarr; Artist name
       song value &rarr; song title
- for more attribute &rarr; add new attribute &rarr; choose data type &rarr; enter data for chosen attributes &rarr; create item
- To add more data &rarr; repeat the steps above in task 2.

 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/Dynamo%20DB%20Task%202.1.png)
  
### **Task 3: Modify an existing data item**
- This is neccesary if theres an error in existing item
- In DynamoDB dashboard: choose explore items &rarr; choose music button &rarr; choose item with error &rarr; ammend erred attribute &rarr; save changes. Item should be updated.
  
 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%203.png)

### **Task 4: Query the table**
- There are 2 ways to query a table in DynamoDB: Query and scan
- To query: provide partion and sort key &rarr; run. Only tems associated with entered keys will show up in the results.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%204%20QUERY.png)
  
- To scan: expand filters &rarr; provide attribute name, type and value &rarr; run. Only items associate with the provided attributes will show up in the results.

 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/DynamoDB%20Task%204%20SCAN.png)

### **Task 5: Delete the table**
- In DynamoDb dashboard: under tables &rarr; Update settings &rarr; choose table &rarr; Actions &rarr; delete table.
- On confirmation panel will pop up, follw prompt &rarr; delete table

 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/8ccbe0ca18d63359dc96719aaf5240fc86a01703/Labs/Databases/Intro%20to%20DynamoDB/Images/Intro%20to%20DyanmoDB%2008.png)
 
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
