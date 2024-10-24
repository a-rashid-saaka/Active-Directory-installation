  <h1 align="center">Active directory deployment and setup</h1>


<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>


<p> 
  This is a continuation of the first project that set up our Active Directory environment, we now move to the next step in our tutorial series..Welcome to the "Active Directory deployment and setup" project. We will cover the essentials of deploying and refining an Active Directory system, focusing on installation, forest creation, user account management, domain integration, and Remote Desktop access.
</p>
<h2>Prerequisites</h2>

- <a href="https://github.com/a-rashid-saaka/Azure_VM_setup_and_Network_Configuration"> Azure VM setup and Network Configuration </a>

<h2>Objectives</h2>
<h3>Active Directory Installation</h3>

-  Setup and install Active Directory services on the specified Domain Controller virtual machine.

<h3>Forest Creation</h3>

- Setup a new Active Directory forest.

<h3>Administrator Account Creation</h3>

- Create and manage user accounts with admin privileges for better Active Directory administration.

<h3>Domain Joining</h3>

- Connect the Client-1 virtual machine to the domain so it can communicate smoothly with the Active Directory.

<h3>Remote Desktop Setup</h3>

- Set up Remote Desktop access for non-administrative users. This will improve user access while keeping security measures in place.

  <h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services
- Command Prompt

<h2>Operating Systems Used </h2>

- Windows (Windows Server 2019 Datacenter)
- Windows (Windows 10 Pro)

  <h2>Configuration Steps</h2>

<h3>&#9312; Install Active Directory in DC-01</h3>


- In the server manager click on "Add Roles and Features" -> Role-based or feature-based installation -> Select a server from the server pool -> Active Directory domain services -> Add Features, and follow the prompt to complete the installation <br>


![Screenshot (89)](https://github.com/user-attachments/assets/e4919f8e-fe95-40a6-b67e-17cbc112e414)
- After the installation, notice the flag in the top right corner of the Server Manager. 
- Click on the flag to promote VM1-DC to a Domain Controller.

  
  ![FLag](https://github.com/user-attachments/assets/dac2626b-8ce8-4853-ab54-0aeea882226e)



- Select "Add a new forest" , enter your domain name, and click "Next"


  ![Screenshot (92)](https://github.com/user-attachments/assets/89a31c17-bf4f-4ff6-b721-2ad4c8e09eee)

- Enter restore password and follow the prompt to complete the setup

    
![DC1](https://github.com/user-attachments/assets/6a193677-2dc5-4868-814e-97517b24d4b9)

- Restart your PC once the setup is complete , and login again using "your admin username"@domain.com, together with the admin password.
<br>
<br>
<br>

<h3>&#9313; Create Organizational Units and Admin user</h3>

- From the server manager, click on "Tools" and select "Active Directory Users and Computers"

![dc](https://github.com/user-attachments/assets/5cf69578-7c46-4f4d-941c-f481e1471457)

- To create an "EMPLOYEES" organizational unit, right click on "domain.com" -> New -> Select "Organizational Unit"

  ![DC2](https://github.com/user-attachments/assets/918b3571-b06e-4dce-8e08-1b5f18def1b7)

- Enter the name of the Organizational Unit and click on "OK".

    ![image](https://github.com/user-attachments/assets/927ffc31-455e-40a0-8593-672da31d8c74)

 - Right click on Users and create a new user named "Sam Samuels" with the username S-Samuels


   ![image](https://github.com/user-attachments/assets/46acdade-a2d8-41d0-86a7-4d3ffef87572)
- To make Sam Samuels an Admin, right click on his name -> Properties -> select " Member of" -> click on "Add" -> search "Domain Admins" and click "OK" -> click on "Apply" and "OK" for the change to take effect

  
  ![image](https://github.com/user-attachments/assets/7b2371ec-5983-448b-9039-4bd09ec7c1ed)
![image](https://github.com/user-attachments/assets/fde40a9f-6f52-4539-9558-1ebfbbecf8ca)


- You can now log back in to VM1-DC with Sam Samuel's credentials


  ![image](https://github.com/user-attachments/assets/f49f741d-b3ae-4e13-8448-affe1cd93007)
