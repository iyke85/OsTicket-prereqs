<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this project, I successfully set up osTicket, an open-source support ticket system, on a Windows Server hosted on an Azure Virtual Machine (VM). This involved configuring IIS (Internet Information Services), PHP, and MySQL, as well as installing and configuring osTicket. The following steps detail the entire process, from installation to configuration and setup.



.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of items used</h2>

- Internet Information Services (IIS)
- PHP Manager for IIS
- URL Rewrite Module
- PHP 7.3.8
- Visual C++ Redistributable
- MySQL 5.5.62
- osTicket
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/n8Yw7wD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/LZa4oFw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
  <img src="https://i.imgur.com/VdDEM0a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
1. Create and Configure Azure VM:
Created an Azure Virtual Machine and named it OS-TICKET.
Configured the VM with Windows Server and necessary network settings.

2. Install and Enable IIS:
Enabled IIS (Internet Information Services) in Windows with the following features:
CGI
Common HTTP Features
IIS Management Console

3. Install PHP Manager and Rewrite Module:
Downloaded and installed PHP Manager for IIS.
Downloaded and installed the Rewrite Module (rewrite_amd64_en-US.msi).

4. Setup PHP:
Created a directory C:\PHP on the C drive.
Downloaded PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzipped the contents into C:\PHP.
Downloaded and installed the Visual C++ Redistributable (VC_redist.x86.exe).
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Install MySQL:
Downloaded and installed MySQL 5.5.62 (mysql-5.5.62-win32.msi).
Choose Typical Setup.
Launched Configuration Wizard after installation.
Selected Standard Configuration.
Set the root password to Password1.

6. Configure IIS for PHP:
Opened IIS as an Admin.
Registered PHP from within IIS.
Reloaded IIS (Stopped and Started the server).

7. Install and Configure osTicket:
Downloaded osTicket and extracted the “upload” folder to `C:\inet
pub\wwwroot`.
Renamed “upload” to “osTicket”.
Reloaded IIS (Stopped and Started the server).
Accessed osTicket via Default -> osTicket in IIS and clicked “Browse *:80”.

8. Enable PHP Extensions:
Noted that some extensions were not enabled.
Went back to IIS, and navigated to sites -> Default -> osTicket.
Double-clicked PHP Manager.
Clicked “Enable or disable an extension”.
Enabled php_imap.dll.
Enabled php_intl.dll.
Enabled php_opcache.dll.
Refreshed the osTicket site in the browser to observe the changes.

9. Configure osTicket:
Renamed ost-sampleconfig.php to ost-config.php in C:\inetpub\wwwroot\osTicket\include.
Assigned permissions to ost-config.php:
Disabled inheritance and removed all existing permissions.
Added new permissions: Everyone -> All.
10. Setup MySQL Database:

Downloaded and installed HeidiSQL.
Opened HeidiSQL and created a new session with the credentials root/Password1.
Connected to the session and created a database named osTicket.

11. Complete osTicket Setup in Browser:
Continued setting up osTicket in the browser.
Provided the following details:
Helpdesk Name
Default email (receives emails from customers)
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1

Clicked “Install Now!” to complete the installation.

12. Final Steps and Clean Up:
Confirmed successful installation by browsing to the help desk login page: http://localhost/osTicket/scp/login.php.
End Users can access osTicket via: http://localhost/osTicket/.
Cleaned up the installation:
Deleted the setup directory: C:\inetpub\wwwroot\osTicket\setup.
Set ost-config.php to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
                                                 Summary

This project demonstrates my ability to install and configure a web-based application (osTicket) on a Windows Server using IIS, PHP, and MySQL, hosted on an Azure Virtual Machine. The process involved meticulous configuration of server components, database management, and ensuring the security of the setup. This experience showcases my technical skills in system administration, cloud computing, and web application deployment.
</p>
<br />
