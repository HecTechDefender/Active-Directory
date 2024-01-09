<h1>Building a SOC Home Lab</h1>

 ### 

<h2>Description</h2>
In this project, I'm on a mission to build a SOC home lab! This project will cover pfSense, Active Directory, Windows Workstation, Sysmon and CrowdSec. My goal? Creating a space where I can experiment and learn the ropes of real-world cybersecurity from the comfort of my home! 
<br />


<h2>Utilities Used</h2>

- <b>pfSense</b>
- <b>Active Directory</b>
- <b>Windows Workstation</b>
- <b>Sysmon</b>
- <b>CrowdSec</b>


<h2>Environments Used </h2>

- <b>Windows 10</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Go to Microsoft Evalcenter for Windows Server 2022 and Download the ISO file. Download the ISO in 64 bits in English. <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection: <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to the VM properties. In Network tab, activate 3 adapters. Making note of the MAC Addresses of each adapters will be useful for future actions. This will be the RED CARD. (external network) <br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br />
  <br/> This will be the GREEN CARD (internal network)
 
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />
This will be the ORANGE CARD (DMZ) <br/>

<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
 Launch the VM. It will ask you which ISO Virtualbox must mount on the VM, load the pfsense one. <br/>
 
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
 Install and accept the Copyright and Trademark Notices.     <br/>
 
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
       Select "install"       <br/>
       
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
 -Select your keymap
-Use the default partition (we're in a lab, we just need a firewall)
-Proceed with installation (no miror, no encrypt, nothing)
-Wait until the installation is complete   <br/>

<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />

<br />
        Do not load manual configuration    <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<br />
        Reboot on the new system   <br/>
<br />

<br />

<br />
        Now, the server is powered on with the new system. Select 1 to configure interfaces.  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br /> 
<br />


<br />



<br />
 We can see the MAC Addresses. Remember, we recommended to make a note of the MAC addresses. It is always helpful to have/know them. Select the RED INTERFACE for WAN. Select the GREEN INTERFACE for LAN. Select the last one (ORANGE) for DMZ. <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br /> 
<br />
<br />
<br /> Confirm         <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<br />

<br />
<br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />Select 2 to configure the IP address. 
 Leave the WAN interface as DHCP. 
 Select 2 to change the LAN interface. 
 Asssign the IP and subnet you want, the gateway must be none.<br/> <br /> 
<br />
