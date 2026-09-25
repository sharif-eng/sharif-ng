# 🌐 Small Business Routed Network | CCNA 1 Packet Tracer Project

<p align="center">
  <img src="https://img.shields.io/badge/CCNA%201-Introduction%20to%20Networks-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" alt="CCNA 1: Introduction to Networks" />
  <img src="https://img.shields.io/badge/Cisco%20Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" alt="Cisco Packet Tracer" />
  <img src="https://img.shields.io/badge/IPv4-181717?style=for-the-badge" alt="IPv4" />
  <img src="https://img.shields.io/badge/Static%20Routing-2E8B57?style=for-the-badge" alt="Static Routing" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project extends the small-office LAN concept into a routed small-business network with two separate LANs connected through a point-to-point WAN link.

The lab demonstrates how different IP networks communicate through routers and how static routes can be used to make remote networks reachable. The project was implemented in Cisco Packet Tracer with four end devices, two switches, and two routers.

## Objectives

- Build a two-site small-business network.
- Create separate IPv4 LANs for each site.
- Connect the two sites using a /30 WAN network.
- Configure router interfaces and host addressing.
- Configure static routes between the two LANs.
- Verify local and end-to-end connectivity.
- Practice route-table reasoning and troubleshooting.
- Save the completed router configurations.

## Environment / Architecture

### Topology

The lab contains:

- 2 Cisco routers
- 2 switches
- 4 PCs
- 2 LAN networks
- 1 point-to-point WAN network

### Addressing Plan

| Network / Device | Addressing |
|---|---|
| R1 LAN | 192.168.10.0/24 |
| R2 LAN | 192.168.20.0/24 |
| WAN link | 10.0.0.0/30 |
| R1 WAN side | 10.0.0.1 |
| R2 WAN side | 10.0.0.2 |

The LANs are intentionally separated into different IPv4 networks so that traffic between them must be routed.

## Tools & Technologies

- Cisco Packet Tracer
- Cisco IOS
- IPv4
- Static routing
- Ethernet switching
- Point-to-point WAN addressing
- ICMP / ping
- Cisco IOS verification commands

## Implementation Steps

### 1. Build the Network Topology

Two LANs were created, each containing a switch and two PCs. Each switch was connected to a router, and the routers were connected through the `10.0.0.0/30` WAN network.

### 2. Configure the R1 LAN

R1 provides connectivity for the `192.168.10.0/24` network.

The LAN interface was assigned the gateway address for the local hosts.

### 3. Configure the R2 LAN

R2 provides connectivity for the `192.168.20.0/24` network.

The LAN interface was configured as the default gateway for the hosts at the second site.

### 4. Configure the WAN Link

The routers were connected using the /30 network:

- R1: `10.0.0.1`
- R2: `10.0.0.2`

The /30 network provides a small point-to-point address space suitable for the two router interfaces.

### 5. Configure End Devices

Hosts on the first LAN were addressed from `192.168.10.0/24`.

Hosts on the second LAN were addressed from `192.168.20.0/24`.

Each host was configured with the corresponding router interface as its default gateway.

### 6. Configure Static Routes

R1 was configured with a route to the R2 LAN:

```text
ip route 192.168.20.0 255.255.255.0 10.0.0.2
```

R2 was configured with a route to the R1 LAN:

```text
ip route 192.168.10.0 255.255.255.0 10.0.0.1
```

These routes tell each router how to reach the remote LAN through the other router.

### 7. Verify the Routing Configuration

The router configuration and routing information were checked before performing end-to-end tests.

Useful verification commands include:

```text
show ip interface brief
show ip route
```

### 8. Test Router-to-Router Connectivity

The WAN addresses were tested first:

```text
ping 10.0.0.2
```

from R1, and the reverse path was checked from R2.

### 9. Test End-to-End Connectivity

A host on the first LAN was used to test communication with a host on the second LAN.

This verifies the complete path:

**Source PC → Switch → R1 → WAN → R2 → Switch → Destination PC**

### 10. Save the Configurations

The router configurations were saved after successful verification.

```text
copy running-config startup-config
```

## Configuration / Technical Details

### Routing Logic

Traffic destined for `192.168.20.0/24` leaves R1 through next hop `10.0.0.2`.

Traffic destined for `192.168.10.0/24` leaves R2 through next hop `10.0.0.1`.

This project demonstrates the distinction between a directly connected network and a remote network that requires an explicit route.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| Complete routed topology | `assets/01-topology.png` |
| R1 configuration | `assets/02-r1-configuration.png` |
| R2 configuration | `assets/03-r2-configuration.png` |
| End-device addressing | `assets/04-ip-addressing.png` |
| Static route configuration | `assets/05-static-routes.png` |
| Router connectivity | `assets/06-router-connectivity.png` |
| End-to-end connectivity | `assets/07-end-to-end-connectivity.png` |
| Troubleshooting evidence | `assets/08-troubleshooting.png` |
| Saved configuration | `assets/09-configuration-save.png` |

## Challenges

- Keeping the two LAN address spaces separate.
- Understanding which networks were directly connected and which required static routes.
- Ensuring the WAN next-hop addresses matched the routing configuration.
- Troubleshooting connectivity by checking the path one segment at a time.

## Lessons Learned

The project reinforced how routing decisions are made based on destination networks. It also showed why a successful local ping does not automatically prove that remote-network connectivity is correctly configured.

The lab strengthened practical understanding of route tables, next-hop addresses, default gateways, and end-to-end troubleshooting.

## Skills Demonstrated

- IPv4 addressing
- /30 point-to-point subnetting
- Static routing
- Cisco IOS configuration
- Route-table verification
- Network troubleshooting
- End-to-end connectivity testing
- Packet Tracer topology design

## Conclusion

The Small Business Routed Network demonstrates the transition from a single LAN to a multi-network environment where routers are responsible for forwarding traffic between separate subnets. It provides a practical foundation for more advanced enterprise networking and network-security work.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking