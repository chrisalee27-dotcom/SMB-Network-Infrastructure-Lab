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

[Open Screenshot](Screenshots/Network/smblayout.png)

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
# Recommended SMB Hardware Deployment

This section outlines realistic hardware recommendations for deploying the SMB network infrastructure demonstrated in this lab.

The goal was to balance:
- reliability
- scalability
- security
- manageability
- SMB budget considerations

---

# Router / Firewall

## Recommended Options

- Cisco Meraki MX68
- Fortinet FortiGate 40F
- Ubiquiti Dream Machine Pro

## Purpose

- Inter-VLAN routing
- Stateful firewall protection
- NAT/PAT
- VPN connectivity
- Guest network isolation
- Centralized management

## Why These Devices

These devices are commonly used in SMB environments because they provide enterprise-style security and management features without requiring large enterprise budgets.

## Estimated Cost

```text
$400 - $900
```

---

# Managed Switch

## Recommended Options

- Cisco CBS350-24T-4G
- Ubiquiti USW-24
- Aruba Instant On 1930

## Purpose

- VLAN segmentation
- 802.1Q trunking
- QoS
- Voice VLAN support
- Layer 2 switching

## Why These Devices

Managed switches allow the business to separate departments and services into VLANs while maintaining centralized control and scalability.

## Estimated Cost

```text
$250 - $500
```

---

# Wireless Access Points

## Recommended Options

- Ubiquiti U6 Lite
- Cisco Business 140AC
- Aruba Instant On AP22

## Purpose

- Wireless connectivity
- Guest wireless access
- Staff wireless access
- VLAN-aware SSIDs

## Why These Devices

These APs support multiple SSIDs and VLAN tagging, allowing separate guest and employee wireless networks while maintaining centralized management.

## Estimated Cost

```text
$100 - $180 each
```

## Recommended Quantity

```text
2 Access Points
```

---

# Server Hardware

## Recommended Options

- Dell PowerEdge T150
- HPE ProLiant ML30

## Purpose

- Active Directory
- DNS
- DHCP
- File shares
- Authentication services

## Why These Devices

These entry-level business servers provide reliable hardware for centralized infrastructure services in SMB environments.

## Estimated Cost

```text
$900 - $1,500
```

---

# End User Workstations

## Recommended Options

- Dell OptiPlex Micro
- HP ProDesk Mini
- Lenovo ThinkCentre Tiny

## Purpose

- Employee productivity
- Domain authentication
- Access to shared resources

## Why These Devices

Business-class systems provide better reliability, manageability, and lifecycle support than consumer-grade hardware.

## Estimated Cost

```text
$600 - $900 each
```

---

# Printers

## Recommended Options

- HP LaserJet Pro
- Brother Business Laser Printer

## Purpose

- Shared network printing
- Department printing services

## Why These Devices

Business laser printers are reliable for SMB environments and support centralized network printing.

## Estimated Cost

```text
$250 - $400
```

---

# Network Cabling

## Recommended Standard

- Cat6 Ethernet Cabling

## Purpose

- Gigabit network connectivity
- Device uplinks
- Infrastructure backbone

## Why Cat6

Cat6 provides better long-term scalability and performance compared to older cabling standards while remaining cost effective for SMB deployments.

## Estimated Cost

```text
$150 - $300
```

---

# Estimated SMB Deployment Cost

| Item | Estimated Cost |
|---|---|
| Firewall / Router | $700 |
| Managed Switch | $400 |
| Wireless Access Points | $300 |
| Server Hardware | $1,200 |
| End User PCs (5) | $4,000 |
| Printers | $300 |
| Cabling | $250 |

# Estimated Total

```text
~$7,000
```

---

# Future Improvements

Potential future improvements for this environment could include:

- Cloud backups
- Azure AD or hybrid identity
- VPN remote access
- SIEM monitoring
- Network monitoring tools
- Wireless controller integration
- Redundant internet connectivity
- Layer 3 switching
- VoIP deployment
- Automation with PowerShell or Python

---

# Project Summary

This SMB infrastructure lab demonstrates deployment and troubleshooting of a segmented enterprise-style network integrating:

- Cisco networking
- VLAN segmentation
- ACL security policies
- NAT/PAT
- DHCP relay
- Active Directory
- DNS services
- RBAC
- SMB file sharing
- Domain authentication
---

# Lessons Learned

This project reinforced several important infrastructure concepts:

- VLAN segmentation improves both security and network organization
- ACLs require careful testing and troubleshooting
- DNS is critical for Active Directory functionality
- DHCP relay simplifies centralized address management
- File share permissions require both share and NTFS permissions to function correctly
- Troubleshooting connectivity issues requires a layered approach across switching, routing, DNS, and authentication services

The project also emphasized the importance of documentation and validation during infrastructure deployment.

---

# Future Improvements

Potential future improvements for this environment include:

- VPN remote access
- Cloud backup integration
- Network monitoring tools
- Wireless controller deployment
- SIEM and centralized logging
- PowerShell automation
- Python-based network automation
- Layer 3 switching
- Redundant internet connectivity
- Azure AD or hybrid identity integration

---

# Topology Overview

The environment was designed using a router-on-a-stick architecture with centralized Windows infrastructure services.

Core services included:

- Active Directory
- DNS
- SMB File Shares
- VLAN segmentation
- ACL security policies
- NAT/PAT
- DHCP relay

Network segmentation was used to isolate:
- management systems
- employee workstations
- servers
- printers
- guest devices
- voice devices

This structure simulates a realistic SMB enterprise network environment.
The project was designed to simulate realistic SMB infrastructure deployment and troubleshooting workflows while strengthening networking and systems administration skills.
The lab was built to simulate real-world enterprise infrastructure deployment and troubleshooting workflows while strengthening both networking and systems administration skills.
