<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket through Azure. 
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- Internet Information Services (IIS)
- Microsoft Web Platform Installer
- PHP Manager
- My SQL
- C++ 2008 Redistributable

<h2>Installation Steps</h2>

<p>
https://imgur.com/gallery/1cJ9rA5 
Create a Virtual Machine with Azure to run this lab. Remote Desktop into the created VM. 
</p>

Install/Enable Internet Internet Information Services (IIS) in windows: control panel> programs> Turn Windows features on or off> check box titled “Internet Information Services".

<p>
https://imgur.com/a/pui2L0P

Search for the installation files you will need to install. Find and install: Web Platform Installer. Search Web Platform Installer to add MySQL 5.5 & search to add all simple versions of PHP. Create a username and password when installation is finished. Web installer will attempt to finish installing all of the prerequisites that are checked. 
</p>
<br />




Click the PHP Manager option in ISS,Enable or disable an extension> enable the following extensions: 
php_imap.dll 
php_intl.dll 
php_opcahe.dll 
refresh OsTicket in the browser window.
</p>
<br />

Rename 
C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php> Assign permissions: under security tab> click advanced> disable inheritance: remove all inheritance> allow all permissions: click add, select a principal, enter everyone in object name field> allow full control permissions. This will allow full control for everyone. 
</p>
<br />
After all previous steps are complete, the OsTicketing system should be fully functional and you should be allowed to create actual Helpdesk tickets. Please see test ticket above. You have to fill out most, if not all, of the information for this setup. *The email address must be different for the system settings and the admin user to not create conflict. 
</p>
<br />

<p>
https://imgur.com/a/No0hGjS
You should see a congratulations screen in the browser window if everything was done correctly. Clients are now able to successfully create help desk tickets.
