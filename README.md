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

- PHP Manager for Internet Information Services (IIS)
- Rewrite Module
- Visual C++
- PHP 7.3.8 (file)
- My SQL
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/f807VMW.png"/>
</p>
<p>
First, go to portal.azure.com, create a resource group, then create a virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/KLzsL9o.png"/>
</p>
<p>
Open up remote desktop, put in the public IP address, then enter your credentials.
</p>
<br />

<p>
<img src="https://i.imgur.com/AUb3xcI.png"/>
</p>
<p>
Next, go to control panel--->Programs--->Turn features on or off--->Internet Information Services--->World Wide Web Services--->Application Development Features--->check the box for CGI. Press ok
</p>
<br />

<p>
<img src="https://i.imgur.com/BlfYFbG.png"/>
</p>
<p>Install PHP Manager for IIS. Then install the rewrite module.
</p>
<br />

<p>
<img src="https://i.imgur.com/Jddb6Q7.png"/>
</p>
<p>
Next, create a file called PHP in the "C:" portion of File Explorer
</p>
<br />

<p>
<img src="https://i.imgur.com/6zx7I53.png"/>
</p>
<p>
Download php 7.3.8 and click "keep anyway"
</p>
<br />

<p>
<img src="https://i.imgur.com/osnBibj.png"/>
</p>
<p>
Unzip the contents of PHP 7.3.8 into the C:\PHP file. Then , download the Visual C++ file (VC_redist.x86.exe)
</p>
<br />

<p>
<img src="https://i.imgur.com/W19Bk7E.png"/>
</p>
<p>
Right Click IIS in Start, and press "run as admin"
</p>
<br />

<p>
<img src="https://i.imgur.com/9kzCJaP.png"/>
</p>
<p>
Download the osTicket file. Within C:\inetpub\wwwroot, rename the "upload" folder to "osTicket"
</p>
<br />

<p>
<img src="https://i.imgur.com/1od21Xn.png"/>
</p>
<p>
Open IIS, refresh and go to sites --->Default --->osTicket. On the right click Browse*80. After the osticket page comes up, go back to IIS and double click PHP manager Enable: php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osticket page and observe changes
</p>
<br />

<p>
<img src="https://i.imgur.com/NdmOujh.png"/>
</p>
<p>
Go to inetpub> wwwroot> osticket>include and rename "ost-sampleconfig" to "ost-config"
</p>
<br />

<p>
<img src="https://i.imgur.com/lNvmzjc.png"/>
</p>
<p>
Input info for osTicket account
</p>
<br />

<p>
<img src="https://i.imgur.com/mxPzUjx.png"/>
</p>
<p>
Download Heidi SQL. Enter credentials for your "root" account
</p>
<br />

<p>
<img src="https://i.imgur.com/mxPzUjx.png"/>
</p>
<p>
Enter "root" account in the basic info for osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/KDkCpCp.png"/>
</p>
<p>
Enable the database in Heidi SQL
</p>
<br />

<p>
<img src="https://i.imgur.com/VY8Fi5i.png"/>
</p>
<p>
A congratulations page should appear when this is done.
</p>
<br />

<p>
<img src="https://i.imgur.com/0h8JtWf.png"/>
</p>
<p>
Delete the setup folder in the C:\-->inetpub--->wwwroot
</p>
<br />

<p>
<img src="https://i.imgur.com/cwFcOdP.png"/>
</p>
<p>
Go to osTicket--->include--> right click ost-config.php--->more options-->properties-->security-->advanced-->change permissions--->select a principal-->enter "Everyone"--press ok
</p>
<br />

<p>
<img src="https://i.imgur.com/dNVdTu8.png"/>
</p>
<p>
Enter osTicket credentials and log in
</p>
<br />
