# SMB Network Infrastructure Lab

A simulated Small-to-Medium Business network environment integrating Cisco networking with Windows Active Directory infrastructure. Built to demonstrate real-world enterprise deployment and troubleshooting workflows.

---

## What Was Built

- VLAN segmentation across 6 departments
- Inter-VLAN routing using router-on-a-stick architecture
- NAT/PAT for internet simulation
- ACL security policies
- DHCP relay across VLANs
- Windows Active Directory with DNS
- Role-Based Access Control (RBAC) with SMB file shares
- Domain authentication and domain join process

---

## Technologies Used

| Tool | Purpose |
|---|---|
| Cisco Packet Tracer | Network simulation |
| Windows Server 2019 | AD DS / DNS / File Services |
| Windows 10 | Client systems |
| Oracle VirtualBox | Virtualization |
| Cisco IOS CLI | Router and switch configuration |

---

## Network Design

**Architecture:** Router-on-a-stick with centralized Windows server infrastructure

| VLAN | Name | Subnet | Purpose |
|---|---|---|---|
| 10 | Management | 192.168.10.0/24 | IT/Admin Devices |
| 20 | Staff | 192.168.20.0/24 | Employee Workstations |
| 30 | Servers | 192.168.30.0/24 | AD/DNS/File Services |
| 40 | Printers | 192.168.40.0/24 | Network Printers |
| 50 | Guest | 192.168.50.0/24 | Guest Wireless |
| 60 | Voice | 192.168.60.0/24 | IP Phones |

---

## Network Screenshots

**SMB Network Layout**
![SMB Network Layout](Screenshots/Network/smblayout.png)

**VLAN Verification**
![VLAN Verification](Screenshots/Network/vlanbrief.png)

**Trunk Port Configuration**
![Trunk Configuration](Screenshots/Network/trunk.png)

**Router Interface Configuration**
![Router Interfaces](Screenshots/Network/routerinterfacefacebrief.png)

**Router Running Configuration**
![Router Running Config](Screenshots/Network/routerrunningconfig.png)

**ACL Configuration**
![ACL Configuration](Screenshots/Network/accesslists.png)

**NAT Translation Table**
![NAT Translations](Screenshots/Network/nattranslations.png)

**PAT Configuration**
![PAT Configuration](Screenshots/Network/pat.png)

**DHCP Validation — Printers VLAN**
![DHCP Printers](Screenshots/Network/dhcponprinters.png)

**DHCP Validation — Voice VLAN**
![DHCP Voice](Screenshots/Network/dhcponphone.png)

**Connectivity Testing — VLAN 10**
![VLAN 10 Pings](Screenshots/Network/vlan10pings.png)

**Connectivity Testing — VLAN 20**
![VLAN 20 Pings](Screenshots/Network/vlan20pings.jpg)

**Printer VLAN Ping Test**
![Printer VLAN Ping](Screenshots/Network/pingtovlan40.png)

**Guest VLAN Ping Test**
![Guest VLAN Ping](Screenshots/Network/pingtovlan50.png)

---

## Active Directory Infrastructure

Domain: `corp.local`

Configured services:
- Active Directory Domain Services
- DNS
- Organizational Units (Management, Staff, Users, Groups, Computers)
- Security Groups with RBAC
- SMB file shares with NTFS permissions
- Domain authentication

**AD + DNS Installation**
![AD and DNS](Screenshots/Active%20Directory/addomainanddns.png)

**Roles and Features**
![Roles and Features](Screenshots/Active%20Directory/addrolesandfeatures.png)

**DNS Validation**
![DNS Proof](Screenshots/Active%20Directory/dnsproof.png)

**PowerShell Domain Setup**
![PowerShell](Screenshots/Active%20Directory/powershellworkaround.png)

**Management Groups**
![Management Groups](Screenshots/Active%20Directory/mgmtgroups.png)

**Management Users**
![Management Users](Screenshots/Active%20Directory/mgmtusers.png)

**Staff Groups**
![Staff Groups](Screenshots/Active%20Directory/staffgroups.png)

**Staff Users**
![Staff Users](Screenshots/Active%20Directory/staffusers.png)

**Domain Join**
![Domain Join](Screenshots/Active%20Directory/joindomain.png)

**Successful Domain Membership**
![Domain Joined](Screenshots/Active%20Directory/domainjoined.png)

---

## RBAC and File Share Security

Security groups implemented: `HR_Users` · `Staff_Users` · `Sales_Users` · `IT_Admins`

**HR Share — Authorized Access**
![HR Share Access](Screenshots/Active%20Directory/chrisleenaccesshrshare.png)

**Management Share — Authorized Access**
![Management Share](Screenshots/Active%20Directory/chrileemanagementshar.png)

**HR User Access Validation**
![HR User](Screenshots/Active%20Directory/jjohnsonaccesshrshare.png)

**Unauthorized Access Denied**
![Access Denied](Screenshots/Active%20Directory/jjhonsonaccessdeniedmgmtshare.png)

**Elevated IT Admin Permissions**
![IT Admin](Screenshots/Active%20Directory/elevateitadminpriv.png)

---

## Skills Demonstrated

**Networking:** VLAN segmentation · Trunking · Router-on-a-stick · ACL implementation · NAT/PAT · DHCP relay · DNS troubleshooting

**Systems Administration:** Active Directory · Organizational Units · Group management · RBAC · SMB file shares · Domain joins

**Troubleshooting:** Connectivity issues · Access control validation · DNS resolution · DHCP relay · Permission conflicts

---

## Lessons Learned

- VLAN segmentation improves both security and network organization
- ACLs require careful planning and layered testing
- DNS is critical for Active Directory functionality — most AD issues trace back to DNS
- File share permissions require both share-level and NTFS permissions to work correctly
- Troubleshooting requires a methodical layered approach across switching, routing, DNS, and authentication

