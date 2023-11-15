# Active-Directory

We are going to continue the configuration of the Active Directory from our last post. 

# Process

First We need to create our machine, in this case, Windows Server 2019 64-bit, and click on the default configurations, we will add the ISO image once we start the server, before starting the server, click on Settings >  System > Processor and give it 4, this will stabilize the whole process. 

![processor](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/e81a1f92-798c-445b-8c2a-f44d4d675610)


![ISO FILE](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/78e7aa36-8f1e-41e8-8f1b-a23c547012f2)

Select the ISO file from your host and click on “mount and retry boot”, this will start the installation of Windows 2019. Select your language and right after, you need to select the OS that you want to install, choose the (Data Center Evaluation - Desktop Experience x64) otherwise the GUI will not be habilitated. 

![gui](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/03389e34-061b-41ba-8029-77ef9db10afa)

 
Type of installation, choose the Custom one and click on Next. The installation process could take a while, that will depend on your workstation. 

![passwdr](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/385862b0-1cbf-482a-b9e2-04d9c73b4380)

Set up an administrator password, and click next. Before you gain access to the desktop, you will not be able to use the keyboard, instead click on: Input > Keyboard > Press Ctrl+Alt+Delete. Enter your Administrator password. 

By default, the Server Manager will open, from here we are going to be able to create and delete groups and users, domains, servers, etc.

![manager](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/101bb077-f426-4c53-ba54-c6be3bd4c31c)

Now we are going to add Servers, click on: Add Role and Features Wizard, select Next, and then select DNS, DHCP, and Active Directory Domain Services. Note that before adding DNS and DHCP, we need to give a static IP address to our server.  

![roles](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/3e4b5edb-9de9-4f1e-bea4-2fb485267884)

Open Network & Internet Settings > Network and Sharing Center > Ethernet Properties > IPv4 and then we will assign the IP address, mask, default gateway, and a DNS.

![Network settings](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/a07bb764-0575-456e-b5fa-63dd23d0fd1e)

We will share the default gateway to give it access to the network, and the Google DNS. If we looking to isolate our server from the internet, we will assign the same IP address as a DNS server, and not assign any default gateway, also from the setting of the network, we swap from “NAT to Internal Network” 

In the top right, there is a flag asking us to create a new Domain, so we will click: Create a new Domain (homelab.com), click next and next. The Server will reboot to install the features. 

![Domain](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/975737c4-b92c-4cc9-911e-0c0cdd30833a)

Once you log in again, go to the top right and click on Tools >  Users and Computers. From there you can manage users, and groups, remove and give access.

![group,folder](https://github.com/Wfrestrepo/Active-Directory/assets/108705302/3ee9b7e9-89e1-4e5d-b671-a28f815aef2b)






