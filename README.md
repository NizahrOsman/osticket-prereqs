<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project demonstrates the installation and configuration of osTicket, an open-source help desk ticketing system .<br />


<h2></h2>



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- PHP Manager (IIS)
- MySQL
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Desktop or laptop capable of running windows 10 virtual machine
- Microsoft Azure account to create virtual machine
- osTicket installation files and dependencies (PHP, VC Redist, Rewrite Module, PHP Manager, MySQL, HeidiSQL)
- Basic knowledge of Remote Desktop, Windows Files System, and IIS.

<p>
Created a Windows 10 VM in Microsoft Azure (2 vCPUs, 8GB Ram) and accessed via Remote Desktop. Prepared and unzipped the required installation files for osTicket, including PHP, Rewrite Module, PHP Manager for IIS, VC Redistributable, and MySQL/HeidiSQL.
  
</p> 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

  <h2>IIS & CGI Configuration</h2>
  
- Enabled IIS (Internet Information Services) to host and serve web applications. 
- Activated CGI (Common Gateway Interface) under Application Development tab to allow external scripts and applications to run on IIS, in this case PHP.
- Installed PHP Manager for IIS this allows simplification of managing PHP config and extensions, so osTicket will run properly.
- Installed Rewrite Module to rewrite and map the user-friendly URLs to corresponding backend URLs.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
 <h2>PHP & MySQL Setup</h2>
  
- Created folder C:\PHP and unzip PHP 7.3.8, will provide language runtime for osTicket.  
- Installed VC Redistributable to allow PHP to run dependant libraries correctly.
- Installed MySQL 5.5.62 to set up root user, this will be the database for osTicket.
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
 <h2>osTicket Installation & Config</h2>
  
- Copied unzipped osTicket 'upload' folder into c:\inetpub\root and renamed it to osTicket.
- Registered PHP in IIS and restarted server to apply changes.
- Enable PHP extensions:
  - php_imap.dll (email)
  - php_intl.dll (internationalization support)
  - php_opcache.dll (performance optimization)
- Renamed ost-sampleconfig.php to ost-config.php and assign proper permissions.
- Complete browser setup, and linking osTicket to to the MySQL database.
<br />
