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

![image](https://github.com/user-attachments/assets/8bbd647e-bada-4001-8200-0a3bbaa882bf)

Next, create a root password for the user.











