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
  
### 4. Run osTicket Installer
Open a browser and navigate to http://localhost/osTicket/setup/

Complete the installer using:
- Database Name: osTicket
- MySQL User: osticketuser
- Password: yourpassword

### 5. Post-Installation Cleanup
Delete setup/ directory after installation

- Rename ost-config.php to remove write permissions

- Disable write access to sensitive folders


### 🖼️ Installation Screenshots

Below are some reference screenshots taken during installation for visual guidance:

![image](https://github.com/user-attachments/assets/f3ea15a9-8c20-4fdf-a2ae-3b67ac1c52b4)
![image](https://github.com/user-attachments/assets/b17b4aba-0f62-4245-bf95-7a76ef5eb83e)
![image](https://github.com/user-attachments/assets/674c81d9-cbaf-40c7-9e59-22351ab065e4)
![image](https://github.com/user-attachments/assets/0b55fada-d7aa-48ab-ab76-259a04bd8a52)
![image](https://github.com/user-attachments/assets/05ec41a3-d311-44f4-9ce2-6fcec87f4daf)
![image](https://github.com/user-attachments/assets/b19928cf-1879-4444-9bd6-ab4fe2d9721a)

### 🧪 Final Notes
osTicket is now fully installed and ready to use!
Regularly back up your database and configuration files.
