# ☁️ AWS VPC Security Lab

<p align="center">
  <img src="https://img.shields.io/badge/AWS-VPC-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" alt="Amazon VPC" />
  <img src="https://img.shields.io/badge/Cloud%20Security-232F3E?style=for-the-badge" alt="Cloud Security" />
  <img src="https://img.shields.io/badge/Networking-1BA0D7?style=for-the-badge" alt="Networking" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project is a practical AWS networking and cloud-security lab focused on designing and configuring a Virtual Private Cloud.

The lab covers the core building blocks required to create controlled network connectivity in AWS: VPC addressing, subnets, route tables, an Internet Gateway, and security groups. The objective is to understand how these components work together rather than treating cloud networking as a collection of isolated console settings.

## Objectives

- Create an AWS VPC with a defined IPv4 address range.
- Divide the VPC into subnets.
- Configure route tables for the required network paths.
- Attach and configure an Internet Gateway for internet connectivity where required.
- Configure security groups as network access controls.
- Verify that the components work together as designed.
- Document the final cloud-network configuration.
- Build a foundation for more advanced AWS security architecture.

## Environment / Architecture

The lab uses:

- Amazon VPC
- IPv4 CIDR addressing
- Subnets
- Route tables
- Internet Gateway
- Security Groups
- AWS Management Console

### Architecture Relationship

**VPC → Subnets → Route Tables → Internet Gateway**

Security groups provide traffic controls for resources associated with the relevant network interfaces.

## Tools & Technologies

- Amazon Web Services (AWS)
- Amazon VPC
- Subnets
- Route Tables
- Internet Gateway
- Security Groups
- AWS Management Console
- IPv4 networking

## Implementation Steps

### 1. Design the VPC Address Space

The first step was to define the VPC network before creating individual resources.

A planned CIDR range makes it easier to reason about subnet allocation and future expansion.

### 2. Create the VPC

The VPC was created as the logical network boundary for the lab.

This establishes the private address space in which the subnet resources are organized.

### 3. Create Subnets

Subnets were created within the VPC address space.

Subnetting separates resources into smaller network segments and provides a basis for controlling routing and resource placement.

### 4. Configure Route Tables

Route tables were configured to determine how traffic from the associated subnets should be forwarded.

The route-table configuration was reviewed to ensure that routes matched the intended architecture.

### 5. Configure Internet Connectivity

An Internet Gateway was configured where internet connectivity was required.

The gateway was associated with the VPC and referenced by the relevant routing configuration.

### 6. Configure Security Groups

Security groups were configured as network-level access controls for AWS resources.

Rules were considered in terms of:

- Source
- Destination
- Protocol
- Port
- Direction
- Required access

The goal was to avoid treating security groups as unrestricted connectivity mechanisms.

### 7. Verify the Configuration

Each major VPC component was reviewed after configuration:

- VPC
- Subnets
- Route tables
- Internet Gateway
- Security groups

Verification was performed before considering the lab complete.

### 8. Review the Final Architecture

The completed configuration was reviewed as one system rather than as individual AWS console pages.

This final review connected addressing, subnet placement, routing, internet connectivity, and security controls.

## Configuration / Technical Details

The lab demonstrates several important AWS networking relationships:

| Component | Role |
|---|---|
| VPC | Logical network boundary |
| Subnet | Network segment inside the VPC |
| Route Table | Determines traffic paths |
| Internet Gateway | Provides a path between the VPC and internet |
| Security Group | Controls allowed network traffic for associated resources |

The security model depends on the combination of network segmentation, routing, and traffic-control rules.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| VPC overview | `assets/01-vpc-overview.png` |
| VPC configuration | `assets/02-vpc-configuration.png` |
| Subnets | `assets/03-subnets.png` |
| Route table | `assets/04-route-table.png` |
| Internet Gateway | `assets/05-internet-gateway.png` |
| Security group | `assets/06-security-group.png` |
| Connectivity test | `assets/07-connectivity-test.png` |
| Final architecture | `assets/08-final-architecture.png` |

## Challenges

- Designing the address space before creating individual subnets.
- Understanding the relationship between subnets and route tables.
- Separating routing decisions from security-group controls.
- Ensuring internet connectivity was supported by the required combination of gateway and route configuration.
- Verifying the final architecture as an integrated cloud network.

## Lessons Learned

The project reinforced that cloud networking is built from interacting components. Creating a subnet does not by itself define how traffic should flow, and adding a route does not replace the need for appropriate traffic controls.

The lab also strengthened practical understanding of how traditional networking concepts such as CIDR addressing, segmentation, routing, and access control translate into AWS.

## Skills Demonstrated

- AWS VPC design
- Cloud networking
- CIDR and subnetting
- Route-table configuration
- Internet Gateway configuration
- Security Group configuration
- Cloud security fundamentals
- Network troubleshooting
- AWS Management Console

## Conclusion

The AWS VPC Security Lab establishes a practical foundation for cloud security engineering by connecting core networking concepts with AWS infrastructure. It provides the base knowledge required for later work involving IAM, compute security, logging, monitoring, and secure cloud architecture.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking