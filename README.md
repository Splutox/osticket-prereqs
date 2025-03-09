<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation Guide</h1>
An easy to follow tutorial on the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Files To Download</h2>

- FILE EXAMPLE

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Instructions</h2>
<p align="center"><strong>Start by creating a free (or paid) <a href="https://azure.microsoft.com/en-us/free/"> Microsoft Azure Subscription</a>. Once logged in, find and open the "Virtual Machines" service, and click the "create" button, and then "create virtual machine".</strong></p>

<p>
<img src="https://i.imgur.com/G5rgCvc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align= "center">Now before we create the VM(virtual machine), we will need to create a resource group. At "Resource Group" click the "Create new" underneath the dropdown, and type in a name for it. It can be anything you want, I used "Os-Ticket" for example. Then press "ok"</strong></p>

<br />

<p>
<img src="https://i.imgur.com/C5TQuQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next under "Instance Details" you will type in a name for the virtual machine, I used "OsTicket-VM". Make sure "Reigon" is set to "(US) East US", then go to "Image" and select "Windows 10 Pro, version 22H2 - x64 Gen2" 
</p>
<br />

<p>
<img src="https://i.imgur.com/vpNAdOO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Scroll further down to "Size" and select "Standard_D2s_v3 - 2 vcpus, 8 GiB memory". For the "Administrator Account", create a username, and password, and be sure to write them down somewhere. Don't forget to check the licencing agreement at the bottom. After this, select the "Review + create" button.
</p>
<br />

<p>
<img src="https://i.imgur.com/p4iONMX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make your way back to the home screen and select "Virtual Machines" again, scroll to the right and copy your VM's "public IP address"
</p>
<br />

<p>
<img src="https://i.imgur.com/7xhwZrQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Next, go to the search bar on your taskbar and search for "remote desktop connection". once your in, hit the drop down that says "Show Options", then paste your IP adress where it says "computer", and use the username from the admministrator account you wrote down earlier, and hit "OK".
<p>
<img src="https://i.imgur.com/XA2qX5m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After you hit "OK" you should get a pop-up asking for your password, just type in the password you wrote down, and hit "OK" again. Their will also be another security pop-up, just click don't show this again, and hit OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/aG8svGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now that your in your virtual machine open the internet explorer, copy this <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD"> Download File</a> and paste it into the browser, then download the content. Open file explorer and find the fie you downloaded, left click it and hit "extract", and "extract all" 
</p>
<br />

<p>
<img src="https://i.imgur.com/JBTMpbM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we need to download/enable IIS in Windows. Search for "Control Panel" in the taskbar, and open it. once your in select "Programs", and select "Turn Windows features on or off".
</p>
<br />

<p>
<img src="https://i.imgur.com/jRszDjZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/SNjfZM6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Once you open the Window Features, find "Internet Infromation Services", click the checkbox. Next, hit the dropdown beside it, and find "World Wide Web Services", and hit the drop down beside that, then hit another dropdown beside "Application Development Features", Find "CGI" and click the checkbox for it, and hit OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/yKEOjXr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Close out of the Control Panel, and head back to the unzipped file you downloaded. Double click it and find PHPmanager and download it. Then download rewrite_amd aswell.
</p>
<br />

<p>
<img src="https://i.imgur.com/pyGpN4x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Head back to the file explorer, and find "This PC", click it, then double tap "Windows (C:)". Then create a new folder called "PHP".
</p>
<br />

<p>
<img src="https://i.imgur.com/fbXIJbl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After creating the PHP file, head back to the unzipped OS ticket installation files, and find the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), and extract it into the “C:PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/GF0yQik.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Back in the Os ticket installation folder, find VC_redist.86, and download it. 
</p>
<br />

<p>
<img src="https://i.imgur.com/fr35a2A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the same file download the mysql application aswell, when you get to the screen shown below, select "Typical", and install.
</p>
<br />

<p>
<img src="https://i.imgur.com/6y85udt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

As you continue to set up MySQL, when you get to "configuration type", select "Standard Configuration". When you get to "Security Options", for the password, type in "root". (This password is just for example, if you were accually doing this, you would use your own password.) Hit next, then execute.
</p>
<br />

<p>
<img src="https://i.imgur.com/hDjAjcD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/32jUgM9.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

TEXT
</p>
<br />

<p>
<img src="https://i.imgur.com/9NyitcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
TEXT
</p>
<br />
