<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1 align = "center">Installing and Configuring Active Directory</h1>
This Lab demonstrates how to install and configure Active Directory using Azure. We will be using two virtual machines on Azure that are on the same virtual network. One virtual machine will be installed with Active Directory and configured to be the Domain Controller and other virtual machine will be used as a Client. Then, we will configure the Active Directory to allow the Client to join the domain as well as creating user accounts using a Powershell script. 

<br />

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Active Directory Domain Services</li>
  <li>Powershell</li>
  <li>Notepad (Optional): for writing down usernames and passwords for virtual machines</li>
</ul>

<br />

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows Server 2022</li>
  <li>Windows 10 Pro (21H2)</li>
</ul>

<br />


<h2>Installation Steps</h2>

<h3>Creating Resources in Azure</h3>

<p>
  <ul>
</p>
Go to Azure Portal, create a virtual machine for the Domain Controller, name it DC-1
</p>
<img src="https://i.imgur.com/mz8HuAI.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
Create a second virtual machine and name it Client-1, the vms should be on the same virtual networks. Give the resources some time to load, approximately five to ten minutes
<p>
<img src="https://i.imgur.com/dBKmM5w.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
Go to DC-1 click on Networking under Setttings, click on the Network Interface link. Go to IP configurations under Settings. Click on ipconfig link to open up a window, change the IP Configuration to Static under Allocation
<p>
It being dynamic will make it difficult for the vm to communicate with our client vm
<p>
<img src="https://i.imgur.com/7RszLbd.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<p>
</p>
</ul>

<br />

<h3>Ensuring Connectivity</h3>

<p>
<ul>
<p>
Connect to Remote Desktop with Client-1 public ip address. Open command prompt and enter the command ping -t [DC-1 private ip address]. To send endless ping in order ensure reachability with the Domain Controller. Connection should time out after the first ping due to the Domain Controller's Firewall Settings.
<p>
<img src="https://i.imgur.com/SQyRnqp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<p>
Log into DC-1 vm, click start and open wf.msc in search bar to open windows defender firewall and advanced security. Go to Inbound Rules and enable the rules under the protocol ICMPv4, specifically Core Networking Diagnostics - ICMP Echo Request (ICMPv4-In)
<p>
<img src="https://i.imgur.com/ZtDs3kS.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<p>
Go to Client-1 vm and you should be able to see replies. Enter Ctrl C to end traffic
<p>
<img src="https://i.imgur.com/3DsTP8X.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
</p>

<br />

<h3>Installing Active Directory on the Domain Controller</h3>

<p>
In DC-1, go to the Server Manager Dashboard and click on Add Roles and Features. Go through the installation process, at Server Roles check the box for Active Directory Domain Services
<p>
<img src="https://i.imgur.com/wXo6MHZ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
