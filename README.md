<h1>Active Directory Home Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7e)

<h2>Description</h2>
In this Lab, I will guide you through the process of creating an Active Directory home lab environment using Oracle VirtualBox. This step-by-step tutorial is designed to enhance your understanding of Active Directory and Windows networking by providing hands-on experience in configuring and running a virtual lab. To maximize your learning, we recommend working through the lab multiple times and attempting the setup independently before referring to the video. If you have any questions or need further assistance, please do not hesitate to ask. Your engagement and proactive approach will greatly contribute to your mastery of these critical concepts.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Links used</h2>

-<b>Oracle Virtual Box <b> (https://www.virtualbox.org/wiki/Downloads)
 
-<b>Windows Isnatllation Media <b> (https://www.microsoft.com/en-us/software-download/windows10)

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
Download and Install Oracle VirtualBox: <br/>
<img src="https://imgur.com/uM2qtIy.png" height="80%" width="80%" alt="Download and Install Oracle VirtualBox"/>
<br /> For the project, start by downloading VirtualBox. Use the link in the description to access the download page, select the appropriate version for your operating system (Windows or Mac), and install it. Once VirtualBox is installed, download and install the Extension Pack from the same page—it should be easy to find. After completing these installations, proceed to the next step as outlined in the description.

<p align="center">
Download windows 10 ISO: <br/>
<img src="https://imgur.com//Hcd3HKy.png" height="80%" width="80%" alt="Download Windows 10 ISO"/>
<br /> The next step is to download the Windows 10 ISO. You can do this through the Installation Media Tool by selecting the option to create installation media and choosing the ISO file format. Follow these steps: Go to the download page, select Windows 10, and you might need to fill out a few details such as choosing your language (e.g., English) and confirming. Make sure to select the 64-bit version. Save the ISO file to an easily accessible location, like your desktop, to avoid losing track of it.

 <p align="center">
Download the Server 2019 ISO: <br/>
<img src="https://imgur.com//AS4AHhj.png" height="80%" width="80%" alt="Download the Server 2019 ISO"/>
<br /> The following step is to download the Server 2019 ISO. Go to the download page and select Server 2019. You may need to provide some information and choose the appropriate version for your needs. Save the ISO file to a convenient location, such as your desktop, to keep it easily accessible. Once you have both ISOs downloaded, you can proceed to create the virtual machines in VirtualBox.

<p align="center">
Set Up and Configure the Server 2019 Virtual Machine in VirtualBox: <br/>
<img src="https://imgur.com//RBAjgWa.png" height="80%" width="80%" alt="Set Up and Configure the Server 2019 Virtual Machine in VirtualBox"/>
<br /> Next, we'll create our virtual machines in VirtualBox. Open VirtualBox and click "New" to start the process. For the first VM, create one for Server 2019. Name it something simple like "DC" for Domain Controller, select "Windows 64-bit," and proceed. --Allocate RAM; 2 GB (2048 MB) is recommended if you have at least 8 GB of RAM, then continue with the default disk settings.

Once the VM is created, go to "Settings" to configure it. Under "Advanced," set both "Share Clipboard" and "Drag and Drop" to "Bidirectional" for easier file and clipboard sharing between the host and the VM.

Next, in the "System" section, adjust the "Processor" setting. Increase the number of cores to 4 if possible; otherwise, keep it at 1 if you have a less powerful CPU.

For the network settings, ensure you have two network adapters: the first should be set to NAT for internet access, and the second should be configured for an internal network.

Finally, start the VM, and when prompted, select the Server 2019 ISO you downloaded earlier. Add the ISO if necessary, select it, and then start the virtual machine. The installation process may take some time.

 
 <!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
