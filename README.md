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

- Once the installation is done, notice the flag on the top left of the Server Manager
- Click on the flag and promote DC-01 to Domain Controller.
