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

## 📫 Connect With Me
- **GitHub:** [@lielti-gebreamlak](https://github.com/lielti-gebreamlak)
- **LinkedIn:** [Lielti Gebreamlak](https://www.linkedin.com/in/lielti-gebreamlak-253555392/)

## 📚 Resources Used
- Microsoft Learn: Active Directory Domain Services
- VirtualBox documentation
- r/sysadmin homelab community guides
