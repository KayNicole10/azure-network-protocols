# azure-network-protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, I observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Command-Line Tools
- Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 
- Ubuntu Server 

<h2>Steps</h2>

- Step 1: Create Windows 10 and Ubuntu Server Virtual Machines 
- Step 2: Download Wireshark 
- Step 3: Analyze ICMP Traffic between the VMs 
- Step 4: Deny and Allow ICMP Traffic from Ubuntu Server 
- Step 5: Analyze SSH Traffic from Ubuntu Server
- Step 6: 
<h2>Actions and Observations</h2>

<h3>Step 1: Create Windows 10 and Ubuntu Server Virtual Machines</h3>

<p>
<img src="https://i.imgur.com/TYs8iQU.png" height="80%" width="80%" alt="Remote Desktop Connection"/>
</p>
<p>
<img src="https://i.imgur.com/5pa9HN3.png" height="80%" width="80%" alt="Windows 10 VM"/>
</p>
<p>
Log into the Azure portal, set up two virtual machines (one running Windows 10 and the other running Ubuntu Server, make sure they are on the same virtual network), and then use Remote Desktop Connection to access the Windows 10 VM.
</p>
<br />

<h3>Step 2: Download Wireshark</h3>

<p>
<img src="https://i.imgur.com/rAzFB2s.png" height="80%" width="80%" alt="Wireshark"/>
</p>
<p>
Within the Windows 10 VM, download <a href="https://www.wireshark.org/download.html">Wireshark</a>
from the internet and select the "Windows x64 Installer" option.
</p>
<br />

<h3>Step 3: Analyze ICMP Traffic between the VMs</h3>
<p>
<img src="https://i.imgur.com/vOrET5I.png" height="80%" width="80%" alt="Private IP"/>
</p>
<p>
<img src="https://i.imgur.com/vE3cs9r.png" height="80%" width="80%" alt="Ping"/>
</p>
<p>
<img src="https://i.imgur.com/M0QR7H6.png" height="80%" width="80%" alt="analyze"/>
</p>
<p>
Copy the private IP address of VM2 (Ubuntu Server), return to VM1 (Windows 10), open PowerShell, and use the ping command to analyze ICMP traffic in Wireshark.
</p>
<br />

<h3>Step 4: Deny and Allow ICMP Traffic from Ubuntu Server</h3>

<p>
Begin by executing the perpetual ping command with the "-t" flag, allowing continuous pinging of VM2 (Ubuntu Server) to observe replies.
</p>
<p>
<img src="https://i.imgur.com/7s0NENO.png" height="80%" width="80%" alt="perpetual ping"/>
</p>
<p>
Next, return to the Azure portal, access the network security groups settings, and navigate to "Inbound Rules." Within this section, add a new rule that specifically denies ICMP traffic originating from VM2 (Ubuntu Server). This addition effectively blocks the perpetual ping operation initiated earlier, halting the continuous flow of replies.
</p>
<p>
<img src="https://i.imgur.com/DDX9VAQ.png" height="80%" width="80%" alt="network security groups"/>
</p>
<p>
<img src="https://i.imgur.com/AWhC9BQ.png" height="80%" width="80%" alt="denies"/>
</p>
<p>
<img src="https://i.imgur.com/v1K6BnH.png" height="80%" width="80%" alt="halt"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
