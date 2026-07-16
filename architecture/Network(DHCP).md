# Network Architecture

The virtual environment simulates a small enterprise network using Hyper-V which happens to be hosted in Proxmox

---

## Network Topology

The following is a representation of the logical structure of the network

| Machine | Operating System | Role | IP Address | Services |
|--------|-----------------|------|-----------|----------|
| Host Machine | Windows Server 2022 | Virtualization Host | N/A | Hyper-V |
| WinSvr2022-01 | Windows Server 2022 (desktop) | Domain Controller | 192.168.100.22 | Active Directory, DNS, DHCP |
| WinSvr2022-02 | Windows Server 2022 (core) | Domain Controller | 192.168.100.23 | Active Directory, DNS, DHCP, WDS |
| Win10-01 | Windows 10 Pro | Domain Controller | 192.168.126.10 | Active Directory, DNS, DHCP |

All virtual machines communicate within the same VMware virtual network.

---

## Network Configuration

| Component | Configuration |
|-----------|---------------|
| Network | 192.168.100.0 |
| Subnet | 255.255.255.224 (/24) |
| Broadcast | 192.168.100.31 |
| Gateway | 192.168.100.1 |
| DNS Server | 192.168.100.22 (Windows Server) |