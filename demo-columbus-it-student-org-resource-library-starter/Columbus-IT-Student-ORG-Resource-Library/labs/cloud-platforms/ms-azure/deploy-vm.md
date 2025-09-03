# Lab: Deploy a Virtual Machine (VM) on Azure Free Tier

## Objective
Learn how to create a virtual machine and connect to it.

## Steps
1. Log in to the [Azure Portal](https://portal.azure.com/).  
2. Navigate to **Virtual Machines → Create → Azure virtual machine**.  
3. Choose **Windows Server 2019 Datacenter (Free Tier)** or **Ubuntu Server (Free Tier)**.  
4. Select the **B1s** size (free tier eligible).  
5. Configure username/password (for Windows) or SSH key (for Linux).  
6. Click **Review + Create → Create**.  
7. Once deployed, connect:  
   - **Windows VM:** Use RDP with public IP.  
   - **Linux VM:** Use SSH:  
     ```bash
     ssh username@<Public-IP-address>
     ```
8. Run basic commands to verify connectivity:  
   - Linux: `ls`, `pwd`, `whoami`  
   - Windows: check desktop and folders  

## Notes
- Stop the VM when not in use to save free credits.
- This lab helps practice managing cloud servers safely.
