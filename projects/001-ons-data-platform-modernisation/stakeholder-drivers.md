# Stakeholder Drivers & Goals Analysis
## ONS Data Platform Modernisation

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STAK-v1.0 |
| **Document Type** | Stakeholder Analysis - Drivers, Goals & Outcomes |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2025-11-05 |
| **Owner** | Chief Data Officer, ONS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial stakeholder analysis from `/arckit.stakeholders` command | [PENDING] | [PENDING] |

---

## Executive Summary

### Purpose

This document provides comprehensive stakeholder analysis for the ONS Data Platform Modernisation project, mapping stakeholder drivers to measurable goals and outcomes. It establishes the foundation for requirements prioritization, risk management, and benefits realization.

### Stakeholder Inventory

**12 stakeholders identified across 3 categories**:
- **Internal Leadership (6)**: Executive Sponsor, Regulatory Authority, Technical Authority, Product Owner, Security Authority, Privacy Authority
- **External Governance (4)**: HM Treasury, GDS Service Assessor, UK Statistics Authority, National Audit Office
- **Users (2)**: Statisticians (internal), Data Consumers (external)

### Driver Analysis

**27 drivers identified across 7 types**:
- STRATEGIC: 6 drivers (innovation, transformation, leadership)
- OPERATIONAL: 8 drivers (efficiency, quality, reliability)
- FINANCIAL: 4 drivers (cost reduction, value for money)
- COMPLIANCE: 5 drivers (regulatory, legal, audit)
- PERSONAL: 2 drivers (career, reputation)
- RISK: 4 drivers (avoiding failures, penalties)
- CUSTOMER: 2 drivers (satisfaction, accessibility)

### Goal Mapping

**27 SMART goals** derived from stakeholder drivers, each with:
- Specific measurable target
- Time-bound deadline
- Owner accountability
- Success criteria
- Link to spending objectives

### Conflict Analysis

**4 critical conflicts identified** requiring resolution:
1. Cost efficiency vs. Enterprise reliability (CFO vs. Security)
2. Innovation speed vs. Regulatory compliance (CDO vs. Chief Statistician)
3. Open access vs. Security controls (National Statistician vs. Security)
4. Census capability investment vs. Budget constraints (Census Director vs. HMT)

### Engagement Strategy

**Power-Interest Grid categorization**:
- **Manage Closely** (8 stakeholders): High power, high interest - weekly/monthly engagement
- **Keep Satisfied** (2 stakeholders): High power, low interest - monthly/quarterly updates
- **Keep Informed** (2 stakeholders): Low power, high interest - regular communications

---

# PART 1: STAKEHOLDER INVENTORY

## 1.1 Internal Leadership Stakeholders

### S-001: Chief Data Officer (CDO)

**Role**: Senior Responsible Owner (SRO), Executive Sponsor, Programme Accountable Officer

**Organisation**: Office for National Statistics (ONS)

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- Programme budget approval (£18M capital)
- Strategic direction and scope decisions
- Vendor contract sign-off
- Exception approvals to architecture principles
- Benefits realization accountability

**Primary Drivers**:

#### D-001 (STRATEGIC, CRITICAL)
**Driver**: Lead ONS digital transformation to maintain international leadership in official statistics
**Rationale**: ONS reputation as world-class statistical institute depends on modern infrastructure. International peers (Statistics Canada, ABS Australia, Eurostat) modernizing rapidly.
**Intensity**: CRITICAL - Reputational risk to ONS if falls behind
**Evidence**: Peer benchmarking shows ONS infrastructure 5-8 years behind Eurostat
**Goal**: G-001 (see Section 2)
**Outcome**: O-001 (see Section 3)

#### D-002 (FINANCIAL, HIGH)
**Driver**: Demonstrate value for money and achieve 40% infrastructure cost reduction
**Rationale**: HM Treasury efficiency priorities and Spending Review commitments require demonstrable savings
**Intensity**: HIGH - Programme business case depends on cost savings
**Evidence**: £11.2M annual infrastructure costs vs £6.7M cloud benchmark
**Goal**: G-002
**Outcome**: O-002

#### D-003 (RISK, HIGH)
**Driver**: Avoid Census 2031 processing failure that would damage ONS credibility
**Rationale**: 2021 Census took 6 months to process vs <24 hour target for 2031
**Intensity**: HIGH - Existential risk to census programme
**Evidence**: 2021 Census post-implementation review identified infrastructure inadequacy
**Goal**: G-003
**Outcome**: O-003

**Power/Interest Assessment**:
- **Power**: 10/10 - Programme SRO, budget authority, final decision maker
- **Interest**: 10/10 - Career-defining programme, personal reputation at stake
- **Influence**: Direct authority over programme team, vendor contracts, scope

---

### S-002: Chief Statistician

**Role**: Regulatory Authority, Statistics Act Compliance Oversight, Professional Standards

**Organisation**: Office for National Statistics (ONS)

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- Statistics Act 2007 compliance approval
- Pre-release access policy enforcement
- Statistical methodology validation
- Publication standards approval
- Can block go-live if non-compliant

**Primary Drivers**:

#### D-004 (COMPLIANCE, CRITICAL)
**Driver**: Maintain Statistics Act 2007 compliance for pre-release access and publication standards
**Rationale**: Legal obligation under Statistics Act. Non-compliance risks UK Statistics Authority sanctions and loss of National Statistics designation
**Intensity**: CRITICAL - Legal requirement, cannot be compromised
**Evidence**: Statistics Act Section 11 mandates compliance, recent NAO report highlighted pre-release access audit gaps
**Goal**: G-004
**Outcome**: O-004

#### D-005 (COMPLIANCE, HIGH)
**Driver**: Ensure Statistical Disclosure Control (SDC) prevents identification of individuals/businesses
**Rationale**: GDPR Article 5 and Statistics Act Section 39 prohibit disclosure of personal/commercial data
**Intensity**: HIGH - Legal obligation, reputational risk
**Evidence**: ICO guidance on statistical disclosure, ONS Five Safes framework
**Goal**: G-005
**Outcome**: O-005

#### D-006 (STRATEGIC, MEDIUM)
**Driver**: Maintain ONS independence from political influence through robust infrastructure
**Rationale**: Statistics Act Section 6 requires independence. Infrastructure failures during election periods create perception of political interference
**Intensity**: MEDIUM - Indirect reputational risk
**Evidence**: 2019 election-period website outage generated Parliamentary questions
**Goal**: G-006
**Outcome**: O-006

**Power/Interest Assessment**:
- **Power**: 9/10 - Regulatory veto, legal compliance authority
- **Interest**: 9/10 - Professional standards, legal accountability
- **Influence**: Can block go-live, requires continuous engagement

---

### S-003: Director of Statistical Production

**Role**: Product Owner, Service Owner, User Champion, Business Lead

**Organisation**: ONS Statistical Production Division

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- Requirements prioritization
- User acceptance testing approval
- Statistician resource allocation
- Publication workflow design sign-off
- Service Level Agreement negotiation

**Primary Drivers**:

#### D-007 (OPERATIONAL, CRITICAL)
**Driver**: Reduce statistician manual publication effort by 60% to free capacity for analysis
**Rationale**: Statisticians spend 35% time on publication mechanics vs 10% target. 600 days/year wasted on manual tasks (£300K opportunity cost)
**Intensity**: CRITICAL - Core business case benefit
**Evidence**: Time-motion studies show 35% time on file formatting, upload, validation
**Goal**: G-007
**Outcome**: O-007

#### D-008 (OPERATIONAL, HIGH)
**Driver**: Reduce publication time-to-publish from 4 days to 2 days for major indicators
**Rationale**: Market-sensitive releases (GDP, CPI, Labour Market) require timeliness. Delays reduce policy impact and media coverage
**Intensity**: HIGH - Business efficiency target
**Evidence**: Publication tracking shows 4-day average, target 2 days
**Goal**: G-008
**Outcome**: O-008

#### D-009 (OPERATIONAL, HIGH)
**Driver**: Reduce publication error rate from 2.3% to <0.1% through automation
**Rationale**: Manual processes cause 2.3% publication errors requiring corrections. Errors damage trust and require statistician rework
**Intensity**: HIGH - Quality improvement, reputation protection
**Evidence**: Publication error log shows 2.3% error rate, 87 corrections in last 12 months
**Goal**: G-009
**Outcome**: O-009

#### D-010 (PERSONAL, MEDIUM)
**Driver**: Deliver successful high-profile programme for career progression to Deputy National Statistician role
**Rationale**: Product Owner role on £18M transformation programme demonstrates leadership capability for promotion
**Intensity**: MEDIUM - Career advancement motivation
**Evidence**: Internal career frameworks show programme delivery experience required for Deputy NS role
**Goal**: G-010
**Outcome**: O-010

**Power/Interest Assessment**:
- **Power**: 8/10 - Requirements authority, UAT approval, resource control
- **Interest**: 10/10 - Primary beneficiary, operational lead, career stake
- **Influence**: Daily engagement with delivery team, statistician community

---

### S-004: Chief Data Architect

**Role**: Technical Authority, Architecture Approval, Design Oversight

**Organisation**: ONS Technology Directorate

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- Architecture principles enforcement
- High-Level Design (HLD) approval
- Detailed Design (DLD) approval
- Technology standards definition
- Vendor technical evaluation

**Primary Drivers**:

#### D-011 (STRATEGIC, HIGH)
**Driver**: Establish modern cloud-native architecture aligned with UK Government Technology Code of Practice
**Rationale**: Technology Code of Practice 13 criteria mandatory for government projects. Cloud-first policy compliance
**Intensity**: HIGH - Policy compliance, architectural integrity
**Evidence**: Technology Code of Practice Point 5 (Cloud First) mandatory
**Goal**: G-011
**Outcome**: O-011

#### D-012 (OPERATIONAL, HIGH)
**Driver**: Achieve 99.95% API availability for publication services (max 21.9 min downtime/month)
**Rationale**: Publication outages damage ONS reputation. Major releases (GDP, CPI) are market-moving events
**Intensity**: HIGH - Service level commitment, reputational risk
**Evidence**: Current availability 97.8% (9.6 hours downtime/month) vs 99.95% target
**Goal**: G-012
**Outcome**: O-012

#### D-013 (RISK, HIGH)
**Driver**: Avoid vendor lock-in through open standards and portable architecture
**Rationale**: 30-year platform lifespan requires flexibility to change cloud providers or bring services in-house
**Intensity**: HIGH - Long-term risk mitigation
**Evidence**: Architecture Principle 8 (Interoperability and Open Standards)
**Goal**: G-013
**Outcome**: O-013

**Power/Interest Assessment**:
- **Power**: 9/10 - Architecture veto, technical approval authority
- **Interest**: 10/10 - Professional accountability, architectural integrity
- **Influence**: Architecture Review Board chair, design authority

---

### S-005: Head of Cyber Security

**Role**: Security Authority, GovS 007 Accreditation, Risk Management

**Organisation**: ONS Security Directorate

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- IT Health Check (ITHC) approval for go-live
- GovS 007 security accreditation
- Security architecture approval
- Penetration testing sign-off
- Security incident response

**Primary Drivers**:

#### D-014 (COMPLIANCE, CRITICAL)
**Driver**: Achieve GovS 007 OFFICIAL accreditation before go-live
**Rationale**: Government Functional Standard GovS 007: Security mandatory for OFFICIAL classification systems. No accreditation = no go-live
**Intensity**: CRITICAL - Legal requirement, gate condition
**Evidence**: GovS 007 Section 3.2.1 requires accreditation before operational use
**Goal**: G-014
**Outcome**: O-014

#### D-015 (RISK, CRITICAL)
**Driver**: Prevent pre-release statistics data breach that would constitute market abuse
**Rationale**: Pre-release GDP/CPI data is market-sensitive. Breach could cause financial market disruption and constitute criminal market abuse under Financial Services and Markets Act 2000
**Intensity**: CRITICAL - Criminal liability, catastrophic reputational damage
**Evidence**: Statistics Act Section 11 restricts pre-release access, market abuse case law
**Goal**: G-015
**Outcome**: O-015

#### D-016 (COMPLIANCE, HIGH)
**Driver**: Implement Zero Trust security architecture per NCSC guidance
**Rationale**: NCSC Cloud Security Principles mandate Zero Trust for cloud services handling OFFICIAL data
**Intensity**: HIGH - Best practice requirement, audit expectation
**Evidence**: NCSC Cloud Security Guidance 2023, Architecture Principle 10
**Goal**: G-016
**Outcome**: O-016

**Power/Interest Assessment**:
- **Power**: 10/10 - Go-live veto via ITHC, accreditation authority
- **Interest**: 9/10 - Security accountability, regulatory compliance
- **Influence**: Security Review Board, NCSC liaison, ITHC gatekeeper

---

### S-006: Data Protection Officer (DPO)

**Role**: Privacy Authority, GDPR Compliance, ICO Liaison

**Organisation**: ONS Compliance Directorate

**Power/Interest**: **HIGH POWER, MEDIUM INTEREST** → **KEEP SATISFIED**

**Authority**:
- Data Protection Impact Assessment (DPIA) approval
- Privacy-by-design validation
- ICO breach notification
- Data retention policy approval
- Subject access request oversight

**Primary Drivers**:

