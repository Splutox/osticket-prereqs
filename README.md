<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation Guide</h1>
An easy-to-follow tutorial on installing the open-source help desk ticketing system osTicket.<br />

<p align="center"><strong>
<h2>Environments and Technologies Used</h2>

<p align="center"><strong>
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)


<p align="center"><strong>
<h2>Operating Systems Used </h2>

<p align="center"><strong>
- Windows 10</b> (21H2)


<h2>Instructions</h2>
<p align="center"><strong>Start by creating a free (or paid) <a href="https://azure.microsoft.com/en-us/free/"> Microsoft Azure Subscription</a>. Once logged in, find and open the "Virtual Machines" service, click the "create" button, and then "create virtual machine".</strong></p>

<p>
<p align="center"><img src="https://i.imgur.com/G5rgCvc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Now before we create the VM(virtual machine), we will need to create a resource group. At "Resource Group" click the "Create new" underneath the dropdown, and type in a name for it. It can be anything you want, I used "Os-Ticket" for example. Then press "ok"</strong></p>

<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/C5TQuQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Next under "Instance Details" you will type in a name for the virtual machine, I used "OsTicket-VM". Make sure "Reigon" is set to "(US) East US", then go to "Image" and select "Windows 10 Pro, version 22H2 - x64 Gen2" 
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/gYfzSSB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Scroll further down to "Size" and select "Standard_D2s_v3 - 2 vcpus, 8 GiB memory". For the "Administrator Account", create a username, and password, and be sure to write them down somewhere. Don't forget to check the licensing agreement at the bottom. After this, select the "Review + Create" button.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/701GC7d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Make your way back to the home screen and select "Virtual Machines" again, scroll to the right, and copy your VM's "public IP address"
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/7xhwZrQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center"><strong>Next, go to the search bar on your taskbar and search for "remote desktop connection". once you are in, hit the drop-down that says "Show Options", then paste your IP address where it says "computer", use the username from the administrator account you wrote down earlier and hit "OK".
<p>
<p align="center"><strong><img src="https://i.imgur.com/XA2qX5m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>After you hit "OK" you should get a pop-up asking for your password, type in the password you wrote down and hit "OK" again. There will also be another security pop-up, click "Don't show this again", and hit OK.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/sZEWlaW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Now that you are in your virtual machine open Internet Explorer, copy this <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD"> Download File</a> and paste it into the browser, then download the content. Open File Explorer and find the file you downloaded, left-click it, and hit "extract", and "extract all" 
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/JBTMpbM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Now we need to download/enable IIS in Windows. Search for "Control Panel" in the taskbar, and open it. once your in select "Programs", and select "Turn Windows features on or off".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/jRszDjZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center"><strong><img src="https://i.imgur.com/SNjfZM6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Once you open the Window Features, find "Internet Information Services", and click the checkbox. Next, hit the dropdown beside it, find "World Wide Web Services", and hit the drop-down beside that, then hit another dropdown beside "Application Development Features", Find "CGI" and click the checkbox for it, and hit OK.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/e2XRVRr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Close out of the Control Panel, and head back to the unzipped file you downloaded. Double-click it, find PHPmanager, and download it. Then download rewrite_amd as well.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/pyGpN4x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Head back to the file explorer, and find "This PC", click it, then double tap "Windows (C:)". Then create a new folder called "PHP".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/hME4Cfb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>After creating the PHP file, head back to the unzipped OS ticket installation files, and find the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), and extract it into the “C: PHP” folder.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/GF0yQik.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Back in the Os ticket installation folder, find VC_redist.86, and download it. 
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/fr35a2A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>In the same file download the MySQL application as well, when you get to the screen shown below, select "Typical", and install.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/jZgxOVX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>As you continue to set up MySQL, when you get to "configuration type", select "Standard Configuration". When you get to "Security Options", for your password, type in "root". (This password is just for example, if you were applying this for a real company, you would use your password.) Hit next, then execute.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/hDjAjcD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center"><strong><img src="https://i.imgur.com/32jUgM9.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>After you've completed the download, go to the search on the taskbar, search ISS, and run as administrator.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/XQKeV3X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Once you open it, find and open "PHP Manager".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/g9wZXsZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>After opening PHP manager, press "Register new PHP version", press the browse button, then go to your PHP file in your (C:) file, find "php-cgi" and double click it. Then press OK. 
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/MxyV17o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Next we'll restart IIS, under connections, right-click "Osticket-VM", and press "stop". Once it stops, right-click it again, and press "Start".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/snR57g3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Now head back to your OS-ticket installation folder, and find "osTicket v1.15.8", right-click it, and extract it. 
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/IJqgxkc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>After the file finishes extracting, 2 files should appear. Open another file explorer, and go to the (C:) drive, open "inetpub", then open "wwwroot". Look to the other file explorer that opened, and drag "upload" into the "wwwroot" file.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/bnb86kP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Rename the "upload" file to "OsTicket".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/4Z2NGs9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Head back to IIS, and stop and start the server again.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/snR57g3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the left, hit the drop-down on OsTicket, then "sites", then "default website", and press "OsTicket". Look to the right and press "Browse *:80 (HTTP) to open the Os ticket installer.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/TDf9XVd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Look back to IIS, in OSTicket, double click "PHP manager".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/3ytYnmS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Scroll Down to "PHP Extensions", and click “Enable or disable an extension”
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/LB0HnL6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Scroll down the list, right-click and enable: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Go back to the Osticket installer, and refresh the page.

</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/YAer89A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Now open File Explorer and make your way to "include" in the (C:)drive (windows (C:) > inetpub > wwwroot > OsTicket > include), and find "ost-sampleconfig.php" and rename it to "ost-config.php".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/IAXi12r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong> Right-click the file that you just changed and click "properties", another tab will open, click "security" at the top, then click "advanced"
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/UzcOuL3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Click "Disable inheritance", and "Remove all inherited permissions from this object"
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/SMZ0hew.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Now click "add", and for "principle", click it and type in "everyone" (not something you would normally do, this is just for practice.), press "check names", and ok.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/WpNwXV9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Under "Basic Permissions" check the "Full Control" box, and press ok. Then Aplly and ok, and ok again.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/oLY6Xww.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center"><strong><img src="https://i.imgur.com/GgF7v4v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center"><strong><img src="https://i.imgur.com/0fyyywc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Continue with the OsTicket installer and press "continue". Then fill out the signup information, fill it out as you like, as long as you keep track of the emails and passwords for later.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/gnWC34u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Head back to the file explorer, to your OsTicket installation file and install "HeidiSQL_12.3.0.6589_Setup".
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/ykvZWob.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Open HediSQL, click skip, then new, and in the password box, type in "root" from the password you saved earlier and hit open.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/97jwS9w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong> Right-click the "unnamed" dropdown and click "create new". Then click "Database"
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/o55Sllg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>Name the database “osTicket”, and hit ok.

<p align="center"><strong><img src="https://i.imgur.com/Fr19Kd0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
<p align="center"><strong>Head back to Osticket in the browser type in "OsTicket" for "MySQL Database", and "root" for the username and password, and click install.
<p>
<p align="center"><strong><img src="https://i.imgur.com/G9ayMsB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><strong>Congrats! you've installed OsTicket! Now click "Admin Panel" on the side to get to the login page.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/zTfPplS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center"><strong>You made it! Congrats again on successfully downloading OsTicket! You can sign in using the credentials you made before you installed Osticket.
</p>
<br />

<p>
<p align="center"><strong><img src="https://i.imgur.com/0a0IlZ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
