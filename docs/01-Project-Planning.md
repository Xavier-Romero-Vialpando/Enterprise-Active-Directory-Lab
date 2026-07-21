# 01 – Project Planning

---

# Executive Summary

This project documents the planning, design, deployment, configuration, and security hardening of a simulated enterprise Active Directory environment for **Phoenix Health Systems**, a fictional healthcare organization with approximately 150 employees.

The primary objective is to design and implement a secure, scalable, and professionally documented Windows Server infrastructure using industry best practices. The environment will provide centralized identity and access management through Active Directory Domain Services (AD DS), while also delivering essential enterprise services such as DNS, DHCP, Group Policy, and centralized authentication.

This project is intended to demonstrate practical experience with enterprise infrastructure planning, Windows Server administration, identity and access management, security hardening, troubleshooting, and professional technical documentation.

---

# Business Scenario

Phoenix Health Systems is a growing healthcare organization with approximately 150 employees operating from a central headquarters, with plans for future expansion.

The organization currently lacks centralized identity management and requires an enterprise solution capable of managing employee accounts, workstations, security policies, and network services.

As the Systems Administrator, I have been tasked with designing and deploying the organization's Active Directory infrastructure while following industry best practices for security, scalability, documentation, and maintainability.

The completed environment will provide:

- Centralized authentication
- Identity and Access Management (IAM)
- Domain-based administration
- Centralized DNS services
- DHCP address management
- Group Policy management
- Role-Based Access Control (RBAC)
- Enterprise security policies
- A foundation for future infrastructure growth

---

# Project Scope

## In Scope

The following objectives are included in Phase One of this project:

- Enterprise infrastructure planning
- Network architecture design
- Windows Server installation
- Static IP configuration
- Active Directory Domain Services installation
- Domain Controller deployment
- DNS configuration
- DHCP configuration
- Organizational Unit (OU) design
- User account creation
- Security group implementation
- Group Policy deployment
- Windows 11 domain integration
- Enterprise security hardening
- System validation and testing
- Professional documentation

---

## Out of Scope

The following technologies are intentionally excluded from Phase One and may be implemented during future phases:

- Microsoft Entra ID (Azure AD)
- Hybrid Identity
- Multiple Domain Controllers
- Active Directory Certificate Services
- VPN Infrastructure
- Remote Desktop Services
- File Server
- SQL Server
- Microsoft Exchange
- High Availability
- Disaster Recovery
- Backup Infrastructure
- Enterprise SIEM
- Vulnerability Management Platform

---

# Project Objectives

The primary objectives of this project are to:

1. Design a realistic enterprise Active Directory environment.
2. Deploy Windows Server as a Domain Controller.
3. Configure Active Directory Domain Services.
4. Configure enterprise DNS services.
5. Configure enterprise DHCP services.
6. Create Organizational Units based on business departments.
7. Create enterprise user accounts and security groups.
8. Implement Group Policy Objects (GPOs).
9. Join Windows 11 clients to the domain.
10. Apply foundational security-hardening practices.
11. Produce professional technical documentation throughout the project.

---

# Business Requirements

Phoenix Health Systems requires an infrastructure capable of supporting:

- Approximately 150 employees
- Centralized authentication
- Secure user management
- Standardized workstation configuration
- Centralized policy management
- Secure password enforcement
- Simplified administration
- Future organizational growth
- Enterprise security controls
- Reliable internal name resolution
- Dynamic IP address management

---

# Technical Requirements

## Virtualization Platform

- Oracle VirtualBox

## Operating Systems

- Windows Server
- Windows 11 Enterprise
- Ubuntu Server
- pfSense Firewall

## Enterprise Services

- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- Organizational Units
- User Management
- Security Groups

## Networking

- TCP/IP
- IPv4
- Static Addressing
- DHCP
- DNS
- Private Enterprise Network

---

# Proposed Infrastructure

| System | Hostname | Purpose |
|---------|----------|----------|
| Firewall | PFSENSE01 | Routing, NAT, firewall, future VLANs |
| Domain Controller | DC01 | Active Directory, DNS |
| Windows Workstation | CLIENT01 | Enterprise workstation |
| Ubuntu Server | UBUNTU01 | Linux administration |

Future systems may include:

- FILE01
- SQL01
- BACKUP01
- WEB01
- SENTINEL01

---

# Active Directory Domain

The Active Directory forest and domain will use:

```text
phoenixhealth.local
```

This private domain will provide centralized authentication, authorization, and directory services throughout the simulated enterprise.

---

# Network Design

## Enterprise Network

```text
192.168.10.0/24
```

---

## IP Addressing Plan

| Device | Address | Assignment |
|---------|----------|-----------|
| PFSENSE01 | 192.168.10.1 | Static |
| DC01 | 192.168.10.10 | Static |
| UBUNTU01 | 192.168.10.20 | Static |
| CLIENT01 | DHCP | Dynamic |

Infrastructure systems use static addressing to ensure predictable availability while workstations receive addresses dynamically through DHCP.

---

# Naming Standards

To ensure consistency throughout the environment, the following naming convention will be used.

| Device Type | Naming Convention | Example |
|--------------|------------------|----------|
| Domain Controller | DC## | DC01 |
| Client Workstation | CLIENT## | CLIENT01 |
| Linux Server | UBUNTU## | UBUNTU01 |
| Firewall | PFSENSE## | PFSENSE01 |
| File Server | FILE## | FILE01 |
| Backup Server | BACKUP## | BACKUP01 |

---

# Organizational Units

The initial Active Directory structure will include:

```text
Phoenix Health Systems

├── Users
│
├── Computers
│
├── Servers
│
├── Groups
│
└── Service Accounts
```

Departmental Organizational Units will include:

- Information Technology
- Human Resources
- Finance
- Executive
- Operations
- Marketing

---

# Security Objectives

The enterprise environment will be designed around the following security principles:

- Least Privilege
- Defense in Depth
- Role-Based Access Control
- Strong Password Policies
- Account Lockout Policies
- Windows Defender
- Windows Firewall
- Secure DNS
- Secure DHCP
- Group Policy Enforcement
- Administrative Separation
- Secure Configuration Management
- Documentation of all configuration changes

---

# Risks

| Risk | Impact | Mitigation |
|------|----------|------------|
| Incorrect DNS configuration | Authentication failures | Validate DNS before domain deployment |
| Insufficient host resources | Poor VM performance | Allocate CPU and RAM appropriately |
| Group Policy misconfiguration | User disruption | Test GPOs before deployment |
| IP conflicts | Network communication failures | Maintain documented addressing plan |
| Excessive administrator permissions | Increased security risk | Apply least privilege |
| Poor documentation | Difficult troubleshooting | Document every implementation phase |

---

# Assumptions

This project assumes:

- The environment is isolated from production systems.
- The environment is used solely for educational purposes.
- Sufficient host hardware resources are available.
- A single Domain Controller is adequate for Phase One.
- Phoenix Health Systems employs approximately 150 users.
- Future expansion will introduce additional infrastructure and security technologies.

---

# Success Criteria

The project will be considered successful when:

- Windows Server is deployed successfully.
- Active Directory Domain Services is operational.
- The `phoenixhealth.local` domain functions correctly.
- DNS resolves internal resources successfully.
- DHCP assigns valid addresses to clients.
- Organizational Units are implemented.
- User accounts and security groups are created.
- Group Policies are successfully applied.
- Windows 11 joins the domain successfully.
- Administrative authentication functions correctly.
- Security hardening has been completed.
- Documentation accurately reflects the implementation.

---

# Deliverables

The completed project will include:

- Enterprise Project Planning
- Network Architecture Documentation
- IP Addressing Plan
- Windows Server Installation Guide
- Active Directory Deployment Guide
- DNS Configuration Guide
- DHCP Configuration Guide
- Organizational Unit Documentation
- User and Group Management Guide
- Group Policy Documentation
- Windows 11 Domain Join Guide
- Security Hardening Documentation
- Validation and Testing Results
- Lessons Learned
- Screenshots
- Network Diagrams

---

# Future Expansion

Future phases of this enterprise environment will include:

- Microsoft Sentinel SIEM
- Sysmon
- pfSense Firewall
- VLAN Segmentation
- Enterprise Logging
- Threat Hunting
- Detection Engineering
- Vulnerability Management
- PowerShell Automation
- Python Security Automation
- Incident Response
- Windows Server Administration
- Linux Administration
- Enterprise Security Monitoring

---

# Project Status

| Phase | Status |
|---------|----------|
| Project Planning | 🟡 In Progress |
| Infrastructure Design | ⏳ Planned |
| Windows Server Deployment | ⏳ Planned |
| Active Directory Deployment | ⏳ Planned |
| DNS Configuration | ⏳ Planned |
| DHCP Configuration | ⏳ Planned |
| Group Policy | ⏳ Planned |
| Windows Client Integration | ⏳ Planned |
| Security Hardening | ⏳ Planned |
| Documentation | ⏳ Planned |

---

**Document Version:** 1.0  
**Author:** Xavier Romero-Vialpando  
**Project:** Enterprise Active Directory Lab  
**Status:** In Progress
