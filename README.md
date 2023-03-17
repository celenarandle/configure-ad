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
<img src="https://i.imgur.com/rNObYhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After having installed Active Directory and promoted the server to Domain Controller, the domain can be named.
</p>
<br />

<p>
<img src="https://i.imgur.com/mM5DHVm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At this point, Organizational Units and Groups may be created in order to group Users into. Users themselves may be added as well.
</p>
<br />

<p>
<img src="https://i.imgur.com/4fU7121.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
A script was run in Powershell ISE here in order to add a very large number of employees at once. Once those users were added, Active Directory can then be used for all types of functions, such as changing passwords, adding Users to Groups, Organizational Units, disabling Users, etc.
</p>
<br />
