<p align="center">
<img src="IMGUR-LINK-HERE" alt="osTicket logo" width="300px"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

This project walks through the full **installation and configuration** of the open-source ticketing system **osTicket** on a Windows 10 Virtual Machine hosted in Microsoft Azure.

---

<h2>📸 Project Overview</h2>

**Files needed for installation (Prerequisites Folder)**  
<p align="center">
<img src="https://imgur.com/a/qaKgxB5" alt="Prerequisite Files" width="80%"/>
</p>

**osTicket displaying missing prerequisites before installation**  
<p align="center">
<img src="https://imgur.com/a/qaKgxB5" alt="osTicket Missing Extensions" width="80%"/>
</p>

**osTicket setup & admin account creation page**  
<p align="center">
<img src="IMGUR-LINK-HERE" alt="osTicket Setup Page" width="80%"/>
</p>

**IIS Manager installed and ready**  
<p align="center">
<img src="IMGUR-LINK-HERE" alt="IIS Manager" width="80%"/>
</p>

---

<h2>🧰 Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- PHP 7.3.8
- MySQL 5.5.62
- HeidiSQL

---

<h2>💻 Operating System Used</h2>

- <b>Windows 10 Pro</b> (21H2)

---

<h2>📝 Step 1: Create the Virtual Machine in Azure</h2>

Create a Windows 10 VM with:

- **Name:** osticket-vm  
- **vCPUs:** 4  
- **Username:** labuser  
- **Password:** osTicketPassword1!  

Connect via Remote Desktop.

---

<h2>📝 Step 2: Download Installation Files</h2>

Inside the VM:

1. Download **osTicket-Installation-Files.zip**  
2. Unzip it → folder becomes **osTicket-Installation-Files**

---

<h2>📝 Step 3: Enable IIS + CGI</h2>

Enable the following in Windows Features:

- Internet Information Services
- **CGI**
- Application Development Features
- IIS Management Console

---

<h2>📝 Step 4: Install Prerequisites</h2>

From the installation folder:

✔ PHP Manager for IIS  
✔ Rewrite Module  

Create:

