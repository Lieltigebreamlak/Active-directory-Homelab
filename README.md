# Active Directory Homelab

![Active Directory OU Structure](screenshots/ad-ou-structure.png)
*Active Directory structure with departmental OUs (Finance, HR, IT, Sales)*

## 📌 Overview
A hands-on Active Directory homelab built to practice user/group management for help desk roles. This lab simulates a production environment with department-specific OUs, security groups, and user accounts.

**Current Status:** Active Directory configured ✓  
**In Progress:** Group Policy Objects, DHCP setup

## 🏗️ Current Lab Environment
| Component | Details |
|-----------|---------|
| **Hypervisor** | Oracle VirtualBox |
| **Domain Controller** | Windows Server 2025 (WS2026-DC) |
| **Domain** | Homelab.local |
| **Active Directory Role** | Fully installed and configured |

## 📁 Active Directory Structure (Completed)

### Organizational Units Created
Homelab.local
├── Builtin
├── Computers
├── Domain Controllers
├── Finance
│ ├── Computers
│ ├── Groups
│ └── Users
├── ForeignSecurityPrincipals
├── HR
│ ├── Computers
│ ├── Groups
│ └── Users
├── IT
│ ├── Computers
│ ├── Groups
│ └── Users
├── Managed Service Accounts
├── Sales
│ ├── Computers
│ ├── Groups
│ └── Users
└── Users

![Full AD Hierarchy](screenshots/ad-full-hierarchy.png)
*Complete Active Directory Users and Computers view showing all OUs*

### 👥 User Management
Sample users created across all departments including:

**IT Department:**
- Alex Rivera
- Jamie Smith

**Additional Users Across OUs:**
- Mike Chen
- Sarah Johnson
- *(Plus additional users in Finance, HR, and Sales OUs)*

![User Properties](screenshots/ad-user-properties.png)
*User account configuration showing account options and expiration settings*

### 🔐 Security Groups
| Group Name | Members | Purpose |
|------------|---------|---------|
| IT-FullAccess | Alex Rivera, Jamie Smith | Full access to IT resources |
| IT-ReadOnly | *(Configured as needed)* | Read-only access for auditing |

![IT-FullAccess Group Members](screenshots/ad-group-membership.png)
*Security group showing IT department members with full access permissions*

## ✅ Skills Demonstrated (Current)
- Active Directory Domain Services installation
- Organizational Unit (OU) design and hierarchy
- User account creation across multiple departments
- Security group creation and membership management
- Understanding of ADUC navigation and structure
- Department-specific OU organization (Finance, HR, IT, Sales)

## 🚧 In Progress (Coming Soon)
- Group Policy Objects (drive maps, password policies)
- DHCP server configuration
- Additional client VM for testing
- Ticketing system integration

## 🎯 Help Desk Relevance
This AD environment directly supports common help desk tasks:
- Password resets and account unlocks
- New hire user creation
- Department transfers (moving users between OUs)
- Access requests via security group membership
- Account troubleshooting
- Understanding departmental structure for proper user placement

## 📅 Update History
- **March 18, 2026** - Initial AD structure complete with Finance, HR, IT, Sales OUs and users across all departments. Security groups configured for IT access control.
- *Next update* - GPO implementation

  Client Deployment & Troubleshooting Journey
After building the AD structure, I deployed a Windows 11 client and joined it to the domain. Here's the journey:

1. Domain Controller Network Configuration
https://screenshots/dc-network-config.png
Domain Controller with dual NICs: NAT (192.168.1.10) for internet and Internal Network (192.168.100.1) for homelab communication.

2. Active Directory Structure
https://screenshots/ad-ou-structure.png
Complete AD structure with departmental OUs (Finance, HR, IT, Sales) and dedicated Workstations OU for client machines. Initial Domain Join Attempt
https://screenshots/domain-join-error.png
First attempt to join domain failed - Domain Controller could not be contacted despite correct domain name.

4. Network Connectivity Verified
https://screenshots/ping-success.png
Confirmed basic network connectivity: Client successfully pinging DC at 192.168.100.1 with 0% loss.

5. DNS Resolution Confirmed
https://screenshots/network-dns-tests.png
Verified DNS resolution: nslookup homelab.local returns DC IP addresses, confirming DNS is working properly.

6. Success! Domain Login Achieved
https://screenshots/domain-login-success.png
Client successfully joined to domain - domain user Alex Rivera can now log in. This confirms all troubleshooting was successful.

✅ Troubleshooting Lessons Learned

Network connectivity must be verified first (ping)

DNS resolution is critical for domain discovery

Firewall rules can block domain join even when ping works

SRV records must be present for clients to locate DC

Persistence pays off - every error is solvable

- Current Status

✅ Domain Controller configured and running

✅ AD structure with department OUs complete

✅ DNS functioning with proper SRV records

✅ Windows 11 client successfully joined to domain

✅ Domain user login verified

⏳ Group Policy Objects (next phase)

⏳ DHCP configuration (next phase)



## 📫 Connect With Me
- **GitHub:** [@lielti-gebreamlak](https://github.com/lielti-gebreamlak)
- **LinkedIn:** [Lielti Gebreamlak](https://www.linkedin.com/in/lielti-gebreamlak-253555392/)

## 📚 Resources Used
- Microsoft Learn: Active Directory Domain Services
- VirtualBox documentation
- r/sysadmin homelab community guides
