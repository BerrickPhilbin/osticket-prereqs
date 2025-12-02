<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="200"/>
</p>

<h1 align="center">🎟️ osTicket — Prerequisites & Full Installation Guide</h1>

<p align="center">
A complete walkthrough for deploying <strong>osTicket v1.15.8</strong> on a Windows 10 VM in Azure.
</p>

---

## 🧰 **Environments & Technologies Used**

- ☁️ Microsoft Azure (Virtual Machines)
- 🖥️ Windows 10 (21H2)
- 🔐 Remote Desktop Protocol (RDP)
- 🌐 Internet Information Services (IIS)
- 🧩 PHP 7.3.8
- 🗄️ MySQL 5.5
- 🛠️ HeidiSQL

---

## 📌 **Installation Overview (13 Steps)**

1. Create Azure VM & Log In  
2. Download osTicket Installation Files  
3. Enable IIS + CGI  
4. Install PHP Manager  
5. Install Rewrite Module  
6. Create `C:\PHP` Directory  
7. Install PHP 7.3.8  
8. Install Visual C++ Redistributable  
9. Install MySQL 5.5  
10. Register PHP in IIS  
11. Install osTicket Files  
12. Enable PHP Extensions  
13. Complete Web Setup & Database Configuration  

---

# 📝 **Full Step-By-Step Installation Guide**

---

## ⭐ **🖥️ Step 1 — Create Azure VM & Log In (RDP Connection)**

Create a Windows 10 VM in Azure:

- **Name:** `osticket-vm`  
- **Size:** 4 vCPUs  
- **Username:** `labuser`  
- **Password:** `osTicketPassword1!`  

> ⚠️ *Passwords are shown only for lab exercises—never store or share real passwords in plaintext. Use a password manager such as KeePass, 1Password, or NordPass in real environments.*

After deployment:  
1. Copy the VM's **public IP**  
2. Open **Remote Desktop Connection**  
3. Log in with your set credentials
<p align="center">
  <img src="https://i.imgur.com/G4MkTgz.png" width="80%" alt="VM Setup" />
</p>

---

## 📥 **🗂️ Step 2 — Download & Unzip osTicket Installation Files**

Inside the VM:

- Download `osTicket-Installation-Files.zip`
- Extract to Desktop → Folder will appear as **osTicket-Installation-Files**

<p align="center">
  <img src="https://i.imgur.com/uMoQq6v.png" width="80%" alt="VM Setup" />
</p>

---

## 🌐 **⚙️ Step 3 — Install & Enable CGI with IIS**

Enable the following Windows features:

```
World Wide Web Services
 → Application Development Features
      → [✔] CGI
```

<p align="center">
  <img src="https://i.imgur.com/BHq3VZm.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/cNGIDFV.png" width="80%" alt="VM Setup" />
</p>

---

## 🧩 **📦 Step 4 — Install PHP Manager for IIS**

Run:

```
PHPManagerForIIS_V1.5.0.msi
```

<p align="center">
  <img src="https://i.imgur.com/Z7LmO16.png" width="80%" alt="VM Setup" />
</p>

---

## 🔁 **🔧 Step 5 — Install the IIS Rewrite Module**

Run the following installer:

```
rewrite_amd64_en-US.msi
```

<p align="center">
  <img src="https://i.imgur.com/rWuf4dR.png" width="80%" alt="VM Setup" />
</p>

---

## 📁 **📂 Step 6 — Create the PHP Directory**

Create the folder by going into your C:drive and than creating a new folder named:

```
C:\PHP
```

---

## 🧬 **📤 Step 7 — Install PHP 7.3.8**

Extract:

```
php-7.3.8-nts-Win32-VC15-x86.zip
```

Into:

```
C:\PHP
```

<p align="center">
  <img src="https://i.imgur.com/6QlmoxM.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/sinz33w.png" width="80%" alt="VM Setup" />
</p>

---

## 🏗️ **📌 Step 8 — Install Visual C++ Redistributable**

