<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket - Prerequisites and Installation Guide</h1>

<p align="center">
  A step-by-step guide for installing and configuring <strong>osTicket</strong>, an open-source support ticket system, on a Windows environment using Microsoft Azure and IIS.
</p>

---

## 🧰 Environments and Technologies Used

- **Microsoft Azure** – Virtual Machines for hosting the Windows OS  
- **Remote Desktop Protocol (RDP)** – For accessing the virtual machine  
- **Internet Information Services (IIS)** – To serve the osTicket web application  

## 💻 Operating System

- **Windows 10 Pro** (Version 21H2)

---

## ✅ Prerequisites

Ensure the following components are installed and configured before proceeding with the installation:

1. **Enable IIS and CGI**
   - Go to: `Control Panel > Programs > Turn Windows features on or off`
   - Enable:
     - Internet Information Services (IIS)
     - Web Management Tools
     - World Wide Web Services > Application Development Features > CGI

2. **Install PHP Manager for IIS**  
   - 🔗 [PHP Manager Download](https://www.iis.net/downloads/community/2018/05/php-manager-for-iis-10)

3. **Install URL Rewrite Module**  
   - 🔗 [Rewrite Module Download](https://www.iis.net/downloads/microsoft/url-rewrite)

4. **Install Required Packages**
   - **VC_redist.x86.exe** – 🔗 [Download](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)
   - **MySQL Server 5.5.62** – Download and install (remember your root password)

5. **Install HeidiSQL**
   - 🔗 [HeidiSQL Download](https://www.heidisql.com/)
   - Create a new database called `osTicket`

---

## 🚀 Installation Steps

### 1. Download osTicket

- 🔗 [Download osTicket](https://osticket.com/download/)
- Extract the files to:  
  `C:\inetpub\wwwroot\osTicket`

### 2. Configure IIS

- Open **IIS Manager**
- Add a new website:
  - Site name: `osTicket`
  - Physical path: `C:\inetpub\wwwroot\osTicket`
  - Port: `80` (or any available port)
- Configure PHP using PHP Manager
- Set correct permissions:
  - `ost-config.php` → Allow write for `IUSR` and `IIS_IUSRS`
  - `include/` and `scp/` folders → Temporary write access

### 3. Setup MySQL Database

- Launch **HeidiSQL**
- Create a new database:
  ```sql
  CREATE DATABASE osTicket;
