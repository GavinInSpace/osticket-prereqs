<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b>

<h2>List of Prerequisites</h2>

- Enable IIS in windows with CGI/Common HTTP Features/IIS Management Console
- Download/Install PHP
- Download/Install PHP manager for IIS
- Download/Install the Rewrite Module 
- Download/Install the Microsoft Visual C++ Redistributable
- Download/Install MySQL

<h2>Installation Steps</h2>


![image](https://github.com/GavinInSpace/osticket-prereqs/assets/153689700/b335462f-4c52-48c5-ac49-bd64361b7b05)

<p>
  Navigate to the Programs and Features tab inside of the Control Panel and find the "turn windows features on and off" selection. A popup should come up with a list of services and a toggle box to enable or disable them. Scroll to the Internet Information Services tab, enable and expand it. After you expand the tab you should see multiple selections, one being "World Wide Web Services", expand this tab as well and navigate to the Application Development Features and enable CGI. Next find and enable the Common HTTP Features inside the orginal expanded World Wide Web Services tab. Click "Ok". 
  
  ![image](https://github.com/GavinInSpace/osticket-prereqs/assets/153689700/d06605c8-e230-4dd7-b050-151cd9f4d368)

  Once the files are found and activated you should be able to go to your loopback address(127.0.0.1) in a web browser and see the IIS main page, this shows that your web server is working correctly. If you don't see the page show above, repeat this step. Next we have to install the prerequsites for Osticket, namely PHP, PHP Manager, the Microsoft Visual C++ Redistributable, and MySQL.
</p>
<br />

![image](https://github.com/GavinInSpace/osticket-prereqs/assets/153689700/6054894c-f453-48e1-b0bd-b677a05fd819)

<p>
  PHP Manager for IIS can be found at IIS.net, download/install this extension. Next we will download and install the Microsoft Visual C++ Redistributable from the microsoft website. This helps with a special configuration in OsTicket that does something with the URLs(this is admittedly above my understanding but is a prerequisite to install OsTicket).  After PHP manager and Microsoft Redistributable are downloaded we move on to installing PHP from PHP.net. 
</p>
<br />

![image](https://github.com/GavinInSpace/osticket-prereqs/assets/153689700/989e129a-1f99-4c56-be8c-fc4373702219)

<p>
  Installing PHP should be pretty straight forward (it will make later steps easier if you save it to its own file on your (:C) drive) and after its finished we can move on to downloading and installing MySQL which will create a database on your computer(this will help with saving customers/accounts/tickets/etc). This will require creating login credentials for MySQL, make sure not to forget them! After you've installed MySQL and PHP you must register PHP inside of IIS (Internet Information Services).
</p>

  To do this we go to the start menu on our machine and type in IIS in the search bar. Instead of simply clicking IIS we must right click and "run as administrator". Once you've done this you will see PHP manager as well as the rewrite programs we downloaded earlier, navigate to PHP manager. You will see a link labeled "register php version" and once you click it you will be asked to provide the path to the file in which you downloaded PHP. Use the path to PHP.CGI folder that we downloaded earlier. It is good practice to now restart IIS. Once these steps are completed we are finally ready to download OsTicket.

<p>
  
</p>
<br />
