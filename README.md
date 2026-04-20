# Active Directory Home Lab

## Overview
Built a Windows Server home lab using Active Directory, DNS, DHCP, and Group Policy to simulate a small enterprise environment. Configured domain services, joined Windows clients to the domain, created OUs and user accounts, and applied GPOs for centralized management.

## Lab Environment
- Hypervisor: VirtualBox
- Server OS: Windows Server 2025
- Client OS: Windows 10 Pro
- Network Type:
  - Internal Network
  - NAT Adapter (optional for internet access)

## Objectives
- Configure a Domain Controller
- Install and configure DNS
- Install and configure DHCP
- Create Organizational Units (OUs)
- Create users and admin accounts
- Join client machines to the domain
- Apply Group Policy Objects (GPOs)

## Network Configuration
### Domain Controller
- Static IP: 192.168.10.10
- DNS: 192.168.10.10
- Domain: Stephenslab.com

### DHCP Scope
- Range: 192.168.10.100 - 192.168.10.200
- Subnet Mask: 255.255.255.0
- DNS Server: 192.168.10.10

## Steps Completed
1. Created an internal LAN using VirtualBox
2. Assigned a static IP to the Domain Controller
3. Installed Active Directory Domain Services
4. Promoted the server to a Domain Controller
5. Configured DNS forwarders
6. Installed and authorized DHCP
7. Created Organizational Units
8. Created domain user accounts
9. Joined Windows 10 clients to the domain
10. Created and linked Group Policy Objects

## Group Policy Example
Created a GPO named `LabUsers` and linked it to the appropriate OU to apply settings to test accounts.

## Screenshots

/screenshots
  01-network-setup.png
  02-static-ip.png
  03-domain-controller.png
  04-dns-manager.png
  05-dhcp-scope.png
  06-ou-structure.png
  07-domain-join.png
  08-gpo-link.png
```

## Skills Demonstrated
- Active Directory Administration
- DNS Configuration
- DHCP Management
- Group Policy Management
- Windows Networking
- Virtualization
- Troubleshooting

## Lessons Learned
- DNS must point to the Domain Controller
- DHCP must be authorized in Active Directory
- Cloned VMs need unique MAC addresses
- Windows 10 Home cannot join a domain
- Group Policy only applies when linked to the correct OU
