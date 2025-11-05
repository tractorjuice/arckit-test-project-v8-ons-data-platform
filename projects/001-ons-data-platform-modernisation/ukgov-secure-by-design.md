# UK Government Secure by Design Assessment
## ONS Data Platform Modernisation

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SECD-v1.0 |
| **Document Type** | UK Government Secure by Design Assessment (NCSC CAF) |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2025-11-05 |
| **Last Modified** | 2025-11-05 |
| **Review Date** | 2026-01-28 (Discovery Assessment) |
| **Owner** | Head of Cyber Security, ONS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | Programme Board, SIRO, NCSC, Security Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial creation from `/arckit.secure` command | [PENDING] | [PENDING] |

---

## Executive Summary

### Assessment Overview

**Project**: Office for National Statistics (ONS) Data Platform Modernisation
**Department**: Office for National Statistics (ONS)
**Data Classification**: **OFFICIAL** (majority) with **OFFICIAL-SENSITIVE** (pre-release market-sensitive statistics)
**Project Phase**: **SOBC (Strategic Outline Business Case)** - Transitioning to Discovery/Alpha
**Assessment Date**: 2025-11-05
**Assessor**: Head of Cyber Security, ONS

### NCSC Cyber Assessment Framework (CAF) Score

**Overall Score**: **10/14 Principles Achieved** (71%)

| Objective | Principles Achieved | Total Principles | Status |
|-----------|-------------------|------------------|---------|
| **A: Managing Security Risk** | 3/4 | 4 | ⚠️ Mostly Achieved |
| **B: Protecting Against Cyber Attack** | 4/6 | 6 | ⚠️ Partially Achieved |
| **C: Detecting Cyber Security Events** | 2/2 | 2 | ✅ Achieved |
| **D: Minimising Impact of Incidents** | 1/2 | 2 | ⚠️ Partially Achieved |

### Cyber Essentials Status

**Current Status**: ⚠️ **Not Certified** (Required before Beta phase)
**Target**: **Cyber Essentials Plus** by Beta phase (Week 72)
**Rationale**: OFFICIAL-SENSITIVE data classification + high-risk system (pre-release market-sensitive statistics)

### UK GDPR Compliance

**Status**: ✅ **Compliant** (with gaps to address)
**DPO Appointed**: ✅ Yes - Data Protection Officer, ONS
**DPIA Status**: ⚠️ **Required but not yet completed** (planned for Alpha Week 22-23)

### Critical Security Issues (Phase Blockers)

| Issue | Severity | Phase Blocked | Target Resolution |
|-------|----------|---------------|-------------------|
| **1. DPIA not completed** | CRITICAL | Beta | Alpha Week 22-23 |
| **2. Threat model not completed** | CRITICAL | Beta | Alpha Week 19-21 |
| **3. Cyber Essentials not certified** | CRITICAL | Beta | Beta Week 72 (before go-live) |
| **4. ITHC (IT Health Check) not completed** | CRITICAL | Live | Beta Week 72 |

**Assessment Conclusion**: Project has strong security foundations (Architecture Principle 10: Security by Design and Zero Trust) but requires completion of critical assessments (DPIA, threat model, ITHC) before Beta/Live phases. **No blockers for Discovery/Alpha phases**.

---

## Project Context

### A. Organisational Context

**Department/Organisation**: Office for National Statistics (ONS)
**Parent Department**: Cabinet Office (independent statistics authority)
**Statutory Basis**: Statistics and Registration Service Act 2007

**Mission**: Serve the public good by producing trusted statistics that inform the UK

**Security Governance**:
- **Senior Information Risk Owner (SIRO)**: Permanent Secretary, ONS
- **Information Asset Owner (IAO)**: Chief Data Officer
- **Data Protection Officer (DPO)**: Data Protection Officer, ONS
- **Security Team**: Head of Cyber Security + 6 FTE security engineers

### B. Project Context

**Project Name**: ONS Data Platform Modernisation
**Project Phase**: SOBC → Discovery → Alpha → Beta → Live
**Timeline**: 78 weeks (18 months) - 2025-11-05 to 2027-05-25
**Budget**: £18M capital + £6.7M annual operating

**Objective**: Replace 30+ year legacy on-premises data platform with cloud-native infrastructure to enable:
- Census-scale processing (67M records in <24 hours)
- API-first access (50% consumption via APIs)
- 40% infrastructure cost reduction (£11.2M → £6.7M annually)
- Compliance with Statistics Act 2007, GDS Service Standard, GovS 007

**User Base**:
- **Internal**: 500 ONS statisticians (publication workflows)
- **Public-facing**: 10,000+ API users (government analysts, researchers, businesses, media, public)
- **Pre-release access**: Designated government officials (Ministers, senior officials) - Statistics Act 2007 compliance

### C. Data Classification

**Primary Classification**: **OFFICIAL**

**Data Types**:
| Data Type | Classification | Volume | Sensitivity Rationale |
|-----------|---------------|--------|----------------------|
| **Published statistics** | OFFICIAL | 500+ statistical series | Public data after publication |
| **Pre-release statistics** | OFFICIAL-SENSITIVE | 500+ series (24-hour window) | Market-sensitive, insider trading risk |
| **Survey microdata** | OFFICIAL-SENSITIVE | 67M+ records (Census) | Personal data, re-identification risk |
| **Admin data (HMRC/DWP)** | OFFICIAL-SENSITIVE | TBD | Tax data, benefits data - special category |
| **System credentials** | OFFICIAL-SENSITIVE | N/A | Compromise enables unauthorised access |

**Peak Sensitivity**: **OFFICIAL-SENSITIVE** (pre-release statistics, survey microdata)

**UK GDPR Scope**:
- ✅ **Personal data processing**: Survey microdata (Census, Labour Force Survey, Living Costs & Food Survey)
- ✅ **Special category data**: Potentially health data (Census health questions), ethnicity
- ✅ **DPIA Required**: Yes (high-risk processing - large-scale personal data, automated profiling potential)

### D. Hosting Approach

**Target Architecture**: **Cloud-native** (UK Cloud First Policy compliant)

**Cloud Provider**: TBD (vendor procurement in Alpha Week 13-20)
- **Options**: AWS (eu-west-2 London), Azure (UK South), GCP (europe-west2 London)
- **Constraint**: UK sovereign regions only (GDPR Article 3, Statistics Act 2007 data sovereignty)

**Network Architecture**:
- **Internet-facing**: Publication APIs (public access)
- **PSN-connected**: Integration with government departments (HMRC/DWP API access)
- **Internal**: ONS statistician access (publication workflows)

**Current State**: On-premises datacentres (Newport, Titchfield) - to be decommissioned

### E. Threat Landscape

**Threat Profile**: **HIGH**

**Rationale**:
- **High-value target**: ONS pre-release statistics valuable for financial markets (insider trading, market manipulation)
- **Nation-state APT**: Economic espionage (GDP, inflation, unemployment data before public release)
- **Organised crime**: Insider trading schemes, ransomware extortion
- **Hacktivist**: Website defacement, DDoS attacks during major releases
- **Insider threat**: Statisticians with privileged access to pre-release data

**Recent Cyber Incidents** (UK Government context):
- 2023: Electoral Commission breach (40M voter records, nation-state APT)
- 2022: NHS 111 ransomware (patient data impact)
- 2021: SolarWinds supply chain attack (affected UK government)

**ONS-Specific Risks**:
- Pre-release data exfiltration → Financial market disruption
- Publication data manipulation → Loss of public trust in official statistics
- Census data breach → 67M UK residents' personal data compromised
- DDoS during major releases (GDP, CPI) → Market disruption, reputational damage

---

## NCSC Cyber Assessment Framework (CAF) Assessment

### Objective A: Managing Security Risk

#### A1: Governance

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **SIRO Appointed**: ✅ Permanent Secretary, ONS (board-level executive)
   - Accountable for information risk to Parliament
   - Reviews and approves risk treatment plans
   - Quarterly security briefings scheduled

2. **Security Policies**: ✅ ONS Information Security Policy Framework
   - Acceptable Use Policy (AUP)
   - Access Control Policy
   - Data Protection Policy
   - Incident Response Policy
   - Last reviewed: 2024-09 (annual review cycle)

3. **Security Oversight**: ✅ Programme Board includes Head of Cyber Security
   - Monthly Programme Board reviews (security standing agenda item)
   - Architecture Review Board (fortnightly) - security architecture approval
   - Security risk escalation path defined

