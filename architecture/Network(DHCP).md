# Network Architecture

The virtual environment simulates a small enterprise network using Hyper-V which happens to be hosted in Proxmox

---

## Network Topology

The following is a representation of the logical structure of the network

| Machine | Operating System | Role | IP Address | Services |
|--------|-----------------|------|-----------|----------|
| Host Machine | Windows Server 2022 | Virtualization Host | N/A | Hyper-V |
| WinSvr2022-01 | Windows Server 2022 (desktop) | Domain Controller | 192.168.100.22 | Active Directory, DNS, DHCP(hot), WDS |
| WinSvr2022-02 | Windows Server 2022 (core) | Domain Controller | 192.168.100.23 | Active Directory, DNS, DHCP (standby) |
| WinSvr2022-03 | Windows Server 2022 (core) | Domain Controller | 192.168.100.24 | Active Directory, DNS |
| Win10-01 | Windows 10 Pro | Client | DHCP Assigned | Active Directory, DNS, DHCP |
| 

All virtual machines currently communicate within the same virtual network.

---

## Network Configuration

| Component | Configuration |
|-----------|---------------|
| Network | 192.168.100.0 |
| Subnet | 255.255.255.224 (/24) |
| Broadcast | 192.168.100.31 |
| Gateway | 192.168.100.1 |
| DNS Server | 192.168.100.22 |
---

## DHCP Configuration

### Servers

| Machine | Balancing |
|---------|-----------|
| WinSvr2022-01 | Hot |
| WinSvr2022-02 | Standby |
---

### IP Scopes

| Type | Start | End |
| :--- | :--- | :--- |
| **Pool** | 192.168.100.2 | 192.168.100.30 |
| **Xxclusion** | 192.168.100.20 | 192.168.100.20 |
---

### IP Reservations
| IP | Name | MAC |
| --- | --- | --- |
| 192.168.100.22 | WinSvr2022-01 | 00155D019801 |
| 192.168.100.23 | WinSvr2022-02 | 00155D019805 |
---
