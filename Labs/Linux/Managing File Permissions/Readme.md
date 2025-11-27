# 💾 Lab: Managing File Permissions

## Overview

Managing file permissions on Linux is important for controlling who can read, write and execute files or directories. proper permission management ensures system security, prevents unauthorised access and allows multiple users to work safely on the same system. Understanding how to set and modify persmissions using commands is a key skill.

## Objectives
- Change all folder and file permissions to match appropriate group structure
- Modify file permissions for a user
- Update the company folder structure

## Steps taken to achive the objectives:

### **Task 1: Use SSH to connect to an Amazon Linux EC2 Instance**
Download PuTTY and configure SSH using the provided .ppk or .pem and public IP, depending on operating system. Login and validate as a user

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/67a00a331f9ab8bb3bbf8b45d5ded84e8c35b70d/Linux/Managing%20File%20Permissions/Images/Linux%20Managing%20File%20Permissions%2000.png)

### **Task 2:Change file & folder ownership**
!NOTE: 'pwd' validates location or folder & 'ls' validates changes or additions made.

Validate folder using 'pwd' &rarr; if not in folder enter 'cd foldername' &rarr; enter.
The 'chown' command to changeS the owner and/or group of a file or directory
Use 'sudo' and 'chown'commands to change ownership of the folder. To validate changes use 'ls -laR' command &rarr; enter.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/67a00a331f9ab8bb3bbf8b45d5ded84e8c35b70d/Linux/Managing%20File%20Permissions/Images/Linux%20Managing%20File%20Permissions%2001.png)

### **Task 3:Change permission modes**
The 'chmod' command changes the read, write, and execute permissions of files and directories.
Use vim to create a file &rarr; enter 'sudo vi createdfilename' &rarr; save and close file &rarr; press 'Esc' on keyboard &rarr; enter ':wq' &rarr; press enter.
To use absolute mode for 'chmod' to change file permissions &rarr; enter ' sudo chmod 764 createdfilename' &rarr; press enter.
!NOTE: 764 MEANS USER HAS READ, WRITE AND EXECUTE PERMISSIONS ON CREATED FILE.
To confirm infomation &rarr; enter 'ls -l'&rarr; enter

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/67a00a331f9ab8bb3bbf8b45d5ded84e8c35b70d/Linux/Managing%20File%20Permissions/Images/Linux%20Managing%20File%20Permissions%2002.png)

### **Task 4:Assign Permissions**
Permissions define access rights for the owner, group, and others. Using 'chown' you can assign and manage permissions to ensure proper access control, system security, and safe collaboration between users.
To change onwership of 'created' folder to Unathi &rarr; enter 'sudo chown -R unathi:created created' &rarr; enter
to validate the changes &rarr; 'ls -laR' &rarr; enter

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/67a00a331f9ab8bb3bbf8b45d5ded84e8c35b70d/Linux/Managing%20File%20Permissions/Images/Linux%20Managing%20File%20Permissions%2003.png)

## Overall learning experience
**Challenges**
- struggle with connecting and using Linux terminal- difficulting connecting SSH with all the right permissions
- file systems- navigating file systems was a bit tricky and the commands were strange
- difficulty understanding permissions strings and symbols and telling folders apart
- 'chmod' symbols- not knowing when or why numbers are being used with chmod instead of letters or symbols
- Confusion with file permissions- the meanings of the symbols
- Lack of visual interface.

**Wins**
- learning how remote access works, connecting to an external server and got comfortable running basic commands
- Understanding Linux security- protecting files, roles and the principle of least privilege
- Ability to control access files- learn how to modify permissions and which commnads to use and when.
- Imroved commnand line confidence and troubleshooting skills
  
## Conclusion

Effectively managing file permissions helps maintain the integrity and security of a Linux system. It demonstrates a strong understanding of Linux security principles and the ability to control access to critical resources, a fundamental skill valued in system administration and development environments.
