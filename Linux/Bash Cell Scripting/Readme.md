# 💾 Lab: Bash Cell Scripting

## Overview
This lab showcases the creation of a directory using bash cell scripting, allowing an automated organisation of files and folders in Linux. By writing a script, directories can be created consistently and efficiently. This is a a particularly useful way to manage multiple projects or tasks. Bash Cell Scripting provides the flexibility to add conditions or multiple directories at ones

## Steps taken to achieve this:

### **Task 1: Use SSH to connect to an Amazon Linux EC 2 Instance**
Download PuTTY and configure SSH using the provided .ppk or .pem and public IP, depending on operating system.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/c77e3d503e95df36fae5d80367c05361145d5299/Linux/Bash%20Cell%20Scripting/Images/Bash%20Cell%20Scripting%201.png)

### **Task 2: Challenge
Write a bash script creating 25 empty files. the script should be designed such that everytime it ran it creates the next batch of 25 files with increasing numbers, but starting with the ones that already exist.

Do the following:
1. In open terminal: Login &rarr; open nano (nano create_files.sh).
2. In nano: write the code as displayed in image below &rarr; Save in nano (CTRL + O) &rarr; Write filename (create_files.sh) &rarr; exit nano (CTRL+X)

   ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/58e89a741381d5479842ac5bcd6f9836c58118a8/Linux/Bash%20Cell%20Scripting/Images/Bash%20Cell%20Scripting%202.png)
   
4. In terminal: Execute chmod+x create_files.sh &rarr; Run Script ,/create_files.sh for 25 files &rarr; run again for 50 files




