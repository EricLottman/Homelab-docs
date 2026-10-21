# Homelab-docs
IT homelab built to learn more about practical IT and to gather hands-on experience

---

## Status: lab retired (October 2026)

This repository documented a study lab: a small-scale simulation of a generic corporate enterprise IT environment (Windows Server, Active Directory, Group Policy, DNS, DHCP, and WDS), built to learn practical IT by doing it.

That lab has been shut down. The hardware it ran on has been repurposed to run functional production services instead, so these documents are preserved as the record of the lab as it was designed and built, not as a description of what the homelab runs today.

---

## Overview

This repository is documentation for my personal IT Home Lab, that simulates a corporate enterprise IT environment in a small scale. It includes the following operating systems:\


- Windows Server 2022
- Windows 10 Clients
- Windows 11 Clients

---

- **Active Directory** and **Group Policy** configuration
- Windows Server 2022, Windows 10, and Windows 11 administration
- Network setup, IP addressing, and connectivity testing
- Documentation and portfolio organization
- **DNS** Configuration
- **DHCP** Configuration
- **WDS** Configuration

---

## Virtual Home Lab Folder Structure

```text
📂 homelab-docs
├─ 📄 README.md
├─ 📄 ToDo.txt
├─ 📂 architecture
|   ├─ 📂 screenshots
|   └─ 📄 Network(DHCP).md
├─ 📂 active-directory
|   ├─ 📄 configuration.md
|   ├─ 📂 group-policy
|   │   ├─ 📂 compliance-GPO
|   │   |   └─ 📄 placeholder
|   │   └─ 📂 company-standards-GPO
|   │       └─ 📄 placeholder
└─ 📂 WDS
    ├─ 📄 Windows Deployment Server.md
    └─ 📂 Testing
        ├─ 📂 Win 10
        ├─ 📂 Win 11
        └─ 📂 WinSvr2022