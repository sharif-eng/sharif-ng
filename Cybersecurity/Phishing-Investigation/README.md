# 🎣 Phishing Investigation

<p align="center">
  <img src="https://img.shields.io/badge/Phishing%20Investigation-D9534F?style=for-the-badge" alt="Phishing Investigation" />
  <img src="https://img.shields.io/badge/SOC%20Analysis-111111?style=for-the-badge" alt="SOC Analysis" />
  <img src="https://img.shields.io/badge/Email%20Security-0078D4?style=for-the-badge" alt="Email Security" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project documents a structured phishing investigation workflow for analyzing a suspicious email and the technical indicators associated with it.

The investigation focuses on recognizing phishing indicators, examining URLs and domains, extracting indicators of compromise, mapping observed behavior to relevant attack techniques, and documenting the evidence used to reach an investigation finding.

## Objectives

- Identify common phishing indicators in a suspicious message.
- Examine suspicious URLs and domains.
- Extract relevant indicators of compromise.
- Analyze the relationship between the email, URLs, and domains.
- Identify attack techniques represented by the observed behavior.
- Organize evidence into a repeatable SOC investigation workflow.
- Produce clear investigation findings.

## Environment / Architecture

The investigation follows this workflow:

**Suspicious Email → Indicator Extraction → URL Analysis → Domain Analysis → Technique Mapping → Findings**

The project is designed around defensive investigation rather than interacting with suspicious infrastructure unnecessarily.

## Tools & Technologies

- Email security analysis
- URL analysis
- Domain analysis
- IOC extraction
- Phishing investigation methodology
- SOC investigation concepts
- MITRE ATT&CK-style technique mapping

## Implementation Steps

### 1. Preserve the Suspicious Email

The original suspicious message is treated as the primary investigation artifact.

Relevant content and metadata are preserved before analysis so that the investigation remains evidence-based.


![### 1. Preserve the Suspicious Email evidence](./assets/01-suspicious-email.png)

### 2. Identify Phishing Indicators

The message is reviewed for indicators such as:

- Suspicious sender information
- Unexpected requests
- Urgency or pressure
- Suspicious links
- Mismatched domains
- Unusual formatting or wording
- Requests for credentials or sensitive information

The presence of one indicator is not automatically treated as proof. Indicators are correlated.


![### 2. Identify Phishing Indicators evidence](./assets/02-phishing-indicators.png)

### 3. Extract URLs and Domains

Links and domains contained in the message are identified and separated into investigation artifacts.

The purpose is to understand what infrastructure the message attempts to direct the recipient toward.

### 4. Analyze the URLs

The URLs are reviewed for characteristics that may indicate suspicious behavior, including:

- Domain mismatches
- Unusual paths
- Obfuscation
- Unexpected redirects
- Credential-collection patterns


![### 4. Analyze the URLs evidence](./assets/03-url-analysis.png)

### 5. Analyze Domains

The associated domains are examined as separate indicators.

Domain analysis helps distinguish the visible branding or sender identity from the infrastructure referenced by the message.


![### 5. Analyze Domains evidence](./assets/04-domain-analysis.png)

### 6. Extract Indicators of Compromise

Relevant indicators are organized into categories such as:

| Indicator Type | Example Evidence |
|---|---|
| Email | Sender or message metadata |
| URL | Suspicious link |
| Domain | Referenced domain |
| IP | Address if present in the evidence |
| Hash | File hash if an attachment exists |

Only indicators actually present in the investigation evidence should be recorded.

### 7. Map Observed Techniques

Observed behaviors can be mapped to relevant phishing or credential-access techniques where the evidence supports the mapping.

The goal is to describe what the message attempts to achieve rather than assigning a technique without supporting evidence.

### 8. Document the Investigation Finding

The final record should clearly separate:

- Evidence observed
- Indicators extracted
- Analysis performed
- Technique mapping
- Investigation conclusion
- Recommended defensive action


![### 8. Document the Investigation Finding evidence](./assets/05-investigation-findings.png)

## Configuration / Technical Details

The investigation uses a simple analyst workflow:

1. Preserve evidence.
2. Identify suspicious characteristics.
3. Extract indicators.
4. Analyze URLs and domains.
5. Correlate findings.
6. Map supported techniques.
7. Document the result.

This workflow can be adapted to phishing triage in a SOC environment.

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| Suspicious email | `assets/01-suspicious-email.png` |
| Phishing indicators | `assets/02-phishing-indicators.png` |
| URL analysis | `assets/03-url-analysis.png` |
| Domain analysis | `assets/04-domain-analysis.png` |
| Investigation findings | `assets/05-investigation-findings.png` |

## Challenges

- Distinguishing meaningful phishing indicators from ordinary email characteristics.
- Correlating sender, URL, and domain information.
- Avoiding conclusions based on a single suspicious-looking field.
- Organizing technical indicators into a clear investigation record.
- Mapping behavior to techniques only when the evidence supports the mapping.

## Lessons Learned

Phishing analysis is strongest when multiple indicators are correlated. Sender information, URLs, domains, message content, and available metadata should be considered together.

The project also reinforced the importance of documenting exactly what was observed and separating evidence from interpretation.

## Skills Demonstrated

- Phishing analysis
- Email security
- IOC extraction
- URL analysis
- Domain analysis
- SOC triage
- Threat investigation
- MITRE ATT&CK-style technique mapping
- Security documentation

## Conclusion

The phishing investigation project demonstrates a repeatable defensive workflow for moving from a suspicious email to structured evidence and documented findings. It supports practical SOC skills in email analysis, indicator extraction, and investigation reporting.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking