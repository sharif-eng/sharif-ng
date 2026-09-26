# 📧 Email Header Analysis

<p align="center">
  <img src="https://img.shields.io/badge/Email%20Security-0078D4?style=for-the-badge" alt="Email Security" />
  <img src="https://img.shields.io/badge/Digital%20Investigation-5C2D91?style=for-the-badge" alt="Digital Investigation" />
  <img src="https://img.shields.io/badge/Completed-2E8B57?style=for-the-badge" alt="Completed" />
</p>

## Introduction

This project documents a practical email-header analysis workflow used to investigate suspicious or unusual email activity.

Email headers contain technical metadata that can help an analyst understand message routing, sender information, authentication results, timestamps, and other indicators relevant to an investigation. The project focuses on extracting and correlating these fields rather than relying only on the visible email content.

## Objectives

- Understand the structure of an email header.
- Identify important header fields used during investigations.
- Trace message routing information.
- Examine sender and recipient metadata.
- Review available authentication indicators.
- Identify technical information that can support an investigation.
- Organize findings into an analyst-friendly investigation record.

## Environment / Architecture

The project uses sample email-header data as the investigation artifact.

The analysis process can be summarized as:

**Raw Header → Header Parsing → Routing Analysis → Authentication Analysis → Indicators → Findings**

## Tools & Technologies

- Raw email headers
- Email security analysis
- Header field analysis
- Message routing analysis
- Authentication indicators
- Digital investigation techniques

## Implementation Steps

### 1. Obtain the Raw Header

The investigation begins with the raw email header rather than only the rendered email message.

Preserving the original header is important because the investigation depends on technical metadata contained within it.


![### 1. Obtain the Raw Header evidence](./assets/01-email-header.png)

### 2. Identify Core Header Fields

Relevant fields are reviewed, including:

- `From`
- `To`
- `Date`
- `Subject`
- `Message-ID`
- `Received`
- Authentication-related fields where present


![### 2. Identify Core Header Fields evidence](./assets/02-header-analysis.png)

### 3. Analyze Message Routing

The `Received` headers are examined to understand the path the message took through mail infrastructure.

Because email systems can add multiple `Received` entries, the analyst needs to interpret the sequence rather than treating one line in isolation.


![### 3. Analyze Message Routing evidence](./assets/04-routing-analysis.png)

### 4. Examine Sender Information

Sender-related fields are compared to identify inconsistencies or information requiring further investigation.

The visible sender address is not treated as sufficient evidence on its own.

### 5. Review Authentication Indicators

Where available, authentication results are examined to understand whether the message provides evidence related to sender-domain authentication.

These indicators are treated as investigation evidence rather than a complete verdict by themselves.


![### 5. Review Authentication Indicators evidence](./assets/03-authentication-analysis.png)

### 6. Extract Investigation Indicators

Potential indicators are organized from the header, such as:

- IP addresses
- Domains
- Mail servers
- Message identifiers
- Authentication results
- Timestamps


![### 6. Extract Investigation Indicators evidence](./assets/05-findings.png)

### 7. Correlate the Evidence

The individual fields are considered together to build a coherent interpretation of the message path and sender infrastructure.

### 8. Document Findings

The final investigation record should distinguish:

- Observed evidence
- Interpretation
- Indicators requiring additional investigation
- Limitations of the available header data

## Configuration / Technical Details

The analysis emphasizes evidence preservation and correlation.

A useful investigation table can contain:

| Field | Observation | Investigation Relevance |
|---|---|---|
| From | Sender information | Identity consistency |
| Received | Mail-routing information | Delivery path |
| Message-ID | Message identifier | Correlation |
| Authentication | Available results | Sender authentication context |
| Date | Timestamp | Timeline analysis |

## Screenshots & Evidence

Screenshots will be added to the `assets/` directory after the project evidence is uploaded.

| Evidence | Planned File |
|---|---|
| Raw email header | `assets/01-email-header.png` |
| Header analysis | `assets/02-header-analysis.png` |
| Authentication analysis | `assets/03-authentication-analysis.png` |
| Routing analysis | `assets/04-routing-analysis.png` |
| Investigation findings | `assets/05-findings.png` |

## Challenges

- Reading long and unfamiliar header fields without losing the investigation context.
- Understanding that different header fields serve different purposes.
- Correlating routing information across multiple `Received` entries.
- Separating observed evidence from assumptions.
- Presenting technical findings in a form that another analyst can review.

## Lessons Learned

Email investigation benefits from a structured approach. A header should be treated as a collection of evidence that must be correlated rather than as a single field that proves whether a message is legitimate or malicious.

The project also reinforced the importance of documenting uncertainty and preserving the original evidence used for analysis.

## Skills Demonstrated

- Email security analysis
- Header analysis
- Digital investigation
- IOC extraction
- Authentication analysis
- Timeline reasoning
- Evidence documentation
- SOC investigation fundamentals

## Conclusion

The project demonstrates a practical approach to analyzing email metadata during a security investigation. It strengthens the ability to extract technical evidence, correlate message-routing information, and document findings clearly.

## Project Status

**Completed**

## Author

**Angole Sharif Abubakar**  
BSc Computer Science | Cybersecurity | Cloud Security | Networking