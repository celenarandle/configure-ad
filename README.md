<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Establish Domain Controller
- Install Active Directory
- Create Domain
- Add Users and Computers to Active Directory

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/bFa9zZ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I. In order to get started, both a Domain Controller (DC) and a Client Virtual Machine need to be created and connected to the same Vnet. Set the DC's Network Interface Card (NIC) to Static (in Azure, go to the correct VM>Networking>IP Configuration>click IP>change Assignment to 'Static').
</p>
<br />

<p>
<img src="https://i.imgur.com/1RDm5IR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
II. Enable ICMPv4 on the Firewall. From the Search bar at the bottom of the DC, open 'mf.msc'>Inbound Rules>click to sort by 'Protocol'>find ICMPv4>enable both rules.
</p>
<br />

<p>
<img src="https://i.imgur.com/UILe0ZS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
III. Log into the DC and install Active Directory by clicking 'Add Roles and Features' from the Server Manager>click 'Next' until 'Active Directory Domain Services' is available, choose and install.
</p>
<br />

<p>
<img src="https://i.imgur.com/XliuFwL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
IV. Promote server to an actual domain controller by clicking the flag in the right-hand corner and choosing 'Promote this server to a domain controller'.
</p>
<br />

<p>
<img src="https://i.imgur.com/rNObYhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
V. After having installed Active Directory and promoted the server to Domain Controller, the domain can be named by choosing 'Add a new forest'>name the domain>create a password>click 'Next' until able to install>system will restart>log back in as 'domainname\username' (ex: mydomain.com\celena).
</p>
<br />

<p>
<img src="https://i.imgur.com/mM5DHVm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VI. From this point, Active Directory is able to be used to create Organizational Units, Groups, and so much more!
</p>
<br />

<p>
<img src="https://i.imgur.com/4fU7121.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VII. Here, a script was run in Powershell ISE in order to add thousands of employees at once. Once Users added, Active Directory can then be used for all types of functions such as changing passwords, adding Users to Groups, Organizational Units, disabling Users, etc. Active Directory is your oyster!
</p>
<br />
