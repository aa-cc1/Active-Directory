#
<p align="center">
<img src="active directory.png"/>
</p>

<h1>On-premises Active Directory Deployed in Azure </h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022

<h2>Steps Taken</h2>

- Create two VMs (Domain Controller on the server / Windows 10)
- Ensure Connectivity between both VMs
- Install Active Directory (AD)
- Create Administrator and User Account
- Login with Admin/User Account to verify setup

<h2>Actions and Observations</h2>

<p>
Within AZure, create a Resource Group (RG) that has two Virtual Machines (VMs) on the same network, or Virtual Netowrk (vNet).        
<img src="Resources.png"/>

    
***Client-1*** is running Windows 10 and the ***Domain Controller*** is running Windows Server 2022, where its iP address is set to static.    
<img src="DC Static IP.png"/>


To confirm that both VMs on the same network, view the _topology_ in Network Watcher. 
<img src="vNET Topology.png"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We need to ensure that there is connectivity between the Client and Domain Controller, by iniating a ping request. If the ping request timed-out check the Indbound Rules for the Domain Controller Firewall to see if ICMP requests are enabled.
  
</p>  