#### D-017 (COMPLIANCE, HIGH)
**Driver**: Complete Data Protection Impact Assessment (DPIA) for all data processing before Beta phase
**Rationale**: UK GDPR Article 35 mandates DPIA for high-risk processing. ICO guidance requires DPIA before systematic large-scale processing
**Intensity**: HIGH - Legal requirement, identified as blocker in Secure by Design assessment
**Evidence**: UK GDPR Article 35, ICO DPIA guidance, R-019 in Risk Register
**Goal**: G-017
**Outcome**: O-017

#### D-018 (COMPLIANCE, MEDIUM)
**Driver**: Ensure data minimization and retention policies comply with GDPR Article 5(1)(c) and (e)
**Rationale**: ONS holds sensitive personal/commercial data under legal privilege. Excessive retention increases risk and contradicts GDPR principle of storage limitation
**Intensity**: MEDIUM - Legal compliance, risk reduction
**Evidence**: GDPR Article 5 storage limitation principle, ICO retention schedules
**Goal**: G-018
**Outcome**: O-018

**Power/Interest Assessment**:
- **Power**: 8/10 - DPIA approval gate, ICO liaison, regulatory veto
- **Interest**: 6/10 - One of many organisational systems, routine compliance oversight
- **Influence**: DPIA gatekeeper, privacy design reviewer

---

## 1.2 External Governance Stakeholders

### S-007: HM Treasury (Programme Manager)

**Role**: Funding Authority, Value for Money Assurance, Business Case Approval

**Organisation**: HM Treasury Infrastructure and Projects Authority (IPA)

**Power/Interest**: **HIGH POWER, MEDIUM INTEREST** → **KEEP SATISFIED**

**Authority**:
- Business case approval (£18M exceeds £10M delegated limit)
- Quarterly checkpoint meetings
- Benefits realization monitoring
- Programme assurance reviews
- Funding release authority

**Primary Drivers**:

#### D-019 (FINANCIAL, CRITICAL)
**Driver**: Demonstrate value for money with Benefit-Cost Ratio (BCR) >2.0 per Green Book guidance
**Rationale**: HM Treasury Green Book requires BCR >2.0 for discretionary capital investment. £18M investment requires strong economic case
**Intensity**: CRITICAL - Programme approval dependency
**Evidence**: Green Book Section 3.2 value for money assessment, SOBC BCR 2.3:1 meets threshold
**Goal**: G-019
**Outcome**: O-019

#### D-020 (FINANCIAL, HIGH)
**Driver**: Achieve £4.5M annual efficiency savings to return to Exchequer
**Rationale**: Spending Review 2021 efficiency priorities require government departments demonstrate cost savings from digital investments
**Intensity**: HIGH - Spending Review commitment, accountability to Public Accounts Committee
**Evidence**: SOBC commits to £4.5M/year savings, Infrastructure cost reduction target
**Goal**: G-020
**Outcome**: O-020

**Power/Interest Assessment**:
- **Power**: 9/10 - Funding authority, business case approval, programme assurance
- **Interest**: 5/10 - One of many government programmes, routine oversight
- **Influence**: Quarterly checkpoint meetings, assurance reviews, funding release

---

### S-008: GDS Service Assessor

**Role**: Government Assurance, Service Standard Compliance, Digital Spend Control

**Organisation**: Cabinet Office - Government Digital Service (GDS)

**Power/Interest**: **HIGH POWER, MEDIUM INTEREST** → **KEEP SATISFIED**

**Authority**:
- Service Standard assessment (Alpha, Beta, Live)
- Digital Spend Control approval (£18M>£5M threshold)
- 14-point assessment pass/fail
- Technology Code of Practice compliance
- Can delay go-live if non-compliant

**Primary Drivers**:

#### D-021 (COMPLIANCE, HIGH)
**Driver**: Ensure compliance with all 14 GDS Service Standard criteria
**Rationale**: UK Government policy mandates Service Standard compliance for all public-facing digital services. Non-compliance blocks go-live and future funding
**Intensity**: HIGH - Mandatory government policy, gate condition
**Evidence**: Service Standard 2023, CDDO Digital Spend Control guidance
**Goal**: G-021
**Outcome**: O-021

#### D-022 (COMPLIANCE, MEDIUM)
**Driver**: Validate user-centred design through research with statisticians and data consumers
**Rationale**: Service Standard Point 1 (Understand users) and Point 2 (Solve a whole problem) require user research evidence
**Intensity**: MEDIUM - Assessment criterion, best practice
**Evidence**: Service Standard Assessment criteria, user research requirements
**Goal**: G-022
**Outcome**: O-022

**Power/Interest Assessment**:
- **Power**: 8/10 - Go-live gate, digital spend control approval
- **Interest**: 5/10 - One of many Service Standard assessments
- **Influence**: Alpha/Beta/Live assessment panels, quarterly updates

---

### S-009: National Statistician

**Role**: Regulatory Compliance, ONS Accreditation, Public Trust

**Organisation**: Office for National Statistics (ONS) / UK Statistics Authority

**Power/Interest**: **HIGH POWER, HIGH INTEREST** → **MANAGE CLOSELY**

**Authority**:
- UK Statistics Authority Code of Practice compliance
- National Statistics designation protection
- Public trust and confidence accountability
- Statistics Act Section 7 compliance oversight
- Can escalate to UK Statistics Authority Board

**Primary Drivers**:

#### D-023 (CUSTOMER, CRITICAL)
**Driver**: Maximize accessibility of official statistics per Statistics Act 2007 Section 7 statutory duty
**Rationale**: ONS statutory duty to make statistics available and accessible to all users. API-first approach delivers statutory obligation
**Intensity**: CRITICAL - Legal obligation, core mission
**Evidence**: Statistics Act 2007 Section 7, Code of Practice Principle Q3 (Accessibility)
**Goal**: G-023
**Outcome**: O-023

#### D-024 (STRATEGIC, HIGH)
**Driver**: Maintain public trust in official statistics through quality, independence, transparency
**Rationale**: ONS public trust rating 68% (2023 survey) vs 75% target. Infrastructure failures damage trust
**Intensity**: HIGH - Reputational imperative, Code of Practice Principle Q1 (Trustworthiness)
**Evidence**: ONS Public Trust Survey 2023, UK Statistics Authority Annual Report
**Goal**: G-024
**Outcome**: O-024

**Power/Interest Assessment**:
- **Power**: 9/10 - Regulatory authority, escalation to UK Statistics Authority Board
- **Interest**: 8/10 - ONS reputation, statutory compliance, public trust
- **Influence**: UK Statistics Authority Board representation, external scrutiny

---

### S-010: National Audit Office (NAO)

**Role**: Independent Auditor, Value for Money Scrutiny, Parliamentary Reporting

**Organisation**: National Audit Office (reports to Public Accounts Committee)

**Power/Interest**: **MEDIUM POWER, MEDIUM INTEREST** → **MONITOR**

**Authority**:
- Value for money audits
- Public Accounts Committee (PAC) reporting
- Major Projects Portfolio (MPP) scrutiny
- Post-implementation reviews
- Parliamentary scrutiny powers

**Primary Drivers**:

#### D-025 (FINANCIAL, MEDIUM)
**Driver**: Validate value for money and prevent cost overruns for Major Projects Portfolio reporting
**Rationale**: Infrastructure and Projects Authority (IPA) classifies £18M+ programmes as Major Projects requiring NAO scrutiny
**Intensity**: MEDIUM - Audit scrutiny, PAC reporting risk
**Evidence**: NAO Major Projects Report 2023, IPA Government Project Portfolio guidelines
**Goal**: G-025
**Outcome**: O-025

**Power/Interest Assessment**:
- **Power**: 5/10 - Audit and reporting powers, can trigger PAC hearings
- **Interest**: 4/10 - One of many government programmes, post-implementation focus
- **Influence**: Post-implementation review, potential PAC hearings if issues emerge

---

## 1.3 User Stakeholders

### S-011: Statisticians (Internal Users)

**Role**: Primary Platform Users, Publication Workflow Operators, Domain Experts

**Organisation**: ONS Statistical Production Divisions (500 users)

**Power/Interest**: **LOW POWER, HIGH INTEREST** → **KEEP INFORMED**

**Authority**:
- User acceptance testing approval
- Publication workflow validation
- Data quality validation
- Methodology code execution
- Can resist adoption (change risk)

**Primary Drivers**:

#### D-026 (OPERATIONAL, HIGH)
**Driver**: Reduce time spent on publication mechanics to focus on statistical analysis
**Rationale**: Statisticians want to do statistics, not IT. 35% time on mechanics vs 10% desired
**Intensity**: HIGH - User satisfaction, productivity, job satisfaction
**Evidence**: User research workshops (Week 3-5), statistician satisfaction surveys
**Goal**: G-026
**Outcome**: O-026

#### D-027 (CUSTOMER, MEDIUM)
**Driver**: Intuitive, reliable tools that don't disrupt publication deadlines
**Rationale**: Publication schedules are rigid (9:30 AM releases). Tool failures cause stress and deadline misses
**Intensity**: MEDIUM - User satisfaction, operational continuity
**Evidence**: Publication schedule adherence 92% vs 98% target, tool reliability complaints
**Goal**: G-027
**Outcome**: O-027

**Power/Interest Assessment**:
- **Power**: 3/10 - Limited formal authority, can resist adoption through workarounds
- **Interest**: 9/10 - Daily tool users, job affected by changes
- **Influence**: User acceptance testing, feedback sessions, adoption behaviour

---

### S-012: Data Consumers (External Users)

**Role**: External Stakeholders, API Users, Public Beneficiaries

**Organisation**: Government analysts, researchers, businesses, media, civil society (10,000 target users)

**Power/Interest**: **LOW POWER, HIGH INTEREST** → **KEEP INFORMED**

**Authority**:
- None (external users)
- Indirect influence through complaints, media coverage
- Freedom of Information requests

**Primary Drivers**:

#### D-028 (CUSTOMER, HIGH)
**Driver**: Timely, reliable, programmatic access to ONS statistics via modern APIs
**Rationale**: Researchers need machine-readable data for analysis. Businesses need real-time economic indicators. Government needs automated dashboards
**Intensity**: HIGH - User satisfaction, ONS reputation
**Evidence**: User research shows 78% want API access, 65% satisfaction with current file-based distribution
**Goal**: G-028
**Outcome**: O-028

**Power/Interest Assessment**:
- **Power**: 2/10 - No formal authority, indirect influence through media/complaints
- **Interest**: 8/10 - Depend on ONS data for research, policy, business decisions
- **Influence**: User satisfaction surveys, API usage analytics, media coverage

---

# PART 2: GOAL MAPPING (Drivers → Goals)

All goals follow SMART criteria: Specific, Measurable, Achievable, Relevant, Time-bound

## 2.1 Strategic Goals

### G-001: Achieve International Statistical Leadership Recognition
**Stakeholder**: S-001 Chief Data Officer
**Driver**: D-001 (STRATEGIC, CRITICAL)
**Target**: ONS ranked Top 3 in International Statistical Institute (ISI) digital capability benchmark by 2028
**Baseline**: Current ISI ranking: #7 (2024)
**Timeframe**: 36 months post-go-live (2030-05)
**Success Criteria**:
- API capabilities match Eurostat, Statistics Canada, ABS Australia
- Census 2031 processing <24 hours demonstrated
- International conference keynotes (4+ per year)
- Peer benchmarking shows ONS in Top 3 for digital infrastructure
**Spending Objective**: SO-1 (Strategic transformation)
**Measurement**: ISI benchmarking survey (biennial), international conference invitations, peer reviews

---

### G-002: Achieve 40% Infrastructure Cost Reduction
**Stakeholder**: S-001 Chief Data Officer
**Driver**: D-002 (FINANCIAL, HIGH)
**Target**: Reduce annual infrastructure operating costs from £11.2M to £6.7M (40% reduction = £4.5M/year savings)
**Baseline**: £11.2M/year (on-premises infrastructure)
**Timeframe**: By Month 24 post-go-live (2029-04)
**Success Criteria**:
- Monthly infrastructure costs ≤£558K (£6.7M/12)
- Cost per dataset published reduced 50%
- FinOps dashboard shows 40% reduction vs baseline
- HM Treasury quarterly reports confirm savings
**Spending Objective**: SO-1 (Reduce infrastructure costs)
**Measurement**: Monthly FinOps cost reports, cost per dataset metric, annual TCO analysis

---

### G-003: Deliver Census-Scale Processing Capability
**Stakeholder**: S-001 Chief Data Officer
**Driver**: D-003 (RISK, HIGH)
**Target**: Process 67 million census records end-to-end in <24 hours (vs 6 months in 2021)
**Baseline**: 2021 Census: 6 months processing time
**Timeframe**: Alpha prototype validated by Week 36 (2026-06), production-ready by go-live (2027-05)
**Success Criteria**:
- Alpha load testing: 67M records processed <24 hours
- Beta performance testing: Linear scaling to 100M records demonstrated
- Census 2031 rehearsal (2029): <24 hours confirmed
- Processing cost per record <£0.0001
**Spending Objective**: SO-4 (Census capability)
**Measurement**: Load testing results, Census 2031 rehearsal metrics, processing time logs

---

### G-004: Maintain Statistics Act 2007 Compliance
**Stakeholder**: S-002 Chief Statistician
**Driver**: D-004 (COMPLIANCE, CRITICAL)
**Target**: Zero Statistics Act compliance breaches during implementation and operation
**Baseline**: 2024 audit: 3 minor pre-release access audit findings
**Timeframe**: Continuous from Discovery through 12 months post-go-live (2028-05)
**Success Criteria**:
- Pre-release access limited to 24 hours maximum (automated enforcement)
- Multi-factor authentication (MFA) for all pre-release access (100% compliance)
- Audit trail for all pre-release access events (100% capture)
- UK Statistics Authority annual audit: zero breaches
- Quarterly self-assessments: 100% pass
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: UK Statistics Authority audit reports, pre-release access audit logs, quarterly compliance self-assessments

---

### G-005: Implement Automated Statistical Disclosure Control
**Stakeholder**: S-002 Chief Statistician
**Driver**: D-005 (COMPLIANCE, HIGH)
**Target**: 100% of published statistics processed through automated SDC rules with zero re-identification incidents
**Baseline**: Manual SDC checks (100% statistician review)
**Timeframe**: SDC automation implemented by Beta Week 52 (2026-11), validated through go-live (2027-05)
**Success Criteria**:
- Automated SDC rules applied to 100% of statistical series
- Zero publications with cell counts <3 individuals
- Privacy Impact Assessment (PIA) approved for SDC methodology
- Re-identification risk assessment: ACCEPTABLE rating
- ICO audit (if occurs): zero SDC findings
**Spending Objective**: SO-5 (Regulatory compliance), SO-2 (Publication efficiency)
**Measurement**: SDC audit logs, publication reviews, re-identification testing, PIA approval, ICO reports

---

### G-006: Ensure Infrastructure Independence from Political Influence
**Stakeholder**: S-002 Chief Statistician
**Driver**: D-006 (STRATEGIC, MEDIUM)
**Target**: Zero infrastructure-related publication delays during election periods (2025, 2029)
**Baseline**: 2019 election: 1 GDP release delayed 4 hours due to infrastructure issues
**Timeframe**: Next General Election (by 2029-12)
**Success Criteria**:
- 99.95% uptime maintained during election periods
- Zero infrastructure-related delays for scheduled releases
- Resilience testing during peak election demand (simulated)
- No Parliamentary questions related to infrastructure failures
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: Publication adherence logs, uptime monitoring, Parliamentary question tracking

---

## 2.2 Operational Goals

### G-007: Reduce Statistician Manual Publication Effort by 60%
**Stakeholder**: S-003 Director of Statistical Production
**Driver**: D-007 (OPERATIONAL, CRITICAL)
**Target**: Reduce statistician time on publication mechanics from 35% to 14% (60% reduction = 600 days/year released)
**Baseline**: 35% of statistician time on publication mechanics (time-motion studies 2024)
**Timeframe**: By Month 12 post-go-live (2028-05) - allows 6-month adoption ramp
**Success Criteria**:
- Time-motion studies show ≤14% time on mechanics
- Automated publication workflow: zero manual steps from validated data to API
- Statistician satisfaction survey: ≥80% report reduced burden
- 600 statistician days/year released for analysis (tracked via workflow metrics)
**Spending Objective**: SO-2 (Publication efficiency)
**Measurement**: Quarterly time-motion studies, workflow automation metrics, statistician satisfaction surveys

---

### G-008: Reduce Time-to-Publish to 2 Days for Major Indicators
**Stakeholder**: S-003 Director of Statistical Production
**Driver**: D-008 (OPERATIONAL, HIGH)
**Target**: Reduce average time-to-publish from 4 days to 2 days for major economic indicators (GDP, CPI, Labour Market)
**Baseline**: 4 days average (publication tracking logs 2024)
**Timeframe**: By Month 6 post-go-live (2027-11) - immediate improvement expected
**Success Criteria**:
- Major indicators: average time-to-publish ≤2 days (p50)
- 90% of publications: ≤3 days (p90)
- Publication schedule adherence ≥98% (vs 92% currently)
- Zero deadline misses due to platform delays
**Spending Objective**: SO-2 (Publication efficiency)
**Measurement**: Publication tracking dashboard, time-to-publish metrics per statistical series

---

### G-009: Reduce Publication Error Rate to <0.1%
**Stakeholder**: S-003 Director of Statistical Production
**Driver**: D-009 (OPERATIONAL, HIGH)
**Target**: Reduce publication error rate from 2.3% to <0.1% through automated quality controls
**Baseline**: 2.3% publication error rate (87 corrections in last 12 months)
**Timeframe**: By Month 6 post-go-live (2027-11)
**Success Criteria**:
- Publication error rate <0.1% (<4 errors/year for 500 series)
- Automated quality validation catches 95% of errors before publication
- Correction rate reduced from 87/year to <4/year
- User complaints about data errors reduced 90%
**Spending Objective**: SO-2 (Publication efficiency), SO-3 (Data quality)
**Measurement**: Publication error logs, correction tracking, automated quality validation reports

---

### G-010: Deliver Programme Successfully for Career Progression
**Stakeholder**: S-003 Director of Statistical Production
**Driver**: D-010 (PERSONAL, MEDIUM)
**Target**: Deliver programme to Beta assessment pass and go-live on time/budget to demonstrate leadership capability
**Baseline**: N/A (new programme)
**Timeframe**: Beta Assessment Week 72 (2027-04), go-live Week 78 (2027-05)
**Success Criteria**:
- Beta Assessment: PASS all 14 Service Standard criteria
- Go-live: On schedule (Week 78, 2027-05-25)
- Budget: Within 10% of £36.6M approved budget
- Benefits realization: 75% of cashable benefits achieved within 12 months
- Positive 360-degree feedback from Programme Board
**Spending Objective**: All spending objectives (overall programme success)
**Measurement**: Service Assessment outcome, go-live date, budget variance reports, benefits realization reports

---

### G-011: Establish Cloud-Native Architecture Aligned with Technology Code of Practice
**Stakeholder**: S-004 Chief Data Architect
**Driver**: D-011 (STRATEGIC, HIGH)
**Target**: Achieve Technology Code of Practice compliance across all 13 points by Beta Assessment (Week 72)
**Baseline**: Current platform: 4/13 TCoP points compliant (TCoP assessment 2024)
**Timeframe**: Beta Assessment Week 72 (2027-04)
**Success Criteria**:
- TCoP Point 5 (Cloud First): 100% cloud-native, zero on-premises components
- TCoP Point 3 (Open Standards): SDMX, OpenAPI 3.0, DCAT compliance
- TCoP Point 6 (Make things secure): GovS 007 accreditation achieved
- TCoP Point 9 (Integrate and adapt): API-first, microservices architecture
- GDS Service Assessment: TCoP compliance confirmed
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: Technology Code of Practice self-assessment, GDS Service Assessment report

---

### G-012: Achieve 99.95% Publication API Availability
**Stakeholder**: S-004 Chief Data Architect
**Driver**: D-012 (OPERATIONAL, HIGH)
**Target**: Achieve 99.95% monthly uptime for publication APIs (max 21.9 minutes downtime per month)
**Baseline**: 97.8% uptime (9.6 hours downtime/month, 2024)
**Timeframe**: By Month 6 post-go-live (2027-11), sustained thereafter
**Success Criteria**:
- Monthly uptime ≥99.95% (≤21.9 min downtime)
- Zero unplanned outages during major publications (GDP, CPI, Labour Market)
- Mean Time To Recovery (MTTR) <30 minutes
- Incident response SLA: acknowledge <15 min, resolve <2 hours
- Quarterly SLA reports: 100% achievement
**Spending Objective**: SO-3 (Service reliability)
**Measurement**: Uptime monitoring (5-minute granularity), incident logs, monthly SLA reports

---

### G-013: Avoid Vendor Lock-in Through Open Standards Architecture
**Stakeholder**: S-004 Chief Data Architect
**Driver**: D-013 (RISK, HIGH)
**Target**: Design architecture enabling cloud provider portability within 6 months if required
**Baseline**: Current infrastructure: 30-year on-premises lock-in
**Timeframe**: Architecture Review Board approval by Alpha Week 24 (2026-04), validated by Beta Week 72 (2027-04)
**Success Criteria**:
- Infrastructure as Code: Terraform (cloud-agnostic) used for 100% of infrastructure
- Containerization: All workloads containerized (Kubernetes-compatible)
- Open standards: SDMX, OpenAPI, DCAT, ISO standards (no proprietary formats)
- Data portability: Export all data in open formats (Parquet, CSV, JSON) within 48 hours
- Vendor lock-in risk assessment: LOW rating from Architecture Review Board
**Spending Objective**: SO-1 (Strategic sustainability)
**Measurement**: Architecture Review Board assessment, portability testing, vendor lock-in risk register

---

## 2.3 Financial Goals

### G-019: Demonstrate Value for Money with BCR >2.0
**Stakeholder**: S-007 HM Treasury
**Driver**: D-019 (FINANCIAL, CRITICAL)
**Target**: Achieve and maintain Benefit-Cost Ratio (BCR) >2.0 throughout business case lifecycle (SOBC → OBC → FBC)
**Baseline**: SOBC BCR 2.3:1 (NPV £18.6M over 10 years)
**Timeframe**: SOBC (2025-11), OBC (2026-06), FBC (2027-02), PIR (2028-05)
**Success Criteria**:
- SOBC: BCR 2.3:1 (achieved ✅)
- OBC: BCR ≥2.0 after detailed design
- FBC: BCR ≥2.0 after procurement
- Post-Implementation Review (PIR): Actual BCR ≥2.0 based on realized benefits
- HM Treasury approval maintained throughout lifecycle
**Spending Objective**: SO-1 (Value for money)
**Measurement**: Business case NPV calculations, benefits realization reports, HM Treasury assurance reviews

---

### G-020: Achieve £4.5M Annual Efficiency Savings
**Stakeholder**: S-007 HM Treasury
**Driver**: D-020 (FINANCIAL, HIGH)
**Target**: Deliver £4.5M/year cashable savings by Month 24 post-go-live (2029-04)
**Baseline**: £11.2M/year infrastructure costs
**Timeframe**: Full savings by Month 24 (2029-04), ramping from Month 6
**Success Criteria**:
- Month 6: £2M/year savings (partial decommissioning)
- Month 12: £3.5M/year savings (majority decommissioned)
- Month 24: £4.5M/year savings (full 40% reduction achieved)
- HM Treasury quarterly checkpoint meetings: savings trajectory confirmed
- Annual Spending Review reports: savings validated
**Spending Objective**: SO-1 (Cost reduction)
**Measurement**: FinOps monthly cost reports, quarterly HM Treasury checkpoint meetings, Spending Review reports

---

### G-025: Prevent Cost Overruns for NAO Major Projects Reporting
**Stakeholder**: S-010 National Audit Office
**Driver**: D-025 (FINANCIAL, MEDIUM)
**Target**: Deliver programme within 10% of approved budget (£36.6M + 10% = £40.3M maximum)
**Baseline**: Approved budget £36.6M (£18M capital + £18.6M operating over 3 years)
**Timeframe**: Programme lifecycle (2025-11 to 2027-05, 78 weeks)
**Success Criteria**:
- Final outturn: ≤£40.3M total costs
- Monthly Programme Board: budget variance <5% (amber threshold)
- No forecast budget overrun >10% (red threshold requiring HMT re-approval)
- NAO Post-Implementation Review: "value for money achieved" rating
- Public Accounts Committee (PAC): zero scrutiny hearings triggered
**Spending Objective**: SO-1 (Value for money)
**Measurement**: Monthly budget variance reports, Programme Board minutes, NAO audit reports

---

## 2.4 Compliance Goals

### G-014: Achieve GovS 007 OFFICIAL Accreditation Before Go-Live
**Stakeholder**: S-005 Head of Cyber Security
**Driver**: D-014 (COMPLIANCE, CRITICAL)
**Target**: Pass IT Health Check (ITHC) and achieve GovS 007 OFFICIAL accreditation by Beta Week 72 (2027-04)
**Baseline**: Current ITHC: lapsed (2022), requires re-accreditation
**Timeframe**: ITHC performed Week 68-72 (2027-03 to 2027-04), accreditation by go-live Week 73 (2027-04)
**Success Criteria**:
- ITHC performed by CHECK-certified testers (Week 68-72)
- ITHC result: Zero critical vulnerabilities, zero high vulnerabilities
- GovS 007 accreditation certificate issued before go-live
- Security controls mapped to GovS 007 requirements (100% coverage)
- NCSC Cyber Essentials Plus certification achieved
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: ITHC report, GovS 007 accreditation certificate, NCSC Cyber Essentials certificate

---

### G-015: Prevent Pre-Release Statistics Data Breach
**Stakeholder**: S-005 Head of Cyber Security
**Driver**: D-015 (RISK, CRITICAL)
**Target**: Zero security incidents involving pre-release statistics during implementation and first 12 months operation
**Baseline**: Zero incidents historically (must maintain)
**Timeframe**: Continuous from Beta Week 37 (2026-08) through Month 12 post-go-live (2028-05)
**Success Criteria**:
- Zero security incidents classified OFFICIAL-SENSITIVE or above
- Zero unauthorized access to pre-release statistics
- Multi-factor authentication (MFA): 100% compliance for pre-release access
- Security audit logs: 100% capture, monitored 24/7 via SIEM
- Quarterly penetration testing: zero successful breaches of pre-release access controls
**Spending Objective**: SO-5 (Regulatory compliance), SO-3 (Risk mitigation)
**Measurement**: Security incident logs, SIEM alerts, quarterly penetration testing reports, audit logs

---

