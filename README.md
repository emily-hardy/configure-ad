<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in Azure</h1>
<i>In this project, I implement on-premesis Active Directory using Azure Virtual Machines. You'll see an initial "labuser" account created to set up the virtual machines, a "Fred_Admin" account created to represent an employee with Administrator permissions, and a "Joan_User" to represent a general employee account. </i>
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Configuration Steps</h2>

1. Create 2 virtual machines in Azure to act as the domain controller and client
2. Deploy Active Directory within the Domain Controller to create a domain
3. Configure the static IP address within the virtual machines
4. Create and assign new security groups and users within the Active Directory

<h2>Deployment and Configuration Steps</h2>
<br />

<p>-Creating the virtual machines in Azure, one Windows 10 and one Windows Server:</p>
<a href="https://imgur.com/uxu1P0Y"><img src="https://i.imgur.com/uxu1P0Y.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Setting the private IP Address on the Server to static (10.0.0.4):</p>
<a href="https://imgur.com/4nZmDK3"><img src="https://i.imgur.com/4nZmDK3.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Manually changing Client 1's IP Address to match the static private IP Address of the Domain Controller:</p>
<a href="https://imgur.com/XqF09e4"><img src="https://i.imgur.com/XqF09e4.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Logging in to the Server as "labuser" and deploying Active Directory to create the Domain Controller:</p>
<a href="https://imgur.com/4FakV03"><img src="https://i.imgur.com/4FakV03.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/9ZVplAO"><img src="https://i.imgur.com/9ZVplAO.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Changing inbound traffic rules to allow all ICMP traffic:</p>
<a href="https://imgur.com/dgsxI22"><img src="https://i.imgur.com/dgsxI22.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Logging in to Client 1 as labuser to join it to the Domain Controller's network:</p>
<a href="https://imgur.com/BDOUkcH"><img src="https://i.imgur.com/BDOUkcH.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Logging back into the DC and adding organizational units to exampledomain.com called "_Admins" and "_Employees":</p>
<a href="https://imgur.com/FfsF6Wh"><img src="https://i.imgur.com/FfsF6Wh.png" title="source: imgur.com" /></a>

<p>-Creating "Fred Rogers" under "_ADMINS" and assigning the account to the "Domain Admins" security group:</p>
<a href="https://imgur.com/6TqsYoW"><img src="https://i.imgur.com/6TqsYoW.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Successfully logging back into the DC as Fred_Admin and creating a new user under "_Employees" called Joan Cusack:</p>
<a href="https://imgur.com/4XpG1gd"><img src="https://i.imgur.com/4XpG1gd.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/dDqOVCz"><img src="https://i.imgur.com/dDqOVCz.png" title="source: imgur.com" /></a>
<br />
<br />
<br />
<p>-Logging out of DC-1 as Fred_Admin and testing the new login for Joan_User on Client 1, confirming it is active and on the same network:</p>
<a href="https://imgur.com/tyhfcDo"><img src="https://i.imgur.com/tyhfcDo.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/idfsfId"><img src="https://i.imgur.com/idfsfId.png" title="source: imgur.com" /></a>
<br />
<br />
