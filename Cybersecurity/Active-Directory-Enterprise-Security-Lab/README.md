# 🏢 Active Directory Enterprise Security Lab

<p align="center">
  <img src="https://img.shields.io/badge/Windows%20Server%202019-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Server 2019" />
  <img src="https://img.shields.io/badge/Active%20Directory-005A9C?style=for-the-badge" alt="Active Directory" />
  <img src="https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project builds a small enterprise-style Windows domain environment using Windows Server 2019, Windows 10, and Windows 7 virtual machines.

The lab focuses on centralized identity and endpoint administration. A Windows Server domain controller provides Active Directory Domain Services, while Windows clients join the domain and authenticate against the centralized directory.

The environment forms the foundation for the IAM, Group Policy, and Wazuh monitoring projects in this portfolio.

## Objectives

- Deploy a Windows Server 2019 domain controller.
- Install and configure Active Directory Domain Services.
- Create the `shariflabs.local` domain.
- Prepare Windows client machines for domain membership.
- Join Windows 10 and Windows 7 clients to the domain.
- Verify centralized authentication.
- Verify that domain computers are visible in Active Directory.
- Build a repeatable enterprise-style Windows lab.

## Environment / Architecture

### Components

| Component | Role |
|---|---|
| Windows Server 2019 | Domain Controller |
| Windows 10 | Domain Client |
| Windows 7 | Domain Client |
| VirtualBox | Virtualization platform |
| Active Directory Domain Services | Centralized identity and directory service |

### Domain

`shariflabs.local`

The domain controller provides centralized directory services while the client systems participate as domain members.

## Tools & Technologies

- Windows Server 2019
- Active Directory Domain Services
- Windows 10
- Windows 7
- VirtualBox
- Windows domain authentication
- DNS / domain-resolution concepts

## Implementation Steps

### 1. Prepare the Virtual Machines

The Windows Server and client operating systems were prepared as separate virtual machines in VirtualBox.

The environment was kept within the lab network so that domain traffic could be tested without depending on production infrastructure.


![### 1. Prepare the Virtual Machines evidence](./assets/01-virtualbox-environment.png)

### 2. Configure Windows Server

Windows Server 2019 was configured as the server that would host the Active Directory environment.

Basic system and network configuration was completed before installing the directory services role.


![### 2. Configure Windows Server evidence](./assets/02-windows-server.png)

### 3. Install Active Directory Domain Services

The Active Directory Domain Services role was installed on the server.

The server was then promoted to a domain controller for:

`shariflabs.local`


![### 3. Install Active Directory Domain Services evidence](./assets/03-ad-ds-installation.png)

![### 3. Install Active Directory Domain Services evidence](./assets/04-domain-controller.png)

### 4. Verify the Domain Controller

The domain controller configuration was checked before connecting client systems.

The purpose was to ensure that the directory environment was ready before attempting domain joins.

### 5. Prepare the Windows 10 Client

The Windows 10 virtual machine was configured to communicate with the domain environment.

The client was then prepared for domain membership.


![### 5. Prepare the Windows 10 Client evidence](./assets/05-windows10-configuration.png)

### 6. Join Windows 10 to the Domain

The Windows 10 client was joined to:

`shariflabs.local`

The join process was verified from both the client and the Active Directory environment.


![### 6. Join Windows 10 to the Domain evidence](./assets/06-windows10-domain-join.png)

### 7. Prepare and Join Windows 7

The Windows 7 client was similarly configured and joined to the domain.

This provided a second domain member for testing centralized management across different Windows client systems.


![### 7. Prepare and Join Windows 7 evidence](./assets/07-windows7-configuration.png)

![### 7. Prepare and Join Windows 7 evidence](./assets/08-windows7-domain-join.png)

### 8. Verify Domain Authentication

Domain authentication was tested using domain credentials.

The purpose was to confirm that clients could participate in the centralized identity environment rather than operating only as standalone workstations.


![### 8. Verify Domain Authentication evidence](./assets/09-domain-authentication.png)

### 9. Verify Domain Computers

The domain controller was checked for the registered Windows 10 and Windows 7 computers.

This provides evidence that the clients successfully became members of the domain.


![### 9. Verify Domain Computers evidence](./assets/10-domain-computers.png)

## Configuration / Technical Details

The lab establishes the following relationship:

**Domain Controller → Active Directory Domain → Domain Clients**

The domain environment is later extended with:

- Organizational Units
- Security groups
- Group Policy
- Password controls
- Account lockout controls
- Security auditing
- Wazuh endpoint monitoring

This separation of responsibilities mirrors the way identity and endpoint administration can be organized in a larger Windows environment.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| VirtualBox environment | `assets/01-virtualbox-environment.png` |
| Windows Server | `assets/02-windows-server.png` |
| AD DS installation | `assets/03-ad-ds-installation.png` |
| Domain controller | `assets/04-domain-controller.png` |
| Windows 10 configuration | `assets/05-windows10-configuration.png` |
| Windows 10 domain join | `assets/06-windows10-domain-join.png` |
| Windows 7 configuration | `assets/07-windows7-configuration.png` |
| Windows 7 domain join | `assets/08-windows7-domain-join.png` |
| Domain authentication | `assets/09-domain-authentication.png` |
| Domain computers | `assets/10-domain-computers.png` |

## Challenges

- Keeping the virtual machines on a network where domain communication worked reliably.
- Ensuring the clients could locate and communicate with the domain controller.
- Troubleshooting domain-join dependencies before attempting authentication.
- Maintaining consistent configuration across multiple Windows virtual machines.

## Lessons Learned

The project demonstrated that Active Directory is more than a user database. Successful domain operation depends on coordinated identity, networking, name resolution, client configuration, and centralized administration.

It also provided the base environment needed to study access control and security monitoring in later projects.

## Skills Demonstrated

- Windows Server administration
- Active Directory deployment
- Domain controller configuration
- Windows domain joining
- Centralized authentication
- Virtual lab design
- Endpoint administration
- Troubleshooting

## Conclusion

This lab establishes a realistic small enterprise Windows environment and provides the foundation for identity management, policy enforcement, and security monitoring. It connects networking fundamentals with practical enterprise cybersecurity operations.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking