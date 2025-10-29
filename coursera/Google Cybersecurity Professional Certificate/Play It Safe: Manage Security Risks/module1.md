# Module 1: Security Domains

> *Created: 29 October 2025 | Last Updated: 29 October 2025*

## Navigation

- [Introduction to Security Domains](#introduction-to-security-domains)
- [CISSP Security Domains](#cissp-security-domains)
  - [Security and Risk Management](#1-security-and-risk-management)
  - [Asset Security](#2-asset-security)
  - [Security Architecture and Engineering](#3-security-architecture-and-engineering)
  - [Communication and Network Security](#4-communication-and-network-security)
  - [Identity and Access Management](#5-identity-and-access-management)
  - [Security Assessment and Testing](#6-security-assessment-and-testing)
  - [Security Operations](#7-security-operations)
  - [Software Development Security](#8-software-development-security)
- [Threats, Risks, and Vulnerabilities](#threats-risks-and-vulnerabilities)
  - [Understanding Key Concepts](#understanding-key-concepts)
  - [Risk Management Strategies](#risk-management-strategies)
  - [Common Risk Factors](#common-risk-factors)
  - [Notable Vulnerabilities](#notable-vulnerabilities)
- [NIST Risk Management Framework](#nist-risk-management-framework-rmf)
- [Impacts and Consequences](#impacts-and-consequences)
- [Glossary](#glossary)
- [Resources](#resources)

---

## Introduction to Security Domains

As an analyst, you can explore various areas of cybersecurity that interest you. One way to explore those areas is by understanding different security domains and how they're used to organize the work of security professionals. In this reading, you will learn more about CISSP's eight security domains and how they relate to the work you'll do as a security analyst.

---

## CISSP Security Domains

### 1. Security and Risk Management

**Security posture** is an organization's ability to manage its defense of critical assets and data and react to change.

**Key Elements:**
- Security goals and objectives
- Risk mitigation processes
- Compliance
- Business continuity plans
- Legal regulations
- Professional and organizational ethics

**Information Security (InfoSec)** processes include:
- Incident response
- Vulnerability management
- Application security
- Cloud security
- Infrastructure security

*Example: Adapting PII handling to comply with GDPR*

[Back to top](#module-1-security-domains)

### 2. Asset Security

Manages cybersecurity processes for organizational assets, including storage, maintenance, retention, and destruction of physical and virtual data.

**Key Activities:**
- Security impact analysis
- Recovery planning
- Data exposure management
- Backup creation and management

[Back to top](#module-1-security-domains)

### 3. Security Architecture and Engineering

Focuses on managing data security through effective tools, systems, and processes.

**Key Principles:**
- **Shared responsibility**: All individuals actively lower risk
- Threat modeling
- Least privilege
- Defense in depth
- Fail securely
- Separation of duties
- Zero trust
- Trust but verify

*Example: Using SIEM tools to monitor unusual login activity*

[Back to top](#module-1-security-domains)

### 4. Communication and Network Security

Manages and secures physical networks and wireless communications, including on-site, remote, and cloud communications.

**Key Focus:** Designing network security controls for secure remote access.

[Back to top](#module-1-security-domains)

### 5. Identity and Access Management (IAM)

Keeps data secure by ensuring user identities are trusted and authenticated.

**Principle of Least Privilege:** Granting only minimal access required to complete tasks.

*Example: Limiting customer service access to customer data only during issue resolution*

[Back to top](#module-1-security-domains)

### 6. Security Assessment and Testing

Identifies and mitigates risks, threats, and vulnerabilities through security assessments and penetration testing.

**Key Activities:**
- Security control testing
- Data collection and analysis
- Security audits
- User permission validation

[Back to top](#module-1-security-domains)

### 7. Security Operations

Investigates potential breaches and implements preventative measures after security incidents.

**Tools and Processes:**
- Training and awareness
- Intrusion detection/prevention
- SIEM tools
- Log management
- Incident management
- Playbooks
- Post-breach forensics

[Back to top](#module-1-security-domains)

### 8. Software Development Security

Uses secure programming practices to create secure applications throughout the software development life cycle.

**Key Requirements:**
- Security integration at each development stage
- Application security testing
- Quality assurance
- Performance standards validation

*Example: Ensuring proper encryption configuration for medical devices*

[Back to top](#module-1-security-domains)

---

## Threats, Risks, and Vulnerabilities

### Understanding Key Concepts

**Threat:** Any circumstance or event that can negatively impact assets
- *Examples:* Insider threats, Advanced Persistent Threats (APTs)

**Risk:** Anything that can impact the confidentiality, integrity, or availability of an asset
- *Formula:* Risk = Likelihood of a threat

**Vulnerability:** A weakness that can be exploited by a threat

[Back to top](#module-1-security-domains)

### Risk Management Strategies

- **Acceptance:** Accepting risk to maintain business continuity
- **Avoidance:** Creating plans to avoid risks
- **Transference:** Transferring risk to third parties
- **Mitigation:** Lessening impact of known risks

[Back to top](#module-1-security-domains)

### Common Risk Factors

- **External risk:** Threats outside the organization
- **Internal risk:** Current/former employees, vendors, partners
- **Legacy systems:** Outdated but still operational systems
- **Multiparty risk:** Third-party vendor access
- **Software compliance:** Unupdated or non-compliant software

[Back to top](#module-1-security-domains)

### Notable Vulnerabilities

- **ProxyLogon:** Microsoft Exchange server vulnerability
- **ZeroLogon:** Netlogon authentication protocol weakness
- **Log4Shell:** Remote code execution in Java applications
- **PetitPotam:** Windows NTLM authentication manipulation
- **Security logging failures:** Insufficient monitoring capabilities

[Back to top](#module-1-security-domains)

---

## NIST Risk Management Framework (RMF)

### The Seven-Step Process

1. **Prepare**  
   Manage security and privacy risks before breaches occur

2. **Categorize**  
   Develop risk management processes and tasks

3. **Select**  
   Choose, customize, and document protective controls

4. **Implement**  
   Execute security and privacy plans

5. **Assess**  
   Determine if controls are implemented correctly

6. **Authorize**  
   Account for existing security and privacy risks

7. **Monitor**  
   Maintain awareness of system operations

[Back to top](#module-1-security-domains)

---

## Impacts and Consequences

### Three Key Impact Areas

1. **Financial Impact**
   - Interrupted production
   - Correction costs
   - Compliance fines

2. **Identity Theft**
   - PII exposure through dark web sales
   - Data breaches and leaks

3. **Reputation Damage**
   - Customer loss
   - Negative publicity
   - Legal penalties

### Web Layers and Ransomware

**Web Layers:**
- Surface web: Browser-accessible content
- Deep web: Authorization-required content (intranets)
- Dark web: Special software required (often illicit)

**Ransomware:** Malicious attacks encrypting data for ransom payments

[Back to top](#module-1-security-domains)

---

## Glossary

**A**  
**Assess:** Determine if controls are implemented correctly (NIST RMF Step 5)  
**Authorize:** Account for security and privacy risks (NIST RMF Step 6)

**B**  
**Business continuity:** Maintain productivity through disaster recovery plans

**C**  
**Categorize:** Develop risk management processes (NIST RMF Step 2)

**E**  
**External threat:** Anything outside the organization harming assets

**I**  
**Implement:** Execute security and privacy plans (NIST RMF Step 4)  
**Internal threat:** Employee/vendor/partner posing security risk

**M**  
**Monitor:** Maintain system operation awareness (NIST RMF Step 7)

**P**  
**Prepare:** Manage risks before breaches occur (NIST RMF Step 1)

**R**  
**Ransomware:** Data encryption attack demanding payment  
**Risk:** Impact on asset confidentiality, integrity, or availability  
**Risk mitigation:** Procedures to quickly reduce risk impact

**S**  
**Security posture:** Ability to manage defense and react to change  
**Select:** Choose and document protective controls (NIST RMF Step 3)  
**Shared responsibility:** All individuals actively lower risk  
**Social engineering:** Human error exploitation for information access

**V**  
**Vulnerability:** Weakness exploitable by threats

[Back to top](#module-1-security-domains)

---

## Resources

- [OWASP Top Ten](https://owasp.org/www-project-top-ten/)
- [NIST RMF](https://csrc.nist.gov/projects/risk-management)
- NIST National Vulnerability Database
- CISA Known Exploited Vulnerabilities Catalog

[Back to top](#module-1-security-domains)
