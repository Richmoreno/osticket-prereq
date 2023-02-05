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

- Azure Account
- Resource Group
- Virtual Machine
- osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/q4LVime.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
(Create Virtual Machine in Azure)
Create a Resource Group
Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
When creating the VM, allow it to create a new Virtual Network (Vnet)
Next, log in to your virtual machine. 


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install and Enable IIS in Windows with CGI

- Go to the start menu, search and open "Control Panel", and type "Programs" click "Turn Windows features on or off" under "Programs and features".
- Check off "Internet Information Services (IIS)" and expand it. (Click the + sign to expand) You then expand "World Wide Web". Expand "Application Developer" and finally check "CGI" and press "OK". IIS is now installed. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager 

- You can search for PHP Manager in any search engine and download from the web and install from your "Downloads Folder"
- Next, search in a search engine rewrite_amd64_en-US.msi. Download into your downloads folder and install. 
- You will now create the directory C:\PHP
- Go to your Windows C: drive, create a "New Folder" and name it "PHP" 
- Next, in your search engine search for "php-7.3.5-nts-Win32-VC15-x86.zip" and download. 
- In your downloads folder right click on "php-7.3.5-nts-Win32-VC15-x86.zip" and "Extract All"
- In the next page click on "Browse" then, click on "This PC" > "C:\ drive" then click on the "PHP" folder, and click on "Extract" 
- Download and install "Microsoft C++" from your browser.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Install "MySQL" 5.5.62

- Download and intall "MySQL" from your browser. (Do a typical install)
- After the install is finished, the Configuration Wizard will open up. You then do a "Standard Configuration" 
- Set a password for "root", then click "next", then click "execute" and finally press "finish". (remember your password)


<p>
<img src="https://i.imgur.com/4YA4k8C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Open IIS as an Admin / Register PHP from within IIS.

- Click on "Start" search for (IIS) Manager, you then right click on the app and "Run as Adminastrator"
- Next, double click on the "PHP Manager" icon. Under PHP Setup, click on "Register new PHP Version"
- On the pop-up window click on "..." and browse to your (C:) drive, and double click on "php.cgi" and press "OK"
- Now, click on "restart" to refresh your IIS Manager located on the "Manager Server" the right, top corner of the IIS Manager window. 

<p>
<img src="https://i.imgur.com/yTboQQ7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Install osTicket v1.15.8 (from your browswer)

- Now, you will need to Extract and copy “upload” folder to c:\inetpub\wwwroot
- Open another File Explorer window and go to your "downloads".
- On one file explorer window double click on the "osTicket zip Folder"
- On the other File explorer window, open your (C:) drive, click on "inetpub" folder, then open the "wwwroot" folder. 
- You then go to the original file explorer and drag the "upload" folder into the "wwwroot" window.
- Now you should have the "upload" folder in the "wwwroot" folder.
- Next, rename the "upload" folder" you just dragged and name it "osTicket".
- Click on "restart" to refresh your IIS Manager located on the "Manager Server" the right, top corner of the IIS Manager window. 
- Click on bottom arrow next to "sites" on the left column inside the IIS Manager, then click on the arrow next to "Deafult Web Site", and double click on the "osTicket" Folder. Next, on the right column of the IIS Manager window click on "Browse*:80 (http)"
- The osTicket Installer should open in your browser. 
- Next we're going to enable a few extensions on the osTicket Installer. 

<p>
<img src="https://i.imgur.com/vAKZXaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Enabling Extensions on osTicket

- Go to the IIS window and click on "sites" on the left column and then open the "osTicket" Folder, and finally click on "PHP Manager" 
- On the new window under PHP Extensions click on, "Enable or Disable an Extension". Next, you will enable the extensions. 
- To enable click on the extension below and on the right column of the window uner "Actions" click enable and continue to do so until all extensions listed below are enabled. 
- Extension to enable.
-Enable: php_imap.dll
-Enable: php_intl.dll
-Enable: php_opcache.dll
-Refresh the osTicket site in your browser, and observe the changes.

<p>
<img src="https://i.imgur.com/PQ8c5FR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Rename ost-config.php and Give "Everyone" Full Permissions.

-Go to your file explorer, go to your (C:) drive > inetpub > wwwroot > osTicket
- Click on the "include" folder and rename the PHP file "ost-sampleconfig.php" and name it "ost-config.php".
- Next, you will assign permissions to the "ost-config.php" file.
- Right click the "ost-config.php" file and click on "Properties". Click on the "Security" tab > Click on "Advanced" > click on "Disable inheritance" > click on "remove all inherited permissions from this object" > click on "add" > click on "Select a principal". Now type "everyone" in the "Select User Or Group" window > click on "check names" > click on "ok" > check the "Full control" box > click "ok" > click "apply and OK".
-Now everyone has permissions to the folder. 

<p>
<img src="https://i.imgur.com/qFAhJ4T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Set up osTicket in the browser. (Click Continue)

Fill out all your information (Write everything down)

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Download and Install "HeidiSQL" from your browser.

-Once HeidiSQL is installed the Session Manger window will open. 
- On the bottom, left corner of the window click on "+New" 
- The username should be root. Input the password you set up when installing MySQL and click on "Open"
- You now connected HeidiSQL with MySQL server. 
- Go back to the OsTicket set up page.
- Enter "root" under "MySQL Username:" and enter your password under "My SQL Password:". DO NOT click on "Install Now" just yet. 
- We need to create a database called "osTicket" in HeidiSQL first. 
- Right click on "Unnamed" located on the left column and go to "create new" > click "Database" 
- Under "name" type "OsTicket" > click ok. 
- Go back to the osTicket set up page, and type in osTicket under "MySQL Database" which you just created. Now you can click on "Install Now"
- Congratualtions! You just installed osTicket! We're almost done! 

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Clean Up

-Go to your (C:) drive > inetpub > wwwroot > open the osTicket. Right click the "setup" folder and delete it. 
- Now, were going to set the permissions back to "read only" on the "ost-config.php" file. 
- Inside the osTicket Folder click on the "include" folder > right click on the "ost-config.php" folder > go to "Properties" > Click on the "Security" tab > click "Advanced" > click and highlight on "Everyone" > click "Edit". Only "Read & Execute" and "Read" should be checked off > click on "ok" and then "apply".
  
- Browse to your help desk login page and you should be able to log in with your Admin credentials and start using the osTicketing System! Click the link to log in! http://localhost/osTicket/scp/login.php  
  
- End users osTicket URL: http://localhost/osTicket/ 
  
 -Congratualtions! You have succesfully installed and configured the osTicketing System! Hope you enjoyed this repository. 
  


</p>
<br />


