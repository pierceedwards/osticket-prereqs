<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS in windows with CGI
- Install PHP Manager for IIS and Rewrite Module
- Install VC_redist.x86.exe and MySQL 5.5.62
- Launch Configuration Wizard and setup username and password
- Install HeidiSQL and create an new database called "osTicket"

<h2>Installation Steps</h2>

<p>

  ![image](https://github.com/user-attachments/assets/649a59ef-925b-407f-bd55-78a983cf8005)
![image](https://github.com/user-attachments/assets/aa78c39b-e552-4f17-8957-dbfb0afb7ed5)

</p>
<p>
Enable Internet Information Services, check the CGI box ,and install PHP Manager

![image](https://github.com/user-attachments/assets/a56d9601-e2cc-4eb0-bcf9-8e554cd65a4a)
</p>

 ![image](https://github.com/user-attachments/assets/f8f682b8-cd92-4591-8092-c860d8746111)
 
Install VC_redist.x86.exe and MySQL 5.5.62 and launch the Configuration Wizard to setup a username and password
<br />

<p>
   

![image](https://github.com/user-attachments/assets/a3a944d0-72c0-44f2-a32f-b1d6ed45e031)


<p>
  
</p>
<br />
Once installed create a database called "osTicket" (essentially we are doing the backend work to make the system function) once done we enter that information into our osticket installer and complete!
<p>

  ![image](https://github.com/user-attachments/assets/a40df611-29ab-4ae8-819e-8737c52d0d12)
</p>
<p>

</p>
<br />
