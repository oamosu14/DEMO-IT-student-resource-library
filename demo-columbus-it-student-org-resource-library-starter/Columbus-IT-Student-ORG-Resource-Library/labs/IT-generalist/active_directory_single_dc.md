# Windows Lab – Stand up Active Directory (Single DC)
**Estimated time:** 45–60 minutes  
**Prereqs:** Windows Server 2019/2022 VM, 4 GB RAM+, local admin

## Steps
1) **Set hostname & IP** (example)
```powershell
Rename-Computer -NewName "DC1" -Restart
# After restart, set a static IP in Settings or via:
New-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.56.10 -PrefixLength 24 -DefaultGateway 192.168.56.1
Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses 127.0.0.1
```

2) **Install AD DS role**
```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

3) **Promote to new forest**
```powershell
Install-ADDSForest -DomainName "lab.local" -DomainNetbiosName "LAB"
# You will be prompted for DSRM password; server restarts.
```

4) **Create a test user**
```powershell
Import-Module ActiveDirectory
New-ADUser -Name "Test User" -SamAccountName tuser -AccountPassword (Read-Host -AsSecureString "PW") -Enabled $true
```

## Validation
- `Active Directory Users and Computers` shows domain and user.
- DNS service is installed and running.

## Cleanup
- Snapshot the VM as `AD-Base`.
