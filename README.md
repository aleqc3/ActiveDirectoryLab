<h1>Active Directory Home Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7e)

<h2>Description</h2>
In this Lab, I will guide you through the process of creating an Active Directory home lab environment using Oracle VirtualBox. This step-by-step tutorial is designed to enhance your understanding of Active Directory and Windows networking by providing hands-on experience in configuring and running a virtual lab. To maximize your learning, we recommend working through the lab multiple times and attempting the setup independently before referring to the video. If you have any questions or need further assistance, please do not hesitate to ask. Your engagement and proactive approach will greatly contribute to your mastery of these critical concepts.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Links used</h2>

-<b>Windows Isnatllation Media <b> (https://www.microsoft.com/en-us/software-download/windows10)

-<b>Oracle Virtual Box <b> (https://www.virtualbox.org/wiki/Downloads)

-<b>Server 2019 ISO <b> (https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

-<b>Create Account Scripts <b> (https://github.com/aleqc3/ActiveDirectoryLab/blob/main/AD_PS-master%20(1).zip)

<h2>Environments Used </h2>
- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Lab Plan: <br/>
<img src="https://imgur.com/BM4kXVV.png" height="80%" width="80%" alt="Lab plan"/>
<br /> Here are the steps we’re going to take for the project:

-Download and Install Oracle VirtualBox: This will be our platform for running virtual machines.

-Obtain Windows 10 and Server 2019 ISOs: We’ll use these to install the operating systems on two separate VMs.

-Create the Domain Controller VM: Set up this VM with Server 2019, configure it with two network adapters—one for internet access and one for a private network connecting to the clients.

-Install and Configure Server 2019: Install the OS, assign IP addresses (with the internal network set manually and the external network handled by your home router), name the server, and set up Active Directory.

-Configure Routing and DHCP: Ensure that clients on the private network can access the internet through the domain controller and configure DHCP to automatically assign IP addresses to new VMs.

-Run a PowerShell Script: Execute a script to create a thousand users in Active Directory and review the script to understand its functionality.

-Create and Configure the Client VM: Install Windows 10 on a new VM, name it Client1, join it to the domain, and log in using one of the domain accounts.

By following these steps, we will set up a basic Windows networking environment with Active Directory.

<p align="center">
Lab Plan: <br/>
<img src="https://imgur.com/BM4kXVV.png" height="80%" width="80%" alt="Lab plan"/>
<br /> 

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