Install:

```
VC_redist.x86.exe
```

<p align="center">
  <img src="https://i.imgur.com/mDv1fVC.png" width="80%" alt="VM Setup" />
</p>

---

## 🗄️ **🛢️ Step 9 — Install MySQL 5.5.62**

Follow this setup:

- **Installation Type:** Typical  
- **Configuration Wizard:** Launch  
- **Mode:** Standard Configuration  
- **Username:** root  
- **Password:** root  

<p align="center">
  <img src="https://i.imgur.com/lvuD4Z3.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/KaLj94F.png" width="80%" alt="VM Setup" />
</p>


---

## 🛠️ **🔗 Step 10 — Register PHP in IIS**

In **IIS Manager**:

```
PHP Manager → Register new PHP version
```

Point to:

```
C:\PHP\php-cgi.exe
```

Restart IIS afterward.

<p align="center">
  <img src="https://i.imgur.com/VNxigOz.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/yd3ef7F.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/iXN7ZSr.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/f5bbGLi.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/F3vQv5P.png" width="80%" alt="VM Setup" />
</p>

---

## 📦 **📝 Step 11 — Install osTicket Files**

1. Extract: `osTicket-v1.15.8.zip`
2. Copy **upload** folder →  
   ```
   C:\inetpub\wwwroot
   ```
3. Rename:  
   ```
   upload → osTicket
   ```

Restart IIS again.

<p align="center">
  <img src="https://i.imgur.com/sIbVIMH.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/zfA7JAc.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/3jpmNVe.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/yPX0DS7.png" width="80%" alt="VM Setup" />
</p>

---

## 🔧 **🧩 Step 12 — Enable Required PHP Extensions**

In IIS → PHP Manager → Enable/Disable Extensions:

Enable:

- `php_imap.dll`
- `php_intl.dll`
- `php_opcache.dll`

<p align="center">
  <img src="https://i.imgur.com/BsUYP14.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/hPZCHKT.png" width="80%" alt="VM Setup" />
</p>

---

## 🚀 **🎉 Step 13 — Complete osTicket Web Setup & Database Configuration**

### 🔧 Rename Config File

```
C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
→ ost-config.php
```

<p align="center">
  <img src="https://i.imgur.com/EPfB6tK.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/FizqK5c.png" width="80%" alt="VM Setup" />
</p>


### 🔐 Set Permissions

- Disable inheritance  
- Remove ALL permissions  
- Add: **Everyone → Full Control**

<p align="center">
  <img src="https://i.imgur.com/Wqk22ZW.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/qbML7H8.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/s5gSePK.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/rUVbKRG.png" width="80%" alt="VM Setup" />
</p>

---

### 🗄️ Create Database (HeidiSQL)

- Install HeidiSQL from the osTicket installation files
- Open HeidiSQL  
- Connect using: `root / root`  
- Create database named: **osTicket**

<p align="center">
  <img src="https://i.imgur.com/bnQxMUz.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/rHZmgsV.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/cAJ7YlV.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/4LaGtmQ.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/xIja8Ha.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/nONdBnP.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/5ykYl1q.png" width="80%" alt="VM Setup" />
</p>

---

### 🌐 Final Browser Setup

Visit:

```
http://localhost/osTicket/scp/login.php
```

Enter MySQL settings:

- Database: `osTicket`
- Username: `root`
- Password: `root`

Click **Install Now!**

<p align="center">
  <img src="https://i.imgur.com/itvcKNk.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/pcm0cTG.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/rcYNhVY.png" width="80%" alt="VM Setup" />
</p>

<p align="center">
  <img src="https://i.imgur.com/WJIuGwG.png" width="80%" alt="VM Setup" />
</p>

Than press "install now"
---

# 🎉 You're Done!
osTicket is now fully installed and ready for use.

<p align="center">
  <img src="https://i.imgur.com/sykaJbu.png" width="80%" alt="VM Setup" />
</p>

