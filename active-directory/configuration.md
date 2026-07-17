# Active Directory

Below is overally AD DC configuration in which all servers are partnered all together.

## Servers

| Name | OS | IP | Controller Type | Site |
| --- | --- | --- | --- | --- |
| WinSvr2022-01 | Windows Server 2022 | 192.168.100.22 | Global Catalog | Default-First-Site |
| WinSvr2022-02 | Windows Server 2022 Core | 192.168.100.23 | Global Catalog | Default-First-Site |
| WinSvr2022-03 | Windows Server 2022 Core | 192.168.100.24 | Global Catalog | Default-First-Site |

---

## FSMO Configuration

*Schema Master*: WinSvr2022-01
*Domain Naming Master*: WinSvr2022-01
*PDC Emulator*: WinSvr2022-02
*RID Master*: WinSvr2022-03
*Infrastructure Master*: WinSvr2022-03

