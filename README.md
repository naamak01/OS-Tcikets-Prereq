![OStICKETiMAGE](https://github.com/user-attachments/assets/0cfda3d5-1880-4b05-9f6c-6477908c4cc6)

# osTicket - Prerequisites and Installation

This tutorial provides a detailed overview of the prerequisites and step-by-step instructions for installing the open-source
 help desk ticketing system, osTicket.

## Environments and Technologies Used

* Microsoft Azure (Virtual Machines/Computer)

* Remote Desktop

* Internet Information Services (IIS)

## Operating Systems Used

* Windows 10 November 2021 Update (Version 21H2)

## List of Prerequisites

* IIS (Internet Information Services) W/ CGI

* PHP Manager for IIS

* Microsoft URL Rewrite Module for IIS (x64)

* PHP 7.3.8 Non-Thread Safe (NTS) for Windows (x86)

* Microsoft Visual C++ 2015-2019 Redistributable (x86)

* MySQL Community Server 5.5.62

## Installation Step 1: Setup a Virtual Machine in Azure
![image](https://github.com/user-attachments/assets/3f5b3d2a-61ec-45b3-b8ca-137cd69589f5)

* To create a virtual machine in Azure, navigate to the Virtual Machines section.
* Next, click the "Create" dropdown button, highlighted in blue.
* If you don't have a resource for it, just create by Clicking Resource Group.
*  Next, enter the project details in the resource group and name it "OS-Ticket."

![image](https://github.com/user-attachments/assets/d2ef7871-7804-4506-a8f1-6e79f4062115)

Next, name the VM "OSticket-vm"
Select Location based on where you are located.


![image](https://github.com/user-attachments/assets/3d9716dd-a373-43a6-ac74-96cbfb2aeafe)


Select, the image Windows 10

* Leave the zone as it is

![image](https://github.com/user-attachments/assets/96af12d4-fe8e-46da-a730-da3158b0ce4f)


Select a virtual machine size that includes at least 2 vCPUs to ensure sufficient processing power for your needs.

* CLick next all the way then Review + Create.
* Sometimes clicking Review + Create right away can lead to an Error.


![image](https://github.com/user-attachments/assets/9971b5fb-d069-4f47-b182-edc214d060f8)


Now, review and create Virtual Machine, and notice it states "Deployment in progress".

![image](https://github.com/user-attachments/assets/66206810-195f-4652-821f-a004ab17efe1)

Congratulations! If all allocations are correct, you will have successfully created a virtual machine on your resource page with a valid IP address.

![image](https://github.com/user-attachments/assets/4d639173-04dd-4d4a-a6e8-83e2a7ed8daf)


# Installation Step 2: How to Connect to Remote Desktop and Install the osTicket Requirements.

For windows only. Look up how to Connect to Remote Destop on Googgle or YouTube for Mac.

![image](https://github.com/user-attachments/assets/217532f8-398a-455c-861e-259e3ee329c3)

Open Remote Desktop on your computer, enter the public IP address of the virtual machine previously created on Azure, and press Connect.

Go to Azure, Click on your VM and Copy your Public IP and paste in here to connect
Will then ask for your USERNAME and PASSWORD you used when creating your VM, then Connect.

![image](https://github.com/user-attachments/assets/bc240fc9-1a9f-46a3-b4b5-e86055ea47da)

Once you are on the virtual machine desktop, open Microsoft Edge, and download all required files.

![image](https://github.com/user-attachments/assets/4f8921b3-e3b0-4679-8514-82d8fc14b726)

Utilizing this link, we will install the requirements needed to set up osTicket.

![image](https://github.com/user-attachments/assets/67151884-34bf-4a2e-9564-4176144be283)


# Installation Step 3: How to Install the OS Ticket requirements

![image](https://github.com/user-attachments/assets/1857f2b0-9126-48c5-980a-f5b26ee3f84f)

Once files have been downloaded, navigate to your downloaded file, right click and select extract all.

![image](https://github.com/user-attachments/assets/6a7e525d-a430-4443-8354-8ce0e736b9ca)

Browse the destination folder and nevigate to desktop and press extract.

![image](https://github.com/user-attachments/assets/535f2f30-77a3-4404-8ff8-d7d55037e5c3)

Now, navigate to the Control Panel on your VM, notice the "Programs," section and then choose "Uninstall a program," highlighted in blue underneath "Programs."


![image](https://github.com/user-attachments/assets/b6803002-c075-4618-8967-d5791aed0e99)

In the next window, select "Turn Windows features on or off." Located on the left side of the menu.

![image](https://github.com/user-attachments/assets/2d8ff0f6-8a83-498b-a76b-38fe878f0ef8)

When the "Turn Windows features on or off" window opens, expand "Internet Information Services."

![image](https://github.com/user-attachments/assets/62ff1e1e-df6a-470b-ab36-3e16926fcaad)

Expand "Application Development Features," select "CGI," press "OK," and allow the system to update."

![image](https://github.com/user-attachments/assets/9e488c50-d829-4e35-8ec0-f4dca0da7378)

From your desktop, open the file folder that was downloaded.

![image](https://github.com/user-attachments/assets/eeff0f87-0bff-4ed5-bc95-208fa80a6b1d)

Then type in your local browser Example Explorer 127.0.0.1 which is your local host to see if it loads properly.

![image](https://github.com/user-attachments/assets/609a29eb-0924-475e-a0a9-9fcd6a9599ab)

Then go into your extracted OSTicket Folder and Install The PHP Manager

![image](https://github.com/user-attachments/assets/61cb543c-d062-4445-8fb6-50aaf93fb98c)

Say yes to everything and then Install. Ones Installed, hit close

Then Install Rewrite also in the OSTicket Folder

![image](https://github.com/user-attachments/assets/9f2bbbd1-e990-4ec4-8457-023370fe1a59)

Then Create the directory C:\PHP
![image](https://github.com/user-attachments/assets/87f381c6-199f-4c96-8b2c-f5135967558d)

Once these files are downloaded, open File Explorer, navigate to the C: drive, create a new folder, and name it "PHP."

![image](https://github.com/user-attachments/assets/479987c3-414f-4b38-ba86-112d68c762b5)

Extract the files from the zipped PHP file and move them into the newly created PHP folder in the C: drive.

![image](https://github.com/user-attachments/assets/fa9e7971-a0be-431b-b743-9bad071282c5)

Next Go to OSTicket Folder and Install CV

![image](https://github.com/user-attachments/assets/be4b8cd3-4c50-46e6-a442-0f6cdf2a159d)

Ones it displays Successful, Install MySQL.

OSTicket will use MySQL  which is a database system to store user information and other info relating to our work in the ticket
system.

![image](https://github.com/user-attachments/assets/5b94259d-0183-4de9-b907-d3436ef2fca2)


Once that is complete, install MySQL.

![image](https://github.com/user-attachments/assets/6cd3cd7d-1731-4da6-92a9-de2c2cb11697)

Once MySQL is downloaded, select the standard configuration.

Next, create a root password for the user.

![image](https://github.com/user-attachments/assets/8bbd647e-bada-4001-8200-0a3bbaa882bf)

Open Windows and run IIS Manager as an administrator.

![image](https://github.com/user-attachments/assets/32050c64-7b33-43b4-8bfe-391f35196f06)

Once IIS manager is open navigate to PHP manager.

![image](https://github.com/user-attachments/assets/f72223f4-4490-427d-bb2b-eb6ca7909336)

Register new PHP.

nAVIGATE TO THE php folder in C drive and click the Executable file

![image](https://github.com/user-attachments/assets/ea3de13d-8147-471b-b968-c2a53b5e9ef1)


Click Here: You will notice a pop-up menu to the right with Restart, Start and Steop

![image](https://github.com/user-attachments/assets/d84d133e-72d6-445b-a331-ce7b69f7e170)

![image](https://github.com/user-attachments/assets/79d4a24a-0a95-424c-813d-5c00f03f5e01)

Reload IIS (Open IIS, Stop and Start the server)
In IIS Manager, navigate to the Connections tab and select the "Default Web Site."

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

![image](https://github.com/user-attachments/assets/077f91ce-4686-4e42-bf22-b73d63805df9)

![image](https://github.com/user-attachments/assets/15329fe3-758b-40ff-aa41-122da82ee2b4)

![image](https://github.com/user-attachments/assets/8f2f1640-72be-4372-aa49-2498238c07c1)

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

NOTE: IF IS TICKET DOES NOT SHOW THE DEFAULT WEB SITE: REFRESH IT 

![image](https://github.com/user-attachments/assets/2925023c-a92f-4974-822e-26ac536a4ae6)

Now, on the right-hand tab under "Manage folder," select "Browse *80 (HTTP)."

If everything is correct so far, it should take you to the osTicket installer.

![image](https://github.com/user-attachments/assets/98cc5a5f-1728-418c-b600-b095baf5cd45)

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager

![image](https://github.com/user-attachments/assets/da880a4e-5444-4e69-a642-938daa2e1d2a)

![image](https://github.com/user-attachments/assets/508b1694-6dc0-4bab-b411-65b4414f17f9)


Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll

![image](https://github.com/user-attachments/assets/4b5f981d-1989-4329-ba16-97bb1f2fa1a4)

Refresh the osTicket site in your browser, observe the changes

Additional Extensions enabled

![image](https://github.com/user-attachments/assets/676a78b8-9491-4596-8539-6b8243d04662)


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

On your Windows C drive, navigate to inetpub > wwwroot > osTicket > include.

![image](https://github.com/user-attachments/assets/5382291a-0ac1-4de6-97f9-c2afafd7f3ce)

Navigate down to the file named ost-sampleconfig.php

![image](https://github.com/user-attachments/assets/88a14e83-47ef-4b4b-b759-987de3220b4d)

change this to ost-config.php.

Right Click and select Rename


![image](https://github.com/user-attachments/assets/4b28cefe-3551-4e57-8f31-2839cf1fc50f)

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

Next, right click on folder and open properties.

![image](https://github.com/user-attachments/assets/62556abd-9768-42dd-aeee-b30dab22943d)

Select SECURITY

![image](https://github.com/user-attachments/assets/d460caaf-d08d-49d7-ab44-64fc51adc96d)

Then Aadvance

Then Disable Inheritance or current permissions away

![image](https://github.com/user-attachments/assets/19b46c2d-e48e-47cd-98cc-9acf68ee7a53)

Select, remove all inherited permissions from this object.


## Step 3: Now we will add permissions to allow all users access.

![image](https://github.com/user-attachments/assets/ee20a336-1077-46c3-a60c-b2c16688dff0)

Select Add, Located above enable inheritance

Then select Principles

![image](https://github.com/user-attachments/assets/ed5c29cf-5c46-4807-8881-b837b6cf8789)

Then type in EVeryone: 
 * NOTE: DO NOT TYPE IN EVERYONE IN REAL LIFE. ONLY TYPE IN THE USER WHO CAN HAVE ACCESS TO IT

![image](https://github.com/user-attachments/assets/3aaa1469-906e-4518-b78b-a257c59dfc3a)

Click Check Names to the Right and then OK

![image](https://github.com/user-attachments/assets/cac7691d-2f2c-43ac-bd53-af0e8ca8168d)


Then Check Full Control and then Ok

![image](https://github.com/user-attachments/assets/8bb9499b-9bda-4fd3-ae08-388ff076c107)


sHOULD LOOK LIKE THIS

![image](https://github.com/user-attachments/assets/dbda0b41-e645-42f9-be5b-fff13afd1d45)

Notice, that the permissions to allow all users access has now been added.

cLICK ON Everyone, Apply and OK

![image](https://github.com/user-attachments/assets/eceaaf70-1987-472f-836f-16bb3a74f2ca)


Then go back to OS Ticket on the Website and Select Continue

![image](https://github.com/user-attachments/assets/7d4f23ba-4e90-4777-8370-6aba88b3c23b)

Now that we have changed the settings, the osTicket extensions are enabled. The ones that are not enabled at this point are not needed at this time.

Then fill out all the info requested Here and Below

![image](https://github.com/user-attachments/assets/6a31fed4-8960-489b-bae3-9e9411d61b27)

NEXT: Go into OS Ticket installation folder to create a user login for the MySQL

* NOTE: Leave the OS Ticket installation. Do not click install now Until done with setting up MySQL

![image](https://github.com/user-attachments/assets/3dccbe52-ac41-4d27-9465-e0e64146cbda)


## Step 4: Installation configuration of OS Ticket

Click on HeidiSQL to Install:

* From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL

![image](https://github.com/user-attachments/assets/91cb41e2-f282-45b7-8b21-f5bc2b065c8c)

Next, until it is done installing. 

![image](https://github.com/user-attachments/assets/2ab8093e-b715-4689-9411-6ffc1d714cd1)

Make sure Launch HeidiSQL is check before clicking finished

![image](https://github.com/user-attachments/assets/d5fdd527-5353-4397-b137-9d4f0ba346db)

Then Skip 














