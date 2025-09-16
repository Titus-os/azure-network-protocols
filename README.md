<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Virtual Machines(Linux/Windows 10 Pro)
- Install Wireshark on the Windows 10 VM and Filter for ICMP Traffic  
- Use SSH From Windows machine to connect to Linux VM
- Observe DNS Traffic using nslookup from the Windows 10 VM/Wireshark



<h2>Actions and Observations</h2>

<p>
<img width="911" height="174" alt="image" src="https://github.com/user-attachments/assets/2af991be-514a-4e55-8769-99e0e9dfe677" />
<img width="996" height="221" alt="image" src="https://github.com/user-attachments/assets/eb9f3e8b-4989-40b2-90ac-e2fe17ee94cc" />


</p>
<p>
Creating a resource group and deploying a Windows 10 VM and an Ubuntu VM in the same virtual network (VNet) and subnet is critical because it establishes the cloud infrastructure for the lab. Ensuring both VMs share the same VNet/subnet enables direct communication (e.g., via private IPs), which is essential for testing network protocols like ICMP and SSH.
</p>
<br />

<p>
<img width="1906" height="479" alt="image" src="https://github.com/user-attachments/assets/5373c5a3-7bc6-435b-a199-40a3f3b463c0" />
</p>
<p>
Establishing an SSH connection from the Windows 10 VM to the Ubuntu VM (using its private IP) and filtering for SSH traffic in Wireshark is essential for analyzing secure remote access. This step shows encrypted communication in action, reinforcing understanding of application-layer protocols and their traffic patterns.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using nslookup to query the IP addresses of public websites (e.g., google.com, disney.com) and filtering for DNS traffic in Wireshark is key to understanding name resolution. This step illustrates how DNS queries and responses function, a fundamental aspect of network communication for accessing online resources.
</p>
<br />
