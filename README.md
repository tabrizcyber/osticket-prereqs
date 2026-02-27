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

- 1. We have to login to the PC.In our situation this is a VirtualMachine created in Azure Portal
- 2. We have to enable IIS in Windows
- 3. We have to download osTicket free ticketing sytem.
- 4. After downloading and extracting the files we have to install mandatory programs and extensions as PHP, VC_redist.x86.exe, MySql.
- 5. After installations we have to configure IIS and setup Localhost Web Server.

<h2>Installation Steps</h2>
<img src="https://github.com/tabrizcyber/images/blob/main/VirtualMachine.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here is the screenshot of Vitual Machine created in Microsoft Azure Portal. I'll use this VM to install osTicket</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/RDP.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>This screenshot shows the process of me connecting remotely from my own PC to VM in Azure using public ip.</p>
</p>


<p>
<img src="https://github.com/tabrizcyber/images/blob/main/osTicketExtracting.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I've logged in VM, and the screenshot shows the process of extracting files from osTicket-installation-files.zip.</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/IIS_CGI.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm instaling and enabling IIS with CGI. The steps are following:Expand Internet Information Services → World Wide Web Services → Application Development Features.
Select CGI, click OK, and wait for installation..</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/install_PHP.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm installing PHP from the osTicket installing package, which is straight forward process as many other installation processes</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/PHP_Folder.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm creating PHP folder in drive C: so I can unzip the appropriate version of php with all the required files and folders to make it work on server side</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/upgradingPHP.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm installing and upgrading PHP within IIS(PHP Manager -> C:\PHP\php-cgi.exe)</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/inetRoot.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm unzipping “osTicket-v1.15.8.zip” folder and copy the “upload” folder into “c:\inetpub\wwwroot”</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/Browse80.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>After unzipping the folder I'm reloading the IIS and browsing port(80).</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/osTicketFirstView.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>And this is how osTicket actually looks like. We might notice that some extensions haven't been installed so guess the next steps</p>
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/extensions.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm enabling few PHP extensions.Just double click on PHP Manager within IIS and click "enable or disable an extension". Extensions are following:php_imap.dll, php_intl.dll, php_opcache.dll
</p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/ostconfig.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm renaming ost-sampleconfig.php from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to "ost-config.php" </p>
<p>
<img src="https://github.com/tabrizcyber/images/blob/main/Permissions.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm disambling inheritance with advance sections of security in properties</p>
</p>
<img src="https://github.com/tabrizcyber/images/blob/main/NewPermision.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>And this is new permission for eceryone with full access</p>

<img src="https://github.com/tabrizcyber/images/blob/main/continueInstallationOsTicket.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here some steps to continue installation is osTicket like registering user within the platform</p>

<img src="https://github.com/tabrizcyber/images/blob/main/HeidiSql.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>Here I'm installing HeidiSql to create database</p>
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
