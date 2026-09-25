# 🔐 Active Directory IAM & Group Policy Security Lab

<p align="center">
  <img src="https://img.shields.io/badge/Active%20Directory-005A9C?style=for-the-badge" alt="Active Directory" />
  <img src="https://img.shields.io/badge/IAM-6C2E8C?style=for-the-badge" alt="Identity and Access Management" />
  <img src="https://img.shields.io/badge/Group%20Policy-C2185B?style=for-the-badge" alt="Group Policy" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project extends the `shariflabs.local` Active Directory environment into a practical Identity and Access Management lab.

The lab focuses on organizing users and computers, creating role-based security groups, applying Group Policy, and enforcing basic account security controls. The objective is to demonstrate how centralized identity can be structured and governed rather than simply creating individual user accounts.

The environment also provides the identity and policy layer used by the Wazuh monitoring project.

## Objectives

- Organize Active Directory objects using Organizational Units.
- Create users and security groups around functional roles.
- Establish role-oriented access structures.
- Configure password and account-lockout policies.
- Apply Group Policy within the domain.
- Enable security auditing relevant to the lab.
- Verify that policies are applied to client systems.
- Demonstrate practical IAM and access-control concepts.

## Environment / Architecture

### Domain

`shariflabs.local`

### Organizational Units

The lab includes OUs for:

- AI
- Cybersecurity
- DataSci
- Executives
- HR
- IT
- Sales
- Workstations
- Software
- Users
- Service Accounts

### Security Groups

The environment includes:

- IT Admins
- IT Team
- Cyber Team
- Data Team
- Executive Team
- Sales Team
- Dev Team

A shared resource structure named `SharifLabs-IAM-Resources` was also used within the lab.

## Tools & Technologies

- Windows Server
- Active Directory Users and Computers
- Group Policy Management
- Security Groups
- Organizational Units
- Windows 10 client
- VirtualBox
- Windows security auditing

## Implementation Steps

### 1. Establish the Active Directory Domain

The IAM work was built on the existing:

`shariflabs.local`

domain environment.

### 2. Design the OU Structure

Organizational Units were created to separate users, departments, workstations, software-related objects, and service accounts.

The goal was to avoid keeping all directory objects in a single flat structure.

### 3. Create Security Groups

Security groups were created around functional responsibilities such as IT, cybersecurity, data, sales, development, and executive roles.

This provides a foundation for assigning access according to role instead of assigning permissions independently to every user.

### 4. Organize User Accounts

User accounts were placed within the appropriate directory structure and associated with the relevant groups.

The resulting structure provides a clearer relationship between users, departments, roles, and permissions.

### 5. Configure Group Policy

Group Policy was used to centralize security settings.

The lab included password and account-lockout controls, providing a practical example of domain-wide security policy enforcement.

### 6. Configure Password Policy

Password controls were configured through Group Policy.

The purpose was to move account security away from individual workstation settings and into centralized domain administration.

### 7. Configure Account Lockout

Account-lockout settings were configured to provide protection against repeated unsuccessful authentication attempts.

### 8. Enable Security Auditing

Security auditing was enabled within the environment so that relevant security activity could be observed and later consumed by monitoring tools.

### 9. Apply and Verify Policies

The policy configuration was checked from the Windows client environment to confirm that the expected settings were being enforced.

### 10. Review Access-Control Structure

The final IAM model was reviewed as a relationship between:

**Users → Groups → Organizational Structure → Policies → Resources**

This makes the security model easier to reason about and maintain.

## Configuration / Technical Details

### IAM Model

| Layer | Purpose |
|---|---|
| Users | Individual identities |
| Security Groups | Role-based membership |
| OUs | Administrative and organizational separation |
| GPOs | Centralized security policy |
| Resources | Objects and services requiring controlled access |
| Auditing | Visibility into security-relevant activity |

The project emphasizes centralized administration and role-oriented access control.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| Active Directory console | `assets/01-active-directory.png` |
| Organizational Units | `assets/02-organizational-units.png` |
| User accounts | `assets/03-ad-users.png` |
| Security groups | `assets/04-security-groups.png` |
| Group Policy | `assets/05-group-policy.png` |
| Password policy | `assets/06-password-policy.png` |
| Account lockout | `assets/07-account-lockout.png` |
| Windows 10 client | `assets/08-windows10-client.png` |
| Policy verification | `assets/09-policy-verification.png` |
| Access-control evidence | `assets/10-access-control.png` |

## Challenges

- Designing an OU structure that remained understandable as the environment grew.
- Separating administrative roles from general users.
- Translating security requirements into Group Policy settings.
- Verifying that domain policies were actually applied to the client.
- Keeping IAM structure consistent with the intended organizational roles.

## Lessons Learned

The project reinforced the principle that identity security depends on structure. Users, groups, OUs, policies, and resources need to have clear relationships.

It also demonstrated why centralized policy enforcement is useful in Windows environments: security controls can be managed consistently rather than configured independently on every workstation.

## Skills Demonstrated

- Active Directory administration
- Identity and Access Management
- Role-based access concepts
- Organizational Unit design
- Security group management
- Group Policy
- Password policy
- Account lockout controls
- Security auditing
- Windows security administration

## Conclusion

The Active Directory IAM and Group Policy lab demonstrates how an enterprise identity environment can be organized and protected through centralized directory services and policy enforcement. It provides a practical bridge between Windows administration and cybersecurity operations.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking