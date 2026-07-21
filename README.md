# 🏢 Enterprise Active Directory Lab

> **Designing, deploying, securing, and documenting a Windows Active Directory enterprise environment from the ground up.**

![Project Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Platform](https://img.shields.io/badge/Platform-Windows%20Server-blue)
![Virtualization](https://img.shields.io/badge/VirtualBox-Lab-orange)
![License](https://img.shields.io/badge/License-Educational-green)

---

# 📖 Project Overview

This project documents the design, deployment, configuration, and security hardening of a simulated enterprise Active Directory environment.

The objective is to build a realistic Windows domain from the ground up while following enterprise infrastructure and security best practices. Every stage of the project is fully documented to demonstrate both technical implementation and engineering decision-making.

Rather than simply completing a lab, this repository serves as a professional portfolio project that showcases enterprise systems administration, security, and technical documentation skills.

---

# 🏢 Business Scenario

This lab simulates the deployment of IT infrastructure for **Phoenix Health Systems**, a fictional healthcare organization with approximately 150 employees.

The organization requires a secure, centralized identity and access management solution capable of supporting users, workstations, servers, and future infrastructure growth.

As the Systems Administrator, my responsibility is to design, deploy, secure, and document the organization's Active Directory environment using industry best practices.

---

# 🎯 Project Objectives

- Design an enterprise Active Directory environment
- Deploy Windows Server as a Domain Controller
- Configure Active Directory Domain Services (AD DS)
- Configure DNS and DHCP
- Implement Organizational Units (OUs)
- Create users and security groups
- Configure Group Policy Objects (GPOs)
- Join Windows 11 clients to the domain
- Apply enterprise security hardening
- Document every phase of the deployment

---

# 🛠️ Technologies Used

## Operating Systems

- Windows Server
- Windows 11 Enterprise
- Ubuntu Linux

## Infrastructure

- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- Organizational Units
- NTFS Permissions

## Networking

- TCP/IP
- Network Segmentation
- Static IP Addressing

## Security

- Windows Defender
- Windows Firewall
- Least Privilege
- Group Policy Security Settings

## Virtualization

- Oracle VirtualBox

---

# 🏗️ Planned Lab Architecture

```text
                    Internet
                         │
                  ┌─────────────┐
                  │   pfSense   │
                  │  Firewall   │
                  └──────┬──────┘
                         │
                Enterprise Network
                         │
        ┌────────────────┼─────────────────┐
        │                │                 │
   Domain Controller   Windows 11      Ubuntu Server
        DC01           CLIENT01          UBUNTU01
```

*A detailed network diagram will be added as the project progresses.*

---

# 📂 Repository Structure

```text
Enterprise-Active-Directory-Lab/
│
├── README.md
│
├── docs/
│   ├── 01-Project-Planning.md
│   ├── 02-Network-Architecture.md
│   ├── 03-IP-Addressing.md
│   ├── 04-Windows-Server-Installation.md
│   ├── 05-Active-Directory.md
│   ├── 06-DNS.md
│   ├── 07-DHCP.md
│   ├── 08-Organizational-Units.md
│   ├── 09-Users-and-Groups.md
│   ├── 10-Group-Policy.md
│   ├── 11-Domain-Join.md
│   ├── 12-Security-Hardening.md
│   └── 13-Lessons-Learned.md
│
├── diagrams/
│
└── images/
```

---

# 🚀 Project Roadmap

| Phase | Status |
|-------|--------|
| Project Planning | 🟡 In Progress |
| Network Design | ⏳ Planned |
| Windows Server Installation | ⏳ Planned |
| Active Directory Deployment | ⏳ Planned |
| DNS Configuration | ⏳ Planned |
| DHCP Configuration | ⏳ Planned |
| Organizational Units | ⏳ Planned |
| Users & Groups | ⏳ Planned |
| Group Policy | ⏳ Planned |
| Windows 11 Domain Join | ⏳ Planned |
| Security Hardening | ⏳ Planned |
| Documentation & Validation | ⏳ Planned |

---

# 💼 Skills Demonstrated

This project demonstrates experience with:

- Windows Server Administration
- Active Directory Administration
- Identity and Access Management (IAM)
- DNS Administration
- DHCP Administration
- Group Policy Management
- Enterprise Network Design
- Security Hardening
- Systems Documentation
- Technical Troubleshooting

---

# 📚 Documentation

Detailed implementation guides can be found in the **docs** directory.

Documentation includes:

- Project Planning
- Network Architecture
- Installation Guides
- Configuration Procedures
- Security Hardening
- Lessons Learned

---

# 🔄 Future Enhancements

Future phases of this enterprise environment will include:

- Microsoft Sentinel SIEM
- Sysmon Logging
- pfSense Firewall
- Enterprise VLANs
- Threat Hunting
- Detection Engineering
- Vulnerability Management
- PowerShell Automation
- Python Security Automation

---

# ⚠️ Disclaimer

This repository is intended for educational and professional portfolio purposes. All infrastructure is deployed within an isolated virtual lab environment and does not represent a production system.

---

## 👨‍💻 Author

**Xavier Romero-Vialpando**

Security+ Certified | M.S. Cybersecurity

Building enterprise cybersecurity projects through hands-on learning, documentation, and continuous improvement.
