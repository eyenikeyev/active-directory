<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1 align = "center">Installing and Configuring Active Directory</h1>
This Lab demonstrates how to install and configure Active Directory using Azure. We will be using two virtual machines on Azure that are on the same virtual network. One virtual machine will be installed with Active Directory and configured to be the <b>Domain Controller</b> and other virtual machine will be used as a <b>Client</b>. Then, we will configure the Active Directory to allow the Client to join the domain as well as creating user accounts using a Powershell script. 

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
Go to Azure Portal, create a virtual machine for the Domain Controller, name it DC-1. Create a second virtual machine and name it Client-1, the vms should be on the same virtual networks. Give the resources some time to load, approximately five to ten minutes.
</p>
<p>
