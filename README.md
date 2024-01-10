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
Go to Microsoft Evalcenter for Windows Server 2022 and Download the ISO file. Download the ISO in 64 bits in English. And then follow the steps below. <br/>
<br />
<br />
 Create a new virtual machine <br/>
<img src="https://i.imgur.com/LCtbzdp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
             <br/>
<img src="https://i.imgur.com/n41HWQK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://i.imgur.com/HbPNcSX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <br/>
<img src="https://i.imgur.com/uIdQ6cH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
           <br/>
<img src="https://i.imgur.com/zJpd5Nc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
           <br />
<img src="https://i.imgur.com/nTHp01d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br />
  <br/> Go to the VM properties. In the Network tab, change the configuration to use internal network: GREEN
 
<img src="https://i.imgur.com/uOTBJhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Launch the VM: It will ask you which ISO, load the Windows Server one. <br/>

<br />

<br />
 Select the English language to install. The other settings can be adjusted with your favorite configuration but the Windows must be installed in English.                   <br/>
 
<img src="https://i.imgur.com/re2PbNx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
 Select "install now." Select "Windows Server 2022 Datacenter Evaluation (Desktop Experience)". For a lab, the GUI can be usefull if you start a fresh career in IT.           <br/>
 
<img src="https://i.imgur.com/ZPrb0AI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
      Accept software license and select custom install.       <br/>
       
<img src="https://i.imgur.com/iDurh47.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
      Select the only drive mount and click "next"                    <br/>

<img src="https://i.imgur.com/DXf9Mho.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />

<br />
  Wait until the installation is complete and the system reboots itself. Set your password (remember it's a lab, you can have a weak password)   <br/>
<img src="https://i.imgur.com/TWVRyJa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<br />
Connect to your administrator account. Go to "Open Network & Internet Settings." Change adapter options. Select your card properties. Go to "Internet Protocol Version 4" Properties. Assign IP. Try to join the gateway. (so your LAN INTERFACE in pfsense) Rename the server with an easy name to remember/use.   <br/>
<img src="https://i.imgur.com/fsARCiF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />

<br />

<br />
                  <br/>
<img src="https://i.imgur.com/ekAi53u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
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
