# Internal Security Audit & Risk Assessment: Botium Toys

## Executive Summary
This project consists of a comprehensive internal security audit and risk assessment conducted for Botium Toys. The objective was to evaluate the organization's current security posture, identify critical vulnerabilities in asset management and access controls, and align operational practices with the NIST Cybersecurity Framework (NIST CSF). This audit provides actionable remediation strategies to mitigate business risks and ensure compliance with industry standards.

---

## Business Objectives & Scope

### Operational Scope
*   Review of corporate infrastructure, including employee devices (physical and remote), network protocols, and storage solutions.
*   Assessment of internal access management policies and user privileges.
*   Evaluation of current compliance with relevant data privacy regulations (GDPR, PCI-DSS).

### Business Goals
*   Establish robust security controls to safeguard proprietary intellectual property.
*   Protect customer Personally Identifiable Information (PII) and financial transaction data.
*   Ensure continuous business availability and minimize the risk of operational disruption from ransomware or data breaches.

---

## Framework Alignment: NIST CSF
The audit evaluated current practices against the core functions of the **NIST Cybersecurity Framework**:

### 1. Identify
*   **Current State:** Botium Toys lacks a centralized, up-to-date asset inventory, making it difficult to account for all hardware, software, and data locations.
*   **Risk:** Untracked assets may run legacy software, introducing unpatched vulnerabilities into the corporate network.

### 2. Protect
*   **Current State:** Multi-Factor Authentication (MFA) is not enforced globally, and password complexity rules are weak. Legacy, unencrypted protocols are active on the internal network.
*   **Risk:** High susceptibility to credential stuffing, brute-force attacks, and network sniffing/interception.

### 3. Detect
*   **Current State:** Intrusion Detection Systems (IDS) and centralized log management (SIEM) are not fully deployed across all network segments.
*   **Risk:** Security incidents could go unnoticed for extended periods, maximizing potential adversary dwell time.

### 4. Respond
*   **Current State:** The organization lacks a formalized, documented Incident Response Plan (IRP) and an assigned response team.
*   **Risk:** Confused, delayed, or ineffective handling of an active breach, potentially compounding financial and legal damages.

### 5. Recover
*   **Current State:** While backups exist, they are not stored immutable/offsite, and restoration procedures are not regularly tested.
*   **Risk:** Ransomware could compromise online backups, leaving the business unable to recover critical data.

---

## Controls Assessment (Current vs. Target)

| Security Control Category | Current Status | Target Implementation |
| :--- | :--- | :--- |
| **Asset Management** | ❌ Incomplete / Manual | Deploy automated asset discovery and inventory tools. |
| **Access Control (MFA)** | ❌ Not enforced | Mandatory MFA integration across all corporate endpoints and IAM roles. |
| **Network Encryption** | ❌ Legacy protocols active | Deprecate unencrypted protocols; enforce TLS 1.3 and SSH. |
| **Log Monitoring** |  Partial coverage | Establish centralized SIEM log aggregation and alerting. |
| **Incident Response** | ❌ No documented plan | Author and operationalize an Incident Response Plan (IRP). |

---

## Actionable Recommendations

### 1. Immediate Actions (High Priority)
*   **Enforce Multi-Factor Authentication:** Deploy MFA through an Identity Provider (IdP) for all remote connections, email access, and privileged accounts.
*   **Patch & Protocol Management:** Disable legacy, plaintext communication protocols and run a comprehensive vulnerability scan on all external-facing systems.

### 2. Short-Term Actions (Medium Priority)
*   **Formalize an Incident Response Plan:** Draft an explicit step-by-step playbook detailing communication trees, roles, and containment procedures during a breach.
*   **Network Segmentation:** Segregate the cardholder data environment (CDE) to reduce the scope of PCI-DSS compliance and protect transaction data.

### 3. Long-Term Actions (Strategic)
*   **Security Awareness Training:** Launch recurring phishing simulations and data privacy hygiene training for all employees.
*   **Business Continuity Testing:** Schedule bi-annual backup restoration drills to guarantee reliable disaster recovery capabilities.
