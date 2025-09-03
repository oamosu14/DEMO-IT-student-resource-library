# Linux Lab 2 – Create a Linux VM with VirtualBox
**Estimated time:** 30–45 minutes  
**Prereqs:** Host OS with VirtualBox installed; Ubuntu ISO  

## Steps
1) **Create VM**
   - Name: `sec-lab-ubuntu`
   - Type: Linux, Version: Ubuntu (64-bit)
   - Memory: 4096 MB, CPU: 2
   - Disk: 25 GB (VDI, dynamically allocated)

2) **Attach ISO**
   - Settings → Storage → Controller: IDE → add the Ubuntu ISO.

3) **Install Ubuntu**
   - Normal install; allow updates; create local user.
   - Reboot; remove ISO when prompted.

4) **Guest Additions (optional)**
   ```bash
   sudo apt update && sudo apt install -y build-essential dkms linux-headers-$(uname -r)
   # Devices → Insert Guest Additions CD → run VBoxLinuxAdditions.run
   ```

## Validation
- VM boots; you can login and open a terminal.

## Cleanup
- Take a snapshot named `fresh-install`.
