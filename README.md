<p align="center">
<img src="https://i.imgur.com/VStvYjF.png" alt="osTicket logo" width="300px"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

This project walks through the full **installation and configuration** of the open-source ticketing system **osTicket** on a Windows 10 Virtual Machine hosted in Microsoft Azure.

---

<h2>🧰 Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- <b>Windows 10 Pro (21H2)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- PHP 7.3.8
- MySQL 5.5.62
- HeidiSQL

---

<h2>📝 Step 1: Create the Virtual Machine in Azure</h2>

Create a Windows 10 VM with:

- **Name:** osticket-vm  
- **vCPUs:** 4  
- **Username:** labuser  
- **Password:** osTicketPassword1!  

Connect via Remote Desktop.
<p align="center">
<img src="https://i.imgur.com/G4MkTgz.png" alt="Prerequisite Files" width="80%"/>
</p>
---

<h2>📝 Step 2: Download Installation Files</h2>

Inside the VM:

1. Download **osTicket-Installation-Files.zip**  
2. Unzip it → folder becomes **osTicket-Installation-Files**
<p align="center">
<img src="https://i.imgur.com/J6Go1Bg.png" alt="Prerequisite Files" width="80%"/>
</p>
---

<h2>📝 Step 3: Enable IIS + CGI</h2>

Enable the following in Windows Features:

- Internet Information Services
- **CGI**
- Application Development Features
- IIS Management Console
<p align="center">
<img src="https://i.imgur.com/GzpH3fk.png" alt="Prerequisite Files" width="80%"/>
</p>
---

<h2>📝 Step 4: Install Prerequisites</h2>

From the installation folder:

✔ PHP Manager for IIS  
✔ Rewrite Module  

<p align="center">
<img src="https://i.imgur.com/J6Go1Bg.png" alt="Prerequisite Files" width="80%"/>
</p>

---

<h2>📝 Step 5: ISS manager setup </h2>

From within the IIS manager the setup is completed by:

properly setting up the routing for the previously mentioned C:drive file,
setting things up in the root file,
and refreshing the server between step

<p align="center">
<img src="https://i.imgur.com/1D4O9sM.png" alt="Prerequisite Files" width="80%"/>
</p>

---

<h2>📝 Step 6: Setting up the admin user </h2>

Now for the final step of the instilation process, setting up the admin user account, which requires:

Help desk name, and email.
First name and last name.
and a second seperate Email from the first Email, password, username.

<p align="center">
<img src="https://i.imgur.com/GVdsifL.png" alt="osTicket Setup Page" alt="Prerequisite Files" width="80%"/>
</p>
