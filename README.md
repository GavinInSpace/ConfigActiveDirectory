<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory on Windows Server Domain Controller
- Create an Account inside of Active Directory

<h2>Summary</h2>
<p>
  This is all a very high level explanation and Active Directory has much more to it that what we are going to cover, but I feel this is a good introduction to the basics. To practice this I built two virtual machines on Microsoft Azure, making one a client and one a Domain Controller to practice it from both ends. To do this you must set your clients DNS IP to the static IP of the Domain Controller but I felt that was out of the scope of what I was trying to convey with this particular tutorial. Thank you for reading, it is much appreciated!
</p>


<h2>Deployment and Configuration Steps</h2>

<h3>Installing Active Directory</h3>

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/2287a2f7-8ad0-4da9-b6ae-078512ebac92)

<p>
  To begin installing Active Directory we must be on the windows server machine (this entire project is done on Microsoft Azure Virtual Machines) and we must have the Server Manager open on the Dashboard tab. This screen should show up by default when accessing the machine but can be started via the start menu. Then we click the add roles and features link which will bring up an add roles and features wizard. 

  ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/fc87e835-293f-48e4-b782-7ff7e3e196b7)

  We can click next through most of the sections until we get to Server Roles, wherein we will check the box to install Active Directory Domain Services. After this is done we can "next" through the rest of the wizard and finally click install. Once this is complete we should see a notification in the top right of our Server Manager screen, once of which prompt us to promote this server to a domain controller.

  ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/adc8e585-3f8a-44eb-a14e-279d4e677bbf)
  
  Once we click the link we will be presented with a Deployment Configuration screen. We need to check the bubble that says "add new forest" and choose our domain name and create a password.

 ![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/044288ae-27e1-451f-8866-0694a29ee2ce)
 
  Now we can "next" through the rest of the selections and click install. Once the installation is complete we should restart the machine although this should happen automatically. Now that we have restarted our machine it is a Domain Controller and has Active directory installed.
</p>
<br />

<h3>Creating Admin and user accounts in Active Directory</h3>

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/3405c1d4-f74f-48c3-b911-c02e425f264f)

<p>
  We should now see that our Service Manager Dashboard has some new selections than we had before. To start configuring users we go to the "tools" tab and select Active Directory Users and Computers.

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/b647a0ed-2035-451b-a455-13fdbb342189)

  This is the Active Directory UI. From here we can see multiple different entries under our domain tab including our Users. From this UI we can create things called Organizational Units (essentially a folder) that we can use to seperate different users into different buckets. Such as creating an organizational unit called "EMPLOYEES" and populating it with workers. The pic below shows the same UI after creating two Organizational Units (_EMPLOYEES, _ADMINS).

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/72b51a1d-1fe9-493e-a855-b3e3cc661bda)

   From here we can go into our Organizational Units and create users as well as set their permissions. After creating the user, if we would like to make the user and admin we must go to the users permissions and add it to the Domain Admin group.

![image](https://github.com/GavinInSpace/ConfigActiveDirectory/assets/153689700/3561f3bc-e426-47c0-a2de-79cdb2cdb3f0)

     
</p>
<br />
