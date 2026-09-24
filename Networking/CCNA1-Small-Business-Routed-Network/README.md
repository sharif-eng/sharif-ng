Final Project 2 README
# 🌐 Small Business Routed Network | CCNA 1 Packet Tracer Project

<p align="center">
  <img src="https://img.shields.io/badge/CCNA%201-Introduction%20to%20Networks-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/Cisco%20Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/IPv4-181717?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Static%20Routing-2E8B57?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Networking-2E8B57?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" />
</p>

## 📌 Introduction

This project is a practical Cisco Packet Tracer implementation of a small business network containing two separate LANs connected through two routers.

The project builds on foundational CCNA 1 networking concepts by introducing multiple IPv4 networks, router interfaces, a point-to-point WAN connection, static routing and end-to-end connectivity testing.

---

## 🎯 Objectives

- Build two separate LANs.
- Configure two Cisco routers.
- Configure IPv4 addressing.
- Configure router interfaces.
- Establish a router-to-router connection.
- Configure static routes.
- Test end-to-end communication.
- Practice network troubleshooting.
- Verify routing tables and interface status.
- Save device configurations.

---

## 🏗️ Network Topology

```text
       LAN 1                                      LAN 2

   PC1      PC2                              PC3      PC4
    │        │                                │        │
    └─── S1 ─┘                                └─-S2 ──-┘
         │                                        │
        R1 ═════════════ WAN ═══════════════════ R2

🌐 IP Addressing Plan
Device	Interface	IP Address	Mask	Gateway
R1	G0/0	192.168.10.1	/24	N/A
R1	G0/1	10.0.0.1	/30	N/A
R2	G0/0	192.168.20.1	/24	N/A
R2	G0/1	10.0.0.2	/30	N/A
PC1	NIC	192.168.10.10	/24	192.168.10.1
PC2	NIC	192.168.10.11	/24	192.168.10.1
PC3	NIC	192.168.20.10	/24	192.168.20.1
PC4	NIC	192.168.20.11	/24	192.168.20.1
⚙️ Implementation
1. Network Topology

The network was built using two routers, two switches and four PCs.

Evidence: Completed small business network topology.

2. Router R1 Configuration

R1 was configured with an interface for the local LAN and another interface for the router-to-router connection.

Evidence: R1 interface configuration.

3. Router R2 Configuration

R2 was configured to provide connectivity for the second LAN and the WAN connection.

Evidence: R2 interface configuration.

4. IPv4 Addressing

All end devices were assigned addresses according to the project addressing plan.

Evidence: IPv4 configuration of the network devices.

5. Static Routing

Static routes were configured so each router could reach the remote LAN.

R1:

ip route 192.168.20.0 255.255.255.0 10.0.0.2

R2:

ip route 192.168.10.0 255.255.255.0 10.0.0.1

Evidence: Static routing configuration and routing table verification.

6. Router Connectivity

Connectivity between R1 and R2 was tested across the WAN link.

ping 10.0.0.2
ping 10.0.0.1

Evidence: Successful router-to-router connectivity.

7. End-to-End Connectivity

End-to-end communication was tested between hosts located on different LANs.

Example:

ping 192.168.20.10

Evidence: Successful communication between separate routed networks.

8. Troubleshooting

A routing configuration issue was intentionally introduced, investigated using diagnostic commands and corrected.

Evidence: Troubleshooting and correction of a routing problem.

9. Configuration Persistence

The completed configurations were saved using:

copy running-config startup-config

Evidence: Device configuration saved for persistence.

🧠 Concepts Practiced
IPv4 addressing
Subnetting
Multiple LANs
Router interfaces
WAN connectivity
Static routing
Routing tables
Default gateways
Cisco IOS CLI
Connectivity testing
Troubleshooting
🧪 Verification Checklist
 Two LANs created
 R1 configured
 R2 configured
 End devices addressed
 Router-to-router connectivity verified
 Static routes configured
 Routing tables verified
 End-to-end connectivity tested
 Troubleshooting performed
 Configuration saved
📚 Key Learning Outcomes

This project strengthened my understanding of how routers connect separate IP networks.

It demonstrated the progression from a basic LAN to a routed network:

LAN → Router → WAN → Router → LAN

The project also introduced practical static routing and routing-table verification.

🛠️ Tools
Cisco Packet Tracer
Cisco IOS
IPv4
Ethernet
Static Routing
📁 Project Structure
CCNA1-Small-Business-Routed-Network/
│
├── assets/
│   ├── 01-topology.png
│   ├── 02-r1-configuration.png
│   ├── 03-r2-configuration.png
│   ├── 04-ip-addressing.png
│   ├── 05-static-routes.png
│   ├── 06-router-connectivity.png
│   ├── 07-end-to-end-connectivity.png
│
├── Small-Business-Routed-Network.pkt
│
└── README.md
✅ Project Status

Completed

Built as part of my practical progression through Cisco Networking Academy CCNA 1: Introduction to Networks.

👨‍💻 Author

Angole Sharif Abubakar

BSc Computer Science | Cybersecurity | Cloud Security | Networking