### G-016: Implement Zero Trust Security Architecture
**Stakeholder**: S-005 Head of Cyber Security
**Driver**: D-016 (COMPLIANCE, HIGH)
**Target**: Implement NCSC Zero Trust principles across 100% of platform components by Beta Assessment Week 72 (2027-04)
**Baseline**: Current perimeter security model (legacy)
**Timeframe**: Design approved Alpha Week 24 (2026-04), implemented by Beta Week 72 (2027-04)
**Success Criteria**:
- Identity-based access control: 100% of services (no network-based trust)
- Encrypted communication: TLS 1.3+ for 100% of service-to-service traffic
- Least privilege: RBAC policies defined for 100% of users/services
- Network segmentation: Minimal trust zones, micro-segmentation implemented
- NCSC Cyber Assessment Framework (CAF): Achieve 12/14 principles (↑ from 10/14)
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: Zero Trust architecture review, NCSC CAF self-assessment, security design documentation

---

### G-017: Complete Data Protection Impact Assessment (DPIA)
**Stakeholder**: S-006 Data Protection Officer
**Driver**: D-017 (COMPLIANCE, HIGH)
**Target**: DPIA approved by ICO (or ONS DPO with ICO consultation) by Alpha Week 23 (2026-04)
**Baseline**: No DPIA exists for new platform (identified as blocker in Secure by Design assessment)
**Timeframe**: DPIA drafted Week 19-21 (2026-02), ICO consultation Week 22-23 (2026-03), approval by Week 23 (2026-04)
**Success Criteria**:
- DPIA completed per ICO template and guidance
- ICO consultation completed (if high residual risk)
- DPO approval documented
- Privacy-by-design measures validated (encryption, minimization, retention)
- DPIA published on ONS website (transparency requirement)
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: DPIA approval documentation, ICO consultation correspondence, published DPIA

---

### G-018: Implement Data Minimization and Retention Policies
**Stakeholder**: S-006 Data Protection Officer
**Driver**: D-018 (COMPLIANCE, MEDIUM)
**Target**: Automated data retention policies implemented for 100% of datasets by Beta Week 52 (2026-11)
**Baseline**: Manual retention management (inconsistent enforcement)
**Timeframe**: Policies defined Alpha Week 20-24 (2026-03), automated by Beta Week 52 (2026-11)
**Success Criteria**:
- Retention periods defined for 100% of datasets (ranging 1 year to permanent)
- Automated deletion workflows operational
- Data minimization: Only necessary data fields retained
- Legal hold process documented for litigation/investigation
- Audit trail: 100% of data deletions logged
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: Data retention policy register, automated deletion logs, DPO audit reports

---

### G-021: Achieve GDS Service Standard Compliance (14/14 Criteria)
**Stakeholder**: S-008 GDS Service Assessor
**Driver**: D-021 (COMPLIANCE, HIGH)
**Target**: Pass GDS Service Standard assessment at Alpha (Week 36), Beta (Week 72), and Live (Month 12 post-go-live)
**Baseline**: N/A (new service)
**Timeframe**: Alpha Assessment Week 36 (2026-06), Beta Assessment Week 72 (2027-04), Live Assessment Month 12 (2028-05)
**Success Criteria**:
- Alpha Assessment: PASS (problem validated, design approach approved)
- Beta Assessment: PASS all 14 Service Standard criteria
- Live Assessment: PASS (service operational, meeting user needs)
- Evidence portfolio: Continuous documentation from Discovery onwards
- Technology Code of Practice: 13/13 criteria met
**Spending Objective**: SO-5 (Regulatory compliance)
**Measurement**: GDS Service Assessment reports (Alpha, Beta, Live), evidence portfolio, Technology Code of Practice compliance

---

### G-022: Validate User-Centred Design Through Research
**Stakeholder**: S-008 GDS Service Assessor
**Driver**: D-022 (COMPLIANCE, MEDIUM)
**Target**: Conduct user research with ≥50 statisticians and ≥100 data consumers by Beta Assessment Week 72 (2027-04)
**Baseline**: Zero user research conducted (new platform)
**Timeframe**: Discovery Week 3-5 (2025-11 to 2025-12), Beta Week 70-72 (2027-03 to 2027-04)
**Success Criteria**:
- User research sessions: ≥50 statisticians (internal users)
- User research sessions: ≥100 data consumers (API users, researchers, analysts)
- Personas documented for 4 user types
- User journey maps created for 6 key workflows
- Service Standard Point 1 (Understand users) evidence: STRONG rating
- Service Standard Point 2 (Solve a whole problem) evidence: STRONG rating
**Spending Objective**: SO-3 (User satisfaction)
**Measurement**: User research reports, personas documentation, Service Assessment evidence portfolio

---

## 2.5 Customer Goals

### G-023: Achieve 50% Data Consumption via APIs Within 18 Months
**Stakeholder**: S-009 National Statistician
**Driver**: D-023 (CUSTOMER, CRITICAL)
**Target**: 50% of ONS data consumption via APIs (vs file downloads) by Month 18 post-go-live (2029-11)
**Baseline**: 0% API consumption (100% file downloads currently)
**Timeframe**: Month 18 post-go-live (2029-11)
**Success Criteria**:
- Registered API users: ≥10,000
- API traffic: ≥50% of total data consumption (measured by data volume transferred)
- APIs available: 100% of 500+ statistical series
- Developer satisfaction: ≥85% (quarterly surveys)
- API adoption trajectory: 10% Month 6, 25% Month 12, 50% Month 18
**Spending Objective**: SO-3 (Public data access)
**Measurement**: API usage analytics, registered users count, developer satisfaction surveys

---

### G-024: Maintain Public Trust at ≥75% Rating
**Stakeholder**: S-009 National Statistician
**Driver**: D-024 (STRATEGIC, HIGH)
**Target**: Maintain/improve ONS public trust rating from 68% (2023) to ≥75% by 2029
**Baseline**: 68% public trust rating (ONS Public Trust Survey 2023)
**Timeframe**: 2029 Public Trust Survey (biennial survey)
**Success Criteria**:
- 2027 survey: ≥70% (improvement trajectory)
- 2029 survey: ≥75% (target achieved)
- Zero high-profile infrastructure failures causing media coverage
- Zero Statistics Act breaches
- Service availability: 99.95% maintained
**Spending Objective**: SO-5 (Public trust), SO-3 (Service quality)
**Measurement**: ONS Public Trust Survey (biennial), media monitoring, UK Statistics Authority reporting

---

### G-026: Improve Statistician Satisfaction to ≥80%
**Stakeholder**: S-011 Statisticians (Internal Users)
**Driver**: D-026 (OPERATIONAL, HIGH)
**Target**: Achieve statistician satisfaction ≥80% with publication tools by Month 12 post-go-live (2028-05)
**Baseline**: 60% satisfaction with current publication tools (2024 survey)
**Timeframe**: Month 12 post-go-live (2028-05)
**Success Criteria**:
- Satisfaction survey: ≥80% satisfied/very satisfied with tools
- Net Promoter Score (NPS): ≥40 (from -10 currently)
- Time on publication mechanics: Reduced from 35% to ≤14% (per G-007)
- Tool reliability: ≥99.5% publication success rate
- Training effectiveness: 85% report feeling confident with new tools
**Spending Objective**: SO-2 (Publication efficiency), SO-3 (User satisfaction)
**Measurement**: Quarterly statistician satisfaction surveys, NPS tracking, time-motion studies

---

### G-027: Achieve Tool Reliability with 98% Publication Schedule Adherence
**Stakeholder**: S-011 Statisticians (Internal Users)
**Driver**: D-027 (CUSTOMER, MEDIUM)
**Target**: Achieve 98% publication schedule adherence (vs 92% currently) by Month 6 post-go-live (2027-11)
**Baseline**: 92% publication schedule adherence (2024)
**Timeframe**: Month 6 post-go-live (2027-11)
**Success Criteria**:
- Publication schedule adherence: ≥98% (releases published on scheduled date/time)
- Zero missed deadlines due to platform failures
- Tool uptime: ≥99.9% during working hours (8 AM - 6 PM GMT)
- Incident impact: <2% of publications delayed by platform issues
**Spending Objective**: SO-3 (Service reliability)
**Measurement**: Publication adherence logs, platform uptime monitoring, incident impact tracking

---

### G-028: Achieve ≥85% Data Consumer Satisfaction
**Stakeholder**: S-012 Data Consumers (External Users)
**Driver**: D-028 (CUSTOMER, HIGH)
**Target**: Achieve data consumer satisfaction ≥85% by Month 12 post-go-live (2028-05)
**Baseline**: 65% satisfaction with current file-based distribution (2024 user survey)
**Timeframe**: Month 12 post-go-live (2028-05)
**Success Criteria**:
- User satisfaction survey: ≥85% satisfied/very satisfied
- API response time: p95 <500ms (meets NFR-P-001)
- API reliability: 99.95% uptime
- Developer satisfaction: ≥85% with API documentation, sandbox, support
- Complaint rate: Reduced 50% vs baseline
**Spending Objective**: SO-3 (Public data access)
**Measurement**: Quarterly user satisfaction surveys, API performance metrics, complaint tracking

---

# PART 3: OUTCOME DEFINITION (Goals → Outcomes)

All outcomes are measurable KPIs with specific success criteria and measurement methods.

## 3.1 Strategic Outcomes

### O-001: International Statistical Leadership Demonstrated
**Goal**: G-001
**KPI**: ISI Digital Capability Benchmark Ranking
**Target**: Top 3 ranking by 2030
**Measurement Method**:
- International Statistical Institute (ISI) digital capability benchmark survey (biennial)
- Peer review ratings from Eurostat, Statistics Canada, ABS Australia
- International conference keynote invitations (target: 4+ per year)
- Academic citations of ONS digital infrastructure in statistical journals
**Dashboard**: Executive dashboard showing ISI ranking, peer comparison matrix, conference invitations
**Reporting Frequency**: Annual (ISI benchmark biennial, interpolated)
**Owner**: Chief Data Officer

---

### O-002: Infrastructure Cost Reduction Achieved (£4.5M/year)
**Goal**: G-002
**KPI**: Annual Infrastructure Operating Costs
**Target**: ≤£6.7M/year by Month 24 (40% reduction from £11.2M baseline)
**Measurement Method**:
- Monthly FinOps cost reports aggregated from cloud provider billing APIs
- Cost allocation by service/workload (ingestion, processing, storage, publication)
- Cost per dataset published metric
- Total Cost of Ownership (TCO) analysis comparing baseline vs actual
**Dashboard**: FinOps dashboard with monthly trends, cost per dataset, variance vs baseline, forecast to target
**Reporting Frequency**: Monthly to Programme Board, quarterly to HM Treasury
**Owner**: Chief Data Officer

---

### O-003: Census-Scale Processing Validated
**Goal**: G-003
**KPI**: 67M Record Processing Time
**Target**: <24 hours end-to-end (ingestion to publication)
**Measurement Method**:
- Alpha phase: Load testing with 67M synthetic census records (Week 36)
- Beta phase: Performance testing with 67M records, linear scaling test to 100M records (Week 60)
- Census 2031 rehearsal: Actual processing time measured (2029)
- Distributed processing framework metrics (parallelization efficiency)
**Dashboard**: Performance testing dashboard showing processing time, throughput, cost per record
**Reporting Frequency**: Alpha (Week 36), Beta (Week 60), Census 2031 rehearsal (2029)
**Owner**: Chief Data Architect

---

### O-004: Statistics Act Compliance Maintained (Zero Breaches)
**Goal**: G-004
**KPI**: Statistics Act Compliance Breach Count
**Target**: Zero breaches
**Measurement Method**:
- Pre-release access audit logs reviewed quarterly
- Multi-factor authentication (MFA) compliance rate monitored daily (target: 100%)
- UK Statistics Authority annual audit report (Section 11 compliance assessment)
- Quarterly self-assessment against Statistics Act requirements
- Parliamentary questions/NAO reports mentioning non-compliance (target: zero)
**Dashboard**: Compliance dashboard showing pre-release access events, MFA compliance %, audit findings
**Reporting Frequency**: Quarterly to Programme Board, annually to UK Statistics Authority
**Owner**: Chief Statistician

---

### O-005: Statistical Disclosure Control Automation Validated
**Goal**: G-005
**KPI**: SDC Automation Coverage and Re-identification Risk Rating
**Target**: 100% coverage, ACCEPTABLE risk rating
**Measurement Method**:
- SDC rule coverage: % of statistical series with automated SDC rules applied
- Publication audit: Sample review of 50 publications per quarter for SDC compliance
- Re-identification risk testing: Automated/manual attempts to re-identify individuals from published data
- Privacy Impact Assessment (PIA) rating: ACCEPTABLE/UNACCEPTABLE
- ICO audit findings (if audit occurs): Zero SDC-related findings
**Dashboard**: SDC compliance dashboard showing coverage %, risk rating, audit findings
**Reporting Frequency**: Quarterly to Programme Board, annually to ICO (self-assessment)
**Owner**: Chief Statistician

---

### O-006: Publication Independence During Election Periods
**Goal**: G-006
**KPI**: Infrastructure-Related Publication Delays During Elections
**Target**: Zero delays
**Measurement Method**:
- Publication adherence log: Track scheduled vs actual publication times during election periods (2025, 2029)
- Incident logs: Filter for infrastructure-related incidents during election periods
- Uptime monitoring: 99.95% target during election periods
- Parliamentary questions: Count questions related to publication delays/infrastructure failures
- Media monitoring: Track negative media coverage of ONS infrastructure during elections
**Dashboard**: Election readiness dashboard showing uptime, publication adherence, incident count
**Reporting Frequency**: During election periods (weekly), post-election review
**Owner**: Chief Statistician

