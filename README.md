<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory on Windows Server Domain Controller
- Create an Admin account and a normal account
- Join the domain as a client
- Set up RDP for non admin clients on a client machine

<h2>Deployment and Configuration Steps</h2>

<h3>Installing Active Directory</h3>

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/2287a2f7-8ad0-4da9-b6ae-078512ebac92)

<p>
  To begin installing Active Directory we must be on the windows server machine and we must have the Server Manager open on the Dashboard tab. This screen should show up by default when accessing the machine but can be started via the start menu. Then we click the add roles and features link which will bring up an add roles and features wizard. 

  ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/fc87e835-293f-48e4-b782-7ff7e3e196b7)

  We can click next through most of the sections until we get to Server Roles, wherein we will check the box to install Active Directory Domain Services. After this is done we can "next" through the rest of the wizard and finally click install. Once this is complete we should see a notification in the top right of our Server Manager screen, once of which prompt us to promote this server to a domain controller.

  ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/adc8e585-3f8a-44eb-a14e-279d4e677bbf)
  
  Once we click the link we will be presented with a Deployment Configuration screen. We need to check the bubble that says "add new forest" and choose our domain name and create a password.

 ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/044288ae-27e1-451f-8866-0694a29ee2ce)
 
  Now we can "next" through the rest of the selections and click install. Once the installation is complete we should restart the machine although this should happen automatically.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
