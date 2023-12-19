<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1 align = "center">Installing and Configuring Active Directory</h1>
This lab demonstrates how to install and configure Active Directory using Azure. We will be using two VMs on Azure that are on the same virtual network. One VM will be installed with Active Directory and configured to be the <b>Domain Controller</b> and other VM will be used as a <b>client</b>. Then, we will configure the Active Directory to allow the Client to join the domain as well as creating user accounts using a Powershell script. 

<br />

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Active Directory Domain Services</li>
  <li>Powershell</li>
  <li>(OPTIONAL) Notepad for writing down usernames and passwords for VMs</li>
</ul>

<br />

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows Server 2022</li>
  <li>Windows 10 Pro (21H2)</li>
</ul>

<br />

<h2>Installation Steps</h2>

<h3>Setting up Resources in Azure</h3>

<p>
  <ul>
