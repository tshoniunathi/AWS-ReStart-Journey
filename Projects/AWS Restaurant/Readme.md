# 📂 Project 1: Building and host a static website for a restaurant + Present AWS Migration benefits.

## Overview
Create a static website for a restaurant experiencing operational challenges.  The restaurant is having a high volume of customer bookings, and current system cannot keep up, orders are being mixed up and/or misplaced.
The owner wants to use a static website to streamline customer interactions and improve booking/order management. Additionally, prepaRe a presentation on the benefits of migrating to AWS. 

!NOTE: This was a group project and the collaborators have been tagged at the bottom of the page.

## Objectives
- Build a static website
- Host the website on an Amazon S3
- Presentation on the benefits of AWS Migration

## Steps taken

### **Build Static Website**

- Build a website &rarr; make it user friendly with clean and minimal design
- Make sure it meets the requirements and needs of the client.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3317d56f1e17f950fc7dff84878a475c2943495d/Projects/AWS%20Restaurant/S3%20Bucket/Website%20mockup.png)

### **Host Website on S3**

**prepare the website files** 
- Create a local folder  for files &rarr; html, css and assets

**Create bucket**
- In console: search S3 &rarr; create bucket &rarr; choose a unique name

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/c0677b8f00ddea369ba24873c0d1a3641c81d616/Projects/AWS%20Restaurant/S3%20Bucket/Screenshot%202025-11-10%20143519%20step%201.png)

**Turn on static website hosting**
-In console: open bucket &rarr; go to properties &rarr; static website hosting &rarr;enable &rarr; choose **Host a static website** &rarr; set index document &rarr; save.

  ![image alt]()

**Allow public read**
- S3 has public access blocked by deafault, so its best to use a bucket policy that allowspublic access
- Disable Block Public Access for the bucket (Permissions → Block public access → Edit → uncheck relevant settings and confirm)
  
  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/63e4746cefb2316d211eac2af87c9f53deeebe65/Projects/AWS%20Restaurant/S3%20Bucket/Screenshot%202025-11-10%20143803%201.2.png)

**Upload files and test website**
- Console: Open the bucket → Upload → Add files/folders → Upload.
- Once hosting enabled and files uploaded, open the bucket website endpoint &rarr; find the exact endpoint URL in the bucket Properties → Static website hosting. If index loads, hosting is successful.

 ![image alt]() 

**Presentation**
- There was also, a presentation on benefits of migrating to aws and restaurant overview. This presentation shows the ways in which  Migrating to AWS services offers organizations a modern, scalable, and cost-efficient  environment for running applications and data workloads. The process typically involves assessing existing systems, choosing the right AWS tools, and then moving resources into cloud services. Overall, migration enables businesses to modernize their infrastructure, reduce operational overhead, and take advantage of AWS’s global reliability and innovation. 

For a full walkthrough and visual breakdown, see presentation: 

 [![PDF Preview](./images/slide1.png)](./presentation.pdf)


## Conclusion

Completing a project that involves hosting a static website on Amazon S3 provides valuable, hands-on experience with real cloud infrastructure. Through this process, a solid understanding of how AWS storage services operate was gained, including bucket creation, object management, and website configuration. Tere was also a lesson on how to control access using bucket policies and public access settings, and how these security principles apply to real-world deployments. This project reinforces practical cloud skills. It also demonstrates how scalable, low-cost, serverless solutions like S3 can replace traditional web servers. Overall, this project builds foundational knowledge in cloud architecture, strengthens AWS proficiency.

  

## 🤝 Collaborators

- Olivia Mahuluhulu: https://github.com/Aluwani-tec/AWS-re-start-journey
- Amogelang Menwe : https://github.com/amogelangmenwe-ops
- Nqobile Masango: https://github.com/nqobile-masango
- Madimetja Galane: 









