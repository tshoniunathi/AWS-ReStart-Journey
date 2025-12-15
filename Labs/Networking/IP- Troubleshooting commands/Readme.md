# 💾Lab: Internet Protocol Troubleshooting Commands

## Overview
This is a hands-on lab focused on internet Protocol (IP) troubleshooting commands in an AWS environment. The objective was to practice common network troubleshooting tools to understand how the map to the OSI model, and apply them to the realistic customer support scenario. Acting as anew network administrator, I accessd an amazon Linux EC2 instance and used multiple commands across different network layers to diagnose connectivity, latency, port and application level issues.

## Steps taken to achieve these objectives**
### **Task 1: Use SSH to connect to an Amazon Linux EC2 instance
- I successfully accessed the AWS Management Console and launched the lab environment. Once the lab status was ready, I connected to an Amazon Linux EC2 instance using SSH with key-based authentication.
- After establishing secure access, I practiced a series of troubleshooting commands aligned with the OSI model.

 ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3f793e7ea6f154f87e22cb048c2ebe4da1ca32ec/Labs/Networking/IP-%20Troubleshooting%20commands/IP%20troubleshooting%20commands.png)

### **Task 2: Practice troubleshooting commands**
**Layer 3 (Network Layer)**
- 'ping' to test basic IP connectivity and confirm that ICMP traffic was allowed through security groups and network ACLs.

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3f793e7ea6f154f87e22cb048c2ebe4da1ca32ec/Labs/Networking/IP-%20Troubleshooting%20commands/IP%20troubleshooting%20commands%202.png)

- 'traceroute' to analyze the network path, identify hops, measure latency, and detect potential packet loss between the EC2 instance and an external server.
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3f793e7ea6f154f87e22cb048c2ebe4da1ca32ec/Labs/Networking/IP-%20Troubleshooting%20commands/IP%20troubleshooting%20commands%203.png)

**Layer 4 (Transport Layer)**
- 'netstat' to verify active and listening TCP connections and identify which ports and services were currently in use on the host.
- 'telnet' to test connectivity to specific ports and confirm whether connections were allowed, refused, or timing out, helping distinguish firewall or routing issues

![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3f793e7ea6f154f87e22cb048c2ebe4da1ca32ec/Labs/Networking/IP-%20Troubleshooting%20commands/IP%20troubleshooting%20commands%205.png)

**Layer 7 (Application Layer)**
- 'curl'to send HTTP requests and validate application-level responses, confirming successful connections and HTTP status codes such as '200 ok'
![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/3f793e7ea6f154f87e22cb048c2ebe4da1ca32ec/Labs/Networking/IP-%20Troubleshooting%20commands/IP%20troubleshooting%20commands%206.png)

Throughout the lab, I related each command to practical customer scenarios, such as diagnosing latency, verifying open ports, and confirming that web services were functioning correctly.
  
## Overall Learning experience
**Challenges**
- Interpreting packet loss and failed hops in 'traceroute'
- Remembering command flags and options

**Wins**
- Confirmed network connectivity using multiple troubleshooting layers
- Gained confidence in diagnosing issues using a structured OSI-based approach
- Improved understanding of real-world customer network scenarios

## Conclusion

By completing this lab, I achieved a practical understanding of core IP troubleshooting commands and how they align with the OSI model. I successfully applied these tools to simulate real customer issues, ranging from basic connectivity problems to application-level failures. Overall, the lab strengthened my network troubleshooting skills, improved my confidence in supporting AWS-based workloads, and provided a structured approach to identifying and resolving networking issues efficiently.
