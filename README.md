<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Key Steps</h2>

- Create a resource group
- Create a Windows 10 virtual machine
- Create a Linux(Ubuntu) virtual machine
- Make sure both virtual machines are in the same virtual network/subnet
- Connect to Windows 10 virtual machine
- Install and open Wireshark on Windows 10 virtual machine
- Open PowerShell to observe network traffic
- Clean up Azure environment

<h2>Actions and Observations</h2>

<h3>Create a Resource Group</h3>

<p>
  
- In Azure, navigate to "Resource Groups"
- Click "Create" and fill out corresponding fields
</p>
<p>
<img src="https://i.imgur.com/w5yKzNW.png" height="80%" width="80%" alt="Resource Group Page"/>
</p>
<br />

<h3>Create a Windows 10 Virtual Machine</h3>

<p>

- In Azure, navigate to "Virtual Machines"
- Click "Create" then select "Azure Virtual Machine"
- Under "Resource group", select the resource group you previously created(in my case, I named it "RG-Network-Activities")
<img src="https://i.imgur.com/2DAgUaY.png" height="80%" width="80%" alt="Virtual machine resource group"/>

- Under "Image", select the Windows 10 option
<img src="https://i.imgur.com/JyjH7kb.png" height="80%" width="80%" alt="Virtual machine image selection"/>

- Finish filling out necessary fields and create your virtual machine
</p>

<h3>Create a Linux(Ubunutu) Virtual Machine</h3>

<p>
  
- In Azure, navigate to "Virtual Machines"
- Click "Create" then select "Azure Virtual Machine"
- Just like in the previous step, under "Resource group", select the same resource group you previously created(in my case "RG-Network-Activities"
- Under "Image", select the Ubuntu Server 22.04 LTS or 24.04 LTS option
<img src="https://i.imgur.com/yYDqGp5.png" height="80%" width="80%" alt="Virtual machine image selection 2"/>

- Under "Authenication type", select "password" and fill out your chosen username and password
<img src="https://i.imgur.com/qHy8fEb.png" height="80%" width="80%" alt="Virtual machine authentication"/>

- Navigate to the "Networking" tab, and under "Virtual network", select the virtual network you created when creating the Windows 10 virtual machine(in my case "Lab2-vnet")
<img src="https://i.imgur.com/NQXygVj.png" height="80%" width="80%" alt="Virtual network"/>

- Finish filling out necessary fields and create your virtual machine
  
</p>

<h3>Make sure both virtual machines are in the same virtual network/subnet</h3>

<p>

  - In Azure, navigate to "Virtual Machines"
  - Click on your Windows virtual machine and check the name of the "Virtual network/subnet"
  - Click on your Linux virtual machine and make sure the "Virtual network/subnet" is the same as in your Window virtual machine(in my case "Lab2-vnet/default")
  <img src="https://i.imgur.com/kMZdeJn.png" height="80%" width="80%" alt="Windows 10 Virtual Network"/>
</p>

<br />

<h3>Connect to Windows 10 Virtual Machine</h3>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
