<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Insiallation</h1>
This project showcases the steps required to set up a free, open source, help desk ticketing system called osTicket; using virtual machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computing)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>
- Windows 10</b>

<h2>List of Prerequisites</h2>

- Create Virtual Machine
- Installing IIS
- Installing PHP Manager
- Installing Rewrite Module
- Installing PHP
- Installing VC_redist
- Installing MySQL

<h2>Configuration and Setup</h2>

-Enabling Extensions
-Renaming ost-sampleconfig.php
-Disabling Inheritance and Adding Permission
-Configuring osTicket
-System Settings & Admin User
-Installing Heidi SQL
-Using Heidi SQL
-osTicket SQL Database Settings

<h2>Installation Steps</h2>

<h3>Create Virtual Machine</h3>

<p>
<img src="https://github.com/CJones226/osticket-prereqs/blob/main/Creating%20Resource%20Group.JPG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/f5a4c92b-bc39-420d-b441-6800c5366656" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When creating your virtual machines you have to create a resource group first for the virtual machine to exist on. This will hold all of the information: network, storage, etc. Once that is created next you can create the virtual machine. Simply calling it OsTicket makes it easy and keeps everything organized. The virtual machine should be placed on the resource group you created, it sohuld be a Windows 10 machine with atleast 2 vCPUs; otherwise, the computer will not run very well. Make the username and password uncomplicated and easy to remember. I, for example, made my username "osticket" and the password "@dm1n1strat0r"
</p>
<br />

<h3>Installing IIS</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/24c89532-26c5-46fe-9a7e-971ac71e244b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using Remote Desktop Connection, connect to your virtual machine using the IP Address in Azure. Once connected, login with the username and password you created. Then set up the computer and make it to the home screen. Once that is accomplished you can open up your Control Panel and navigate to Programs->Programs and Features. Then select 'Turn Windows features on or off'. A window will pop up and you can scroll down and select Internet Information Services->Web Management Tools->IIS Management Console, as well as World Wide Web Services->Application Development Features->CGI, as well as Common HTTP Features. Then select OK, the computer will search and install the programs.
</p>
<br />

<h3>Installing PHP Manager for IIS</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/c668f336-079c-4ae4-add1-7d3f39e8bdac" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the virtual machine, navigate to https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10 and download the file. Once downloaded, run the file, accept and agree to the conditions, once done it will install.
</p>
<br />

<h3>Installing Rewrite Module</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/c788d4d3-51c5-4a71-8d4c-bad2524247aa" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the virtual machine navigate to https://www.iis.net/downloads/microsoft/url-rewrite and download the x64 version. Once downloaded run the program. Accept the terms, and click install, and then finish. Once done the module is installed and ready to go.
</p>
<br />

<h3>Installing PHP</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/f50d46ae-33f0-49ac-a87b-95ca21794efa" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the virtual machine navigate to https://drive.google.com/drive/folders/1yOk5ejp5Oe21USJfCgelyvdlJMwHRhxC?usp=drive_link and download PHP, once downloaded it is necessary to unzip the file into its own directory. Within the C drive you should create a file called PHP, within this file extract the PHP file you downloaded.
</p>
<br />

<h3>Installing VC_Redist</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/e7f2c702-154b-4189-95e6-ec0f6a5cd701" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate on the virtual machine to https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=drive_link and download the file. Once downloaded, accept the terms and conditions and install.
</p>
<br />

<h3>Installing MySQL</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/229f395c-ba46-411b-8333-e92dfabb1452" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/44c61b07-b37b-49b4-807b-1c509647d052" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the file is downloaded begin the install. Accept the terms, select the typical install, and then Launch the instance. Once inside choose the standard configuration, and install as a windows service, and execute. Set your password as somethine you can remember, for example I used "password1"
</p>
<br />

<h3>Clean Up</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/8afe5079-8481-4835-ae97-3c1d99d3cf92" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We must finally register the new PHP version. Search the computer for IIS and run as administrator.
</p>
<br />

<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/d53e05b1-74d9-4de5-8629-c543028adf69" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next choose the path to the executable file. If you followed the past steps the php-cgi.exe file is withing PHP, the path you want is C:\PHP\php-7.3.8-nts-Win32-VC15-x86\php-cgi.exe
</p>
<br />

<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/310afa64-418b-4cb5-a156-36a836a9f43f" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally simply reset the server by pressing stop and then start in the Actions tab, under Manage Server. Once this is all done you have successfully completed all the prerequisites for installing OsTicket!
</p>
<br />

<h1>OsTicket Configuration and Setup</h1>

<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/98f79f30-585d-4b59-b62f-ccb55c5d7889" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that all of the prerequisites are installed we can install osTicket! Navigate to https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link and download osTicket. Once downloaded you will want to open the file and copy 'upload' and paste it into wwwroot, the path is as follows: C:\inetpub\wwwroot | Once copied over, rename the copied file within wwwroot from 'upload' to 'osTicket' it is case sensitive. Once completed reset IIS as you did before.
</p>
<br />

<h3>Enabling Extensions</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/c22b5ab0-cb57-4bc6-8cae-877c63abbc51" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside of IIS navigate on the left hand side in the following path sites>Default Web Site>osTicket>PHP Manager>Enable or disable an extension.
</p>
<br />

<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/f2eb553d-33b1-47d1-ad25-e60f9866179d" height="60%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within PHP Extensions enable: php_imap.dll | php_intl.dll | php_opcache.dll
</p>
<br />

<h3>Renaming ost-sampleconfig.php</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/ec70c737-2ed2-4d39-a7e2-c1a13c5c750a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php | once there rename the file from ost-sampleconfig.php to     ost-config.php
</p>
<br />

<h3>Disabling Inheritance and Adding Permissions</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/d992b1d4-524e-40b0-bf76-7d143d4582c4" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Left click on ost-config.php and click on properties. Once inside navigate to the security tab and click advanced. Once you are in the advanced settings you are going to click "Disable inheritance" remove all.
</p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/619acc70-8131-452c-9f32-53be1e5c644a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next click on add, at the top click 'select a principal' and enter everyone, and click 'check names' and click 'ok'. Next give total control and click 'ok' then 'apply then 'ok'.
</p>
<br />

<h3>Configuring osTicket</h3>
<p>
<img src=https://github.com/CJones226/osticket-prereqs/assets/158533476/c11de796-bae8-4c45-837f-af8696176738" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open OsTicket in the browser. Within IIS navigate to the osTicket Home, and click on 'Browse *:80 (http)' on the right hand side. This page should appear click continue.
</p>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/b5958359-dc79-4b74-862a-96e29f17a022" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>System Settings & Admin User</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/cccb8c5c-53a4-4495-8963-7a2e631e4c2c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This will be the next page to appear. Here you are going to name the Help Desk and add the Admin to the account. To keep everything simple I used the name 'osTicket Help Desk' and the email 'osticket@helper.com' once this was done I went even more generic and made the administrator John Doe at a similar email with the password 'password1'.
</p>
<br />

<h3>Installing Heidi SQL</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/blob/main/Heidi%20SQL%20Install.JPG?raw=true" height="80%" width="80%" alt="DIsk Sanitization Steps"/>
</p>
<p>
Navigate to the following link and download Heidi SQL, follow the basic download and leave everything in the automatic setup.
</p>

<h3>Using Heidi SQL</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/blob/main/Heidi%20usage.JPG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once Heidi SQL is downloaded run a session of it, and then create a new Session use the user root, and the password: password1. Then open, once inside make a new Database and call it osTicket
</p>
<br />

<h3>osTicket SQL Database Settings</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/blob/main/Database%20Setup.JPG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enter the information that you just created into the bubbles. Leave "MySQL Table Prefix" "MySQL Hostname" all there auto fill, and then fill in the last three. osTicket, root, and then the password.
</p>
<br />

<h3>Change File Permissions</h3>
<p>
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/d9d5000c-6543-4d88-a7b9-453fdad8b83a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, we are at the portion where we can change the permissions for ost-config.php and we can delete the setup file. Navigate in your files to: C:\inetpub\wwwroot\osTicket\setup and delete the file.'
<img src="https://github.com/CJones226/osticket-prereqs/assets/158533476/d9d5000c-6543-4d88-a7b9-453fdad8b83a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Once that is complete navigate to: C:\inetpub\wwwroot\osTicket\include\ost-config.php once there you are going to go into the properties and change the permissions to "read only."
</p>
<h1>All Prerequisites Complete</h1>
