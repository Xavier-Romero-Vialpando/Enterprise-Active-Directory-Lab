# Project Planning

## Executive Summary

This project documents the design and deployment of a simulated enterprise Active Directory environment for Phoenix Health Systems, a fictional healthcare organization with approximately 150 employees.

The environment will provide centralized identity management, authentication, access control, network services, and security policy enforcement using Windows Server and Active Directory Domain Services.

The project is designed to demonstrate practical experience with enterprise infrastructure planning, Windows Server administration, identity and access management, network services, security hardening, troubleshooting, and professional technical documentation.

---

## Business Scenario

Phoenix Health Systems requires a centralized infrastructure capable of supporting employees, workstations, servers, and future organizational growth.

The organization currently lacks a standardized identity and access management platform. User accounts, workstation access, security policies, and network services need to be centrally administered.

The proposed environment will use Active Directory Domain Services to provide:

- Centralized user and computer management
- Domain-based authentication
- Role-based access control
- Group Policy enforcement
- Centralized DNS services
- DHCP address management
- Security policy standardization
- Support for future enterprise systems

---

## Project Scope

### In Scope

The project includes:

- Designing the virtual enterprise environment
- Installing Windows Server
- Configuring a static IP address
- Deploying Active Directory Domain Services
- Creating a new Active Directory forest and domain
- Configuring DNS
- Configuring DHCP
- Creating Organizational Units
- Creating users and security groups
- Configuring Group Policy Objects
- Joining a Windows 11 workstation to the domain
- Applying security-hardening controls
- Testing and validating the environment
- Documenting implementation steps and lessons learned

### Out of Scope

The following items are not included in the initial phase:

- Production deployment
- High availability
- Multiple domain controllers
- Cloud identity integration
- Microsoft Entra ID synchronization
- Enterprise backup infrastructure
- Remote-access VPN
- Full SIEM deployment
- Multiple geographic locations

These features may be added during future project phases.

---

## Project Objectives

The primary objectives are to:

1. Design a realistic enterprise Active Directory environment.
2. Deploy Windows Server as a Domain Controller.
3. Configure centralized authentication and identity management.
4. Implement DNS and DHCP services.
5. Organize users and computers using Organizational Units.
6. Apply role-based access through security groups.
7. Enforce security and configuration standards through Group Policy.
8. Join and manage a Windows 11 client within the domain.
9. Apply foundational security-hardening practices.
10. Produce clear, professional, and reproducible documentation.

---

## Technical Requirements

The lab will require:

- Oracle VirtualBox
- Windows Server installation media
- Windows 11 Enterprise or Professional installation media
- Ubuntu Linux installation media
- pfSense installation media
- Sufficient processor, memory, and storage resources
- An isolated virtual network
- Internet access for updates and software installation when required

---

## Proposed Systems

| System | Hostname | Purpose |
|---|---|---|
| pfSense Firewall | PFSENSE01 | Gateway, firewall, routing, and future segmentation |
| Windows Server | DC01 | Domain Controller, Active Directory, and DNS |
| Windows 11 Client | CLIENT01 | Domain-joined enterprise workstation |
| Ubuntu Server | UBUNTU01 | Linux administration and future service integration |

Additional systems may be introduced as the lab expands.

---

## Proposed Domain

```text
phoenixhealth.local