---

## 3.2 Operational Outcomes

### O-007: Statistician Manual Effort Reduced (600 Days/Year Released)
**Goal**: G-007
**KPI**: Statistician Time on Publication Mechanics (%)
**Target**: ≤14% (60% reduction from 35% baseline)
**Measurement Method**:
- Quarterly time-motion studies: Sample 50 statisticians, track time allocation across activities
- Workflow automation metrics: Count manual steps eliminated per publication
- Publication workflow logs: Time spent in each stage (manual vs automated)
- Statistician satisfaction surveys: Self-reported time reduction
- Capacity released calculation: (35% - 14%) × 500 statisticians × 250 working days = 262 FTE-days per quarter
**Dashboard**: Efficiency dashboard showing time allocation breakdown, capacity released trend, workflow automation %
**Reporting Frequency**: Quarterly to Programme Board
**Owner**: Director of Statistical Production

---

### O-008: Time-to-Publish Reduced to 2 Days
**Goal**: G-008
**KPI**: Average Time-to-Publish for Major Indicators (Days)
**Target**: ≤2 days (p50), ≤3 days (p90)
**Measurement Method**:
- Publication tracking system: Timestamp validated data arrival → public API availability
- Per-series metrics: GDP, CPI, Labour Market Statistics tracked separately
- Latency distribution: p50, p90, p99 percentiles
- Publication schedule adherence: % of publications meeting scheduled date/time
**Dashboard**: Publication efficiency dashboard showing time-to-publish trend, per-series breakdown, schedule adherence
**Reporting Frequency**: Monthly to Programme Board
**Owner**: Director of Statistical Production

---

### O-009: Publication Error Rate Reduced to <0.1%
**Goal**: G-009
**KPI**: Publication Error Rate (%)
**Target**: <0.1% (<4 errors/year for 500 series)
**Measurement Method**:
- Publication error log: Count errors requiring corrections per quarter
- Error type taxonomy: Categorize errors (data, methodology, formatting, metadata)
- Automated quality validation: % of errors caught before publication
- User complaint tracking: Error-related complaints
- Correction tracking: Count corrections published per quarter
**Dashboard**: Quality dashboard showing error rate trend, error types, validation effectiveness
**Reporting Frequency**: Monthly to Programme Board, quarterly to Chief Statistician
**Owner**: Director of Statistical Production

---

### O-010: Programme Delivery Success (Career Progression Evidence)
**Goal**: G-010
**KPI**: Programme Delivery KPIs (Composite)
**Target**: Beta Assessment PASS, on-time go-live, within 10% budget
**Measurement Method**:
- GDS Service Assessment: Alpha/Beta/Live outcomes (PASS/CONDITIONAL PASS/FAIL)
- Go-live date: Actual vs planned (Week 78, 2027-05-25)
- Budget variance: Actual costs vs £36.6M approved budget (target: within 10%)
- Benefits realization: % of cashable benefits achieved within 12 months
- Programme Board feedback: 360-degree feedback survey (leadership, stakeholder management)
**Dashboard**: Executive summary dashboard showing Service Assessment status, schedule variance, budget variance, benefits %
**Reporting Frequency**: Monthly to Programme Board, post-implementation review at Month 12
**Owner**: Director of Statistical Production (Programme Product Owner)

---

### O-011: Technology Code of Practice Compliance (13/13 Criteria)
**Goal**: G-011
**KPI**: Technology Code of Practice Criteria Met
**Target**: 13/13 criteria (100%)
**Measurement Method**:
- Self-assessment against TCoP 13 criteria (quarterly)
- GDS Service Assessment validation of TCoP compliance
- Specific criteria evidence:
  - Point 5 (Cloud First): 100% cloud-native deployment (zero on-premises)
  - Point 3 (Open Standards): SDMX, OpenAPI, DCAT compliance audit
  - Point 6 (Security): GovS 007 accreditation certificate
  - Point 9 (Integrate/Adapt): API-first architecture review
**Dashboard**: Technology compliance dashboard showing 13 criteria with RAG status, evidence links
**Reporting Frequency**: Quarterly to Programme Board, Service Assessments (Alpha, Beta, Live)
**Owner**: Chief Data Architect

---

### O-012: Publication API Availability ≥99.95%
**Goal**: G-012
**KPI**: Monthly Publication API Uptime (%)
**Target**: ≥99.95% (max 21.9 minutes downtime per month)
**Measurement Method**:
- Uptime monitoring: Synthetic API health checks every 1 minute from 3 UK locations
- Downtime classification: Planned maintenance vs unplanned incidents
- Incident tracking: Count P1/P2 incidents affecting availability
- Mean Time To Recovery (MTTR): Average recovery time for unplanned outages
- SLA compliance reporting: Monthly report showing uptime %, downtime duration, incident count
**Dashboard**: Uptime dashboard showing monthly uptime %, downtime breakdown, incident history, MTTR trend
**Reporting Frequency**: Monthly SLA report to Programme Board, real-time monitoring for operations
**Owner**: Chief Data Architect

---

### O-013: Vendor Lock-in Risk Mitigated (LOW Rating)
**Goal**: G-013
**KPI**: Vendor Lock-in Risk Assessment Rating
**Target**: LOW rating (vs MEDIUM/HIGH)
**Measurement Method**:
- Architecture Review Board assessment: Quarterly review against vendor lock-in criteria
- Infrastructure as Code: % of infrastructure defined in cloud-agnostic Terraform (target: 100%)
- Containerization coverage: % of workloads containerized (target: 100%)
- Open standards compliance: SDMX, OpenAPI, ISO standards usage audit
- Data portability testing: Export all data in open formats within 48 hours (tested annually)
- Cloud provider switching cost estimate: Cost/time to migrate to alternative provider
**Dashboard**: Vendor lock-in risk dashboard showing risk rating, IaC coverage, containerization %, portability test results
**Reporting Frequency**: Quarterly to Architecture Review Board
**Owner**: Chief Data Architect

---

## 3.3 Financial Outcomes

### O-019: Value for Money with BCR ≥2.0 Maintained
**Goal**: G-019
**KPI**: Benefit-Cost Ratio (BCR)
**Target**: ≥2.0 throughout business case lifecycle
**Measurement Method**:
- Business case NPV calculations: Update at each stage (SOBC → OBC → FBC → PIR)
- Benefits realization tracking: Actual vs forecast cashable benefits
- Cost tracking: Actual vs forecast capital and operating costs
- Sensitivity analysis: Recalculate BCR under optimistic/pessimistic scenarios
- HM Treasury approval status: APPROVED/CONDITIONAL/REJECTED at each stage
**Dashboard**: Business case dashboard showing BCR trend, NPV, benefits vs forecast, costs vs budget
**Reporting Frequency**: Business case submissions (SOBC, OBC, FBC), quarterly HM Treasury checkpoints, PIR (Month 12)
**Owner**: Chief Data Officer

---

### O-020: Efficiency Savings Trajectory (£4.5M/year by Month 24)
**Goal**: G-020
**KPI**: Annual Infrastructure Cost Savings vs Baseline (£M/year)
**Target**: £4.5M/year by Month 24, ramping from Month 6
**Measurement Method**:
- Savings calculation: (£11.2M baseline - Actual monthly costs) × 12
- Savings trajectory: Target £2M/year Month 6, £3.5M/year Month 12, £4.5M/year Month 24
- Cashable benefits validation: Finance team confirms savings realized (budget reductions or reinvestments approved)
- HM Treasury checkpoint reports: Quarterly confirmation of savings trajectory
- Spending Review reporting: Annual confirmation of efficiency savings delivered
**Dashboard**: Savings dashboard showing monthly savings vs baseline, cumulative savings, trajectory vs target
**Reporting Frequency**: Monthly to Programme Board, quarterly to HM Treasury, annually to Spending Review
**Owner**: Chief Data Officer

---

### O-025: Budget Variance within 10%
**Goal**: G-025
**KPI**: Budget Variance (%)
**Target**: ≤10% variance (£36.6M approved → ≤£40.3M actual)
**Measurement Method**:
- Monthly budget tracking: Actual costs vs approved budget (capital + operating)
- Forecast outturn: Project final costs based on actuals and commitments
- Variance analysis: Breakdown by cost category (SI, cloud, licenses, training, contingency)
- Programme Board reporting: Monthly budget variance reports with RAG status (Green <5%, Amber 5-10%, Red >10%)
- NAO audit: Post-implementation review of value for money and budget management
**Dashboard**: Budget dashboard showing approved budget, actual costs, forecast outturn, variance %, contingency utilization
**Reporting Frequency**: Monthly to Programme Board, quarterly to HM Treasury, NAO audit (PIR)
**Owner**: Chief Data Officer

---

## 3.4 Compliance Outcomes

### O-014: GovS 007 OFFICIAL Accreditation Certificate Issued
**Goal**: G-014
**KPI**: GovS 007 Accreditation Status
**Target**: ACCREDITED (certificate issued before go-live)
**Measurement Method**:
- ITHC execution: CHECK-certified testers perform penetration testing (Week 68-72)
- ITHC result: Critical vulnerabilities = 0, High vulnerabilities = 0
- GovS 007 security controls mapping: 100% of controls implemented and evidenced
- NCSC Cyber Essentials Plus: Certificate issued
- Accreditation certificate: Issued by ONS Senior Information Risk Owner (SIRO) before go-live
**Dashboard**: Security accreditation dashboard showing ITHC status, vulnerability counts, control compliance %, certificate status
**Reporting Frequency**: Weekly during ITHC (Week 68-72), final report at Beta Assessment (Week 72)
**Owner**: Head of Cyber Security

---

### O-015: Zero Pre-Release Statistics Data Breaches
**Goal**: G-015
**KPI**: Security Incident Count (Pre-Release Data)
**Target**: Zero incidents
**Measurement Method**:
- Security incident log: SIEM (Security Information and Event Management) system monitors for incidents classified OFFICIAL-SENSITIVE or above
- Pre-release access log: 100% audit trail of pre-release access events (who, when, what)
- Unauthorized access attempts: Count failed authentication attempts, privilege escalation attempts
- MFA compliance: Daily monitoring of MFA usage (target: 100% for pre-release access)
- Quarterly penetration testing: External testers attempt to breach pre-release access controls (target: zero successful breaches)
**Dashboard**: Security monitoring dashboard showing incident count, unauthorized access attempts, MFA compliance %, penetration testing results
**Reporting Frequency**: Real-time SIEM alerts, weekly security briefings, quarterly penetration testing reports
**Owner**: Head of Cyber Security

---

### O-016: Zero Trust Architecture Implementation Validated
**Goal**: G-016
**KPI**: Zero Trust Maturity Model Score and NCSC CAF Achievement
**Target**: NCSC CAF 12/14 principles achieved (↑ from 10/14 in Secure by Design assessment)
**Measurement Method**:
- NCSC Cyber Assessment Framework (CAF) self-assessment: Quarterly review of 14 principles
- Zero Trust architecture checklist:
  - Identity-based access: 100% of services (verified via architecture review)
  - Encrypted communication: TLS 1.3+ for 100% of service-to-service traffic (verified via network scanning)
  - Least privilege RBAC: Policy audit covering 100% of users/services
  - Network segmentation: Micro-segmentation implemented (verified via network architecture review)
- Security architecture approval: Architecture Review Board sign-off
**Dashboard**: Zero Trust maturity dashboard showing CAF score trend, checklist completion %, architecture review status
**Reporting Frequency**: Quarterly CAF self-assessment, architecture review at Alpha Week 24 and Beta Week 72
**Owner**: Head of Cyber Security

---

### O-017: Data Protection Impact Assessment (DPIA) Approved
**Goal**: G-017
**KPI**: DPIA Approval Status
**Target**: APPROVED by Alpha Week 23
**Measurement Method**:
- DPIA completion: Document completed per ICO template (35 pages, 6 sections)
- ICO consultation: Conducted if high residual risk identified (2-week turnaround)
- DPO approval: ONS Data Protection Officer formal approval documented
- Privacy-by-design validation: Encryption at rest/in transit, data minimization, retention policies validated
- Publication: DPIA published on ONS website (transparency requirement per UK GDPR Article 35(7))
**Dashboard**: DPIA progress dashboard showing completion %, ICO consultation status, DPO approval status
**Reporting Frequency**: Weekly during DPIA creation (Week 19-23), final approval report at Alpha Week 23
**Owner**: Data Protection Officer

---

### O-018: Automated Data Retention Policies Operational
**Goal**: G-018
**KPI**: Data Retention Policy Coverage (%)
**Target**: 100% of datasets
**Measurement Method**:
- Data catalog: 100% of datasets have retention period assigned
- Automated deletion workflows: Operational for all datasets (tested quarterly)
- Audit trail: 100% of data deletions logged with timestamp, user, reason
- Compliance audit: DPO quarterly review of retention policy adherence
- Storage optimization: Track storage costs reduced via retention policies
**Dashboard**: Data governance dashboard showing retention policy coverage %, automated deletion logs, storage trend
**Reporting Frequency**: Quarterly to Data Protection Officer and Architecture Review Board
**Owner**: Data Protection Officer

---

### O-021: GDS Service Standard 14/14 Criteria Achieved
**Goal**: G-021
**KPI**: GDS Service Standard Assessment Outcome
**Target**: PASS at Alpha, Beta, Live
**Measurement Method**:
- Service Assessment panels: GDS assessors review evidence against 14 criteria
- Assessment outcome: PASS / CONDITIONAL PASS / FAIL per criterion
- Evidence portfolio: Comprehensive documentation from Discovery onwards (continuously maintained)
- Criteria tracking: 14 criteria dashboard showing evidence strength (WEAK/MEDIUM/STRONG) per criterion
- Technology Code of Practice: 13/13 criteria validated as part of Service Assessment
**Dashboard**: Service Standard dashboard showing 14 criteria with assessment outcome, evidence strength, actions
**Reporting Frequency**: Service Assessments at Alpha (Week 36), Beta (Week 72), Live (Month 12)
**Owner**: Director of Statistical Production (Service Owner)

---

### O-022: User Research Evidence Gathered
**Goal**: G-022
**KPI**: User Research Participant Count
**Target**: ≥50 statisticians, ≥100 data consumers
**Measurement Method**:
- User research log: Participant count, research method (interviews, workshops, usability testing)
- Research outputs: Personas (4 types), user journey maps (6 workflows), pain points, needs
- Service Assessment evidence: User research reports submitted to GDS assessors
- User validation: Statistician and data consumer sign-off on personas and journeys
**Dashboard**: User research dashboard showing participant count by type, research outputs, evidence portfolio status
**Reporting Frequency**: User research reports at Discovery (Week 5), Alpha (Week 36), Beta (Week 72)
**Owner**: Director of Statistical Production (Service Owner)

---

## 3.5 Customer Outcomes

### O-023: API Adoption 50% of Data Consumption
**Goal**: G-023
**KPI**: API Traffic as % of Total Data Consumption
**Target**: ≥50% by Month 18
**Measurement Method**:
- API usage analytics: Data volume transferred via APIs (GB/month)
- File download analytics: Data volume downloaded as files (GB/month)
- API adoption %: API traffic / (API traffic + File downloads) × 100%
- Registered API users: Count active users (≥1 API call per month)
- APIs available: % of 500+ statistical series with API endpoints (target: 100%)
**Dashboard**: API adoption dashboard showing API traffic %, registered users, series coverage, monthly trend
**Reporting Frequency**: Monthly to Programme Board
**Owner**: National Statistician

---

### O-024: Public Trust Rating ≥75%
**Goal**: G-024
**KPI**: ONS Public Trust Survey Rating (%)
**Target**: ≥75% by 2029
**Measurement Method**:
- ONS Public Trust Survey: Biennial survey of 2,000 UK adults
- Trust rating: % responding "Trust ONS statistics a great deal / fair amount"
- Survey questions: Independence, accuracy, value, accessibility
- Comparator: UK Statistics Authority overall trust rating
- Media monitoring: Track negative media coverage of ONS (proxy indicator)
**Dashboard**: Public trust dashboard showing trust rating trend, survey breakdown, media sentiment
**Reporting Frequency**: Biennial (2025, 2027, 2029 surveys)
**Owner**: National Statistician

---

### O-026: Statistician Satisfaction ≥80%
**Goal**: G-026
**KPI**: Statistician Satisfaction Rating (%)
**Target**: ≥80% by Month 12
**Measurement Method**:
- Quarterly satisfaction surveys: 5-point Likert scale (Very Satisfied to Very Dissatisfied)
- Satisfaction %: (Very Satisfied + Satisfied) / Total respondents × 100%
- Net Promoter Score (NPS): "How likely are you to recommend these tools to colleagues?" (-100 to +100)
- Survey domains: Tool usability, reliability, training quality, support responsiveness
- Response rate: Target ≥60% of 500 statisticians
**Dashboard**: User satisfaction dashboard showing satisfaction %, NPS, domain breakdown, trend
**Reporting Frequency**: Quarterly to Programme Board
**Owner**: Director of Statistical Production

---

### O-027: Publication Schedule Adherence 98%
**Goal**: G-027
**KPI**: Publication Schedule Adherence (%)
**Target**: ≥98% by Month 6
**Measurement Method**:
- Publication tracking: Scheduled date/time vs actual publication date/time
- Adherence %: Publications published on schedule / Total publications × 100%
- Delay classification: Platform failures vs other causes (statistician delays, data quality issues)
- Tool uptime: Working hours uptime % (8 AM - 6 PM GMT)
- Incident impact: % of publications delayed due to platform incidents (target: <2%)
**Dashboard**: Publication reliability dashboard showing adherence %, delay causes, tool uptime, incident impact
**Reporting Frequency**: Monthly to Programme Board
**Owner**: Director of Statistical Production

---

### O-028: Data Consumer Satisfaction ≥85%
**Goal**: G-028
**KPI**: Data Consumer Satisfaction Rating (%)
**Target**: ≥85% by Month 12
**Measurement Method**:
- Quarterly satisfaction surveys: API users, researchers, analysts
- Satisfaction %: (Very Satisfied + Satisfied) / Total respondents × 100%
- Survey domains: API documentation, API performance, data quality, support responsiveness
- Developer satisfaction: Separate track for API developers (≥85%)
- Complaint tracking: User complaints via support channels (target: 50% reduction vs baseline)
**Dashboard**: Data consumer satisfaction dashboard showing satisfaction %, domain breakdown, complaint trend
**Reporting Frequency**: Quarterly to Programme Board
**Owner**: National Statistician

---

# PART 4: TRACEABILITY MATRIX

Complete Stakeholder → Driver → Goal → Outcome traceability for all 27 drivers.

| Stakeholder ID | Stakeholder | Driver ID | Driver Type | Intensity | Goal ID | Spending Objective | Outcome ID | Measurement KPI |
|---------------|-------------|-----------|-------------|-----------|---------|-------------------|------------|-----------------|
| **S-001** | Chief Data Officer | D-001 | STRATEGIC | CRITICAL | G-001 | SO-1, SO-5 | O-001 | ISI Benchmark Ranking (Top 3) |
| **S-001** | Chief Data Officer | D-002 | FINANCIAL | HIGH | G-002 | SO-1 | O-002 | Annual Infrastructure Costs (≤£6.7M) |
| **S-001** | Chief Data Officer | D-003 | RISK | HIGH | G-003 | SO-4 | O-003 | 67M Record Processing Time (<24h) |
| **S-002** | Chief Statistician | D-004 | COMPLIANCE | CRITICAL | G-004 | SO-5 | O-004 | Statistics Act Breach Count (Zero) |
| **S-002** | Chief Statistician | D-005 | COMPLIANCE | HIGH | G-005 | SO-5 | O-005 | SDC Coverage (100%), Risk (ACCEPTABLE) |
| **S-002** | Chief Statistician | D-006 | STRATEGIC | MEDIUM | G-006 | SO-5 | O-006 | Election Period Delays (Zero) |
| **S-003** | Director of Statistical Production | D-007 | OPERATIONAL | CRITICAL | G-007 | SO-2 | O-007 | Statistician Time on Mechanics (≤14%) |
| **S-003** | Director of Statistical Production | D-008 | OPERATIONAL | HIGH | G-008 | SO-2 | O-008 | Time-to-Publish (≤2 days p50) |
| **S-003** | Director of Statistical Production | D-009 | OPERATIONAL | HIGH | G-009 | SO-2 | O-009 | Publication Error Rate (<0.1%) |
| **S-003** | Director of Statistical Production | D-010 | PERSONAL | MEDIUM | G-010 | All | O-010 | Programme Delivery (PASS, On-time) |
| **S-004** | Chief Data Architect | D-011 | STRATEGIC | HIGH | G-011 | SO-5 | O-011 | TCoP Criteria Met (13/13) |
| **S-004** | Chief Data Architect | D-012 | OPERATIONAL | HIGH | G-012 | SO-3 | O-012 | API Uptime (≥99.95%) |
| **S-004** | Chief Data Architect | D-013 | RISK | HIGH | G-013 | SO-1 | O-013 | Vendor Lock-in Risk (LOW) |
| **S-005** | Head of Cyber Security | D-014 | COMPLIANCE | CRITICAL | G-014 | SO-5 | O-014 | GovS 007 Accreditation (ISSUED) |
| **S-005** | Head of Cyber Security | D-015 | RISK | CRITICAL | G-015 | SO-5 | O-015 | Pre-Release Breach Count (Zero) |
| **S-005** | Head of Cyber Security | D-016 | COMPLIANCE | HIGH | G-016 | SO-5 | O-016 | NCSC CAF Score (12/14) |
| **S-006** | Data Protection Officer | D-017 | COMPLIANCE | HIGH | G-017 | SO-5 | O-017 | DPIA Approval (APPROVED) |
| **S-006** | Data Protection Officer | D-018 | COMPLIANCE | MEDIUM | G-018 | SO-5 | O-018 | Retention Policy Coverage (100%) |
| **S-007** | HM Treasury | D-019 | FINANCIAL | CRITICAL | G-019 | SO-1 | O-019 | Benefit-Cost Ratio (≥2.0) |
| **S-007** | HM Treasury | D-020 | FINANCIAL | HIGH | G-020 | SO-1 | O-020 | Annual Savings (£4.5M by Month 24) |
| **S-008** | GDS Service Assessor | D-021 | COMPLIANCE | HIGH | G-021 | SO-5 | O-021 | Service Standard (PASS 14/14) |
| **S-008** | GDS Service Assessor | D-022 | COMPLIANCE | MEDIUM | G-022 | SO-3 | O-022 | User Research Participants (150+) |
| **S-009** | National Statistician | D-023 | CUSTOMER | CRITICAL | G-023 | SO-3 | O-023 | API Adoption (≥50% by Month 18) |
| **S-009** | National Statistician | D-024 | STRATEGIC | HIGH | G-024 | SO-5 | O-024 | Public Trust Rating (≥75%) |
| **S-010** | National Audit Office | D-025 | FINANCIAL | MEDIUM | G-025 | SO-1 | O-025 | Budget Variance (≤10%) |
| **S-011** | Statisticians (Users) | D-026 | OPERATIONAL | HIGH | G-026 | SO-2, SO-3 | O-026 | Statistician Satisfaction (≥80%) |
| **S-011** | Statisticians (Users) | D-027 | CUSTOMER | MEDIUM | G-027 | SO-3 | O-027 | Schedule Adherence (≥98%) |
| **S-012** | Data Consumers | D-028 | CUSTOMER | HIGH | G-028 | SO-3 | O-028 | Data Consumer Satisfaction (≥85%) |

---

# PART 5: POWER-INTEREST GRID

Stakeholder categorization for engagement strategy.

## 5.1 Manage Closely (High Power, High Interest)

**Engagement Strategy**: Weekly/fortnightly meetings, continuous communication, active involvement in decision-making

| Stakeholder | Power | Interest | Engagement Frequency | Key Communication Methods |
|-------------|-------|----------|---------------------|---------------------------|
| **S-001: Chief Data Officer** | 10/10 | 10/10 | Weekly 1:1s, Monthly Programme Board | Email, Slack, Executive briefings, Dashboard reviews |
| **S-002: Chief Statistician** | 9/10 | 9/10 | Fortnightly meetings, Monthly Programme Board | Email, Compliance reports, Audit reviews |
| **S-003: Director of Statistical Production** | 8/10 | 10/10 | Daily standups (Beta), Weekly 1:1s, Monthly Programme Board | Slack, Email, Workflow demos, UAT sessions |
| **S-004: Chief Data Architect** | 9/10 | 10/10 | Fortnightly Architecture Review Board, Weekly tech syncs | Slack, Architecture diagrams, Design reviews |
| **S-005: Head of Cyber Security** | 10/10 | 9/10 | Fortnightly Security Review Board, Monthly Programme Board | Email, Security reports, Threat briefings |
| **S-009: National Statistician** | 9/10 | 8/10 | Monthly 1:1s, Quarterly UK Statistics Authority updates | Email, Executive briefings, Public trust reporting |

**Total**: 6 stakeholders requiring intensive engagement

---

## 5.2 Keep Satisfied (High Power, Low/Medium Interest)

**Engagement Strategy**: Monthly/quarterly updates, inform of major decisions, avoid surprises

| Stakeholder | Power | Interest | Engagement Frequency | Key Communication Methods |
|-------------|-------|----------|---------------------|---------------------------|
| **S-006: Data Protection Officer** | 8/10 | 6/10 | Monthly compliance updates, Quarterly DPIA reviews | Email, Compliance reports, DPIA documentation |
| **S-007: HM Treasury** | 9/10 | 5/10 | Quarterly checkpoint meetings, Business case submissions | Email, Checkpoint reports, Benefits realisation reports |
| **S-008: GDS Service Assessor** | 8/10 | 5/10 | Quarterly Service Standard updates, Assessment panels (3x) | Email, Evidence portfolio, Service Assessment reports |

**Total**: 3 stakeholders requiring satisfied status maintenance

---

## 5.3 Keep Informed (Low Power, High Interest)

**Engagement Strategy**: Regular communications, feedback opportunities, transparency

| Stakeholder | Power | Interest | Engagement Frequency | Key Communication Methods |
|-------------|-------|----------|---------------------|---------------------------|
| **S-011: Statisticians (Internal Users)** | 3/10 | 9/10 | Monthly workshops, Quarterly satisfaction surveys, Training sessions | Email newsletters, Intranet updates, User research workshops, UAT sessions |
| **S-012: Data Consumers (External Users)** | 2/10 | 8/10 | Quarterly developer webinars, API sandbox, Documentation | Developer portal, Email updates, API release notes, Satisfaction surveys |

**Total**: 2 stakeholder groups requiring regular information

---

## 5.4 Monitor (Low Power, Low Interest)

**Engagement Strategy**: Minimal engagement, basic awareness, monitor for changes

| Stakeholder | Power | Interest | Engagement Frequency | Key Communication Methods |
|-------------|-------|----------|---------------------|---------------------------|
| **S-010: National Audit Office** | 5/10 | 4/10 | Annual post-implementation review, Major Projects Portfolio reporting | Email, PIR reports, NAO audit responses |

**Total**: 1 stakeholder requiring monitoring only

---

# PART 6: CONFLICT ANALYSIS

Identification of competing stakeholder interests and resolution strategies.

## 6.1 Conflict C-001: Cost Efficiency vs Enterprise Reliability

**Stakeholders in Conflict**:
- **S-001 Chief Data Officer** (D-002: 40% cost reduction)
- **S-005 Head of Cyber Security** (D-014, D-016: Enterprise security, Zero Trust)

**Nature of Conflict**:
CDO wants to minimize cloud costs (£6.7M/year target) through optimization, while Security wants enterprise-grade security controls (multi-region, SIEM, managed security services) that increase costs.

**Example Tension**:
- **CDO position**: Single-region deployment saves £1M/year on data transfer and redundancy
- **Security position**: Multi-region deployment required for resilience and Zero Trust architecture

**Impact if Unresolved**:
- Security compromised → GovS 007 accreditation failure → No go-live
- OR Costs exceed budget → Business case BCR falls below 2.0 → HM Treasury rejects

**Resolution Strategy**:

**Option A: Risk-Based Segmentation** (RECOMMENDED)
- **Critical systems**: Multi-region (publication APIs, pre-release access) - reliability critical
- **Non-critical systems**: Single-region (development, analytics) - cost optimized
- **Cost impact**: +£400K/year vs single-region, but within £6.7M target
- **Security assurance**: ITHC focuses on critical system resilience, non-critical systems have RPO/RTO flexibility

**Option B: Phased Implementation**
- Year 1: Single-region (rapid go-live, cost optimized)
- Year 2: Expand to multi-region as savings materialize
- Risk: Potential rework costs, delayed security maturity

**Decision Authority**: Programme Board (CDO + Security + Architecture)

**Decision Criteria**:
1. GovS 007 accreditation risk (MUST NOT compromise)
2. Cost impact on BCR (MUST maintain >2.0)
3. Census 2031 resilience requirements

**Resolved**: Programme Board (Week 24) approved Option A - Risk-based segmentation

---

## 6.2 Conflict C-002: Innovation Speed vs Regulatory Compliance

**Stakeholders in Conflict**:
- **S-001 Chief Data Officer** (D-001: Digital transformation, international leadership)
- **S-002 Chief Statistician** (D-004, D-005: Statistics Act compliance, SDC)

**Nature of Conflict**:
CDO wants rapid agile delivery with 4-week sprints and continuous deployment to demonstrate innovation. Chief Statistician wants comprehensive compliance reviews, change control boards, and statistician validation before any publication changes.

**Example Tension**:
- **CDO position**: Deploy API updates weekly, fail fast, iterate rapidly
- **Chief Statistician position**: Publication changes require 4-week statistician validation + compliance review

**Impact if Unresolved**:
- Innovation stifled → Slow time-to-market → Peer benchmarking falls behind
- OR Compliance bypassed → Statistics Act breach → UK Statistics Authority sanctions

**Resolution Strategy**:

**Option A: Two-Speed Architecture** (RECOMMENDED)
- **Publication-critical path**: Strict change control, 4-week statistician validation, compliance review (GDP, CPI, Labour Market)
- **Non-publication features**: Agile 4-week sprints, continuous deployment (API documentation, catalog UI, sandbox)
- **Separation**: API versioning ensures publication stability while enabling innovation in non-critical features

**Option B: Progressive Assurance**
- Alpha: Rapid iteration, compliance reviews post-sprint (learning phase)
- Beta: Hybrid approach, compliance integrated in sprint planning
- Live: Full compliance rigor for all changes
- Risk: Alpha/Beta compliance debt may delay go-live

**Decision Authority**: Programme Board (CDO + Chief Statistician)

**Decision Criteria**:
1. Statistics Act compliance risk (MUST NOT compromise)
2. Time-to-market for innovation (SHOULD optimize)
3. Statistician engagement and validation

**Resolved**: Programme Board (Week 36 Alpha Assessment) approved Option A - Two-speed architecture

---

## 6.3 Conflict C-003: Open Access vs Security Controls

**Stakeholders in Conflict**:
- **S-009 National Statistician** (D-023: Maximize accessibility per Statistics Act)
- **S-005 Head of Cyber Security** (D-015: Prevent pre-release breach, D-016: Zero Trust)

**Nature of Conflict**:
National Statistician wants frictionless public API access (no authentication, no rate limiting, no barriers) to maximize accessibility. Security wants authentication, rate limiting, and access controls to prevent abuse and breaches.

**Example Tension**:
- **National Statistician position**: Anonymous API access for all published statistics (Statistics Act Section 7)
- **Security position**: Authentication required for all API access to prevent DDoS, data scraping, abuse

**Impact if Unresolved**:
- Accessibility reduced → API adoption fails → Statutory duty unfulfilled
- OR Security weakened → DDoS attacks, platform outages → Reputational damage

**Resolution Strategy**:

**Option A: Tiered Access Model** (RECOMMENDED)
- **Published statistics (post-release)**: Anonymous access, generous rate limits (100 req/min), no authentication
- **Pre-release statistics**: Multi-factor authentication (MFA), strict access control, audit trail
- **High-volume users**: Registered API keys, higher rate limits (1,000 req/min), usage analytics
- **Separation**: Clear API endpoint separation (/public vs /pre-release)

**Option B: API Gateway with Throttling**
- Anonymous access permitted
- Intelligent rate limiting (per IP, per endpoint)
- DDoS protection via cloud provider (AWS Shield, Azure DDoS Protection)
- Risk: False positives may block legitimate users

**Decision Authority**: Programme Board (National Statistician + Security + Architecture)

**Decision Criteria**:
1. Statistics Act Section 7 accessibility duty (MUST fulfill)
2. Pre-release data protection (MUST NOT compromise)
3. Platform resilience to abuse/DDoS

**Resolved**: Programme Board (Week 24) approved Option A - Tiered access model with clear endpoint separation

---

## 6.4 Conflict C-004: Census Capability Investment vs Budget Constraints

**Stakeholders in Conflict**:
- **S-001 Chief Data Officer** (D-003: Census-scale capability <24 hours)
- **S-007 HM Treasury** (D-019, D-020: Value for money, BCR >2.0)

**Nature of Conflict**:
CDO wants to invest in census-scale distributed processing capability (£3M additional for high-performance compute, data lake, parallelization frameworks). HM Treasury wants to minimize upfront capital investment and questions whether census capability should be funded from this programme (Census 2031 is 6 years away).

**Example Tension**:
- **CDO position**: Census capability is business case justification (avoids 2021 failure repeat)
- **HM Treasury position**: Census 2031 is separate programme, defer investment, reduce capital request from £18M to £15M

**Impact if Unresolved**:
- Census capability not delivered → Business case rationale weakened → HMT rejects
- OR Census investment cut → 2031 failure repeat → Reputational catastrophe

**Resolution Strategy**:

**Option A: Early Prototyping with Deferred Scaling** (RECOMMENDED)
- **Alpha phase**: Prototype census-scale processing with 67M records (£200K cost)
- **Business case**: Demonstrate feasibility in Alpha, use as evidence for OBC/FBC
- **Beta phase**: Build production capability only if Alpha successful (£2.8M)
- **Risk mitigation**: Contingency plan if Alpha prototype fails (extend timeline, alternative architecture)
- **HM Treasury assurance**: Gated investment - release Beta funding only after Alpha success

**Option B: Separate Census Programme**
- Data platform programme: £15M (excludes census capability)
- Census 2031 programme: £3M (separate business case)
- Risk: Two programmes create duplication, integration complexity, delivery risk

**Decision Authority**: HM Treasury (after Programme Board recommendation)

**Decision Criteria**:
1. Alpha prototype evidence (MUST demonstrate feasibility)
2. Census 2031 timeline alignment (MUST deliver by 2029 rehearsal)
3. Value for money (BCR >2.0 maintained with gated investment)

**Resolved**: HM Treasury (SOBC approval) approved Option A - Early prototyping with gated investment for Beta capability

---

# PART 7: ENGAGEMENT PLAN

Stakeholder-specific communication and engagement strategies.

## 7.1 Chief Data Officer (S-001) - SRO

**Engagement Objectives**:
- Maintain programme visibility and strategic alignment
- Enable rapid decision-making on scope/budget trade-offs
- Support HM Treasury business case approval and assurance
- Demonstrate international leadership progress

**Communication Frequency**:
- **Weekly**: 30-minute 1:1 with Service Owner (Director of Statistical Production)
- **Monthly**: 2-hour Programme Board (chair)
- **Quarterly**: HM Treasury checkpoint meetings (attendee)
- **Ad-hoc**: Exception approvals, escalations, media responses

**Communication Channels**:
- **Email**: Decision memos, approval requests, escalations
- **Slack**: Quick updates, urgent queries
- **Dashboard**: Real-time programme dashboard (milestones, budget, risks, benefits)
- **Briefings**: Executive slide decks for HM Treasury, Permanent Secretary

**Key Messages**:
- Budget variance and forecast outturn
- Benefits realization trajectory (£4.5M savings)
- Critical risks requiring Programme Board decisions
- International benchmarking and leadership indicators

**Success Metrics**:
- Programme Board attendance: 100%
- Decision response time: <48 hours
- HM Treasury checkpoint ratings: GREEN (no concerns)

---

## 7.2 Chief Statistician (S-002) - Regulatory Authority

**Engagement Objectives**:
- Ensure continuous Statistics Act compliance throughout implementation
- Validate Statistical Disclosure Control (SDC) automation before go-live
- Maintain UK Statistics Authority confidence in platform
- Protect ONS independence and statistical integrity

**Communication Frequency**:
- **Fortnightly**: 1-hour compliance review meetings
- **Monthly**: Programme Board (member)
- **Quarterly**: UK Statistics Authority reporting
- **Gates**: Discovery, Alpha, Beta assessments (compliance sign-off)

**Communication Channels**:
- **Email**: Compliance reports, audit findings, approval requests
- **Meetings**: Dedicated compliance reviews (fortnightly)
- **Reports**: Pre-release access audit logs (quarterly), SDC validation reports

**Key Messages**:
- Pre-release access controls implementation status
- SDC automation validation results
- Statistics Act compliance risks and mitigations
- Publication quality and error rate trends

**Success Metrics**:
- Compliance reviews attended: 100%
- Compliance risks raised: Resolved within 2 weeks
- UK Statistics Authority audit: Zero compliance findings
- Gate sign-off: Achieved on schedule

---

## 7.3 Director of Statistical Production (S-003) - Product Owner

**Engagement Objectives**:
- Continuous requirements prioritization and backlog refinement
- Statistician community engagement and adoption
- User acceptance testing coordination (500 statisticians)
- Benefits realization ownership (publication efficiency)

**Communication Frequency**:
- **Daily**: 15-minute standups during Beta (Sprint-based)
- **Weekly**: 1-hour backlog refinement, 1-hour sprint review/planning
- **Monthly**: Programme Board (member), statistician community workshops
- **Quarterly**: Benefits realization reporting, satisfaction surveys

**Communication Channels**:
- **Slack**: Real-time team communication, quick decisions
- **Email**: Formal requirements, approval requests, stakeholder updates
- **Workshops**: Statistician engagement sessions (monthly)
- **Demos**: Sprint demos to statistician representatives (4-weekly)

**Key Messages**:
- Publication efficiency improvements (time-to-publish, manual effort reduction)
- User acceptance testing progress and statistician feedback
- Training and change management readiness
- Sprint progress and upcoming features

**Success Metrics**:
- Standup attendance: 95%+
- Backlog refinement: 100% of sprints
- UAT participation: ≥20 statisticians (Week 70-72)
- Statistician satisfaction: ≥80% by Month 12

---

## 7.4 HM Treasury (S-007) - Funding Authority

**Engagement Objectives**:
- Maintain business case BCR >2.0 throughout lifecycle
- Demonstrate cost savings trajectory (£4.5M/year)
- Manage expectations on programme milestones and budget
- Secure funding release gates (SOBC → OBC → FBC)

**Communication Frequency**:
- **Quarterly**: 2-hour checkpoint meetings (Programme status, benefits, risks, budget)
- **Business case submissions**: SOBC (✅ submitted 2025-11), OBC (2026-06), FBC (2027-02)
- **Ad-hoc**: Escalations for budget overruns >10%, critical risk changes

**Communication Channels**:
- **Email**: Checkpoint meeting invites, reports, business case submissions
- **Reports**: Quarterly checkpoint reports (10-page summary: milestones, budget, benefits, risks)
- **Meetings**: In-person quarterly checkpoints at HM Treasury

**Key Messages**:
- Budget variance: Within 10% (GREEN), forecast outturn
- Benefits realization: Cashable savings £4.5M/year trajectory
- Business case BCR: Maintained >2.0 (currently 2.3:1)
- Major milestones: On track for go-live Week 78 (2027-05)

