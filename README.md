#
<p align="center">
<img src="active directory.png"/>
</p>

<h1>On-premises Active Directory Deployed in Azure </h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell
<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022

<h2>Key Objectives</h2>

- Create two VMs (Domain Controller on the server / Windows 10)
- Ensure Connectivity between both VMs
- Install Active Directory (AD)
- Create an Administrator and User Accounts
- Login with Admin/User Account to verify setup

<h2>Actions and Observations</h2>



**1.** Within AZure, create a Resource Group (RG) that has two Virtual Machines (VMs) on the same network, or Virtual Netowrk (vNet). To confirm that both VMs on the same network, view the _topology_ in Network Watcher.        
<img src="Resources.png"/>

    
**2.** ***Client-1*** is running Windows 10 and the ***Domain Controller*** is running Windows Server 2022, where its iP address is set to static.    
<img src="DC Static IP.png"/>


**3.** Ensure that there is _connectivity_ between the Client and Domain Controller. Remote Desktop into Client-1 and iniate a ping request to the Domain Controller.  If the ping **_request timed-out_** check the Indbound Rules for the Domain Controller Firewall to see if ICMP requests are enabled.    

<img src="PP to DC.png"/> <img src="ICMPallow.png"/>



    