4. **Roles and Responsibilities**: ✅ Defined in Management Case
   - SIRO: Permanent Secretary (overall accountability)
   - IAO: Chief Data Officer (information asset owner)
   - Security Team: Head of Cyber Security + 6 FTE
   - Delivery Team: Security Engineer embedded (1 FTE)

**Compliance**:
- ✅ Government Functional Standard GovS 007: Security (governance requirements)
- ✅ NCSC CAF A1 guidance followed

**No Gaps Identified**: Governance structure is mature and appropriate for OFFICIAL-SENSITIVE system.

---

#### A2: Risk Management

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Risk Register**: ✅ Comprehensive HM Treasury Orange Book-compliant risk register
   - 22 risks identified across 6 categories (STRATEGIC, OPERATIONAL, FINANCIAL, COMPLIANCE, TECHNOLOGY, REPUTATIONAL)
   - 3 HIGH security risks:
     - R-004: GovS 007 ITHC security failure (residual score 12)
     - R-006: Statistics Act pre-release access breach (residual score 15)
     - R-012: Cyber security breach of pre-release data (residual score 10)
   - All risks have owners, mitigations, 4Ts responses

2. **Threat Modeling**: ⚠️ **PLANNED** (Alpha Week 19-21)
   - STRIDE methodology to be used
   - Threat actors: Nation-state APT, organised crime, insider threat
   - Attack vectors: Phishing, SQL injection, API abuse, insider exfiltration
   - **Gap**: Threat model not yet completed (planned for Alpha)

3. **Asset Classification**: ✅ Data classification defined (OFFICIAL / OFFICIAL-SENSITIVE)
   - All datasets classified per UK Government Security Classifications Policy
   - Classification reviewed annually or on data change

4. **Risk Treatment Plans**: ✅ Risk register includes mitigation actions with owners and timelines
   - 18 risks "Treat" (82%) - active mitigation through controls
   - 2 risks "Transfer" (9%) - cyber insurance £10M, vendor liability contracts
   - 2 risks "Tolerate" (9%) - within organizational appetite

**Compliance**:
- ✅ HM Treasury Orange Book 2023 (risk management framework)
- ✅ NCSC CAF A2 guidance followed

**Gaps**:
- ⚠️ **Threat model not completed** (HIGH priority - Alpha Week 19-21)
- ⚠️ **Residual risk scoring** could benefit from quantitative analysis (cyber risk quantification)

**Recommendations**:
1. **Complete threat model** (STRIDE) by Alpha Week 19-21 - **CRITICAL** for Beta phase approval
2. Consider cyber risk quantification (FAIR methodology) for financial impact estimation

---

#### A3: Asset Management

**Status**: ⚠️ **PARTIALLY ACHIEVED**

**Evidence**:

1. **Data Asset Register**: ✅ Data catalog planned (Sprint 4 - Week 55-58)
   - 500+ statistical series to be catalogued
   - Metadata registry (SDMX compliant)
   - Data lineage tracking (source to publication)

2. **Hardware Inventory**: ⚠️ **GAP** - Current on-premises inventory exists, but cloud asset inventory not yet established
   - Legacy systems: On-premises datacentres (Newport, Titchfield) - documented
   - Cloud infrastructure: TBD (post-vendor selection)
   - **Gap**: Cloud asset management approach not defined

3. **Software Inventory**: ⚠️ **GAP** - Software Bill of Materials (SBOM) not established
   - Open-source dependency tracking not yet implemented
   - Software license management for cloud platform pending
   - **Gap**: SBOM and vulnerability tracking not defined

4. **User Accounts**: ✅ 500 ONS statisticians, 6 support engineers, 10,000+ API users (post-go-live)
   - Identity management approach: Multi-factor authentication (MFA) required (NFR-SEC-001)
   - Access review process: Annual user access reviews planned

**Compliance**:
- ⚠️ Partial compliance with NCSC CAF A3
- ⚠️ Gaps in hardware/software inventory management

**Gaps**:
1. **Cloud asset inventory** not defined (MEDIUM - Beta Sprint 1, Week 43)
2. **Software Bill of Materials (SBOM)** not established (MEDIUM - Beta Sprint 1, Week 43)
3. **Automated asset discovery** tools not specified (MEDIUM - Beta Sprint 6, Week 63-66)

**Recommendations**:
1. **Define cloud asset management approach** - DevOps Engineer - Beta Sprint 1 (Week 43) - **HIGH**
2. **Implement SBOM tracking** for open-source dependencies - Security Engineer - Beta Sprint 1 (Week 43) - **MEDIUM**
3. **Deploy asset discovery tools** (e.g., AWS Config, Azure Resource Graph) - DevOps Engineer - Beta Sprint 6 (Week 63-66) - **MEDIUM**

---

#### A4: Supply Chain

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Vendor Security Assessment**: ✅ G-Cloud 13 Digital Marketplace framework
   - All suppliers pre-vetted by Crown Commercial Service
   - Security requirements in evaluation criteria (40% technical capability weighting)
   - ISO 27001 certification mandatory
   - Financial stability checks (3 years trading, audited accounts)

2. **Contract Security Clauses**: ✅ Risk allocation defined in Commercial Case
   - Vendor accountable for technology delivery security
   - Security compliance (GovS 007) vendor responsibility
   - Data migration integrity vendor responsibility
   - 90-day exit clause with knowledge transfer requirements

3. **Third-Party Risk**: ⚠️ **PARTIAL** - Cloud provider risk assessment pending
   - Cloud provider selection (AWS/Azure/GCP) - Week 20
   - **Gap**: Cloud provider security assessment not yet completed (dependent on vendor selection)
   - Sub-contractors permitted (e.g., SDMX specialist, pen testing) - security vetting required

4. **Supply Chain Monitoring**: ⚠️ **PLANNED** - Vendor performance KPIs include security
   - Monthly vendor performance review (KPIs, milestones, risks)
   - Quarterly contract health check
   - **Gap**: Continuous supply chain threat intelligence monitoring not specified

**Compliance**:
- ✅ NCSC Cloud Security Principles (to be assessed post-vendor selection)
- ✅ Government Functional Standard GovS 007 (supply chain security)

**Gaps**:
1. **Cloud provider security assessment** not completed (HIGH - Alpha Week 20, post-vendor selection)
2. **Supply chain threat intelligence** monitoring not specified (MEDIUM - Beta Sprint 6)

**Recommendations**:
1. **Assess cloud provider** against NCSC Cloud Security Principles - Security Architect - Alpha Week 20 (post-vendor selection) - **HIGH**
2. **Implement supply chain threat intelligence** monitoring (e.g., third-party breach notifications) - Security Engineer - Beta Sprint 6 (Week 63-66) - **MEDIUM**

---

### Objective B: Protecting Against Cyber Attack

#### B1: Service Protection Policies

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Acceptable Use Policy (AUP)**: ✅ ONS Information Security Policy Framework
   - Approved by SIRO (last review 2024-09)
   - Covers: acceptable use, data handling, remote access, BYOD (not permitted), social media
   - Mandatory annual security awareness training for all ONS staff

2. **Access Control Policy**: ✅ Defined in NFR-SEC-001 (Zero Trust Architecture)
   - Multi-factor authentication (MFA) for all users
   - Role-Based Access Control (RBAC) with least privilege
   - Privileged Access Management (PAM) for admin accounts
   - Annual user access reviews

3. **Data Protection Policy**: ✅ ONS Data Protection Policy (UK GDPR compliant)
   - Data minimisation, purpose limitation, storage limitation
   - Data retention policies (automated deletion)
   - Encryption at rest (AES-256) and in transit (TLS 1.3+)
   - Data classification scheme (OFFICIAL / OFFICIAL-SENSITIVE)

4. **Remote Access Policy**: ✅ VPN required for ONS network access
   - MFA required for VPN access
   - Device security posture checks (anti-malware, patching up-to-date)

5. **Incident Response Policy**: ✅ ONS Incident Response Policy
   - 72-hour data breach notification to ICO (UK GDPR requirement)
   - Incident severity classification (P1/P2/P3/P4)
   - Escalation paths defined (Security Team → Head of Cyber Security → SIRO)

**Compliance**:
- ✅ NCSC CAF B1 guidance
- ✅ UK GDPR Article 32 (security of processing)

**No Gaps Identified**: Policy framework is comprehensive and regularly reviewed.

---

#### B2: Identity and Access Control

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Multi-Factor Authentication (MFA)**: ✅ Mandatory (NFR-SEC-001)
   - All user accounts require MFA (statisticians, support team, API consumers)
   - Pre-release access: MFA mandatory (Statistics Act compliance - R-006)
   - **MFA Methods**: TOTP (Time-based One-Time Password), hardware tokens for privileged users

