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

- Download and intall "MySQL" from your browser. (Do a typical install)
- After the install is finished, the Configuration Wizard will open up. You then do a "Standard Configuration" 
- Set a password for "root", then click "next", then click "execute" and finally press "finish".

</p>
<br />
