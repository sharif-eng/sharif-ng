# 🛡️ Wazuh Active Directory Security Monitoring Lab

<p align="center">
  <img src="https://img.shields.io/badge/Wazuh-5C2D91?style=for-the-badge" alt="Wazuh" />
  <img src="https://img.shields.io/badge/SIEM-111111?style=for-the-badge" alt="Security Monitoring" />
  <img src="https://img.shields.io/badge/Active%20Directory-005A9C?style=for-the-badge" alt="Active Directory" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project builds a small Security Operations Center-style monitoring environment around an Active Directory lab using Wazuh.

The environment uses an Ubuntu Server Wazuh manager deployed with Docker and Windows endpoints that generate security telemetry. The project focuses on endpoint visibility, agent deployment, security events, alerts, and investigation of activity within a Windows domain.

## Objectives

- Deploy a Wazuh manager in a practical home-lab environment.
- Connect Windows systems as monitored endpoints.
- Verify agent connectivity.
- Collect endpoint security telemetry.
- Observe security events and alerts.
- Investigate activity from the Wazuh dashboard.
- Monitor an Active Directory environment from a centralized security platform.
- Troubleshoot agent enrollment and connectivity problems.

## Environment / Architecture

| Component | Role |
|---|---|
| Ubuntu Server | Wazuh manager host |
| Docker | Wazuh deployment platform |
| Windows Server | Active Directory / monitored endpoint |
| Windows 10 | Monitored endpoint |
| Windows 7 | Monitored endpoint |
| Wazuh agents | Endpoint telemetry collection |
| Wazuh dashboard | Security visibility and investigation |

The monitoring environment connects the Windows domain lab to a centralized security-monitoring platform.

## Tools & Technologies

- Wazuh
- Wazuh Manager
- Wazuh Agents
- Wazuh Dashboard
- Ubuntu Server
- Docker
- Windows Server
- Windows 10
- Windows 7
- Active Directory
- Security event monitoring

## Implementation Steps

### 1. Prepare the Monitoring Host

Ubuntu Server was prepared as the host for the Wazuh manager.

Docker was used to deploy the Wazuh components in the lab environment.


![### 1. Prepare the Monitoring Host evidence](./assets/01-ubuntu-server.png)

### 2. Deploy Wazuh

The Wazuh manager and supporting components were deployed using Docker.

The deployment was then checked before onboarding Windows endpoints.


![### 2. Deploy Wazuh evidence](./assets/02-wazuh-deployment.png)

### 3. Prepare the Active Directory Environment

The existing Windows domain environment was used as the monitored environment.

This allowed endpoint telemetry to be collected from systems participating in the `shariflabs.local` domain.


![### 3. Prepare the Active Directory Environment evidence](./assets/03-active-directory-environment.png)

### 4. Install and Configure Windows Agents

Wazuh agents were configured on:

- Windows Server
- Windows 10
- Windows 7

Each endpoint was then connected to the Wazuh manager.


![### 4. Install and Configure Windows Agents evidence](./assets/04-windows-server-agent.png)

![### 4. Install and Configure Windows Agents evidence](./assets/05-windows10-agent.png)

![### 4. Install and Configure Windows Agents evidence](./assets/06-windows7-agent.png)

### 5. Verify Agent Connectivity

The Wazuh dashboard was used to verify that the expected agents were connected and available for monitoring.


![### 5. Verify Agent Connectivity evidence](./assets/07-connected-agents.png)

### 6. Troubleshoot Agent Connectivity

One practical issue encountered during the lab was a hostname whitespace problem that affected agent connectivity.

The configuration was corrected and the affected agents were subsequently connected to the monitoring environment.

This was an important troubleshooting exercise because SIEM visibility depends on reliable endpoint telemetry.


![### 6. Troubleshoot Agent Connectivity evidence](./assets/07-connected-agents.png)

### 7. Observe Security Events

Once the agents were connected, endpoint activity and security events could be reviewed through Wazuh.

The objective was to understand how endpoint actions become security telemetry.


![### 7. Observe Security Events evidence](./assets/08-wazuh-dashboard.png)

![### 7. Observe Security Events evidence](./assets/09-security-events.png)

### 8. Investigate Alerts

Security alerts were reviewed through the Wazuh interface to practice moving from an event to an investigation.

The investigation process focused on:

- What happened?
- Which endpoint generated the event?
- What type of activity was observed?
- What evidence is available?
- What additional context is required?


![### 8. Investigate Alerts evidence](./assets/10-alert-investigation.png)

### 9. Review Active Directory Monitoring

The Windows domain environment was used to explore how centralized monitoring can provide visibility across multiple endpoints.


![### 9. Review Active Directory Monitoring evidence](./assets/11-ad-monitoring.png)

## Configuration / Technical Details

The lab follows a simplified SOC monitoring workflow:

**Endpoint → Wazuh Agent → Wazuh Manager → Dashboard → Alert Review → Investigation**

The project demonstrates the importance of telemetry collection and centralized visibility when monitoring multiple Windows systems.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| Ubuntu monitoring host | `assets/01-ubuntu-server.png` |
| Wazuh deployment | `assets/02-wazuh-deployment.png` |
| Active Directory environment | `assets/03-active-directory-environment.png` |
| Windows Server agent | `assets/04-windows-server-agent.png` |
| Windows 10 agent | `assets/05-windows10-agent.png` |
| Windows 7 agent | `assets/06-windows7-agent.png` |
| Connected agents | `assets/07-connected-agents.png` |
| Wazuh dashboard | `assets/08-wazuh-dashboard.png` |
| Security events | `assets/09-security-events.png` |
| Alert investigation | `assets/10-alert-investigation.png` |
| Active Directory monitoring | `assets/11-ad-monitoring.png` |

## Challenges

- Deploying the monitoring stack in a resource-conscious home-lab environment.
- Connecting multiple Windows endpoints to the manager.
- Diagnosing agent connectivity rather than assuming the SIEM deployment was broken.
- Identifying the hostname whitespace issue affecting connectivity.
- Understanding how endpoint events become centralized security alerts.

## Lessons Learned

The project reinforced that a SIEM is only as useful as the telemetry it receives. Agent deployment, endpoint configuration, and connectivity are therefore part of the security-monitoring workflow.

The lab also strengthened the transition from simply viewing alerts to asking investigative questions about the source, endpoint, activity, and available evidence.

## Skills Demonstrated

- Wazuh deployment
- SIEM fundamentals
- Endpoint monitoring
- Security event analysis
- Alert investigation
- Active Directory monitoring
- Docker-based security tooling
- Windows endpoint administration
- Troubleshooting
- SOC workflow fundamentals

## Conclusion

This lab demonstrates a practical monitoring workflow across an Active Directory environment. It connects Windows identity infrastructure with centralized security visibility and provides hands-on experience with the operational side of SOC monitoring.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking