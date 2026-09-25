# ☁️ AWS VPC Security Lab

<p align="center">
  <img src="https://img.shields.io/badge/AWS-VPC-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Cloud%20Security-232F3E?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Networking-1BA0D7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" />
</p>

## 👨‍💻 Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking

## 📌 Introduction

A practical AWS lab focused on designing and securing a **Virtual Private Cloud (VPC)**. The project demonstrates core cloud networking and security concepts including VPC structure, subnetting, routing, internet connectivity, and security controls.

AWS route tables determine where subnet traffic is directed, while security groups control allowed traffic to and from associated resources. citeturn0search0turn0search9

## 🎯 Objectives

- Create and configure an AWS VPC
- Understand VPC CIDR addressing and subnet design
- Configure subnets and route tables
- Configure internet connectivity
- Apply network access controls
- Verify network connectivity
- Document the security architecture

## 🛠️ Tools & Services

**Amazon VPC • Subnets • Route Tables • Internet Gateway • Security Groups • AWS Management Console**

## 🧭 Implementation Steps

### 1. Design the VPC
Defined the VPC network range and planned the subnet and routing structure.

### 2. Create the VPC
Created the VPC and established the base network environment.

### 3. Create Subnets
Created the required subnets within the VPC CIDR range. Each subnet is associated with a route table that controls its routing behavior. citeturn0search1

### 4. Configure Route Tables
Configured routes for the required network paths and associated the appropriate route table with the subnet. AWS route tables contain destination and target information that controls traffic forwarding. citeturn0search2

### 5. Configure Internet Connectivity
Configured the Internet Gateway and the required route for internet-bound traffic where applicable.

### 6. Configure Security Groups
Applied security-group rules to control permitted inbound and outbound traffic. Security groups operate as a virtual firewall for associated resources. citeturn0search9

### 7. Verify the Configuration
Checked the VPC, subnet associations, route tables, security rules, and connectivity to confirm the intended architecture.

## 📸 Evidence

Screenshots will be stored in the **assets/** folder.

- assets/01-vpc-overview.png
- assets/02-vpc-configuration.png
- assets/03-subnets.png
- assets/04-route-table.png
- assets/05-internet-gateway.png
- assets/06-security-group.png
- assets/07-connectivity-test.png
- assets/08-final-architecture.png

## ⚠️ Challenges

The main practical challenge was understanding how the AWS networking components work together. A VPC configuration can appear correct while traffic still fails if subnet associations, routes, gateway configuration, or security rules are inconsistent.

## 📚 Lessons Learned

- A VPC is a network boundary, not a complete network configuration by itself.
- Subnets, route tables, gateways, and security controls must work together.
- Routing determines where traffic can go, while security controls determine what traffic is permitted.
- Explicit subnet-to-route-table associations make the intended routing structure easier to understand and manage. citeturn0search1turn0search3
- Cloud networking fundamentals are closely connected to cloud security.

## 🧠 Skills Demonstrated

**AWS VPC • Cloud Networking • CIDR Addressing • Subnetting • Route Tables • Internet Gateway • Security Groups • Network Security • Cloud Troubleshooting • Secure Architecture**

## ✅ Conclusion

This project provided hands-on experience designing and securing an AWS network environment. It strengthened my understanding of how cloud networking components interact and created a foundation for more advanced AWS security work.

## 📌 Project Status

**Completed**