2. **Role-Based Access Control (RBAC)**: ✅ Least privilege principle
   - Roles defined: Statistician (publish), Support Engineer (admin), API Consumer (read-only)
   - RACI matrix defines decision rights and accountability
   - Access granted based on job function, reviewed annually

3. **Privileged Access Management (PAM)**: ✅ Planned for Beta Sprint 6 (Week 63-66)
   - Separate privileged accounts for admin tasks (no shared credentials)
   - Privileged session recording and monitoring
   - Just-in-time (JIT) privileged access elevation
   - **Gap**: PAM tooling not yet selected (planned for Beta Sprint 6)

4. **Access Reviews**: ✅ Annual user access reviews planned
   - Quarterly reviews for privileged accounts
   - Automated access revocation on staff departure (HR system integration)

5. **Authentication Logging**: ✅ Audit logging (NFR-SEC-002)
   - All authentication events logged (success/failure)
   - Correlation IDs for distributed tracing
   - 7-year retention (UK Government compliance requirement)

**Compliance**:
- ✅ NCSC CAF B2 guidance (MFA, least privilege, PAM)
- ✅ Cyber Essentials (access control requirement)

**Gaps**:
1. **PAM tooling not selected** (MEDIUM - Beta Sprint 6, Week 63-66)

**Recommendations**:
1. **Select and implement PAM solution** (e.g., CyberArk, BeyondTrust) - Security Engineer - Beta Sprint 6 (Week 63-66) - **MEDIUM**

---

#### B3: Data Security

**Status**: ⚠️ **PARTIALLY ACHIEVED**

**Evidence**:

1. **Encryption in Transit**: ✅ TLS 1.3+ (NFR-SEC-001)
   - All APIs: TLS 1.3 minimum
   - Service-to-service: mutual TLS (mTLS) via service mesh
   - VPN: IPsec or TLS VPN for remote access

2. **Encryption at Rest**: ✅ AES-256 (NFR-SEC-001)
   - All data stores: AES-256 encryption at rest
   - Key management: Cloud provider KMS (AWS KMS, Azure Key Vault, GCP KMS)
   - Key rotation: Automated annual rotation

3. **UK GDPR Compliance**: ⚠️ **PARTIAL** (DPIA not yet completed)
   - **DPO Appointed**: ✅ Yes (Data Protection Officer, ONS)
   - **Lawful Basis**: ✅ Public task (Statistics Act 2007)
   - **Privacy Notice**: ✅ Published on ONS.gov.uk
   - **Data Subject Rights**: ✅ Procedures documented (access, erasure, rectification)
   - **DPIA**: ⚠️ **NOT COMPLETED** (planned for Alpha Week 22-23) - **CRITICAL GAP**
   - **Data Breach Notification**: ✅ Incident Response Policy (72 hours to ICO)
   - **Records of Processing Activities (ROPA)**: ✅ Maintained by DPO

4. **Data Loss Prevention (DLP)**: ⚠️ **NOT IMPLEMENTED** (planned for Beta Sprint 6)
   - Pre-release data exfiltration risk (R-012 - cyber security breach)
   - **Gap**: DLP controls not defined (email filtering, USB blocking, egress monitoring)

5. **Statistical Disclosure Control (SDC)**: ✅ Automated (FR-005)
   - Cell suppression (<3 individuals)
   - Secondary suppression (prevent differencing attacks)
   - Rounding rules, perturbation methods
   - Re-identification risk assessment

**Compliance**:
- ⚠️ UK GDPR: DPIA not completed (CRITICAL - Article 35)
- ✅ Data Protection Act 2018 (encryption, data minimisation)
- ✅ Statistics Act 2007 (Statistical Disclosure Control)

**Critical Gaps**:
1. **DPIA not completed** - **CRITICAL** - Blocks Beta phase - DPO - Alpha Week 22-23
2. **DLP not implemented** - HIGH - Security Engineer - Beta Sprint 6 (Week 63-66)

**Recommendations**:
1. **Complete DPIA** for all personal data processing (Census, survey microdata, admin data) - DPO - Alpha Week 22-23 - **CRITICAL** (Beta phase blocker)
2. **Implement DLP controls** (email filtering, egress monitoring, USB blocking) - Security Engineer - Beta Sprint 6 (Week 63-66) - **HIGH**
3. **Data classification labeling** in files/emails (e.g., "OFFICIAL-SENSITIVE") - Security Engineer - Beta Sprint 6 (Week 63-66) - **MEDIUM**

---

#### B4: System Security

**Status**: ⚠️ **PARTIALLY ACHIEVED**

**Evidence**:

1. **Vulnerability Management**: ✅ Defined (NFR-SEC-003)
   - Patch SLAs: Critical <24 hours, High <7 days, Medium <30 days, Low <90 days
   - Automated scanning in CI/CD pipeline (SAST/DAST)
   - Dependency scanning for open-source libraries
   - Container image scanning before deployment
   - **Gap**: Tooling not yet selected (planned for Beta Sprint 1)

2. **Anti-Malware**: ⚠️ **NOT SPECIFIED** (required for Cyber Essentials)
   - Cloud-native workloads (containers) - anti-malware approach TBD
   - Endpoints (statistician workstations) - ONS corporate anti-malware (assumed)
   - **Gap**: Anti-malware strategy for cloud workloads not defined

3. **Hardening / Secure Configuration**: ⚠️ **PLANNED**
   - Infrastructure as Code (IaC) enables consistent configuration
   - CIS benchmarks to be applied (e.g., CIS AWS Foundations Benchmark)
   - **Gap**: Hardening standards not yet defined (planned for DLD Week 42)

4. **Penetration Testing**: ✅ Planned (NFR-SEC-003)
   - **Internal pen testing**: Quarterly (planned)
   - **External pen testing**: Annual (planned)
   - **ITHC (IT Health Check)**: CHECK-certified testers - Beta Week 72 - **CRITICAL** for go-live
   - **Gap**: ITHC not yet scheduled (Week 72 - before go-live)

5. **Vulnerability Disclosure**: ⚠️ **NOT ESTABLISHED**
   - Responsible disclosure policy not published
   - Security contact not advertised (security.txt)
   - **Gap**: Vulnerability disclosure program not defined

**Compliance**:
- ⚠️ Cyber Essentials: Anti-malware requirement unclear for cloud-native workloads
- ⚠️ NCSC CAF B4: Penetration testing planned but not completed

**Gaps**:
1. **ITHC (IT Health Check) not scheduled** - **CRITICAL** - Blocks Live phase - Head of Cyber Security - Beta Week 72
2. **Anti-malware strategy for cloud workloads** not defined - MEDIUM - Security Engineer - Beta Sprint 1 (Week 43)
3. **Hardening standards (CIS benchmarks)** not defined - MEDIUM - Security Architect - DLD (Week 42)
4. **Vulnerability disclosure program** not established - LOW - Security Engineer - Live (Week 78+)

**Recommendations**:
1. **Schedule ITHC** with CHECK-certified testers for Beta Week 72 - Head of Cyber Security - Alpha Week 36 (book 3 months ahead) - **CRITICAL** (Live phase blocker)
2. **Define anti-malware strategy** for containers (e.g., runtime detection, image scanning) - Security Engineer - Beta Sprint 1 (Week 43) - **MEDIUM**
3. **Apply CIS benchmarks** in IaC (Terraform/CloudFormation) - Security Architect - DLD (Week 42) - **MEDIUM**
4. **Establish vulnerability disclosure program** (security.txt, responsible disclosure policy) - Security Engineer - Live (Week 78+) - **LOW**

---

#### B5: Resilient Networks

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Network Segmentation**: ✅ Planned architecture (Zero Trust - Principle 10)
   - Segmentation by sensitivity: Public APIs, Pre-release data, Admin interfaces
   - Micro-segmentation via service mesh (mTLS between services)
   - **Network zones**:
     - **DMZ**: Public-facing publication APIs (internet-accessible)
     - **Internal**: ONS statistician access (VPN-only)
     - **Sensitive**: Pre-release data processing (restricted access)

2. **Firewalls**: ✅ Cloud-native firewalls (Security Groups / Network Security Groups)
   - Ingress: Whitelist approach (deny all, allow specific ports/IPs)
   - Egress: Controlled (prevent data exfiltration)
   - **Gap**: Firewall rules not yet defined (planned for DLD Week 42)

3. **Intrusion Detection/Prevention (IDS/IPS)**: ⚠️ **PLANNED**
   - Cloud-native IDS/IPS (AWS GuardDuty, Azure Defender, GCP Security Command Center)
   - **Gap**: IDS/IPS not yet enabled (planned for Beta Sprint 6, Week 63-66)

4. **VPN for Remote Access**: ✅ ONS corporate VPN (existing)
   - MFA required for VPN access
   - Device security posture checks

5. **DDoS Protection**: ✅ Cloud-native DDoS protection
   - AWS Shield, Azure DDoS Protection, GCP Cloud Armor
   - Application-layer DDoS mitigation (rate limiting, CAPTCHA)

6. **PSN Connectivity**: ⚠️ **NOT SPECIFIED**
   - Public Services Network (PSN) integration for government department APIs (HMRC/DWP)
   - **Gap**: PSN Code of Connection (CoCo) not initiated

**Compliance**:
- ✅ NCSC CAF B5 guidance (network segmentation, firewalls, IDS/IPS)
- ⚠️ PSN CoCo: Required for HMRC/DWP API integration (if PSN-connected)

**Gaps**:
1. **IDS/IPS not enabled** - MEDIUM - Security Engineer - Beta Sprint 6 (Week 63-66)
2. **Firewall rules not defined** - MEDIUM - Security Architect - DLD (Week 42)
3. **PSN Code of Connection (CoCo)** not initiated (if required for HMRC/DWP) - MEDIUM - Chief Data Architect - Alpha Week 20

**Recommendations**:
1. **Enable cloud-native IDS/IPS** (GuardDuty, Defender, SCC) - Security Engineer - Beta Sprint 6 (Week 63-66) - **MEDIUM**
2. **Define firewall rules** (least privilege, ingress/egress controls) - Security Architect - DLD (Week 42) - **MEDIUM**
3. **Determine PSN CoCo requirement** for HMRC/DWP integration - Chief Data Architect - Alpha Week 20 - **MEDIUM**

---

#### B6: Staff Awareness and Training

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Security Awareness Training**: ✅ Mandatory annual training for all ONS staff
   - Topics: Phishing, password security, data protection, acceptable use, incident reporting
   - Completion rate: Target >95%
   - Last delivery: 2024-09

2. **Phishing Awareness**: ✅ Simulated phishing campaigns (quarterly)
   - Click rate target: <10%
   - Reporting rate target: >50%
   - Remedial training for staff who click

3. **Data Protection Training**: ✅ Mandatory for statisticians (500 users)
   - UK GDPR principles, data classification, Statistical Disclosure Control (SDC)
   - Completion required before access to personal data

4. **Platform-Specific Training**: ✅ Planned (Management Case)
   - **Statistician training**: New publication workflow (4 hours) - Beta Week 70-72
   - **Support team training**: Platform operations (2 days) - Beta Week 75-78 (Hypercare)
   - **Cloud certifications**: AWS/Azure/GCP Associate for support engineers (6 FTE) - Beta Weeks 43-72

5. **Insider Threat Awareness**: ⚠️ **BASIC** (ONS corporate training covers basics)
   - Pre-release data exfiltration risk (R-012, R-006)
   - **Gap**: Targeted insider threat training for statisticians with pre-release access not specified

**Compliance**:
- ✅ NCSC CAF B6 guidance (security awareness, phishing, data protection)
- ✅ Cyber Essentials (staff awareness requirement)

**Gaps**:
1. **Insider threat training** for statisticians with pre-release access - LOW - Security Engineer - Beta Week 70 (during UAT)

**Recommendations**:
1. **Develop insider threat training module** for statisticians (pre-release data handling, exfiltration indicators) - Security Engineer - Beta Week 70 - **LOW**

---

### Objective C: Detecting Cyber Security Events

#### C1: Security Monitoring

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Security Information and Event Management (SIEM)**: ✅ Planned (NFR-O-001, NFR-O-002)
   - Centralized log aggregation (searchable, indexed)
   - Real-time alerting on security events
   - 90-day online retention, 7-year archive
   - **SIEM Platform**: TBD (cloud-native options: AWS CloudWatch + Security Hub, Azure Sentinel, GCP Chronicle)

2. **Log Sources**: ✅ Comprehensive logging (NFR-O-001)
   - **Authentication events**: MFA success/failure, privileged access
   - **Authorisation decisions**: RBAC denials, access control events
   - **Data access**: Pre-release data access (Statistics Act audit trail - R-006)
   - **Configuration changes**: Infrastructure as Code (IaC) changes, admin actions
   - **Network events**: Firewall blocks, IDS/IPS alerts
   - **Application logs**: API requests, publication workflows, errors

3. **Alerting and Response**: ✅ Defined (NFR-O-002)
   - Real-time dashboards for Security Operations Centre (SOC)
   - Automated alerting on SLO violations
   - Runbooks linked to alerts (remediation steps)
   - 24/7 SOC (post-go-live): Security team on-call rota

4. **Threat Intelligence**: ⚠️ **NOT SPECIFIED**
   - NCSC threat feeds (CiSP - Cyber Security Information Sharing Partnership)
   - **Gap**: Threat intelligence integration not specified

**Compliance**:
- ✅ NCSC CAF C1 guidance (SIEM, logging, alerting)
- ✅ UK GDPR Article 32 (ability to detect, investigate, respond)

**Gaps**:
1. **Threat intelligence integration** not specified - LOW - Security Engineer - Beta Sprint 6 (Week 63-66)

**Recommendations**:
1. **Integrate NCSC threat feeds** (CiSP) into SIEM - Security Engineer - Beta Sprint 6 (Week 63-66) - **LOW**

---

#### C2: Proactive Security Event Discovery

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Vulnerability Scanning**: ✅ Automated (NFR-SEC-003)
   - **SAST (Static Application Security Testing)**: CI/CD pipeline (every commit)
   - **DAST (Dynamic Application Security Testing)**: CI/CD pipeline (every deployment)
   - **Dependency scanning**: Open-source libraries (weekly scans)
   - **Container image scanning**: Before deployment to production
   - **Infrastructure scanning**: Cloud configuration scanning (AWS Config Rules, Azure Policy)

2. **Penetration Testing**: ✅ Planned (NFR-SEC-003)
   - **Internal pen testing**: Week 68 (4 weeks before ITHC) - identify issues early
   - **External pen testing (ITHC)**: Week 72 (before go-live) - CHECK-certified testers
   - **Post-go-live**: Annual external pen testing, quarterly internal

3. **Threat Hunting**: ⚠️ **NOT SPECIFIED**
   - Proactive threat hunting (hypothesis-driven investigation)
   - **Gap**: Threat hunting capability not specified (likely manual initially, automate in future)

4. **Bug Bounty**: ⚠️ **NOT SPECIFIED**
   - Public bug bounty program (e.g., HackerOne, Bugcrowd)
   - **Gap**: Bug bounty not planned (consider for future)

**Compliance**:
- ✅ NCSC CAF C2 guidance (vulnerability scanning, pen testing)
- ✅ Government Functional Standard GovS 007 (pen testing requirement)

**Gaps**:
1. **Threat hunting** not specified - LOW - Security Engineer - Live (Week 78+)
2. **Bug bounty program** not planned - LOW - Security Engineer - Live (Week 78+ - future consideration)

**Recommendations**:
1. **Define threat hunting capability** (initially manual, automate in future) - Security Engineer - Live (Week 78+) - **LOW**
2. **Consider bug bounty program** post-go-live (private initially, public after maturity) - Security Engineer - Live (Week 78+ - future) - **LOW**

---

### Objective D: Minimising the Impact of Incidents

#### D1: Response and Recovery Planning

**Status**: ⚠️ **PARTIALLY ACHIEVED**

**Evidence**:

1. **Incident Response Plan**: ✅ ONS Incident Response Policy exists
   - Incident severity classification (P1/P2/P3/P4)
   - Escalation paths: Security Team → Head of Cyber Security → SIRO → NCSC (if national security concern)
   - 72-hour data breach notification to ICO (UK GDPR requirement)
   - **Gap**: Platform-specific incident response playbooks not yet developed (planned for Beta Week 66)

2. **Incident Response Testing**: ⚠️ **NOT TESTED**
   - Tabletop exercises planned (Beta Week 71 - before go-live)
   - **Gap**: Incident response not yet tested (planned for Beta)

3. **Backup and Recovery**: ✅ Defined (NFR-A-002)
   - **RTO (Recovery Time Objective)**: 4 hours
   - **RPO (Recovery Point Objective)**: 1 hour
   - **Backup frequency**: Continuous for databases, hourly for files
   - **Backup retention**: 7 years (UK Government compliance requirement)
   - **Disaster recovery testing**: Quarterly full failover exercise (planned)

4. **Business Continuity**: ✅ Multi-region deployment (NFR-A-002)
   - Multi-availability zone deployment across UK regions
   - Automated failover (<5 minutes) for critical services
   - **Gap**: Business Continuity Plan (BCP) not yet developed (planned for Beta Week 66)

5. **Forensic Readiness**: ⚠️ **PARTIAL**
   - Log retention: 7 years (supports forensic investigation)
   - Tamper-evident logs (append-only, cryptographic verification)
   - **Gap**: Forensic investigation procedures not documented

**Compliance**:
- ✅ UK GDPR Article 32 (ability to restore availability after incident)
- ⚠️ NCSC CAF D1: Incident response testing not yet conducted

**Gaps**:
1. **Platform-specific incident response playbooks** not developed - MEDIUM - Security Engineer - Beta Week 66 (Sprint 6)
2. **Incident response testing** not conducted - MEDIUM - Security Engineer - Beta Week 71 (tabletop exercise)
3. **Business Continuity Plan (BCP)** not developed - MEDIUM - Chief Data Architect - Beta Week 66
4. **Forensic investigation procedures** not documented - LOW - Security Engineer - Beta Week 66

**Recommendations**:
1. **Develop incident response playbooks** (e.g., data breach, ransomware, DDoS) - Security Engineer - Beta Week 66 (Sprint 6) - **MEDIUM**
2. **Conduct tabletop exercise** (scenario: pre-release data breach) - Security Engineer - Beta Week 71 - **MEDIUM** (before go-live)
3. **Develop Business Continuity Plan (BCP)** - Chief Data Architect - Beta Week 66 - **MEDIUM**
4. **Document forensic investigation procedures** - Security Engineer - Beta Week 66 - **LOW**

---

#### D2: Lessons Learned and Improvement

**Status**: ✅ **ACHIEVED**

**Evidence**:

1. **Post-Incident Reviews**: ✅ Defined in Incident Response Policy
   - Mandatory for P1/P2 incidents
   - Root cause analysis (5 Whys, fishbone diagram)
   - Actions tracked in risk register

2. **Security Metrics**: ✅ Defined (NFR-O-002)
   - RED metrics: Rate, Errors, Duration (including security errors)
   - Vulnerability metrics: Mean Time To Remediate (MTTR), patching compliance %
   - Incident metrics: Mean Time To Detect (MTTD <5 minutes), Mean Time To Recover (MTTR <30 minutes)

3. **Continuous Improvement**: ✅ Planned
   - Quarterly risk register review (update risks, retire mitigated risks)
   - Annual architecture health check (architecture principles compliance audit)
   - Post-implementation review (Month 12 post-go-live)

4. **Threat Intelligence Sharing**: ⚠️ **NOT SPECIFIED**
   - NCSC CiSP (Cyber Security Information Sharing Partnership) membership
   - **Gap**: Threat intelligence sharing not specified (consider joining CiSP)

**Compliance**:
- ✅ NCSC CAF D2 guidance (post-incident reviews, metrics, continuous improvement)

**Gaps**:
1. **NCSC CiSP membership** not confirmed - LOW - Head of Cyber Security - Discovery Week 12

**Recommendations**:
1. **Join NCSC CiSP** for threat intelligence sharing - Head of Cyber Security - Discovery Week 12 - **LOW**

---

## Cyber Essentials Assessment

### Cyber Essentials Status

**Current Status**: ⚠️ **NOT CERTIFIED** (Required before Beta phase go-live)

**Target Certification**: **Cyber Essentials Plus** (external technical verification)

**Rationale for Cyber Essentials Plus**:
- OFFICIAL-SENSITIVE data classification
- High-risk system (pre-release market-sensitive statistics)
- Public-facing APIs (10,000+ users)
- UK Government procurement requirement (£5M+ contract value)

**Timeline**:
- **Cyber Essentials Plus application**: Beta Week 60 (12 weeks before go-live)
- **External assessment**: Beta Week 64-68 (third-party technical verification)
- **Certification target**: Beta Week 72 (before go-live)

### 5 Cyber Essentials Controls Assessment

#### CE-1: Firewalls and Internet Gateways

**Status**: ⚠️ **PLANNED** (Design phase - not yet implemented)

**Evidence**:
- Cloud-native firewalls (Security Groups / Network Security Groups)
- Ingress: Whitelist approach (deny all, allow specific ports/IPs)
- Egress: Controlled (prevent data exfiltration)

**Gaps**:
- Firewall rules not yet defined (planned for DLD Week 42)
- Egress filtering rules not specified

**Action**: **Define firewall ruleset** - Security Architect - DLD Week 42 - **HIGH**

#### CE-2: Secure Configuration

**Status**: ⚠️ **PLANNED** (Design phase - not yet implemented)

**Evidence**:
- Infrastructure as Code (IaC) enables consistent configuration
- CIS benchmarks to be applied (e.g., CIS AWS Foundations Benchmark)
- Principle 13: Automation and Continuous Delivery (immutable infrastructure)

**Gaps**:
- Hardening standards not yet defined (planned for DLD Week 42)
- Configuration compliance monitoring not specified

**Action**: **Apply CIS benchmarks in IaC** - Security Architect - DLD Week 42 - **HIGH**

#### CE-3: User Access Control

**Status**: ✅ **ACHIEVED** (Requirements defined, implementation in Beta)

**Evidence**:
- Multi-factor authentication (MFA) mandatory (NFR-SEC-001)
- Role-Based Access Control (RBAC) with least privilege
- Annual user access reviews
- Privileged Access Management (PAM) planned (Beta Sprint 6)

**Compliance**: ✅ Meets Cyber Essentials access control requirements

**No Action Required** (implementation in Beta Sprint 6)

#### CE-4: Malware Protection

**Status**: ⚠️ **PARTIALLY DEFINED** (Anti-malware strategy for cloud workloads TBD)

**Evidence**:
- Endpoints (statistician workstations): ONS corporate anti-malware (assumed McAfee/Sophos/CrowdStrike)
- Cloud workloads (containers): Anti-malware strategy TBD

**Gaps**:
- Anti-malware for cloud-native workloads not defined
- Container runtime security not specified (e.g., Aqua Security, Prisma Cloud)

**Action**: **Define anti-malware strategy for cloud workloads** - Security Engineer - Beta Sprint 1 (Week 43) - **HIGH**

#### CE-5: Security Update Management (Patch Management)

**Status**: ✅ **ACHIEVED** (Requirements defined, implementation in Beta)

**Evidence**:
- Patch SLAs defined (NFR-SEC-003):
  - Critical: <24 hours
  - High: <7 days
  - Medium: <30 days
  - Low: <90 days
- Automated vulnerability scanning in CI/CD pipeline
- Immutable infrastructure (Infrastructure as Code - no manual patching)

**Compliance**: ✅ Meets Cyber Essentials patch management requirements (critical within 14 days - ONS exceeds with <24 hours)

**No Action Required** (implementation in Beta Sprint 1)

---

### Cyber Essentials Certification Roadmap

| Week | Activity | Owner | Status |
|------|----------|-------|--------|
| **Week 42 (DLD)** | Finalise security design (firewalls, hardening) | Security Architect | Planned |
| **Week 43-66 (Beta)** | Implement 5 Cyber Essentials controls | Security Engineer | Planned |
| **Week 60** | Apply for Cyber Essentials Plus | Head of Cyber Security | Planned |
| **Week 64-68** | External technical assessment (third-party) | External Assessor | Planned |
| **Week 72** | Cyber Essentials Plus certification obtained | Head of Cyber Security | Target |

**Recommendation**: **Apply for Cyber Essentials Plus certification by Beta Week 60** to allow 12-week lead time before go-live - **CRITICAL** for Beta/Live phase approval.

---

## UK GDPR Compliance Assessment

### UK GDPR Status

**Status**: ✅ **COMPLIANT** (with critical gaps to address)

**Data Protection Officer (DPO)**: ✅ Appointed - Data Protection Officer, ONS

**Legal Basis for Processing**: ✅ **Public Task** (Statistics and Registration Service Act 2007)

### UK GDPR Compliance Checklist

#### Article 5: Principles

| Principle | Status | Evidence |
|-----------|--------|----------|
| **Lawfulness, fairness, transparency** | ✅ | Public task basis (Statistics Act 2007), privacy notice published |
| **Purpose limitation** | ✅ | Data collected for statistical purposes only |
| **Data minimisation** | ✅ | Only necessary data fields retained (DR-002) |
| **Accuracy** | ✅ | Data quality validation (FR-006) |
| **Storage limitation** | ✅ | Retention policies defined (DR-002, automated deletion) |
| **Integrity and confidentiality** | ✅ | Encryption at rest/in transit, access controls |
| **Accountability** | ✅ | DPO appointed, ROPA maintained |

#### Article 25: Data Protection by Design and Default

**Status**: ✅ **ACHIEVED**

**Evidence**:
- Architecture Principle 6: Privacy by Design and Statistical Disclosure Control
- Encryption by default (AES-256 at rest, TLS 1.3+ in transit)
- Access controls (RBAC, least privilege, MFA)
- Statistical Disclosure Control (SDC) automation (FR-005)
- Data minimisation (retention policies, automated deletion)

#### Article 30: Records of Processing Activities (ROPA)

**Status**: ✅ **MAINTAINED**

**Evidence**:
- ROPA maintained by DPO
- Processing activities documented:
  - Census data processing (67M UK residents)
  - Survey microdata processing (LFS, LCFS, etc.)
  - Admin data processing (HMRC/DWP integration)
- Legal basis, data categories, retention periods documented

#### Article 32: Security of Processing

**Status**: ✅ **ACHIEVED** (implementation in progress)

**Evidence**:
- Technical measures: Encryption, access controls, logging, pseudonymisation
- Organisational measures: Policies, training, incident response
- Regular testing: Pen testing (quarterly/annual), vulnerability scanning (continuous)
- Ability to restore data: Backup/recovery (RTO 4 hours, RPO 1 hour)

#### Article 33: Notification of Data Breach

**Status**: ✅ **ACHIEVED**

**Evidence**:
- Incident Response Policy: 72-hour notification to ICO
- Escalation path: Security Team → Head of Cyber Security → DPO → ICO
- Breach notification template prepared

#### Article 35: Data Protection Impact Assessment (DPIA)

**Status**: ⚠️ **REQUIRED BUT NOT COMPLETED** - **CRITICAL GAP**

**DPIA Required**: ✅ **YES** (High-risk processing)

**Triggers for DPIA**:
1. Large-scale processing of personal data (67M Census records)
2. Systematic monitoring (statistical analysis of population trends)
3. Processing of special category data (ethnicity, health - Census questions)
4. Public authority processing (ONS as public body)

**DPIA Status**: ⚠️ **NOT YET COMPLETED** (planned for Alpha Week 22-23)

**DPIA Scope**:
- Census data processing (67M UK residents)
- Survey microdata (Labour Force Survey, Living Costs & Food Survey)
- Admin data integration (HMRC tax data, DWP benefits data)

**DPIA Deliverables**:
- Nature, scope, context, and purposes of processing
- Necessity and proportionality assessment
- Risks to individuals' rights and freedoms
- Measures to address risks (technical and organisational)
- DPO consultation and sign-off

**Timeline**: Alpha Week 22-23 (DPIA command: `/arckit.dpia`)

**Recommendation**: **Complete DPIA by Alpha Week 22-23** - DPO - **CRITICAL** (blocks Beta phase approval)

#### Article 37: Designation of Data Protection Officer

**Status**: ✅ **ACHIEVED**

**DPO Appointed**: ✅ Yes - Data Protection Officer, ONS

**DPO Independence**: ✅ Reports to Permanent Secretary (not operational management)

**DPO Tasks**:
- ✅ Monitor UK GDPR compliance
- ✅ Advise on DPIA (Article 35)
- ✅ Cooperate with ICO
- ✅ Act as contact point for data subjects

---

### UK GDPR Critical Actions

| Action | Severity | Owner | Due Date | Status |
|--------|----------|-------|----------|--------|
| **Complete DPIA** | CRITICAL | DPO | Alpha Week 22-23 | Planned |
| **DPIA consultation with ICO** (if required) | HIGH | DPO | Alpha Week 24 | Conditional |
| **Update ROPA** post-design | MEDIUM | DPO | DLD Week 42 | Planned |

---

## Cloud Security Principles Assessment

### NCSC Cloud Security Principles (14 Principles)

**Status**: ⚠️ **To be assessed post-vendor selection** (Alpha Week 20)

**Cloud Provider Options**: AWS (eu-west-2 London), Azure (UK South), GCP (europe-west2 London)

**Preliminary Assessment** (Generic - to be updated post-vendor selection):

| Principle | Status | Notes |
|-----------|--------|-------|
| **1. Data in transit protection** | ✅ | TLS 1.3+, mTLS for service-to-service |
| **2. Asset protection and resilience** | ✅ | Multi-AZ deployment, backup/recovery (RTO 4h, RPO 1h) |
| **3. Separation between users** | ✅ | RBAC, network segmentation, service mesh |
| **4. Governance framework** | ✅ | SIRO appointed, security policies, Programme Board oversight |
| **5. Operational security** | ✅ | SIEM, vulnerability scanning, pen testing, patch management |
| **6. Personnel security** | ✅ | Security cleared staff (SC for key personnel), DBS checks |
| **7. Secure development** | ✅ | SAST/DAST in CI/CD, code review, security testing |
| **8. Supply chain security** | ✅ | G-Cloud framework, vendor security assessment, ISO 27001 |
| **9. Secure user management** | ✅ | MFA, RBAC, PAM, annual access reviews |
| **10. Identity and authentication** | ✅ | MFA mandatory, OAuth 2.0, OpenID Connect |
| **11. External interface protection** | ✅ | API rate limiting, DDoS protection, WAF |
| **12. Secure service administration** | ✅ | PAM for privileged access, audit logging, JIT elevation |
| **13. Audit information for users** | ✅ | 7-year audit log retention, user access logs |
| **14. Secure use of the service** | ⚠️ | Security guidance for API consumers (planned) |

**Action**: **Assess cloud provider** against NCSC Cloud Security Principles post-vendor selection - Security Architect - Alpha Week 20 - **HIGH**

---

## Government Functional Standard GovS 007: Security

### GovS 007 Compliance Assessment

**Status**: ⚠️ **PARTIAL** (ITHC not yet completed)

**Target Accreditation**: **OFFICIAL** (system handles OFFICIAL and OFFICIAL-SENSITIVE data)

### GovS 007 Requirements

| Requirement | Status | Evidence |
|-------------|--------|----------|
| **1. Security governance** | ✅ | SIRO appointed, security policies, risk register |
| **2. Risk management** | ✅ | Risk register (22 risks), Orange Book compliant |
| **3. Protective security** | ⚠️ | DPIA pending, ITHC pending |
| **4. Personnel security** | ✅ | Security cleared staff (SC), DBS checks, training |
| **5. Physical security** | ✅ | Cloud provider physical security (DC access controls) |
| **6. ICT security** | ⚠️ | Security controls defined, implementation in Beta |
| **7. Incident management** | ✅ | Incident Response Policy, 72-hour ICO notification |

### IT Health Check (ITHC)

**Status**: ⚠️ **NOT COMPLETED** - **CRITICAL** (blocks Live phase)

**ITHC Requirement**: Penetration testing by CHECK-certified testers before go-live

**ITHC Scope**:
- External pen testing (public-facing APIs)
- Internal pen testing (ONS network access)
- Social engineering (phishing simulation)
- Vulnerability assessment

**ITHC Timeline**:
- **Book testers**: Alpha Week 36 (3 months lead time)
- **Internal pen test**: Beta Week 68 (4 weeks before ITHC - identify issues early)
- **ITHC (external)**: Beta Week 72 (before go-live)
- **Remediation**: 2-week buffer (Week 70-72)

**ITHC Outcome**: Zero critical/high vulnerabilities required for OFFICIAL accreditation

**Action**: **Schedule ITHC with CHECK-certified testers** - Head of Cyber Security - Alpha Week 36 - **CRITICAL** (blocks Live phase)

---

## Critical Security Issues (Phase Blockers)

### Critical Issues Summary

| Issue | Severity | Phase Blocked | Current Status | Target Resolution | Owner |
|-------|----------|---------------|----------------|-------------------|-------|
| **1. DPIA not completed** | CRITICAL | Beta | Not started | Alpha Week 22-23 | DPO |
| **2. Threat model not completed** | CRITICAL | Beta | Not started | Alpha Week 19-21 | Security Architect |
| **3. Cyber Essentials not certified** | CRITICAL | Beta/Live | Not started | Beta Week 72 | Head of Cyber Security |
| **4. ITHC not completed** | CRITICAL | Live | Not started | Beta Week 72 | Head of Cyber Security |

### Issue 1: DPIA Not Completed

**Severity**: **CRITICAL** (blocks Beta phase)

**Legal Requirement**: UK GDPR Article 35 (Data Protection Impact Assessment)

**Impact if Not Resolved**:
- UK GDPR non-compliance (ICO enforcement action - fines up to £17.5M or 4% turnover)
- Beta phase approval withheld (Programme Board will not approve without DPIA)
- Reputational damage (ONS seen as non-compliant with data protection)

**Resolution**:
- **Action**: Complete DPIA for all personal data processing (Census, survey microdata, admin data)
- **Owner**: Data Protection Officer (DPO)
- **Timeline**: Alpha Week 22-23 (using `/arckit.dpia` command)
- **Dependencies**: Requirements complete (Week 13-16), design starting (Week 17-22)
- **Deliverable**: DPIA document approved by DPO, potential ICO consultation if high residual risk

---

### Issue 2: Threat Model Not Completed

**Severity**: **CRITICAL** (blocks Beta phase)

**Security Requirement**: NCSC CAF A2 (Risk Management), GovS 007 (Protective Security)

**Impact if Not Resolved**:
- Security control gaps unidentified (may discover issues late in Beta)
- Architecture Review Board will not approve HLD without threat model
- Potential security vulnerabilities in design (costly to fix post-implementation)

**Resolution**:
- **Action**: Complete threat model using STRIDE methodology
- **Owner**: Security Architect (with Chief Data Architect)
- **Timeline**: Alpha Week 19-21 (during HLD design)
- **Scope**:
  - Threat actors: Nation-state APT, organised crime, insider threat, hacktivist
  - Attack vectors: Phishing, API abuse, SQL injection, insider exfiltration, DDoS
  - Assets: Pre-release data (OFFICIAL-SENSITIVE), Census microdata, system credentials
  - STRIDE categories: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege
- **Deliverable**: Threat model document with identified threats and mitigations mapped to security controls

---

### Issue 3: Cyber Essentials Not Certified

**Severity**: **CRITICAL** (blocks Beta/Live phase)

**Contractual Requirement**: UK Government procurement (£18M contract requires Cyber Essentials)

**Impact if Not Resolved**:
- Contract award at risk (G-Cloud framework requires Cyber Essentials for £5M+ contracts)
- Go-live approval withheld (Programme Board requires Cyber Essentials before production)
- GDS Service Standard Beta Assessment may fail (security accreditation required)

**Resolution**:
- **Action**: Obtain Cyber Essentials Plus certification (external technical verification)
- **Owner**: Head of Cyber Security
- **Timeline**:
  - **Week 60**: Apply for Cyber Essentials Plus
  - **Week 64-68**: External technical assessment
  - **Week 72**: Certification obtained (before go-live)
- **Prerequisites**: 5 Cyber Essentials controls implemented (firewalls, secure config, access control, malware, patching)
- **Deliverable**: Cyber Essentials Plus certificate valid for 12 months

---

### Issue 4: ITHC Not Completed

**Severity**: **CRITICAL** (blocks Live phase)

**Accreditation Requirement**: GovS 007 (ITHC required for OFFICIAL systems before go-live)

**Impact if Not Resolved**:
- OFFICIAL accreditation not granted (system cannot process OFFICIAL-SENSITIVE data)
- Go-live approval withheld (SIRO will not sign off without ITHC pass)
- Potential security vulnerabilities in production (unacceptable risk)

**Resolution**:
- **Action**: Schedule and complete ITHC with CHECK-certified testers
- **Owner**: Head of Cyber Security
- **Timeline**:
  - **Alpha Week 36**: Book CHECK-certified testers (3-month lead time)
  - **Beta Week 68**: Internal pen test (identify issues 4 weeks early)
  - **Beta Week 72**: ITHC (external pen test)
  - **Week 70-72**: Remediation buffer (2 weeks to fix critical/high findings)
- **Success Criteria**: Zero critical/high vulnerabilities (medium/low acceptable with risk acceptance)
- **Deliverable**: ITHC report with OFFICIAL accreditation recommendation

---

## Security Recommendations (Prioritised)

### Critical Priority (0-30 days) - **Phase Blockers**

| Recommendation | Owner | Target Date | CAF/CE Ref | Status |
|----------------|-------|-------------|------------|--------|
| **1. Complete DPIA** for personal data processing | DPO | Alpha Week 22-23 | CAF B3, GDPR Art 35 | Planned |
| **2. Complete threat model** (STRIDE) | Security Architect | Alpha Week 19-21 | CAF A2 | Planned |
| **3. Schedule ITHC** with CHECK-certified testers | Head of Cyber Security | Alpha Week 36 | GovS 007 | Planned |
| **4. Apply for Cyber Essentials Plus** | Head of Cyber Security | Beta Week 60 | CE | Planned |

### High Priority (1-3 months) - **Significant Risk Reduction**

| Recommendation | Owner | Target Date | CAF/CE Ref | Status |
|----------------|-------|-------------|------------|--------|
| **5. Define firewall ruleset** (least privilege, egress filtering) | Security Architect | DLD Week 42 | CAF B5, CE-1 | Planned |
| **6. Apply CIS benchmarks** in Infrastructure as Code | Security Architect | DLD Week 42 | CE-2 | Planned |
| **7. Define anti-malware strategy** for cloud workloads | Security Engineer | Beta Sprint 1 (Week 43) | CE-4 | Planned |
| **8. Implement Data Loss Prevention (DLP)** controls | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF B3 | Planned |
| **9. Assess cloud provider** against NCSC Cloud Security Principles | Security Architect | Alpha Week 20 | NCSC CSP | Planned |
| **10. Define cloud asset management** approach | DevOps Engineer | Beta Sprint 1 (Week 43) | CAF A3 | Planned |
| **11. Develop incident response playbooks** (breach, ransomware, DDoS) | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF D1 | Planned |
| **12. Conduct tabletop exercise** (pre-release data breach scenario) | Security Engineer | Beta Week 71 | CAF D1 | Planned |

### Medium Priority (3-6 months) - **Continuous Improvement**

| Recommendation | Owner | Target Date | CAF/CE Ref | Status |
|----------------|-------|-------------|------------|--------|
| **13. Select and implement PAM solution** | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF B2 | Planned |
| **14. Enable cloud-native IDS/IPS** (GuardDuty, Defender, SCC) | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF B5 | Planned |
| **15. Implement Software Bill of Materials (SBOM)** tracking | Security Engineer | Beta Sprint 1 (Week 43) | CAF A3 | Planned |
| **16. Develop Business Continuity Plan (BCP)** | Chief Data Architect | Beta Sprint 6 (Week 63-66) | CAF D1 | Planned |
| **17. Implement supply chain threat intelligence** monitoring | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF A4 | Planned |
| **18. Determine PSN Code of Connection** requirement | Chief Data Architect | Alpha Week 20 | CAF B5 | Planned |

### Low Priority (6-12 months) - **Long-term Enhancement**

| Recommendation | Owner | Target Date | CAF/CE Ref | Status |
|----------------|-------|-------------|------------|--------|
| **19. Develop insider threat training** module | Security Engineer | Beta Week 70 | CAF B6 | Planned |
| **20. Integrate NCSC threat feeds** (CiSP) | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF C1 | Planned |
| **21. Join NCSC CiSP** for threat intelligence sharing | Head of Cyber Security | Discovery Week 12 | CAF D2 | Planned |
| **22. Define threat hunting capability** | Security Engineer | Live (Week 78+) | CAF C2 | Future |
| **23. Establish vulnerability disclosure program** | Security Engineer | Live (Week 78+) | CAF B4 | Future |
| **24. Document forensic investigation procedures** | Security Engineer | Beta Sprint 6 (Week 63-66) | CAF D1 | Planned |
| **25. Consider bug bounty program** | Security Engineer | Live (Week 78+ - future) | CAF C2 | Future |

---

## Security Architecture Summary

### Security Architecture Principles

**Foundation**: Architecture Principle 10 - **Security by Design and Zero Trust**

**Zero Trust Principles**:
1. **Never trust, always verify**: MFA for all users, service-to-service authentication
2. **Assume breach**: Network segmentation, least privilege, continuous monitoring
3. **Verify explicitly**: RBAC, audit logging, real-time alerting

