# 🛡️ Wazuh Active Directory Security Monitoring Lab

<p align="center">
  <img src="https://img.shields.io/badge/Wazuh-5C2D91?style=for-the-badge" />
  <img src="https://img.shields.io/badge/SIEM-111111?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Active%20Directory-005A9C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" />
</p>

## 📌 Introduction

A home SOC monitoring lab integrating **Wazuh** with an Active Directory environment to collect endpoint telemetry, monitor security events, investigate alerts, and observe Windows domain activity.

## 🏗️ Environment

- **Wazuh Manager**: Ubuntu Server
- **Domain Controller**: Windows Server
- **Clients**: Windows 10 and Windows 7
- **Agents**: Wazuh agents on Windows endpoints
- **Environment**: Virtualized home lab

## 🎯 Objectives

- Deploy and configure Wazuh
- Connect Windows endpoints as monitored agents
- Collect security and system events
- Monitor authentication-related activity
- Review security alerts
- Investigate endpoint events
- Monitor activity across the Active Directory environment

## 🧠 Skills Demonstrated

**SOC Monitoring • SIEM Concepts • Wazuh • Endpoint Monitoring • Log Analysis • Security Alerts • Active Directory Monitoring • Windows Security • Linux Administration • Incident Investigation**

## 📸 Lab Evidence

Add screenshots to the `assets/` folder.

- `assets/01-ubuntu-server.png`
- `assets/02-wazuh-deployment.png`
- `assets/03-active-directory-environment.png`
- `assets/04-windows-server-agent.png`
- `assets/05-windows10-agent.png`
- `assets/06-windows7-agent.png`
- `assets/07-connected-agents.png`
- `assets/08-wazuh-dashboard.png`
- `assets/09-security-events.png`
- `assets/10-alert-investigation.png`
- `assets/11-ad-monitoring.png`

## 👨‍💻 Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking

## 🧭 Steps

1. Prepare the Ubuntu Server environment.
2. Deploy the Wazuh manager.
3. Prepare the Windows Server Domain Controller.
4. Install and configure Wazuh agents on the Windows endpoints.
5. Verify that the agents connect to the manager.
6. Generate and collect endpoint security events.
7. Review events and alerts in the Wazuh dashboard.
8. Investigate relevant security events.
9. Monitor activity across the Active Directory environment.
10. Document the investigation evidence.

## ⚠️ Challenges

Agent connectivity and event visibility required careful troubleshooting. Small configuration issues on endpoints can prevent an agent from appearing correctly or reduce the quality of collected telemetry.

## 📚 Lessons Learned

- SIEM monitoring depends on reliable log collection.
- Endpoint agents provide important visibility into host activity.
- Alerts require investigation and context before conclusions are made.
- Active Directory events can provide useful security monitoring data.
- A functional SOC lab combines endpoint telemetry, analysis, and investigation.

## ✅ Conclusion

This project strengthened my practical SOC skills by integrating Wazuh with an Active Directory environment and working through endpoint monitoring, alert review, and security investigation.

## 📌 Project Status

**Completed**
