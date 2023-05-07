<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Resource Group in Azure portal
- Create Windows 10 Virtual Machine with 2-4 virtual CPUs

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/rJmaadl.png" height="80%" width="80%" alt="Step 1"/>
</p>
Step 1 - 
Open Control Panel.
Select "Programs."
Select "Turn Windows Features ON/Off."
Select and open Internet Information Services.
Open "World Wide Services."
Open "Application Development Features."
Select "CGI" and then select "OK."
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224501153-f2015b7c-163b-4a00-bec9-d54d53bd7d29.png" height="80%" width="80%" alt="Step 1"/>
</p>
Step 2 - Install PHP Manager for IIS.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224501486-f2142ab7-6a65-4199-8339-8383abffc6a4.png" height="80%" width="80%" alt="Step 3"/>
</p>
Step 3 - Install the Rewrite module.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224501584-9ae2ea0f-47ab-4275-a865-0c5a20838cb5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 4 - Create a folder named "PHP" in your C: directory.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224501699-e2e5c860-efa7-4cb7-a914-92d51f06c122.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 5 - Install PHP 7.3.8.
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502135-9a9f9ff3-5682-46b4-9115-2bb69040852b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 6 - Unzip PHP 7.3.8 onto your PHP folder.
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502157-fead8fa4-ea0d-4721-9369-4c95928e34da.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7 - Install VC redist.x86.exe.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502174-0db640a1-eee5-4f50-8ec4-7e6adcf5956d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 8 - Install MySQL 5.5.62 using the Typical Setup. Launch the Configuration Wizard after installation and select the Standard configuration. Set the password to "Password1" or create your own, then select "Execute."
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502200-f74c71cd-8e3b-43c7-9d84-ea7f833c68ab.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 9 - Register PHP from within IIS.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502221-49f76209-a33c-4efa-a172-3f204b86ca1f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 10 - Stop and start the IIS server to update.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502241-4fed2d28-8605-41c2-9bde-ff674942a75f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 11 - Install the current version of osTicket. Extract and copy the "upload" folder to C:\inetpub\wwwroot. Within C:\inetpub\wwwroot, rename "upload" to "osTicket."
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502264-73b5ab38-8e46-4fa6-a5ae-84c5de73b970.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 12 - Go to sites, Default, osTicket. On the right side of the IIS screen, click "Browse*80."
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502282-7c85492f-9fad-4b43-8431-6ba8cb381034.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 13 - Open PHP Manager and enable php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh osTicket on your browser to see the changes.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502301-41dd2139-85aa-474e-aa75-42bb21e6083b.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 14 - Open C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename it to ost-config.php.
</p>



<p>
<img src="https://i.imgur.com/oC4kaPR.png" alt="Disk Sanitization Steps"/>
</p>
Step 15 - Right-click ost-config and select Properties. Disable inheritance and remove all permissions, then give "Everyone" new permissions and select all.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502339-7cd7a5b7-3117-4e9b-856d-90e8951e1c47.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 16 - Set up your osTicket in your browser. Steps 18 and 19 are on the same page.
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502462-bfdde141-12bf-49ae-933b-0a11dd07d290.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 17 - Open Heidi SQL and create a new session with root/Password1. Connect to the session and create a database called "osTicket."
</p>



<p>
<img src="https://user-images.githubusercontent.com/126700220/225052564-6db1230b-9740-4959-9101-4d5c5f4fc926.png" width="80%" alt="Disk Sanitization Steps"/>
<p>
Step 18 - Continue setting up osTicket in the browser and enter the MySQL information.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/225053801-2d54545a-3af5-45d7-9380-58b6bd83f794.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 19 - Select "Continue." A "Congratulations" message should appear on your screen.
</p>
<br />



<p>
<img src="https://user-images.githubusercontent.com/126700220/224502540-d5fe63e0-edb1-49d1-aa13-1ce19a818a6d.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Well done, you have completed the install!
</p>
<br />
