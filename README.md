# SMB Network Infrastructure Lab

## Project Overview

This project simulates a segmented Small-to-Medium Business (SMB) network environment integrating Cisco networking technologies with Windows Active Directory infrastructure.

The lab was designed to demonstrate:

- VLAN segmentation
- Inter-VLAN routing
- NAT/PAT
- ACL security policies
- DHCP relay
- Windows Active Directory
- DNS services
- SMB file sharing
- Role-Based Access Control (RBAC)
- Domain authentication
- Network troubleshooting

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Cisco Packet Tracer | Network simulation |
| Windows Server | AD DS / DNS / File Services |
| Windows 10 | Client systems |
| Oracle VirtualBox | Virtualization |
| Cisco IOS CLI | Router and switch configuration |

---

# Network Topology

The environment was built using a router-on-a-stick architecture with centralized server infrastructure.

## VLAN Design

| VLAN | Name | Subnet | Purpose |
|---|---|---|---|
| 10 | Management | 192.168.10.0/24 | IT/Admin Devices |
| 20 | Staff | 192.168.20.0/24 | Employee Workstations |
| 30 | Servers | 192.168.30.0/24 | AD/DNS/File Services |
| 40 | Printers | 192.168.40.0/24 | Network Printers |
| 50 | Guest | 192.168.50.0/24 | Guest Wireless |
| 60 | Voice | 192.168.60.0/24 | IP Phones |

---

# IP Addressing

| Device | Address |
|---|---|
| Router G0/0.10 | 192.168.10.1 |
| Router G0/0.20 | 192.168.20.1 |
| Router G0/0.30 | 192.168.30.1 |
| Router G0/0.40 | 192.168.40.1 |
| Router G0/0.50 | 192.168.50.1 |
| Router G0/0.60 | 192.168.60.1 |
| Windows Server | 192.168.30.11 |

---

# Network Screenshots

## SMB Network Layout

[Open Screenshot](Screenshots/Network/smb%20network%20layoutpkt)

---

## VLAN Verification

[Open Screenshot](Screenshots/Network/vlanbrief.png)

---

## Trunk Port Configuration

[Open Screenshot](Screenshots/Network/trunk.png)

---

## Router Interface Configuration

[Open Screenshot](Screenshots/Network/routerinterfacefacebrief.png)

---

## Router Running Configuration

[Open Screenshot](Screenshots/Network/routerrunningconfig.png)

---

## ACL Configuration

[Open Screenshot](Screenshots/Network/accesslists.png)

---

## NAT Translation Table

[Open Screenshot](Screenshots/Network/nattranslations.png)

---

## PAT Configuration

[Open Screenshot](Screenshots/Network/pat.png)

---

## DHCP Validation - Printers VLAN

[Open Screenshot](Screenshots/Network/dhcponprinters.png)

---

## DHCP Validation - Voice VLAN

[Open Screenshot](Screenshots/Network/dhcponphone.png)

---

## Connectivity Testing

### VLAN 10 Ping Tests

[Open Screenshot](Screenshots/Network/vlan10pings.png)

---

### VLAN 20 Ping Tests

[Open Screenshot](Screenshots/Network/vlan20pings.jpg)

---

### Printer VLAN Ping Test

[Open Screenshot](Screenshots/Network/pingtovlan40.png)

---

### Guest VLAN Ping Test

[Open Screenshot](Screenshots/Network/pingtovlan50.png)

---

# Active Directory Infrastructure

The Windows Server environment was configured with:

- Active Directory Domain Services
- DNS Services
- Organizational Units
- Security Groups
- SMB Shares
- Domain Authentication

Domain:
```text
corp.local
```

---

# Active Directory Screenshots

## Active Directory + DNS Installation

[Open Screenshot](Screenshots/Active%20Directory/addomainanddns.png)

---

## Roles and Features Installation

[Open Screenshot](Screenshots/Active%20Directory/addrolesandfeatures.png)

---

## DNS Validation

[Open Screenshot](Screenshots/Active%20Directory/dnsproof.png)

---

## PowerShell Domain Setup

[Open Screenshot](Screenshots/Active%20Directory/powershellworkaround.png)

---

# Organizational Unit Structure

Separate Organizational Units were created for:

- Management
- Staff
- Users
- Groups
- Computers

---

## Management Groups

[Open Screenshot](Screenshots/Active%20Directory/mgmtgroups.png)

---

## Management Users

[Open Screenshot](Screenshots/Active%20Directory/mgmtusers.png)

---

## Staff Groups

[Open Screenshot](Screenshots/Active%20Directory/staffgroups.png)

---

## Staff Users

[Open Screenshot](Screenshots/Active%20Directory/staffusers.png)

---

# Domain Join Process

Windows clients were successfully joined to:

```text
corp.local
```

---

## Domain Join

[Open Screenshot](Screenshots/Active%20Directory/joindomain.png)

---

## Successful Domain Membership

[Open Screenshot](Screenshots/Active%20Directory/domainjoined.png)

---

# RBAC and File Share Security

Security groups and NTFS/share permissions were implemented to simulate real-world Role-Based Access Control.

Groups included:

- HR_Users
- Staff_Users
- Sales_Users
- IT_Admins

---

# Share Access Validation

## Successful HR Share Access

[Open Screenshot](Screenshots/Active%20Directory/chrisleenaccesshrshare.png)

---

## Successful Management Share Access

[Open Screenshot](Screenshots/Active%20Directory/chrileemanagementshar.png)

---

## HR User Access Validation

[Open Screenshot](Screenshots/Active%20Directory/jjohnsonaccesshrshare.png)

---

## Unauthorized Access Denied

[Open Screenshot](Screenshots/Active%20Directory/jjhonsonaccessdeniedmgmtshare.png)

---

# Administrative Privileges

Administrative privileges were delegated using Domain Admins membership and AD security groups.

## Elevated IT Admin Permissions

[Open Screenshot](Screenshots/Active%20Directory/elevateitadminpriv.png)

---

# Troubleshooting Performed

The project included troubleshooting involving:

- VLAN communication failures
- ACL restrictions
- DNS resolution
- DHCP relay configuration
- SMB share permissions
- Domain authentication
- NAT validation
- Connectivity testing

This troubleshooting process was intentionally documented to simulate real-world enterprise support workflows.

---

# Skills Demonstrated

## Networking

- VLAN segmentation
- Trunking
- Router-on-a-stick
- ACL implementation
- NAT/PAT
- DHCP relay
- DNS troubleshooting

## Systems Administration

- Active Directory
- Organizational Units
- Group management
- RBAC
- SMB file shares
- Domain joins

## Troubleshooting

- Connectivity troubleshooting
- Access control validation
- DNS troubleshooting
- DHCP troubleshooting
- Permission troubleshooting

---

# Estimated Hardware Equivalent Cost

| Equipment | Estimated Cost |
|---|---|
| Cisco Router | $400 |
| Cisco Managed Switch | $300 |
| Windows Server License | $500 |
| Windows Workstations | $2,000 |
| Cabling | $150 |
| Wireless APs | $300 |
| Printers | $250 |

Estimated Total:
```text
~$3,500 - $4,000
```

---

# Project Summary

This project demonstrates deployment and troubleshooting of a segmented SMB enterprise environment integrating:

- Cisco networking
- Active Directory
- DNS
- VLAN segmentation
- RBAC
- NAT/PAT
- DHCP relay
- Access control policies

The lab was built to simulate real-world enterprise infrastructure deployment and troubleshooting workflows while strengthening both networking and systems administration skills.
