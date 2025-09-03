# Lab: Create a Linux Virtual Machine in VMware Workstation Player

## Objective
Install VMware Workstation Player and set up a Linux virtual machine (VM) to practice Linux commands, networking, and system administration in a safe environment.

---

## Step 1: Download VMware Workstation Player
1. Go to [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html).  
2. Select your host OS (Windows or Linux) → Download.  
3. Run the installer and follow on-screen prompts.  

---

## Step 2: Download a Linux ISO
1. Go to [Ubuntu Desktop Download](https://ubuntu.com/download/desktop).  
2. Download the latest **LTS version** ISO file.  

---

## Step 3: Create a New Virtual Machine
1. Open VMware Player → Click **Create a New Virtual Machine**.  
2. Select **Installer disc image file (iso)** → Browse to the Ubuntu ISO.  
3. Click **Next**.  

---

## Step 4: Configure VM Settings
1. **Guest Operating System:** Linux → Ubuntu 64-bit.  
2. **Name the VM** (e.g., Ubuntu-VM) → Select location for VM files.  
3. **Disk Capacity:** Recommended 20 GB → Store as a single file → Click **Next**.  

---

## Step 5: Customize Hardware (Optional)
1. Increase **Memory** to at least 2 GB.  
2. Increase **Processors/Cores** if needed.  
3. Adjust **Network Adapter** settings (NAT or Bridged) based on lab needs.  

---

## Step 6: Start the Virtual Machine
1. Click **Finish** → VM will power on.  
2. Follow Ubuntu installation prompts: language, username, password, time zone.  

---

## Step 7: Install VMware Tools (Recommended)
1. With VM running → Click **Player → Manage → Install VMware Tools**.  
2. Mount the ISO in the VM → Open terminal → Follow instructions to install.  
3. Enhances performance, enables shared folders, clipboard sharing, and better display resolution.  

---

## Notes
- Snapshots: Use **VM Snapshots** to save VM states before major changes.  
- Safe practice: Run Linux commands, server setup, and networking labs without affecting your main system.  
- Delete VM or snapshot when done to free disk space.
