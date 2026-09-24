# 🏢 Small Office LAN | CCNA 1 Packet Tracer Project

<p align="center">
  <img src="https://img.shields.io/badge/CCNA%201-Introduction%20to%20Networks-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/Cisco%20Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/IPv4-181717?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Networking-2E8B57?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" />
</p>

## 📌 Introduction

This project is a practical Cisco Packet Tracer implementation of a small office Local Area Network (LAN).

The network connects three employee workstations through a Cisco switch and router. The project focuses on foundational networking concepts covered in Cisco Networking Academy CCNA 1: Introduction to Networks.

The implementation demonstrates basic device configuration, IPv4 addressing, default gateways, Ethernet connectivity, and network troubleshooting.

---

## 🎯 Objectives

The project was built to:

- Design a basic small office LAN.
- Connect end devices through a network switch.
- Configure a router interface with IPv4 addressing.
- Configure IPv4 addresses on end devices.
- Configure default gateways.
- Verify end-to-end connectivity.
- Practice basic Cisco IOS CLI configuration.
- Use diagnostic commands to verify network operation.
- Practice basic network troubleshooting.
- Document the completed network.

---

## 🏗️ Network Topology

```text
                         R1
                    Cisco Router
                         |
                       G0/0
                         |
                       G0/1
                    ┌────┴────┐
                    │   S1    │
                    │ 2960    │
                    └─┬──┬──┬─┘
                      │  │  │
                    PC1 PC2 PC3
```

### 🌐 IP Addressing Plan

| Device | Interface | IPv4 Address | Subnet Mask | Default Gateway |
|--------|-----------|--------------|-------------|-----------------|
| R1     | G0/0      | 192.168.10.1 | 255.255.255.0 | N/A             |
| PC1    | NIC       | 192.168.10.10 | 255.255.255.0 | 192.168.10.1    |
| PC2    | NIC       | 192.168.10.11 | 255.255.255.0 | 192.168.10.1    |
| PC3    | NIC       | 192.168.10.12 | 255.255.255.0 | 192.168.10.1    |

Network: `192.168.10.0/24`

### ⚙️ Implementation

1. Physical Topology

   The network was created in Cisco Packet Tracer using one router, one 2960 switch, and three PCs.

   Evidence: Completed Packet Tracer topology.

2. Router Interface Configuration

   Router R1 was configured with the LAN gateway address `192.168.10.1/24`.

   The interface was administratively enabled to allow communication with the LAN.

   Evidence: Router interface configuration and interface status.

3. End Device IPv4 Configuration

   The three PCs were assigned IPv4 addresses from the `192.168.10.0/24` network.

   Evidence: IPv4 configuration of the LAN end devices.

4. Switch Configuration

   The Cisco 2960 switch was configured as the LAN switching device.

   Basic device configuration and interface status were verified using Cisco IOS commands.

   Evidence: Basic switch configuration and interface verification.

5. Router Verification

   The router interface configuration was verified using:

   `show ip interface brief`

   Evidence: Router interface and IP status verification.

6. Connectivity Testing

   Connectivity was tested between the PCs and the default gateway using `ping`.

   Examples:

   ```bash
   ping 192.168.10.11
   ping 192.168.10.12
   ping 192.168.10.1
   ```

   Evidence: Successful connectivity tests across the LAN.

7. Troubleshooting

   A configuration error was intentionally introduced and investigated to practice basic network troubleshooting.

   The issue was identified and corrected before repeating the connectivity test.

   Evidence: Troubleshooting and correction of a network configuration issue.

8. Configuration Persistence

   The router configuration was saved from running configuration to startup configuration.

   ```bash
   copy running-config startup-config
   ```

   Evidence: Configuration saved for persistence after device restart.

---

## 🧠 Cisco IOS Concepts Practiced

| Command | Purpose |
|---------|---------|
| `enable` | Enter privileged EXEC mode |
| `configure terminal` | Enter global configuration mode |
| `hostname` | Configure device hostname |
| `interface` | Enter interface configuration mode |
| `ip address` | Assign an IPv4 address |
| `no shutdown` | Enable an interface |
| `show ip interface brief` | Verify interface status |
| `show running-config` | View active configuration |
| `ping` | Test IP connectivity |
| `copy running-config startup-config` | Save configuration |

---

## 🔍 Networking Concepts Demonstrated

- LAN design
- Ethernet
- IPv4 addressing
- Subnet masks
- /24 networks
- Default gateways
- Switch connectivity
- Router interfaces
- Cisco IOS CLI
- Network verification
- Basic troubleshooting

---

## 🧪 Verification Checklist

- [x] Router configured
- [x] Switch configured
- [x] PCs addressed
- [x] Default gateway configured
- [x] Router interface enabled
- [x] PC-to-PC connectivity tested
- [x] PC-to-router connectivity tested
- [x] Configuration verified
- [x] Configuration saved
- [x] Troubleshooting performed

---

## 📚 Key Learning Outcomes

This project strengthened my understanding of how basic network devices communicate within a LAN.

It provided practical experience with:

End Devices → Switch → Router → IP Connectivity

The project also provided hands-on practice with Cisco IOS configuration, IPv4 addressing, connectivity testing, and basic troubleshooting.

---

## 🛠️ Tools

- Cisco Packet Tracer
- Cisco IOS
- IPv4
- Ethernet

---

## 📁 Project Structure

```text
CCNA1-Small-Office-LAN/
├── assets/
│   ├── 01-topology.png
│   ├── 02-router-interface.png
│   ├── 03-ip-addressing.png
│   ├── 04-switch-configuration.png
│   └── 05-connectivity-test
├── Small-Office-LAN.pkt
├── README.md
└── notes/
```

---

## ✅ Project Status

Completed

Built as part of my practical progression through Cisco Networking Academy CCNA 1: Introduction to Networks.

---

## 👨‍💻 Author

Angole Sharif Abubakar

BSc Computer Science | Cybersecurity | Cloud Security | Networking