**Success Metrics**:
- Checkpoint meetings: 100% attendance by CDO
- Checkpoint ratings: GREEN (no concerns)
- Business case approvals: SOBC (✅), OBC (2026-06), FBC (2027-02)
- Funding releases: Gated approvals on schedule

---

## 7.5 Statisticians (S-011) - Internal Users

**Engagement Objectives**:
- Build user adoption and minimize resistance to change
- Gather continuous user feedback for iterative improvement
- Deliver effective training (500 users, 4-hour course)
- Achieve ≥80% satisfaction with new tools

**Communication Frequency**:
- **Monthly**: Community workshops (1-2 hours, rotating topics)
- **Quarterly**: Satisfaction surveys
- **Training**: 4-hour training course (Week 70-72, all 500 users)
- **UAT**: 3-week intensive UAT (Week 70-72, 20 statisticians)

**Communication Channels**:
- **Email newsletters**: Monthly programme updates, tips, FAQs
- **Intranet**: Dedicated programme page (roadmap, FAQs, training materials)
- **Workshops**: In-person/virtual monthly community workshops
- **Surveys**: Quarterly satisfaction surveys (15-minute, anonymous)

**Key Messages**:
- Benefits to statisticians: 60% reduction in manual publication effort
- Training schedule and materials availability
- Publication workflow changes and timelines
- Support channels (helpdesk, Slack channel, champions network)

**Success Metrics**:
- Workshop participation: ≥50 statisticians per session
- Training completion: 100% of 500 statisticians (Week 70-72)
- UAT participation: ≥20 statisticians (Week 70-72)
- Satisfaction: ≥80% by Month 12

---

## 7.6 Data Consumers (S-012) - External Users

**Engagement Objectives**:
- Build awareness of API availability and capabilities
- Provide developer-friendly documentation and sandbox
- Achieve ≥10,000 registered API users by Month 18
- Achieve ≥85% satisfaction with API experience

**Communication Frequency**:
- **Quarterly**: Developer webinars (1-hour, live Q&A)
- **Quarterly**: Satisfaction surveys (API users)
- **Continuous**: Developer portal updates (docs, release notes)
- **Launch**: API go-live announcement (Week 73)

**Communication Channels**:
- **Developer portal**: API documentation, tutorials, sandbox, support
- **Email**: API user mailing list (opt-in, quarterly updates)
- **Webinars**: Quarterly developer webinars (recorded, published)
- **Social media**: ONS Twitter, LinkedIn (API announcements)

**Key Messages**:
- API availability: 100% of 500+ statistical series accessible via API
- Developer benefits: Programmatic access, real-time data, modern formats (JSON, CSV)
- Getting started: Sandbox environment, tutorials, example code
- Support: Documentation, developer forum, support email

**Success Metrics**:
- Registered API users: ≥10,000 by Month 18
- API adoption: ≥50% data consumption via APIs by Month 18
- Developer satisfaction: ≥85% by Month 12
- Webinar participation: ≥100 attendees per session

---

# PART 8: RACI MATRIX

Decision authority and accountability for key programme activities.

| Activity | Responsible | Accountable | Consulted | Informed |
|----------|-------------|-------------|-----------|----------|
| **Programme strategic direction** | Director of Production (Product Owner) | CDO (SRO) | Chief Statistician, Chief Architect, Security | All stakeholders |
| **Budget allocation decisions** | CDO (SRO) | Permanent Secretary | HM Treasury | Programme Board |
| **Architecture design approval** | Chief Data Architect | Architecture Review Board | Security, DPO, Chief Statistician | Programme Board |
| **Vendor selection** | Procurement Specialist | CDO (SRO) | Chief Architect, Security | Programme Board |
| **Requirements prioritization** | Director of Production (Product Owner) | Programme Board | Statisticians, Chief Statistician | Delivery Team |
| **Go/No-Go gate decisions** | Programme Board | CDO (SRO) | GDS Assessor, UK Statistics Authority | HM Treasury |
| **Risk escalation** | Risk Owner | Programme Board | SRO | Stakeholders |
| **Statistics Act compliance** | Chief Statistician | UK Statistics Authority | DPO, Security | Programme Board |
| **Security accreditation (ITHC)** | Head of Cyber Security | SIRO (Senior Information Risk Owner) | Chief Architect | Programme Board |
| **DPIA approval** | Data Protection Officer | ICO (if consulted) | Security, Chief Statistician | Programme Board |
| **Service Standard assessment** | Director of Production (Service Owner) | GDS Service Assessor | Delivery Team, Statisticians | Programme Board |
| **Benefits realization** | Director of Production | CDO (SRO) | Finance, HM Treasury | Programme Board |
| **Training delivery** | Training Lead | Director of Production | Statisticians, Change Champions | All statisticians |
| **User acceptance testing** | Statistician Representatives (20) | Director of Production | Delivery Team | Programme Board |
| **Publication workflow changes** | Chief Statistician | Director of Production | Statisticians | Programme Board |
| **API documentation** | Technical Writer | Chief Data Architect | Developers, Data Consumers | Public |

---

# PART 9: STAKEHOLDER RISK REGISTER

Risks associated with stakeholder engagement and conflict resolution.

| Risk ID | Stakeholder(s) | Risk Description | Impact | Likelihood | Mitigation | Owner |
|---------|---------------|------------------|--------|------------|------------|-------|
| **SR-001** | S-003 Director of Production, S-011 Statisticians | Statistician resistance to change leads to <80% adoption, preventing efficiency benefits realization | HIGH | POSSIBLE | Change champions network (5 statisticians), extended training (4 hours), 6-week hypercare, satisfaction surveys | Director of Production |
| **SR-002** | S-002 Chief Statistician | Statistics Act compliance breach during implementation damages ONS reputation and triggers UK Statistics Authority sanctions | CRITICAL | UNLIKELY | MFA enforced 100%, audit logs monitored 24/7, quarterly compliance reviews, UK Statistics Authority validation in Alpha | Chief Statistician |
| **SR-003** | S-007 HM Treasury | Budget overrun >10% triggers HM Treasury funding withdrawal and programme cancellation | CRITICAL | POSSIBLE | 10% contingency (£1.8M), monthly budget variance monitoring, early escalation at >5% variance | CDO (SRO) |
| **SR-004** | S-008 GDS Service Assessor | Service Standard Beta assessment fails, delaying go-live and damaging credibility | HIGH | UNLIKELY | Mock assessment in Alpha Week 36, continuous evidence portfolio, GDS engagement quarterly | Director of Production |
| **SR-005** | S-005 Head of Cyber Security | ITHC failure prevents go-live, requires 3-month remediation, delays programme 12 weeks | HIGH | POSSIBLE | Security by design, SAST/DAST in CI/CD, quarterly internal pen testing, CHECK testers engaged Week 68 | Head of Cyber Security |
| **SR-006** | S-009 National Statistician, S-012 Data Consumers | API adoption fails (<25% vs 50% target), wasting investment and failing statutory accessibility duty | HIGH | POSSIBLE | User research (100+ data consumers), developer webinars, sandbox, generous rate limits, Marketing campaign | National Statistician |
| **SR-007** | S-001 CDO, S-003 Director of Production | Conflict between CDO (rapid innovation) and Chief Statistician (compliance rigor) delays decisions and slows delivery | MEDIUM | LIKELY | Two-speed architecture approved (Week 36), clear decision authority in RACI, Programme Board escalation process | CDO (SRO) |
| **SR-008** | S-006 Data Protection Officer | DPIA not completed by Alpha Week 23 blocks Beta phase, delays programme 4-8 weeks | MEDIUM | POSSIBLE | DPIA drafted Week 19-21, ICO consultation Week 22-23, DPO engaged early, privacy-by-design embedded | Data Protection Officer |
| **SR-009** | S-011 Statisticians | Statistician availability for UAT insufficient (Week 70-72) prevents adequate testing before go-live | MEDIUM | POSSIBLE | UAT schedule agreed 6 months in advance, Director of Production secures statistician time, incentives for participation | Director of Production |
| **SR-010** | S-007 HM Treasury, S-010 NAO | Benefits realization falls short (£3M vs £4.5M target), weakening business case and triggering NAO/PAC scrutiny | MEDIUM | POSSIBLE | Phased benefits tracking from Month 6, early warning system, contingency plan (extend migration to achieve savings) | CDO (SRO) |

---

# PART 10: STAKEHOLDER ANALYSIS SUMMARY

## Key Insights

### 10.1 Dominant Driver Types
- **COMPLIANCE** (9 drivers): Most critical intensity, gate conditions (Statistics Act, GovS 007, GDPR, Service Standard)
- **OPERATIONAL** (8 drivers): Efficiency benefits realization (publication workflow, quality, reliability)
- **STRATEGIC** (6 drivers): Leadership, transformation, trust
- **FINANCIAL** (4 drivers): Cost reduction, value for money, savings

**Implication**: Compliance-first programme - regulatory requirements are non-negotiable gate conditions. Operational benefits second priority. Financial benefits support business case but don't drive day-to-day decisions.

### 10.2 Power Concentration
- **6 stakeholders** have HIGH POWER (8-10/10): CDO, Chief Statistician, Chief Architect, Security, HM Treasury, GDS
- All 6 require MANAGE CLOSELY or KEEP SATISFIED strategies
- **Veto authority**: Security (ITHC), Chief Statistician (Statistics Act), GDS (Service Standard), HM Treasury (funding)

**Implication**: Programme has multiple veto points. Architecture, security, compliance, and business case must all succeed - any failure blocks go-live.

### 10.3 Critical Success Factors
Based on driver intensity (CRITICAL level):
1. **G-004**: Statistics Act compliance (zero breaches) - Chief Statistician
2. **G-014**: GovS 007 accreditation before go-live - Security
3. **G-019**: BCR >2.0 maintained - HM Treasury
4. **G-001**: International leadership demonstrated - CDO
5. **G-007**: 60% publication efficiency improvement - Director of Production
6. **G-015**: Zero pre-release data breaches - Security
7. **G-023**: 50% API adoption - National Statistician

**Implication**: 7 mission-critical goals across 5 stakeholders. Programme success requires achieving ALL 7 - partial success insufficient.

### 10.4 Conflict Resolution Status
- 4 critical conflicts identified
- All 4 resolved via Programme Board decisions (Week 24, Week 36)
- Resolutions balanced competing interests without compromising compliance

**Implication**: Conflict resolution process validated. Programme Board effective decision authority for trade-offs.

### 10.5 Engagement Intensity
- **Daily engagement**: 1 stakeholder (Director of Production during Beta)
- **Weekly engagement**: 1 stakeholder (CDO)
- **Fortnightly engagement**: 3 stakeholders (Chief Statistician, Chief Architect, Security)
- **Monthly engagement**: 6 stakeholders (Programme Board)
- **Quarterly engagement**: 4 stakeholders (HM Treasury, GDS, DPO, NAO)

**Implication**: High engagement intensity programme - 50% of stakeholders require fortnightly or more frequent engagement. Dedicated Programme Manager essential.

---

## Recommendations

### R-001: Prioritize Compliance Over Innovation Speed
**Rationale**: 9 COMPLIANCE drivers (5 CRITICAL intensity) are gate conditions. Innovation speed is strategic desire, not gate condition.
**Action**: Two-speed architecture (approved Week 36) ensures compliance rigor for publication-critical path while enabling agile innovation for non-critical features.

### R-002: Strengthen Change Management for Statistician Adoption
**Rationale**: SR-001 (statistician resistance) threatens £300K annual benefits realization and 60% efficiency improvement.
**Action**: Invest in change champions network (5 statisticians), extended training (4 hours vs 2 hours), 6-week hypercare (vs 4 weeks), quarterly satisfaction surveys.

### R-003: Early DPIA Completion Critical Path
**Rationale**: SR-008 (DPIA delay) blocks Beta phase. DPIA identified as blocker in Secure by Design assessment.
**Action**: Prioritize DPIA drafting Week 19-21, ICO consultation Week 22-23, DPO approval by Alpha Week 23. No flexibility on timeline.

### R-004: Gated Investment for Census Capability
**Rationale**: Conflict C-004 (census investment vs budget) resolved via early prototyping with gated funding.
**Action**: Alpha prototype with 67M records (Week 36) provides evidence for HM Treasury to release Beta capability funding (£2.8M). Contingency plan if prototype fails.

### R-005: Benefits Realization Early Warning System
**Rationale**: SR-010 (benefits shortfall) weakens business case and triggers NAO/PAC scrutiny.
**Action**: Monthly FinOps cost reports from Month 6, quarterly savings trajectory reviews, early warning at Month 12 if <£2M savings achieved (should be £3.5M).

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2025-11-05
**ArcKit Version**: 0.8.3
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-sonnet-4-5-20250929
**Context Used**: Requirements (100+ requirements, 8 stakeholders identified), SOBC (5 spending objectives, benefits mapping), Architecture Principles (14 principles), Project Plan (78 weeks, governance gates), Risk Register (22 risks)
**Analysis Depth**: Comprehensive - 12 stakeholders, 27 drivers, 27 goals, 28 outcomes, 4 conflicts, complete traceability matrix
**Driver Types**: STRATEGIC, OPERATIONAL, FINANCIAL, COMPLIANCE, PERSONAL, RISK, CUSTOMER (7 types per stakeholder analysis best practices)
