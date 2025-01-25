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




