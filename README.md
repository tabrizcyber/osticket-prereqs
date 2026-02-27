<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- 1. We have to log in to the PC. In our situation, this is a Virtual Machine created in the Azure Portal.
- 2. We have to enable IIS in Windows.
- 3. We have to download the osTicket free ticketing system.
- 4. After downloading and extracting the files, we have to install mandatory programs and extensions such as PHP, VC_redist.x86.exe, and MySQL.
- 5. After the installations, we have to configure IIS and set up the Localhost Web Server.

<h2>Installation Steps</h2>

<img src="https://github.com/tabrizcyber/images/blob/main/VirtualMachine.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here is the screenshot of the Virtual Machine created in the Microsoft Azure Portal. I will use this VM to install osTicket.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/RDP.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>This screenshot shows the process of connecting remotely from my own PC to the VM in Azure using the public IP address.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/osTicketExtracting.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I have logged into the VM, and the screenshot shows the process of extracting files from osTicket-installation-files.zip.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/IIS_CGI.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am installing and enabling IIS with CGI. The steps are as follows: Expand Internet Information Services → World Wide Web Services → Application Development Features. Select CGI, click OK, and wait for the installation to complete.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/install_PHP.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am installing PHP from the osTicket installation package, which is a straightforward process similar to many other software installations.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/PHP_Folder.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am creating a PHP folder in drive C: so I can unzip the appropriate version of PHP with all the required files and folders to make it work on the server side.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/upgradingPHP.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am installing and configuring PHP within IIS (PHP Manager → C:\PHP\php-cgi.exe).</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/inetRoot.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am unzipping the “osTicket-v1.15.8.zip” folder and copying the “upload” folder into “C:\inetpub\wwwroot”.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/Browse80.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>After unzipping the folder, I reload IIS and browse port 80.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/osTicketFirstView.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>This is how osTicket initially looks. We can notice that some required extensions have not been installed yet, which leads to the next steps.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/extensions.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am enabling several PHP extensions. By double-clicking PHP Manager within IIS and selecting “Enable or disable an extension”, I enable the following extensions: php_imap.dll, php_intl.dll, and php_opcache.dll.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/ostconfig.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am renaming ost-sampleconfig.php from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to “ost-config.php”.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/Permissions.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p><i><strong>Here, I am disabling inheritance using the Advanced Security Settings in the folder properties.</strong></i></p>
</p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/NewPermision.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>This shows the new permission settings, granting Everyone full access.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/continueInstallationOsTicket.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>Here are some steps to continue the osTicket installation, such as registering a user within the platform.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/HeidiSql.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>Here, I am installing HeidiSQL to create the database.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/SqlDatabase.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>Here, I have finished creating the database.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/signing_in.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>Here, I am signing into the osTicket admin panel.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/adminPanel.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>This is the actual interface of the osTicket control panel.</strong></i></p>

<p>
<img src="https://github.com/tabrizcyber/images/blob/main/UserPortal.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><i><strong>And this is the user panel portal to create tickets and highlight issues.</strong></i></p>



<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
