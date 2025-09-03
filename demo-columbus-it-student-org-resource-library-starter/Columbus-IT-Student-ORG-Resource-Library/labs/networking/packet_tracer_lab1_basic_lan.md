# Networking Lab – Basic LAN with Router & Switch (Packet Tracer / IOS CLI)
**Estimated time:** 30–45 minutes  
**Prereqs:** Cisco Packet Tracer or GNS3; familiarity with IOS CLI

## Topology
PC1 — Switch — Router — Switch — PC2

## Steps (Router)
```
enable
configure terminal
hostname R1
interface g0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown
exit
interface g0/1
 ip address 192.168.20.1 255.255.255.0
 no shutdown
exit
ip route 0.0.0.0 0.0.0.0 192.168.20.254
end
write memory
```

## Steps (Switch – basic)
```
enable
configure terminal
hostname S1
vlan 10
 name USERS
vlan 20
 name SERVERS
interface range fa0/1-12
 switchport mode access
 switchport access vlan 10
exit
interface range fa0/13-24
 switchport mode access
 switchport access vlan 20
end
write memory
```

## Validation
- Set PC1 IP: 192.168.10.10/24 gw 192.168.10.1
- Set PC2 IP: 192.168.20.10/24 gw 192.168.20.1
- `ping` between PCs succeeds (with router inter‑VLAN routing).

## Cleanup
- Save your Packet Tracer project.
