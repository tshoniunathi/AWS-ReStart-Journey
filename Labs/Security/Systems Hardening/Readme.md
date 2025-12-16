# 💾Lab: Systems Hardening with Patch Manager via AWS Systems Manager

## Overview
In this lab, I worked with AWS Systems Manager Patch Manager to manage and apply operating system patches across multiple EC2 instances. In large organizations, keeping operating systems and applications up to date is critical but challenging. This lab focused on applying a structured patching strategy using default and custom patch baselines, patch groups, and compliance reporting.

I patched Linux instances using a default patch baseline, created a custom patch baseline for Windows security updates, applied patches using patch groups, and verified patch compliance across all instances.

## Steps taken to achieve these objectives
**Task 1: Patch Linux Instances Using Default Baseline**
- I accessed the AWS Systems Manager console from the AWS Management Console
- I navigated to Fleet Manager and reviewed the available Linux and Windows instances
- I verified that the Linux instances were managed by Systems Manager
- I opened Patch Manager and selected Patch now
- I configured the patching operation to Scan and install
- I enabled Reboot if needed
- I targeted instances using tags with:
  - Tag key: Patch Group
  - Tag value: LinuxProd
- I used the AWS-AmazonLinux2DefaultPatchBaseline
- I initiated the patching process and monitored the execution
- I confirmed that all three Linux instances were successfully patched

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dc5d63d11d51a629e27c42851359c38a0e3f44bf/Labs/Security/Systems%20Hardening/systems%20hardening%20patch%20manager%2003.png)
  
**Task 2: Create a Custom Patch Baseline for Windows**
- I returned to Patch Manager and opened the Patch baselines tab
- I created a new patch baseline with the following settings:
  - Name: WindowsServerSecurityUpdates
  - Operating system: Windows
  - Description: Windows security baseline patch
- I configured approval rules for Windows Server 2019 security updates
- I added a rule for:
  - Severity: Critical
  - Classification: SecurityUpdates
  - Auto-approval after 3 days
- I added a second rule for:
  - Severity: Important
  - Classification: SecurityUpdates
  - Auto-approval after 3 days
- I created the patch baseline successfully
- I associated the patch baseline with the patch group WindowsProd

  ![imag alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dc5d63d11d51a629e27c42851359c38a0e3f44bf/Labs/Security/Systems%20Hardening/systems%20hardening%20patch%20manager%2004.png)
  
**Task 3: Patch Windows Instances Using Custom Baseline**
  **Task 3.1: Tag Windows Instances**
  - I opened the EC2 console and selected each Windows instance
  - I added the following tag to all three Windows instances:
    - Key: Patch Group
    - Value: WindowsProd
  **Task 3.2: Patch Windows Instances**
  - I returned to Systems Manager → Patch Manager
  - I selected Patch now
  - I configured the patching operation to Scan and install
  - I enabled Reboot if needed
  - I targeted instances using the WindowsProd patch group
  - I initiated the patching process
  - I reviewed the Execution ID and monitored patch execution through Run Command
  - I confirmed that the correct patch group and baseline were applied

  ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dc5d63d11d51a629e27c42851359c38a0e3f44bf/Labs/Security/Systems%20Hardening/systems%20hardening%20patch%20manager%2006.png)
  
**Task 4: Verify Patch Compliance**
- I navigated to the Patch Manager Dashboard
- I confirmed that the Compliance summary showed all six instances as compliant
- I reviewed the Compliance reporting tab
- I verified compliance details for each Linux and Windows instance
- I checked patch details such as:
  - Critical noncompliant count
  - Security noncompliant count
  - Last operation date
  - Baseline ID
- I opened a Windows instance record to review applied patches and installation times

   ![image alt](https://github.com/tshoniunathi/AWS-ReStart-Journey/blob/dc5d63d11d51a629e27c42851359c38a0e3f44bf/Labs/Security/Systems%20Hardening/systems%20hardening%20patch%20manager%2007.png)
  
## Overall Learning Experience
**Challenges**
- Understanding the relationship between patch baselines and patch groups
- Ensuring correct tagging of instances for accurate targeting
- Navigating multiple Systems Manager components (Patch Manager, Run Command, State Manager)

**Wins**
- Successfully patched Linux instances using the default baseline
- Created and applied a custom Windows security patch baseline
- Used patch groups to target Windows instances accurately
- Verified full compliance across all EC2 instances

## Conclusion
I successfully used AWS Systems Manager Patch Manager to apply operating system patches across both Linux and Windows EC2 instances. I patched Linux instances using a default baseline, created and applied a custom Windows security baseline, and verified compliance for all systems. This lab strengthened my understanding of centralized patch management, automation, and compliance monitoring in AWS environments.






