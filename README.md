<p align="center">
<img width="425" height="118" alt="image" src="https://github.com/user-attachments/assets/3d59a31a-f01e-4a68-8656-a72b6ea2c877" />
</p>

<h1>Observe ICMP Traffic</h1>
In this tutorial we are going to verify the Internet Control Message Protocol (ICMP). ICMP is a network layer protocoal used by network devices to diagnose network communication issues. ICMP is mainly used to determine whether or not data is reaching its intended destination.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Open Remote Desktop Connection 
- Download Wireshark
- Retrieve private IP from Linux (Ubuntu)
- Step 4

<h2>Use Remote Desktop Connection to connect to your Windows 10 Virtual Machine</h2>
Get the public IP address from Azure and open RDC, and login using the credentials that you have previously created.
<p align left>
<img width="305" height="183" alt="image" src="https://github.com/user-attachments/assets/2f611a79-1687-4e76-83de-4c1193d1c8f2" />
<p align left>
<img width="470" height="164" alt="Screenshot 2025-11-25 154958" src="https://github.com/user-attachments/assets/c6a50807-e9d1-46a8-90a9-80cbe3e7b831" />
<p align left>
<img width="335" height="240" alt="image" src="https://github.com/user-attachments/assets/f80710c9-34a5-410f-9bc9-aebef3e7917d" />

When attempting to log into Windows 10 Virtual Machine, you will get this message click yes to continue

<p aling left>
<img width="292" height="307" alt="Screenshot 2025-11-25 161013" src="https://github.com/user-attachments/assets/5f6be25c-d47a-4295-9521-2e24875825d4" />

<h2>Downloading Wireshark in Windows server 2022</h2>
Once connection has been established, you can go to Microsoft Edge and download Wireshark which is the protocol analyzer AKA packet sniffer that will let us see all the activity that is happening on our network inferface or the network traffic.

<p aling left>
<img width="1916" height="1080" alt="image" src="https://github.com/user-attachments/assets/7e714978-98a0-43bb-af11-2af4af8bc342" />

When downloading Wireshark from the website, choose Windows x64 Installer and when the download is complete click on open folder and follow the prompts to install Wireshark
<p aling left>
<img width="500" height="209" alt="Screenshot 2025-11-25 163936" src="https://github.com/user-attachments/assets/a1a1263e-18f3-4af2-b2a8-caa1b6c7ae6f" />

Once the installation is completed, click on Start and look for Wireshark App, run as administrator to start seeing all the traffic
<p align left>
<img width="230" height="289" alt="image" src="https://github.com/user-attachments/assets/a4f11193-4687-4548-9671-0f82effc4537" />

Click on Ethernet, then click on the little shark tail on the upper left corner and you will be able to see all the network traffic happening on the backend of this computer

<p align left>
<img width="506" height="358" alt="Screenshot 2025-11-25 165036" src="https://github.com/user-attachments/assets/20805441-b045-4238-96f3-5228e2cd993f" />
<p align left>
<img width="506" height="265" alt="image" src="https://github.com/user-attachments/assets/3f37f7bd-fb62-42e5-95a8-461e71413787" />

To filter ICMP traffic in Wireshark, you have to click on the search bar and type: icmp and press enter, then you will be able to see the icmp filter traffic.

<p align left>
<img width="506" height="189" alt="Screenshot 2025-11-25 170858" src="https://github.com/user-attachments/assets/b1aa8ae2-a742-4da5-ade3-bb70a5758bd6" />

<h2> Retrieve private IP address for Linux Virtual Machine (Ubuntu)</h2>
Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM
Observe ping requests and replies within WireShark

<p align left>
<img width="254" height="276" alt="Screenshot 2025-11-25 172401" src="https://github.com/user-attachments/assets/54258dff-90ea-43a6-b119-919b16a869d3" />

Within our Windows Virtual Machine, open PowerShell as administrator

<p align left>
<img width="203" height="160" alt="image" src="https://github.com/user-attachments/assets/8e07727a-e58b-4e45-b1cf-6be042587311" />
<p align left>
<img width="375" height="182" alt="image" src="https://github.com/user-attachments/assets/6946107a-d141-46ac-abd2-501d0e9d0848" />

Using Powershell from our Windows Virtual Machine we are going to ping our Linux Virtual Machine 

<p align left>
<img width="503" height="362" alt="image" src="https://github.com/user-attachments/assets/37db95d1-3e8a-47f5-804e-d6b5353aa2bc" />

From Wireshark we can also check the ICMP traffic 

<p align left>
<img width="503" height="211" alt="image" src="https://github.com/user-attachments/assets/ff740988-bb3d-462f-9182-f1d9db972bf4" />

</p>
<br /># azure-network-protocols
