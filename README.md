# Microsoft Security Suite Guide

Welcome to the **Microsoft Security Suite Guide**! This repository is designed to provide you with comprehensive resources, cheat sheets, how-tos, and expert advice on using Microsoft's powerful security tools, including Microsoft Sentinel, Microsoft Defender, and more.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
3. [Microsoft Sentinel](#microsoft-sentinel)
   - [KQL](#kql)
   - [Threat Hunting](#threat-hunting)
   - [Best Practices](#best-practices)
4. [Microsoft Defender](#microsoft-defender)
   - [Defender for Endpoint](#defender-for-endpoint)
   - [Defender for Identity](#defender-for-identity)
   - [Defender for Cloud](#defender-for-cloud)
   - [Advanced Threat Protection](#advanced-threat-protection)
5. [DFIR / IR Best Practices](#dfir--ir-best-practices)
   - [Incident Response Process](#incident-response-process)
   - [DFIR Best Practices](#dfir-best-practices)
6. [Security Best Practices](#security-best-practices)
7. [Resources](#resources)
8. [License](#license)

---

## Introduction

Microsoft's security suite offers a range of tools and capabilities designed to help you protect your organization from threats, detect vulnerabilities, and respond to incidents effectively. This guide provides you with the resources you need to get the most out of these tools, whether you're a beginner or an experienced security professional.

---

## Getting Started

### Prerequisites

- **Microsoft 365 subscription** with access to security features.
- **Azure subscription** for Microsoft Sentinel.
- Basic understanding of cybersecurity principles.

### Installation

1. **Sign up for Microsoft 365 and Azure**:
   - [Microsoft 365](https://www.microsoft.com/microsoft-365)
   - [Azure](https://azure.microsoft.com)

2. **Access Microsoft Security Tools**:
   - **Microsoft Sentinel**: Enable in your Azure portal.
   - **Microsoft Defender**: Configure through the Microsoft 365 Security Center.

3. **Install Azure CLI (optional)**:

   ```bash
   curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
   az login

## Microsoft Sentinel

### KQL

**Kusto Query Language (KQL)** is the primary query language for Microsoft Sentinel, it is a powerful querying language for querying data and systems in your environment and can be used in Threat Hunting capabilities or to create detection rules.

### Threat Hunting
**Threat hunting** in Microsoft Sentinel involves proactively searching through logs and data for suspicious activities. Here's how you can start:

- Identify Hypotheses: Based on known threats or anomalies.
- Use KQL: Write queries to search for indicators of compromise (IOCs).
- Analyze Results: Look for patterns or anomalies.
- Take Action: Respond to any identified threats.

## Microsoft Defender

### Defender for Endpoint

Microsoft Defender for Endpoint provides advanced threat protection for endpoints. Key features include:

- **Endpoint Detection and Response (EDR):** Detect, investigate, and respond to threats.
- **Threat & Vulnerability Management:** Identify and remediate vulnerabilities.

#### Setup Guide

**Onboard Devices:**

- Use Group Policy or Intune for Windows devices.
- Deploy configuration profiles for macOS and Linux.

**Configure Alerts:**

- Set up alert notifications in the Defender portal.

**Automate Responses:**

- Use automated investigations to remediate threats.

### Defender for Identity

Defender for Identity helps protect your Active Directory from advanced attacks. Here's how to get started:

- **Install Sensors:** Deploy sensors on domain controllers.
- **Configure Alerts:** Customize alerts for suspicious activities.
- **Monitor Identity Activities:** Use the Defender for Identity dashboard.

### Defender for Cloud

Microsoft Defender for Cloud (formerly Azure Security Center) provides unified security management and threat protection. Key steps:

- **Enable Defender Plans:** Activate relevant security plans for your resources.
- **Implement Security Recommendations:** Follow guidance to secure your cloud infrastructure.
- **Respond to Alerts:** Use the Security Alerts page to investigate incidents.

### Advanced Threat Protection

Advanced Threat Protection (ATP) is an integral part of Microsoft’s security offerings. Here's a quick guide:

- **Enable ATP:** Configure ATP settings in Microsoft 365 Admin Center.
- **Analyze Threats:** Use threat intelligence to understand attacks.
- **Implement Policies:** Create policies for email protection, safe links, and safe attachments.

---

## DFIR / IR Best Practices Checklist

### Incident Response Process

#### Preparation
- [ ] **Develop an Incident Response Plan (IRP):** Ensure your IRP is comprehensive, up-to-date, and accessible.
- [ ] **Establish an Incident Response Team (IRT):** Clearly define roles and responsibilities.
- [ ] **Conduct Regular Training:** Perform drills and simulations to keep the team prepared.
- [ ] **Inventory Assets:** Maintain a current list of all assets, including hardware, software, and network devices.
- [ ] **Implement Security Controls:** Ensure baseline security measures are in place and effective.

#### Identification
- [ ] **Monitor Systems and Networks:** Use Security Information and Event Management (SIEM) tools to detect anomalies.
- [ ] **Alert Evaluation:** Analyze alerts to determine the validity and severity of potential incidents.
- [ ] **Classify the Incident:** Categorize the incident based on impact and urgency.
- [ ] **Document Initial Findings:** Record initial observations and evidence related to the incident.

#### Containment
- [ ] **Immediate Containment:** Apply temporary measures to prevent further damage (e.g., isolating affected systems).
- [ ] **Determine Containment Strategy:** Choose between short-term (e.g., disconnecting network access) and long-term strategies (e.g., implementing patches).
- [ ] **Preserve Evidence:** Ensure digital evidence is collected and preserved in its original state.
- [ ] **Implement Network Segmentation:** Restrict network access to prevent the lateral movement of threats.

#### Eradication
- [ ] **Identify Root Cause:** Analyze evidence to find the root cause of the incident.
- [ ] **Remove Malicious Artifacts:** Delete malware, unauthorized access points, or compromised credentials.
- [ ] **Apply Patches and Updates:** Ensure all systems are updated with the latest security patches.
- [ ] **Perform Vulnerability Scans:** Verify that vulnerabilities have been remediated.

#### Recovery
- [ ] **Restore Systems and Services:** Bring affected systems back online in a secure manner.
- [ ] **Validate System Integrity:** Conduct checks to ensure systems function correctly post-recovery.
- [ ] **Monitor for Recurrence:** Continue to monitor systems for any signs of further compromise.
- [ ] **Communicate with Stakeholders:** Inform relevant parties of recovery status and any changes made.

#### Lessons Learned
- [ ] **Conduct a Post-Incident Review:** Analyze the response process to identify strengths and weaknesses.
- [ ] **Document the Incident:** Record details, actions taken, and lessons learned for future reference.
- [ ] **Update the Incident Response Plan:** Make improvements based on findings from the review.
- [ ] **Share Findings:** Communicate lessons learned with the broader organization to enhance security awareness.

### DFIR Best Practices

#### Evidence Handling
- [ ] **Chain of Custody:** Maintain detailed records of evidence collection, storage, and handling.
- [ ] **Use Forensic Tools:** Utilize reliable tools to analyze data without altering it.
- [ ] **Secure Evidence Storage:** Ensure physical and digital evidence is stored securely and access is restricted.

#### Communication
- [ ] **Establish Communication Channels:** Use predefined channels for incident communications.
- [ ] **Provide Regular Updates:** Keep stakeholders informed with timely and accurate information.
- [ ] **Coordinate with External Entities:** Engage with law enforcement or third-party experts if necessary.

#### Threat Intelligence
- [ ] **Integrate Threat Intelligence:** Use intelligence feeds to inform and enhance the incident response process.
- [ ] **Analyze Threat Data:** Understand the nature and behavior of threats to inform response strategies.
- [ ] **Share Intelligence:** Collaborate with trusted partners and communities to share threat information.

#### Documentation
- [ ] **Keep Detailed Records:** Document all actions, decisions, and evidence throughout the incident lifecycle.
- [ ] **Use Standardized Templates:** Ensure consistency in documentation using predefined templates.
- [ ] **Maintain Accessibility:** Store documentation in a manner that is accessible for future reference and audits.

#### Continuous Improvement
- [ ] **Regularly Review Procedures:** Schedule periodic reviews of incident response procedures.
- [ ] **Implement Feedback:** Use insights from incidents to improve processes and capabilities.
- [ ] **Stay Informed:** Keep up-to-date with the latest threats and DFIR techniques.

---

## Security Best Practices

- **Multi-Factor Authentication (MFA):** Enable MFA for all users.
- **Conditional Access:** Use conditional access policies to secure access.
- **Regular Audits:** Conduct security audits to identify vulnerabilities.
- **Patch Management:** Keep systems up-to-date with the latest patches.
- **Employee Training:** Educate employees on security awareness.

---

## Resources

- [Microsoft Security Documentation](https://docs.microsoft.com/en-us/microsoft-365/security/)
- [Azure Sentinel Documentation](https://docs.microsoft.com/en-us/azure/sentinel/)
- [Microsoft Defender for Endpoint Documentation](https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/)
- [Incident Response Guide by NIST](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)
- [Digital Forensics Resource Center](https://www.sans.org/digital-forensics/)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


