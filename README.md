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

- Creating Virtual Machines
- Installing IIS
- Installing PHP Manager
- Installing Rewrite Module
- Installing PHP
- Installing VC_redist
- Installing MySQL
- Clean Up

<h2>Installation Steps</h2>

<h3>Creating Virtual Machines</h3>

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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the virtual machine navigate to https://www.iis.net/downloads/microsoft/url-rewrite and download the x64 version. Once downloaded run the program. Accept the terms, and click install, and then finish. Once done the Module is installed
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit emt, consectur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim venium, quis nostrud exercitation ullamco laboris nisis ut alipuip ex ea commodo consequat. Duie aute irure dolor in peprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
