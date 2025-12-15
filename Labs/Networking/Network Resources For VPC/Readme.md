# 💾Lab: Creating Networking Resources in an Amazon Virtual Private Cloud (VPC)

## Overview
This Lab focused on creating networking resources within an Amazon Virtual Private Cloud (VPC) to resolve a customer’s connectivity issue. Acting as a Cloud Support Engineer at AWS, I designed and implemented a routable VPC architecture that allowed an EC2 instance to access the internet. The primary goal was to enable successful outbound connectivity and confirm it by pinging an external destination from within the VPC.

## Architecture
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/Architecture.png)

## Steps taken to achieve these objectives
**Task 1: Investigate the customer's needs**
I reviewed the customer’s request and analyzed their proposed architecture to identify missing or misconfigured networking components. Using the AWS Management Console, I created a complete VPC networking setup following a structured, top-down approach.

**I performed the following steps:**

- Created a VPC with the CIDR range 192.168.0.0/18.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%201.png)
  
- Created a public subnet with the CIDR range 192.168.1.0/26.

  ![image alth](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%202.png)
  
- Created and attached an Internet Gateway (IGW) to the VPC.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%206.png)
  
- Created a public route table, added a 0.0.0.0/0 route targeting the IGW, and associated it with the public subnet.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%203.png)

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%207.png)
  
- Created a Network Access Control List (NACL) allowing all inbound and outbound traffic and associated it with the public subnet.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%209.png)
  
- Created a security group allowing SSH, HTTP, and HTTPS inbound traffic and all outbound traffic.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%2010.png)

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%2011.png)
  
- Launched an Amazon Linux EC2 instance in the public subnet with a public IP address.
  
  ![images alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/45fa0ec4742446030257ff21bf7d41b08e41155d/Labs/Networking/Network%20Resources%20For%20VPC/Images/NETWORK%20RESOURCES%20%20FOR%20VPC%2013.png)
  
- Connected to the EC2 instance using SSH.

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dc5d63d11d51a629e27c42851359c38a0e3f44bf/Labs/Networking/IP-%20Troubleshooting%20commands/Images/Connect%20SSH.png)
  
- Verified internet connectivity by successfully running ping google.com from the instance.
- This confirmed that the VPC was correctly configured and fully routable to the internet.

## Overall Learning Experience

**Challenges**
- Ensuring all required networking components were created and properly linked
- Correctly associating the route table and subnet
- Understanding the difference between security groups and NACL behavior

**Wins**
- Successfully built a fully functional, internet-facing VPC
- Confirmed correct routing through the Internet Gateway
- Verified connectivity with a successful external ping
- Applied a clear, structured approach to VPC troubleshooting

## Conclusions
By completing this lab, I successfully resolved the customer’s networking issue by designing and implementing a properly routed VPC. I demonstrated the ability to configure core AWS networking resources, validate security controls, and confirm internet connectivity from an EC2 instance. This lab strengthened my practical understanding of AWS VPC architecture and improved my confidence in supporting real-world customer networking scenarios.