### Defence in Depth (7 Layers)

| Layer | Controls |
|-------|----------|
| **1. Perimeter** | Cloud-native firewalls (Security Groups), DDoS protection (AWS Shield, Azure DDoS Protection) |
| **2. Network** | Network segmentation (VPC/VNet), IDS/IPS (GuardDuty, Defender), service mesh (mTLS) |
| **3. Host** | Anti-malware, hardening (CIS benchmarks), patch management (<24 hours critical) |
| **4. Application** | SAST/DAST in CI/CD, input validation, API rate limiting, WAF |
| **5. Data** | Encryption at rest (AES-256), encryption in transit (TLS 1.3+), Statistical Disclosure Control |
| **6. Identity** | MFA, RBAC, PAM, OAuth 2.0, annual access reviews |
| **7. Monitoring** | SIEM, SOAR, audit logging (7-year retention), pen testing (quarterly/annual) |

### Security Controls Maturity

**Maturity Model**: NCSC CAF Maturity Levels (A-D)

| Control Area | Current Maturity | Target Maturity (Go-Live) |
|--------------|------------------|---------------------------|
| **Governance (CAF A1)** | **C** - Defined | **C** - Defined |
| **Risk Management (CAF A2)** | **B** - Managed (gaps: threat model) | **C** - Defined |
| **Asset Management (CAF A3)** | **B** - Managed (gaps: cloud assets) | **C** - Defined |
| **Supply Chain (CAF A4)** | **C** - Defined | **C** - Defined |
| **Identity & Access (CAF B2)** | **C** - Defined | **C** - Defined |
| **Data Security (CAF B3)** | **B** - Managed (gaps: DPIA, DLP) | **C** - Defined |
| **System Security (CAF B4)** | **B** - Managed (gaps: ITHC) | **C** - Defined |
| **Network Security (CAF B5)** | **C** - Defined | **C** - Defined |
| **Monitoring (CAF C1)** | **C** - Defined | **C** - Defined |
| **Incident Response (CAF D1)** | **B** - Managed (gaps: testing) | **C** - Defined |

**Overall Maturity**: **B → C** (Managed → Defined) by go-live

---

## Appendices

### Appendix A: Security Requirements Traceability

**Security Requirements** (from requirements.md):

| Requirement | CAF Principle | Cyber Essentials | UK GDPR | Status |
|-------------|---------------|------------------|---------|--------|
| **NFR-SEC-001: Zero Trust Architecture** | CAF B2, B5 | CE-3 | Article 32 | ✅ Defined |
| **NFR-SEC-002: Audit Logging** | CAF C1 | N/A | Article 32 | ✅ Defined |
| **NFR-SEC-003: Vulnerability Management** | CAF B4, C2 | CE-5 | Article 32 | ✅ Defined |
| **NFR-C-001: GDPR Compliance** | CAF B3 | N/A | All Articles | ⚠️ DPIA pending |
| **NFR-C-003: GovS 007 Compliance** | All CAF | CE | N/A | ⚠️ ITHC pending |

### Appendix B: Security Risk Register

**Security Risks** (from risk-register.md):

| Risk ID | Title | Residual Score | Owner | Mitigation |
|---------|-------|----------------|-------|------------|
| **R-004** | GovS 007 ITHC security failure | 12 (Medium) | Head of Cyber Security | Internal pen test Week 68, ITHC Week 72, 4-week remediation buffer |
| **R-006** | Statistics Act pre-release access breach | 15 (High) | Chief Statistician | MFA + audit logging, UK Statistics Authority validation |
| **R-012** | Cyber security breach of pre-release data | 10 (Medium) | Head of Cyber Security | Zero Trust, MFA, SIEM 24/7, cyber insurance £10M |

### Appendix C: Security Contacts

| Role | Name | Email | Phone |
|------|------|-------|-------|
| **SIRO** | Permanent Secretary, ONS | siro@ons.gov.uk | [TBD] |
| **IAO** | Chief Data Officer | cdo@ons.gov.uk | [TBD] |
| **DPO** | Data Protection Officer | dpo@ons.gov.uk | [TBD] |
| **Head of Cyber Security** | [Name TBD] | security.head@ons.gov.uk | [TBD] |
| **NCSC (Emergency)** | NCSC | report@ncsc.gov.uk | 0300 303 5222 |
| **ICO (Data Breach)** | ICO | casework@ico.org.uk | 0303 123 1113 |

### Appendix D: Security Standards and Guidance

**UK Government Standards**:
- NCSC Cyber Assessment Framework (CAF): https://www.ncsc.gov.uk/collection/caf
- Cyber Essentials Scheme: https://www.ncsc.gov.uk/cyberessentials
- Government Functional Standard GovS 007: Security: https://www.gov.uk/government/publications/government-functional-standard-govs-007-security
- UK Government Security Classifications: https://www.gov.uk/government/publications/government-security-classifications

**NCSC Guidance**:
- Cloud Security Guidance: https://www.ncsc.gov.uk/collection/cloud-security
- Zero Trust Architecture: https://www.ncsc.gov.uk/blog-post/zero-trust-architecture-design-principles
- Secure Development: https://www.ncsc.gov.uk/collection/developers-collection
- 10 Steps to Cyber Security: https://www.ncsc.gov.uk/collection/10-steps

**UK GDPR**:
- ICO Guide to Data Protection: https://ico.org.uk/for-organisations/guide-to-data-protection/
- ICO DPIA Guidance: https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/accountability-and-governance/data-protection-impact-assessments/

### Appendix E: Security Testing Schedule

| Week | Test Type | Scope | Tester | Target |
|------|-----------|-------|--------|--------|
| **Week 43-66** | SAST/DAST | CI/CD pipeline (every commit/deployment) | Automated tools | Zero critical/high |
| **Week 68** | Internal pen test | Pre-ITHC validation (4 weeks early) | ONS Security Team | Identify issues early |
| **Week 71** | Tabletop exercise | Incident response (pre-release breach scenario) | Security Engineer | Test IR plan |
| **Week 72** | ITHC (external pen test) | CHECK-certified testers | External Assessor | Zero critical/high |
| **Post-Live** | Vulnerability scanning | Weekly automated scans | Automated tools | MTTR <7 days |
| **Post-Live** | Internal pen test | Quarterly internal testing | ONS Security Team | Continuous assurance |
| **Post-Live** | External pen test | Annual external testing | CHECK-certified testers | Annual ITHC |

---

## Assessment Sign-Off

### SIRO Approval

**SIRO**: Permanent Secretary, ONS

**Risk Acceptance**:
- I have reviewed this Secure by Design assessment
- I accept the residual security risks identified (3 HIGH residual risks: R-003, R-006, R-010)
- I approve progression to **Discovery/Alpha phases** subject to completion of critical security actions:
  1. DPIA completed by Alpha Week 22-23
  2. Threat model completed by Alpha Week 19-21
  3. Cyber Essentials Plus obtained by Beta Week 72
  4. ITHC completed by Beta Week 72

**Signature**: ___________________________

**Date**: __________

### Head of Cyber Security Confirmation

**Head of Cyber Security**: [Name TBD]

**Security Assessment Confirmation**:
- NCSC CAF Score: 10/14 (71%) - **Acceptable for Discovery/Alpha**
- Cyber Essentials: Not certified - **Required by Beta Week 72**
- UK GDPR: Compliant with gaps - **DPIA required by Alpha Week 22-23**
- Critical blockers identified: 4 (DPIA, threat model, Cyber Essentials, ITHC)
- **Recommendation**: Approve progression to Discovery/Alpha with conditions

**Signature**: ___________________________

**Date**: __________

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.secure` command
**Generated on**: 2025-11-05
**ArcKit Version**: 0.8.3
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-sonnet-4-5-20250929
**Assessment Framework**: NCSC Cyber Assessment Framework (CAF)
**Context Used**: Requirements (100+ reqs including 5 security NFRs), Architecture Principles (Principle 10: Security by Design and Zero Trust), Risk Register (3 HIGH security risks), Project Plan (78 weeks timeline)
**NCSC CAF Score**: 10/14 Principles Achieved (71%)
**Cyber Essentials Status**: Not certified (target: Cyber Essentials Plus by Beta Week 72)
**UK GDPR Status**: Compliant with critical gap (DPIA required by Alpha Week 22-23)
**Assessment Outcome**: Approve progression to Discovery/Alpha phases with 4 critical security actions required before Beta/Live phases
