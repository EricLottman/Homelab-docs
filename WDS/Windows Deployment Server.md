# Windows Deployment Server (WDS)

WDS is implemented to provide network based OS deployment through PXE boot

## Server Info

| Name | OS | Domain | IP |
| --- | --- | --- | --- |
| WinSvr2022-01 | Windows Server 2022 | homelab.local | 192.168.100.22 |

---

## WinSvr2022-01

### Config
*Remote Install Location*: W:\RemoteInstall\
*DHCP*: WinSvr2022-01
*PXE Response*: Respond to all client computers

### Boot Images

| Image Name | Operating System | Purpose |
| --- | --- | --- |
| Win10Pro | Windows 10 Pro | Supports legacy applications, to be used where needed |
| Win11Pro | Windows 11 Pro | Default Operating System for Client |
| WinSvr2022 | Windows Server 2022 | Server Operating System for general use |

---

### Install Images


| Image Group | Operating System | Purpose |
| --- | --- | --- |
| Win10Pro | Windows 10 Pro | Supports legacy applications, to be used where needed |
| Win11Pro | Windows 11 Pro | Default Operating System for Client |
| WinSvr2022 | Windows Server 2022 (Desktop Experience), Windows Server 2022 | Server Operating System for general use |

---

