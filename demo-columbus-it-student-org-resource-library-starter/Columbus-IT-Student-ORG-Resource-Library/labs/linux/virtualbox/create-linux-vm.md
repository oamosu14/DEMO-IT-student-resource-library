# Lab: Create a Linux Virtual Machine in VirtualBox

## Objective
Install VirtualBox and set up a Linux virtual machine (VM) to practice Linux commands, networking, and system administration in a safe environment.

---

## Step 1: Download VirtualBox
1. Go to [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads).  
2. Select your host operating system (Windows, macOS, Linux).  
3. Download and run the installer.  

---

## Step 2: Install VirtualBox
1. Run the installer and follow on-screen prompts.  
2. Accept default options unless you have specific preferences.  
3. Finish installation and open VirtualBox.  

---

## Step 3: Download a Linux ISO
1. Go to [Ubuntu Desktop Download](https://ubuntu.com/download/desktop).  
2. Download the latest **LTS version** ISO file (recommended for beginners).  

---

## Step 4: Create a New Virtual Machine
1. Open VirtualBox → Click **New**.  
2. Enter a **Name** (e.g., Ubuntu-VM).  
3. Type: **Linux**, Version: **Ubuntu (64-bit)**.  
4. Click **Next**.  

---

## Step 5: Allocate Memory
1. Recommended: **2048 MB (2GB)** or higher depending on your system.  
2. Click **Next**.  

---

## Step 6: Create a Virtual Hard Disk
1. Select **Create a virtual hard disk now** → Click **Create**.  
2. Disk type: **VDI (VirtualBox Disk Image)** → Click **Next**.  
3. Storage: **Dynamically allocated** → Click **Next**.  
4. Disk size: Recommended **20 GB** → Click **Create**.  

---

## Step 7: Configure ISO for Installation
1. Select your new VM → Click **Settings → Storage**.  
2. Under **Controller: IDE**, click **Empty** → Click the disk icon → **Choose a disk file**.  
3. Select the Ubuntu ISO downloaded earlier → Click **OK**.  

---

## Step 8: Start the Virtual Machine
1. Click **Start**.  
2. Ubuntu installer will load → Follow on-screen prompts to install Ubuntu.  
3. Set username, password, and complete installation.  

---

## Step 9: Install Guest Additions (Optional but Recommended)
1. With VM running, go to **Devices → Insert Guest Additions CD Image**.  
2. Follow instructions to install.  
3. This improves performance, enables shared folders, and allows better display resolution.  

---

## Notes
- Snapshots: Use **Snapshots** in VirtualBox to save VM states before making changes.  
- Practice Linux safely: Commands, networking, server setup, and troubleshooting.  
- Delete VM or snapshot when done to free disk space.  
