# Process Explorer & Access Based Enumeration

## Lab Overview

This lab focuses on practical applications of Windows command-line tools, Process Explorer for security tokens analysis, and the configuration of Access Based Enumeration (ABE) on Windows Server.

## Tools Used
- Windows CLI
- Process Explorer
- Active Directory and Users Computers
- Share and Storage Management for ABE

## Environments
- Windows 7
- Windows 10
- Windows Server 2008 R2

## Lab Steps with Screenshots

### Step 1: Network Commands and Output Filtering
Description: Using the `ping` and `find` commands to limit and filter network request outputs.
<img src="https://i.imgur.com/tkGGBcc.png" height="400px" width="auto" alt="Command-Line Output Filtering"/>

### Step 2: Process Explorer Security Tokens
Description: Analyzing security tokens of processes using Process Explorer.
<img src="https://i.imgur.com/0CEjwMq.png" height="400px" width="auto" alt="Process Explorer Security Tokens"/>

### Step 3: Active Directory Configuration
Description: Creating new user accounts in the INFO6003 OU and configuring permissions.
<img src="https://i.imgur.com/0MJQHUQ.png" height="400px" width="auto" alt="Active Directory Configuration"/>

### Step 4: Setting Permissions with icacls
Description: Using `icacls` to set and verify folder permissions.
<img src="https://i.imgur.com/bk8wic7.png" height="400px" width="auto" alt="Setting Permissions with icacls"/>

### Step 5 & 6: Implementing ABE
Description: Demonstrating the effect of ABE on the visibility of shared folders for different users.

<img src="https://i.imgur.com/6Cv69fA.png" height="400px" width="auto" alt="ABE for Normal User"/>
<img src="https://i.imgur.com/vl40mel.png" height="400px" width="auto" alt="ABE for Backup User"/>

### Step 7: Server Manager on Windows Server 2016
Description: Exploring the Server Manager in preparation for promoting a server to a Domain Controller.

<img src="https://i.imgur.com/s3mmYpz.png" height="400px" width="auto" alt="Server Manager on Windows Server 2016"/>

## Lab Questions and Answers

### Backup User vs. Normal User Access Differences
The Backup User's output differs from the Normal User's output because the Backup User has membership in the "Backup Operators" group. This group membership grants them the ability to bypass standard security restrictions, allowing access to more files and directories due to elevated privileges.

### Considerations Before Promoting to a Primary Domain Controller
Before promoting a server to a Primary Domain Controller, it is crucial to understand the consequences of new functional levels and features on the existing infrastructure. As outlined in the Microsoft documentation, assessing compatibility with organizational needs ensures a deliberate and well-planned upgrade process. This careful approach prevents disruption of services and introduction of potential security vulnerabilities.

<!-- Replace 'URL_to_screenshot_X' with the actual URLs where your screenshots are hosted. -->
