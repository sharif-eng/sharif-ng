# 🐉 Kali Linux & Metasploitable Cybersecurity Lab

<p align="center">
  <img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux" />
  <img src="https://img.shields.io/badge/Metasploitable-CC0000?style=for-the-badge" alt="Metasploitable" />
  <img src="https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project is a controlled penetration-testing and vulnerability-assessment lab built with Kali Linux and Metasploitable in VirtualBox.

The purpose of the lab is to practice the security-testing workflow against an intentionally vulnerable target without exposing real systems to testing. The work covers reconnaissance, service enumeration, vulnerability assessment, controlled exploitation, and basic web application testing.

## Objectives

- Build an isolated security-testing environment.
- Establish network connectivity between the attacker and target systems.
- Perform reconnaissance and service enumeration.
- Identify exposed services and potential weaknesses.
- Use controlled exploitation techniques against the intentionally vulnerable target.
- Practice web application security testing.
- Capture evidence from each stage of the assessment.
- Document the relationship between reconnaissance, exploitation, and findings.

## Environment / Architecture

The environment consists of:

- Kali Linux as the security-testing workstation.
- Metasploitable as the intentionally vulnerable target.
- Oracle VirtualBox as the virtualization platform.
- An isolated virtual network connecting the two systems.

The separation of the lab from production systems is important because the testing activities are deliberately intrusive.

## Tools & Technologies

- Kali Linux
- Metasploitable
- VirtualBox
- Nmap
- Metasploit Framework
- Burp Suite
- Wireshark
- TCP/IP networking

## Implementation Steps

### 1. Prepare the Virtual Lab

Kali Linux and Metasploitable were deployed as virtual machines in VirtualBox.

The first priority was establishing an isolated network where the two systems could communicate without targeting external systems.

### 2. Verify Network Configuration

The IP configuration of both systems was checked before beginning security testing.

Basic connectivity was verified to ensure that the target was reachable from Kali.

### 3. Perform Reconnaissance

Initial reconnaissance was used to identify the target and establish an understanding of the lab environment.

The objective at this stage was discovery rather than exploitation.

### 4. Enumerate Services

Nmap was used to identify listening services and exposed ports.

Example command structure:

```text
nmap <target-ip>
```

Additional enumeration can be used where appropriate to identify service versions and improve understanding of the attack surface.

### 5. Assess the Attack Surface

The discovered services were reviewed to identify areas that required further investigation.

This stage connects reconnaissance results with potential vulnerabilities instead of immediately attempting exploitation.

### 6. Perform Controlled Exploitation

Metasploit was used within the isolated lab to test selected vulnerabilities on the intentionally vulnerable Metasploitable target.

The objective was to understand how an exposed service can progress from discovery to exploitation in a controlled environment.

### 7. Perform Web Application Testing

Burp Suite was used to inspect and test web application behavior available in the lab.

The focus was on understanding requests, responses, application inputs, and common web-security weaknesses.

### 8. Capture Network Evidence

Wireshark was used where useful to inspect network traffic and understand how reconnaissance or application interactions appear at the packet level.

### 9. Document Findings

Findings were organized around:

- Target and scope
- Discovered services
- Potential vulnerabilities
- Testing performed
- Evidence collected
- Security implications
- Lessons learned

## Configuration / Technical Details

The lab follows a simplified assessment workflow:

**Reconnaissance → Enumeration → Vulnerability Assessment → Controlled Exploitation → Web Testing → Evidence Collection → Documentation**

The project is intentionally performed against a vulnerable training target so that exploitation techniques can be studied without unauthorized access to real systems.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| VirtualBox lab environment | `assets/01-virtualbox-lab.png` |
| Kali Linux system | `assets/02-kali-linux.png` |
| Metasploitable target | `assets/03-metasploitable.png` |
| Network configuration | `assets/04-network-configuration.png` |
| Connectivity test | `assets/05-connectivity-test.png` |
| Nmap enumeration | `assets/06-nmap-enumeration.png` |
| Service enumeration | `assets/07-service-enumeration.png` |
| Vulnerability assessment | `assets/08-vulnerability-assessment.png` |
| Metasploit testing | `assets/09-metasploit-testing.png` |
| Web application testing | `assets/10-web-application-testing.png` |
| Assessment workflow | `assets/11-cyber-kill-chain.png` |

## Challenges

- Maintaining an isolated and predictable lab network.
- Interpreting scan results rather than treating every open port as a vulnerability.
- Moving from enumeration to testing in a controlled and documented manner.
- Correlating application-level behavior with network-level observations.
- Keeping evidence organized across multiple stages of the assessment.

## Lessons Learned

The lab demonstrated that penetration testing is a process rather than a single exploitation step. Good reconnaissance and enumeration provide the context required to choose appropriate tests.

It also reinforced the importance of authorization, scope, evidence collection, and clear reporting when performing security assessments.

## Skills Demonstrated

- Linux security tooling
- Network reconnaissance
- Port and service enumeration
- Vulnerability assessment
- Controlled penetration testing
- Metasploit fundamentals
- Web application testing
- Packet analysis
- Security documentation

## Conclusion

The Kali Linux and Metasploitable lab provides a controlled environment for practicing offensive-security fundamentals. It strengthens the ability to move from discovery to evidence-based security testing while maintaining a clear distinction between authorized lab activity and real-world systems.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking