# Stakeholder Drivers & Goals Analysis: ONS Data Platform Modernisation

> **Template Status**: Live | **Version**: 0.11.2 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.1 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2025-11-05 |
| **Last Modified** | 2026-01-26 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-04-26 |
| **Owner** | Chief Data Officer, ONS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, Enterprise Architecture Review Board, UK Statistics Authority |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial stakeholder analysis from `/arckit.stakeholders` command | PENDING | PENDING |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to align with template v0.11.2: enhanced document control, validation & sign-off, change impact assessment, appendices | PENDING | PENDING |

---

## Executive Summary

### Purpose
This document provides comprehensive stakeholder analysis for the ONS Data Platform Modernisation project, mapping stakeholder drivers to measurable goals and outcomes. It establishes the foundation for requirements prioritization, risk management, and benefits realization.

### Key Findings
The programme has **12 stakeholders with 28 distinct drivers** spanning compliance, operational efficiency, and strategic transformation. Four critical conflicts have been identified and resolved through Programme Board governance. The dominant driver type is COMPLIANCE (9 drivers), reflecting the regulatory intensity of UK Government statistical operations. All 6 high-power stakeholders have veto authority over go-live decisions, requiring careful engagement management.

### Critical Success Factors
- **Statistics Act 2007 compliance**: Zero breaches during implementation (Chief Statistician veto)
- **GovS 007 OFFICIAL accreditation**: Issued before go-live (Security veto)
- **BCR >2.0 maintained**: Throughout business case lifecycle (HM Treasury veto)
- **60% publication efficiency improvement**: Core benefits realization metric
- **50% API adoption by Month 18**: Statutory accessibility duty fulfilled

### Stakeholder Alignment Score
**Overall Alignment**: MEDIUM-HIGH

Four critical conflicts were identified between stakeholders (cost efficiency vs security, innovation speed vs compliance, open access vs security controls, census investment vs budget constraints). All four have been resolved through Programme Board decisions using risk-based segmentation, two-speed architecture, tiered access models, and gated investment approaches. Ongoing monitoring required for benefits realization trajectory.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-001: Chief Data Officer | Executive Sponsor / SRO | HIGH | HIGH | Active involvement, decision authority, weekly 1:1s |
| S-002: Chief Statistician | Regulatory Authority / Statistics Act | HIGH | HIGH | Fortnightly compliance reviews, gate sign-offs |
| S-003: Director of Statistical Production | Product Owner / Business Lead | HIGH | HIGH | Daily standups (Beta), backlog management |
| S-004: Chief Data Architect | Technical Authority / Architecture | HIGH | HIGH | Architecture Review Board, design approvals |
| S-005: Head of Cyber Security | Security Authority / GovS 007 | HIGH | HIGH | Security Review Board, ITHC gatekeeper |
| S-006: Data Protection Officer | Privacy Authority / GDPR | HIGH | MEDIUM | Monthly compliance updates, DPIA approval |
| S-011: Statisticians (500 users) | Internal Users / Publication Operators | LOW | HIGH | Monthly workshops, UAT sessions, training |

### External Stakeholders

| Stakeholder | Organization | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-007: HM Treasury | Infrastructure and Projects Authority | Funding Authority | HIGH | MEDIUM |
| S-008: GDS Service Assessor | Cabinet Office - GDS | Service Standard Compliance | HIGH | MEDIUM |
| S-009: National Statistician | UK Statistics Authority | Regulatory Compliance | HIGH | HIGH |
| S-010: National Audit Office | NAO / Public Accounts Committee | Value for Money Audit | MEDIUM | LOW |
| S-012: Data Consumers (10,000 target) | Government, researchers, businesses, media | API Users / Beneficiaries | LOW | HIGH |

### Stakeholder Power-Interest Grid

```
HIGH POWER
    │
    │  [Manage Closely]           │  [Keep Satisfied]
    │  - S-001: CDO (SRO)         │  - S-006: DPO
    │  - S-002: Chief Statistician│  - S-007: HM Treasury
    │  - S-003: Dir. of Production│  - S-008: GDS Assessor
    │  - S-004: Chief Architect   │
    │  - S-005: Head of Security  │
    │  - S-009: National Stat.    │
────┼─────────────────────────────┼─────────────────────
    │  [Keep Informed]            │  [Monitor]
    │  - S-011: Statisticians     │  - S-010: NAO
    │  - S-012: Data Consumers    │
    │                             │
    │                             │
LOW POWER                                       HIGH INTEREST ──────▶
```

---

## Stakeholder Drivers Analysis

### SD-001: Chief Data Officer - Digital Transformation Leadership

**Stakeholder**: S-001 Chief Data Officer (CDO)

**Driver Category**: STRATEGIC

**Driver Statement**: Lead ONS digital transformation to maintain international leadership in official statistics, demonstrating world-class infrastructure to international peers (Eurostat, Statistics Canada, ABS Australia).

**Context & Background**:
ONS reputation as a world-class statistical institute depends on modern infrastructure. International benchmarking shows ONS infrastructure 5-8 years behind Eurostat. The CDO's career progression depends on successful delivery of this transformation programme.

**Driver Intensity**: CRITICAL

**Enablers**:
- Cloud-native architecture enabling rapid innovation
- Modern APIs matching international best practice
- Skilled team with cloud expertise

**Blockers**:
- Compliance requirements slowing innovation pace
- Budget constraints limiting capability investment
- Legacy system dependencies

**Related Stakeholders**:
- S-004 Chief Data Architect (technical enablement)
- S-007 HM Treasury (budget approval)
- S-009 National Statistician (international reputation)

---

### SD-002: Chief Data Officer - Cost Reduction

**Stakeholder**: S-001 Chief Data Officer (CDO)

**Driver Category**: FINANCIAL

**Driver Statement**: Demonstrate value for money and achieve 40% infrastructure cost reduction (£4.5M annual savings) to meet HM Treasury efficiency priorities and Spending Review commitments.

**Context & Background**:
Current annual infrastructure costs: £11.2M. Cloud benchmark target: £6.7M (40% reduction). Spending Review 2021 efficiency priorities require government departments demonstrate cost savings from digital investments.

**Driver Intensity**: HIGH

**Enablers**:
- Cloud-native managed services reducing operational burden
- Auto-scaling reducing over-provisioning
- FinOps practices optimizing spend

**Blockers**:
- Security requirements increasing costs (multi-region, SIEM)
- Census capability investment
- Dual-running during migration

**Related Stakeholders**:
- S-007 HM Treasury (funding authority, BCR tracking)
- S-005 Head of Cyber Security (security costs)
- S-010 NAO (value for money audit)

---

### SD-003: Chief Data Officer - Census 2031 Risk Mitigation

**Stakeholder**: S-001 Chief Data Officer (CDO)

**Driver Category**: RISK

**Driver Statement**: Avoid Census 2031 processing failure that would damage ONS credibility. 2021 Census took 6 months to process vs <24 hour target for 2031.

**Context & Background**:
2021 Census post-implementation review identified infrastructure inadequacy as root cause of processing delays. Census 2031 rehearsal in 2029 requires validated 67M record processing capability.

**Driver Intensity**: HIGH

**Enablers**:
- Distributed processing frameworks (Spark, Dask)
- Cloud-scale compute elasticity
- Data lake architecture

**Blockers**:
- Budget constraints limiting compute investment
- Architecture complexity
- Skills gaps in distributed processing

**Related Stakeholders**:
- S-007 HM Treasury (census investment funding)
- S-004 Chief Data Architect (architecture capability)

---

### SD-004: Chief Statistician - Statistics Act Compliance

**Stakeholder**: S-002 Chief Statistician

**Driver Category**: COMPLIANCE

**Driver Statement**: Maintain Statistics Act 2007 compliance for pre-release access and publication standards. Non-compliance risks UK Statistics Authority sanctions and loss of National Statistics designation.

**Context & Background**:
Legal obligation under Statistics Act Section 11. Recent NAO report highlighted pre-release access audit gaps. Pre-release access limited to 24 hours maximum with MFA enforcement and complete audit trail.

**Driver Intensity**: CRITICAL

**Enablers**:
- Automated pre-release access controls
- MFA enforcement
- Comprehensive audit logging

**Blockers**:
- Manual processes creating compliance gaps
- Legacy system limitations
- User workarounds bypassing controls

**Related Stakeholders**:
- S-005 Head of Cyber Security (access controls)
- S-009 National Statistician (regulatory oversight)
- S-006 DPO (data protection alignment)

---

### SD-005: Chief Statistician - Statistical Disclosure Control

**Stakeholder**: S-002 Chief Statistician

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure Statistical Disclosure Control (SDC) prevents identification of individuals/businesses. GDPR Article 5 and Statistics Act Section 39 prohibit disclosure.

**Context & Background**:
ONS Five Safes framework mandates SDC. ICO guidance on statistical disclosure requires automated controls. Re-identification risk must be assessed as ACCEPTABLE.

**Driver Intensity**: HIGH

**Enablers**:
- Automated SDC rule engine
- Re-identification testing
- Privacy Impact Assessment validation

**Blockers**:
- Complex statistical methodologies
- SDC vs data utility trade-offs
- Cell count thresholds for small geographies

**Related Stakeholders**:
- S-006 DPO (GDPR compliance)
- S-003 Director of Statistical Production (publication workflow)

---

### SD-006: Chief Statistician - Independence from Political Influence

**Stakeholder**: S-002 Chief Statistician

**Driver Category**: STRATEGIC

**Driver Statement**: Maintain ONS independence from political influence through robust infrastructure. Statistics Act Section 6 requires independence; infrastructure failures during election periods create perception of political interference.

**Context & Background**:
2019 election-period website outage generated Parliamentary questions. Zero infrastructure-related publication delays required during 2025 and 2029 elections.

**Driver Intensity**: MEDIUM

**Enablers**:
- 99.95% uptime target
- Multi-region resilience
- Election-period resilience testing

**Blockers**:
- Cost constraints on redundancy
- Single points of failure
- Dependency on cloud provider

**Related Stakeholders**:
- S-004 Chief Data Architect (resilience architecture)
- S-009 National Statistician (independence oversight)

---

### SD-007: Director of Statistical Production - Manual Effort Reduction

**Stakeholder**: S-003 Director of Statistical Production

**Driver Category**: OPERATIONAL

**Driver Statement**: Reduce statistician manual publication effort by 60% to free capacity for analysis. Statisticians spend 35% time on publication mechanics vs 10% target (600 days/year wasted on manual tasks, £300K opportunity cost).

**Context & Background**:
Time-motion studies show 35% of statistician time on file formatting, upload, validation. Target: ≤14% time on publication mechanics, releasing 600 days/year for analytical work.

**Driver Intensity**: CRITICAL

**Enablers**:
- Automated publication workflow
- Self-service metadata management
- Template-driven outputs

**Blockers**:
- Statistician resistance to change
- Training gaps
- Complex edge cases requiring manual intervention

**Related Stakeholders**:
- S-011 Statisticians (primary beneficiaries)
- S-001 CDO (benefits realization accountability)

---

### SD-008: Director of Statistical Production - Time-to-Publish Reduction

**Stakeholder**: S-003 Director of Statistical Production

**Driver Category**: OPERATIONAL

**Driver Statement**: Reduce publication time-to-publish from 4 days to 2 days for major indicators (GDP, CPI, Labour Market). Delays reduce policy impact and media coverage.

**Context & Background**:
Publication tracking shows 4-day average, target 2 days. Market-sensitive releases require timeliness. 92% schedule adherence vs 98% target.

**Driver Intensity**: HIGH

**Enablers**:
- Automated validation and quality checks
- Parallel processing pipelines
- Pre-configured publication templates

**Blockers**:
- Data quality issues upstream
- Compliance review bottlenecks
- Statistician availability

**Related Stakeholders**:
- S-002 Chief Statistician (compliance review)
- S-011 Statisticians (workflow operators)

---

### SD-009: Director of Statistical Production - Publication Error Reduction

**Stakeholder**: S-003 Director of Statistical Production

**Driver Category**: OPERATIONAL

**Driver Statement**: Reduce publication error rate from 2.3% to <0.1% through automation. 87 corrections in last 12 months damage trust and require statistician rework.

**Context & Background**:
Manual processes cause 2.3% publication errors. Automated quality validation can catch 95% of errors before publication. Target: <4 errors/year for 500 series.

**Driver Intensity**: HIGH

**Enablers**:
- Automated quality validation rules
- Pre-publication review workflows
- Version control for statistical outputs

**Blockers**:
- Complex validation rules
- Edge cases in methodology code
- Time pressure for releases

**Related Stakeholders**:
- S-011 Statisticians (quality responsibility)
- S-002 Chief Statistician (publication standards)

---

### SD-010: Director of Statistical Production - Career Progression

**Stakeholder**: S-003 Director of Statistical Production

**Driver Category**: PERSONAL

**Driver Statement**: Deliver successful high-profile programme for career progression to Deputy National Statistician role. Product Owner role on £18M transformation programme demonstrates leadership capability.

**Context & Background**:
Internal career frameworks show programme delivery experience required for Deputy NS role. Personal reputation tied to programme success.

**Driver Intensity**: MEDIUM

**Enablers**:
- Clear programme governance
- Strong delivery team
- Executive sponsor support

**Blockers**:
- Scope creep
- External stakeholder conflicts
- Resource constraints

**Related Stakeholders**:
- S-001 CDO (programme sponsor)
- S-008 GDS Service Assessor (external validation)

---

### SD-011: Chief Data Architect - Technology Code of Practice Compliance

**Stakeholder**: S-004 Chief Data Architect

**Driver Category**: STRATEGIC

**Driver Statement**: Establish modern cloud-native architecture aligned with UK Government Technology Code of Practice (13 criteria mandatory for government projects).

**Context & Background**:
Current platform: 4/13 TCoP points compliant. Target: 13/13 by Beta Assessment. Cloud-first policy compliance (TCoP Point 5) mandatory.

**Driver Intensity**: HIGH

**Enablers**:
- Cloud provider capabilities
- Open standards adoption (SDMX, OpenAPI, DCAT)
- API-first architecture patterns

**Blockers**:
- Legacy system integration
- Skills gaps in cloud-native design
- Vendor lock-in concerns

**Related Stakeholders**:
- S-008 GDS Service Assessor (TCoP validation)
- S-001 CDO (strategic alignment)

---

### SD-012: Chief Data Architect - Publication API Availability

**Stakeholder**: S-004 Chief Data Architect

**Driver Category**: OPERATIONAL

**Driver Statement**: Achieve 99.95% API availability for publication services (max 21.9 min downtime/month). Current availability 97.8% (9.6 hours downtime/month) unacceptable for market-moving releases.

**Context & Background**:
Publication outages damage ONS reputation. Major releases (GDP, CPI, Labour Market) are market-moving events requiring extreme reliability.

**Driver Intensity**: HIGH

**Enablers**:
- Multi-availability zone deployment
- Auto-scaling and load balancing
- Comprehensive observability

**Blockers**:
- Cloud provider outages
- Architecture complexity
- Cost of redundancy

**Related Stakeholders**:
- S-005 Head of Cyber Security (resilience requirements)
- S-003 Director of Statistical Production (SLA expectations)

---

### SD-013: Chief Data Architect - Vendor Lock-in Avoidance

**Stakeholder**: S-004 Chief Data Architect

**Driver Category**: RISK

**Driver Statement**: Avoid vendor lock-in through open standards and portable architecture. 30-year platform lifespan requires flexibility to change cloud providers or bring services in-house.

**Context & Background**:
Architecture Principle 10 (Interoperability and Open Standards) mandates portability. Target: cloud provider migration within 6 months if required.

**Driver Intensity**: HIGH

**Enablers**:
- Infrastructure as Code (Terraform)
- Containerization (Kubernetes)
- Open data formats (Parquet, CSV, JSON)

**Blockers**:
- Cloud-specific managed services
- Proprietary features
- Data egress costs

**Related Stakeholders**:
- S-001 CDO (strategic flexibility)
- S-007 HM Treasury (long-term value)

---

### SD-014: Head of Cyber Security - GovS 007 Accreditation

**Stakeholder**: S-005 Head of Cyber Security

**Driver Category**: COMPLIANCE

**Driver Statement**: Achieve GovS 007 OFFICIAL accreditation before go-live. No accreditation = no go-live. Current ITHC lapsed (2022), requires re-accreditation.

**Context & Background**:
Government Functional Standard GovS 007: Security mandatory for OFFICIAL classification systems. ITHC by CHECK-certified testers required Week 68-72.

**Driver Intensity**: CRITICAL

**Enablers**:
- Security by design from Discovery
- SAST/DAST in CI/CD pipeline
- Quarterly internal pen testing

**Blockers**:
- Vulnerability remediation delays
- Third-party dependency risks
- Complex attack surface

**Related Stakeholders**:
- S-004 Chief Data Architect (security architecture)
- S-001 CDO (go-live authority)

---

### SD-015: Head of Cyber Security - Pre-Release Data Breach Prevention

**Stakeholder**: S-005 Head of Cyber Security

**Driver Category**: RISK

**Driver Statement**: Prevent pre-release statistics data breach that would constitute market abuse. Breach could cause financial market disruption and criminal liability under Financial Services and Markets Act 2000.

**Context & Background**:
Statistics Act Section 11 restricts pre-release access. GDP/CPI data is market-sensitive. Zero tolerance for security incidents.

**Driver Intensity**: CRITICAL

**Enablers**:
- Multi-factor authentication (100% enforcement)
- 24/7 SIEM monitoring
- Quarterly penetration testing

**Blockers**:
- Insider threat
- Social engineering
- Third-party access

**Related Stakeholders**:
- S-002 Chief Statistician (access control policy)
- S-006 DPO (data protection)

---

### SD-016: Head of Cyber Security - Zero Trust Architecture

**Stakeholder**: S-005 Head of Cyber Security

**Driver Category**: COMPLIANCE

**Driver Statement**: Implement Zero Trust security architecture per NCSC guidance. NCSC Cloud Security Principles mandate Zero Trust for cloud services handling OFFICIAL data.

**Context & Background**:
Current perimeter security model (legacy) inadequate. Target: NCSC CAF 12/14 principles achieved (up from 10/14 in Secure by Design assessment).

**Driver Intensity**: HIGH

**Enablers**:
- Identity-based access control
- Network micro-segmentation
- Encrypted service-to-service communication

**Blockers**:
- Legacy system integration
- User experience friction
- Operational complexity

**Related Stakeholders**:
- S-004 Chief Data Architect (architecture implementation)
- S-006 DPO (privacy alignment)

---

### SD-017: Data Protection Officer - DPIA Completion

**Stakeholder**: S-006 Data Protection Officer

**Driver Category**: COMPLIANCE

**Driver Statement**: Complete Data Protection Impact Assessment (DPIA) for all data processing before Beta phase. UK GDPR Article 35 mandates DPIA for high-risk processing.

**Context & Background**:
DPIA identified as blocker in Secure by Design assessment (R-019 in Risk Register). ICO guidance requires DPIA before systematic large-scale processing.

**Driver Intensity**: HIGH

**Enablers**:
- Privacy-by-design embedded in architecture
- ICO DPIA template and guidance
- Early DPO engagement

**Blockers**:
- Processing scope complexity
- Data flow documentation gaps
- ICO consultation delays

**Related Stakeholders**:
- S-005 Head of Cyber Security (security controls)
- S-002 Chief Statistician (SDC alignment)

---

### SD-018: Data Protection Officer - Data Minimization and Retention

**Stakeholder**: S-006 Data Protection Officer

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure data minimization and retention policies comply with GDPR Article 5(1)(c) and (e). Excessive retention increases risk and contradicts storage limitation principle.

**Context & Background**:
ONS holds sensitive personal/commercial data under legal privilege. Manual retention management has inconsistent enforcement. Target: automated retention for 100% of datasets.

**Driver Intensity**: MEDIUM

**Enablers**:
- Data catalog with retention metadata
- Automated deletion workflows
- Audit trail for deletions

**Blockers**:
- Legal hold complexity
- Statistical value of historical data
- Archive vs deletion trade-offs

**Related Stakeholders**:
- S-002 Chief Statistician (statistical data value)
- S-004 Chief Data Architect (data governance)

---

### SD-019: HM Treasury - Value for Money

**Stakeholder**: S-007 HM Treasury

**Driver Category**: FINANCIAL

**Driver Statement**: Demonstrate value for money with Benefit-Cost Ratio (BCR) >2.0 per Green Book guidance. £18M investment requires strong economic case.

**Context & Background**:
HM Treasury Green Book Section 3.2 requires BCR >2.0 for discretionary capital investment. SOBC BCR 2.3:1 meets threshold. Must maintain through OBC, FBC, and PIR.

**Driver Intensity**: CRITICAL

**Enablers**:
- Clear benefits realization plan
- Robust cost estimation
- Quarterly benefits tracking

**Blockers**:
- Cost overruns
- Benefits shortfall
- Optimism bias

**Related Stakeholders**:
- S-001 CDO (benefits accountability)
- S-010 NAO (audit scrutiny)

---

### SD-020: HM Treasury - Efficiency Savings

**Stakeholder**: S-007 HM Treasury

**Driver Category**: FINANCIAL

**Driver Statement**: Achieve £4.5M annual efficiency savings to return to Exchequer per Spending Review 2021 efficiency priorities.

**Context & Background**:
SOBC commits to £4.5M/year savings. Infrastructure cost reduction from £11.2M to £6.7M (40% reduction). Accountability to Public Accounts Committee.

**Driver Intensity**: HIGH

**Enablers**:
- Cloud cost optimization (FinOps)
- Legacy decommissioning
- Managed services reducing operations

**Blockers**:
- Dual-running costs during migration
- Security cost increases
- Census capability investment

**Related Stakeholders**:
- S-001 CDO (savings delivery)
- S-010 NAO (value for money audit)

---

### SD-021: GDS Service Assessor - Service Standard Compliance

**Stakeholder**: S-008 GDS Service Assessor

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure compliance with all 14 GDS Service Standard criteria. Non-compliance blocks go-live and future funding.

**Context & Background**:
UK Government policy mandates Service Standard compliance for all public-facing digital services. Assessment at Alpha, Beta, Live gates.

**Driver Intensity**: HIGH

**Enablers**:
- Continuous evidence portfolio
- User research throughout
- Mock assessments

**Blockers**:
- Evidence gaps
- User research capacity
- Assessment panel availability

**Related Stakeholders**:
- S-003 Director of Statistical Production (Service Owner)
- S-011 Statisticians (user research participants)
- S-012 Data Consumers (user research participants)

---

### SD-022: GDS Service Assessor - User-Centred Design Validation

**Stakeholder**: S-008 GDS Service Assessor

**Driver Category**: COMPLIANCE

**Driver Statement**: Validate user-centred design through research with statisticians and data consumers. Service Standard Point 1 (Understand users) and Point 2 (Solve a whole problem) require user research evidence.

**Context & Background**:
Target: ≥50 statisticians and ≥100 data consumers in user research by Beta Assessment. Personas and user journey maps required.

**Driver Intensity**: MEDIUM

**Enablers**:
- Dedicated user researcher
- Statistician engagement workshops
- Developer portal for data consumers

**Blockers**:
- User availability
- Representative sample challenges
- Research capacity

**Related Stakeholders**:
- S-011 Statisticians (research participants)
- S-012 Data Consumers (research participants)

---

### SD-023: National Statistician - Statistics Accessibility

**Stakeholder**: S-009 National Statistician

**Driver Category**: CUSTOMER

**Driver Statement**: Maximize accessibility of official statistics per Statistics Act 2007 Section 7 statutory duty. API-first approach delivers statutory obligation.

**Context & Background**:
ONS statutory duty to make statistics available and accessible to all users. Target: 50% of data consumption via APIs by Month 18 post-go-live.

**Driver Intensity**: CRITICAL

**Enablers**:
- Modern REST APIs
- Open data formats
- Developer documentation and sandbox

**Blockers**:
- Security controls limiting access
- User adoption
- API discovery

**Related Stakeholders**:
- S-012 Data Consumers (beneficiaries)
- S-005 Head of Cyber Security (access controls)

---

### SD-024: National Statistician - Public Trust

**Stakeholder**: S-009 National Statistician

**Driver Category**: STRATEGIC

**Driver Statement**: Maintain public trust in official statistics through quality, independence, transparency. ONS public trust rating 68% (2023 survey) vs 75% target.

**Context & Background**:
Code of Practice Principle Q1 (Trustworthiness). Infrastructure failures damage trust. Target: ≥75% public trust rating by 2029 survey.

**Driver Intensity**: HIGH

**Enablers**:
- High availability (99.95%)
- Zero Statistics Act breaches
- Transparent operations

**Blockers**:
- Infrastructure failures
- Data quality issues
- Security incidents

**Related Stakeholders**:
- S-002 Chief Statistician (quality standards)
- S-001 CDO (infrastructure delivery)

---

### SD-025: National Audit Office - Cost Overrun Prevention

**Stakeholder**: S-010 National Audit Office

**Driver Category**: FINANCIAL

**Driver Statement**: Validate value for money and prevent cost overruns for Major Projects Portfolio reporting. £18M+ programmes require NAO scrutiny.

**Context & Background**:
Infrastructure and Projects Authority classifies £18M+ programmes as Major Projects. Potential Public Accounts Committee hearings if issues emerge. Post-implementation review expected.

**Driver Intensity**: MEDIUM

**Enablers**:
- Robust budget management
- Contingency management
- Transparent reporting

**Blockers**:
- Scope creep
- Vendor cost escalation
- Unforeseen technical challenges

**Related Stakeholders**:
- S-007 HM Treasury (funding oversight)
- S-001 CDO (programme accountability)

---

### SD-026: Statisticians - Tool Usability

**Stakeholder**: S-011 Statisticians (Internal Users)

**Driver Category**: OPERATIONAL

**Driver Statement**: Reduce time spent on publication mechanics to focus on statistical analysis. Statisticians want to do statistics, not IT. 35% time on mechanics vs 10% desired.

**Context & Background**:
User research workshops (Week 3-5) confirmed frustration with manual processes. 60% satisfaction with current tools, target ≥80%.

**Driver Intensity**: HIGH

**Enablers**:
- Intuitive user interface
- Automated workflows
- Comprehensive training

**Blockers**:
- Change resistance
- Learning curve
- Edge cases requiring workarounds

**Related Stakeholders**:
- S-003 Director of Statistical Production (benefits ownership)

---

### SD-027: Statisticians - Tool Reliability

**Stakeholder**: S-011 Statisticians (Internal Users)

**Driver Category**: CUSTOMER

**Driver Statement**: Intuitive, reliable tools that don't disrupt publication deadlines. Publication schedules are rigid (9:30 AM releases). Tool failures cause stress and deadline misses.

**Context & Background**:
Publication schedule adherence 92% vs 98% target. Tool reliability complaints in user research. Zero missed deadlines due to platform failures required.

**Driver Intensity**: MEDIUM

**Enablers**:
- High availability during working hours
- Fast incident response
- Clear escalation paths

**Blockers**:
- Platform outages
- Performance issues
- Complex error handling

**Related Stakeholders**:
- S-004 Chief Data Architect (platform reliability)

---

### SD-028: Data Consumers - API Access

**Stakeholder**: S-012 Data Consumers (External Users)

**Driver Category**: CUSTOMER

**Driver Statement**: Timely, reliable, programmatic access to ONS statistics via modern APIs. User research shows 78% want API access, 65% satisfaction with current file-based distribution.

**Context & Background**:
Researchers need machine-readable data. Businesses need real-time economic indicators. Government needs automated dashboards. Target: ≥85% satisfaction by Month 12.

**Driver Intensity**: HIGH

**Enablers**:
- Well-documented APIs (OpenAPI 3.0)
- Sandbox environment
- Developer support

**Blockers**:
- Rate limiting
- Authentication complexity
- API discovery

**Related Stakeholders**:
- S-009 National Statistician (accessibility mandate)
- S-004 Chief Data Architect (API design)

---

## Driver-to-Goal Mapping

### Goal G-001: Achieve International Statistical Leadership Recognition

**Derived From Drivers**: SD-001

**Goal Owner**: S-001 Chief Data Officer

**Goal Statement**: ONS ranked Top 3 in International Statistical Institute (ISI) digital capability benchmark by 2028

**Why This Matters**: Fulfills CDO's strategic transformation driver by demonstrating ONS world-class capability to international peers, protecting institutional reputation and enabling talent attraction.

**Success Metrics**:
- **Primary Metric**: ISI Digital Capability Benchmark ranking (Target: Top 3)
- **Secondary Metrics**:
  - API capabilities match Eurostat, Statistics Canada, ABS Australia
  - International conference keynotes (4+ per year)
  - Academic citations of ONS digital infrastructure

**Baseline**: Current ISI ranking: #7 (2024)

**Target**: Top 3 ranking by 2030

**Measurement Method**: ISI benchmarking survey (biennial), peer reviews, conference invitations

**Dependencies**:
- G-002: Cost reduction enabling investment in innovation
- G-003: Census-scale capability demonstrating technical leadership
- G-012: API availability demonstrating operational excellence

**Risks to Achievement**:
- International peers accelerating faster
- Budget constraints limiting innovation investment

---

### Goal G-002: Achieve 40% Infrastructure Cost Reduction

**Derived From Drivers**: SD-002

**Goal Owner**: S-001 Chief Data Officer

**Goal Statement**: Reduce annual infrastructure operating costs from £11.2M to £6.7M (40% reduction = £4.5M/year savings) by Month 24 post-go-live

**Why This Matters**: Addresses CDO's financial driver and HM Treasury efficiency requirements, maintaining BCR >2.0 for continued programme approval.

**Success Metrics**:
- **Primary Metric**: Annual infrastructure operating costs (Target: ≤£6.7M)
- **Secondary Metrics**:
  - Monthly costs ≤£558K
  - Cost per dataset published reduced 50%
  - FinOps dashboard confirms 40% reduction

**Baseline**: £11.2M/year (on-premises infrastructure)

**Target**: £6.7M/year by Month 24 (2029-04)

**Measurement Method**: Monthly FinOps cost reports aggregated from cloud provider billing APIs

**Dependencies**:
- Legacy system decommissioning
- Cloud migration completion
- FinOps capability establishment

**Risks to Achievement**:
- Dual-running costs extending
- Security requirements increasing costs
- Cloud cost escalation

---

### Goal G-003: Deliver Census-Scale Processing Capability

**Derived From Drivers**: SD-003

**Goal Owner**: S-001 Chief Data Officer

**Goal Statement**: Process 67 million census records end-to-end in <24 hours (vs 6 months in 2021)

**Why This Matters**: Mitigates CDO's risk driver by preventing repeat of 2021 Census processing failure, protecting ONS credibility for Census 2031.

**Success Metrics**:
- **Primary Metric**: 67M record processing time (Target: <24 hours)
- **Secondary Metrics**:
  - Linear scaling to 100M records demonstrated
  - Processing cost per record <£0.0001
  - Census 2031 rehearsal validated (2029)

**Baseline**: 2021 Census: 6 months processing time

**Target**: <24 hours by go-live (2027-05)

**Measurement Method**: Alpha load testing (Week 36), Beta performance testing (Week 60), Census 2031 rehearsal

**Dependencies**:
- Distributed processing framework deployment
- Data lake architecture implementation
- Cloud compute capacity

**Risks to Achievement**:
- Architecture complexity
- Skills gaps in distributed processing
- Budget constraints on compute investment

---

### Goal G-004: Maintain Statistics Act 2007 Compliance

**Derived From Drivers**: SD-004

**Goal Owner**: S-002 Chief Statistician

**Goal Statement**: Zero Statistics Act compliance breaches during implementation and operation

**Why This Matters**: Addresses Chief Statistician's compliance driver protecting ONS legal obligations and National Statistics designation.

**Success Metrics**:
- **Primary Metric**: Statistics Act breach count (Target: Zero)
- **Secondary Metrics**:
  - Pre-release access limited to 24 hours maximum
  - MFA compliance 100% for pre-release access
  - Audit trail 100% capture

**Baseline**: 2024 audit: 3 minor pre-release access audit findings

**Target**: Zero breaches continuous from Discovery through Month 12 post-go-live

**Measurement Method**: UK Statistics Authority audit reports, pre-release access audit logs, quarterly self-assessments

**Dependencies**:
- MFA implementation for pre-release access
- Audit logging infrastructure
- Automated access control enforcement

**Risks to Achievement**:
- User workarounds bypassing controls
- System errors creating audit gaps
- Pre-release access scope ambiguity

---

### Goal G-005: Implement Automated Statistical Disclosure Control

**Derived From Drivers**: SD-005

**Goal Owner**: S-002 Chief Statistician

**Goal Statement**: 100% of published statistics processed through automated SDC rules with zero re-identification incidents

**Why This Matters**: Addresses Chief Statistician's compliance driver ensuring GDPR and Statistics Act protection of individuals and businesses.

**Success Metrics**:
- **Primary Metric**: SDC automation coverage (Target: 100%)
- **Secondary Metrics**:
  - Zero publications with cell counts <3 individuals
  - Re-identification risk rating: ACCEPTABLE
  - ICO audit: zero SDC findings

**Baseline**: Manual SDC checks (100% statistician review)

**Target**: 100% automated SDC by Beta Week 52 (2026-11)

**Measurement Method**: SDC audit logs, publication reviews, re-identification testing, PIA approval

**Dependencies**:
- SDC rule engine implementation
- Re-identification testing capability
- Privacy Impact Assessment approval

**Risks to Achievement**:
- Complex statistical methodologies
- SDC vs data utility trade-offs
- New data types requiring rule updates

---

### Goal G-006: Ensure Infrastructure Independence During Elections

**Derived From Drivers**: SD-006

**Goal Owner**: S-002 Chief Statistician

**Goal Statement**: Zero infrastructure-related publication delays during election periods (2025, 2029)

**Why This Matters**: Protects Chief Statistician's strategic driver maintaining ONS independence and avoiding perception of political interference.

**Success Metrics**:
- **Primary Metric**: Infrastructure-related delays during elections (Target: Zero)
- **Secondary Metrics**:
  - 99.95% uptime during election periods
  - Zero Parliamentary questions on infrastructure failures

**Baseline**: 2019 election: 1 GDP release delayed 4 hours due to infrastructure

**Target**: Zero delays by next General Election (2029)

**Measurement Method**: Publication adherence logs, uptime monitoring, Parliamentary question tracking

**Dependencies**:
- Multi-region resilience implementation
- Election-period resilience testing
- Incident response readiness

**Risks to Achievement**:
- Cloud provider outages
- Unexpected traffic spikes
- Unplanned maintenance

---

### Goal G-007: Reduce Statistician Manual Publication Effort by 60%

**Derived From Drivers**: SD-007

**Goal Owner**: S-003 Director of Statistical Production

**Goal Statement**: Reduce statistician time on publication mechanics from 35% to 14% (60% reduction = 600 days/year released)

**Why This Matters**: Core benefits realization metric addressing Director's operational driver and releasing statistician capacity for analytical work.

**Success Metrics**:
- **Primary Metric**: Statistician time on publication mechanics (Target: ≤14%)
- **Secondary Metrics**:
  - Automated workflow: zero manual steps
  - Statistician satisfaction: ≥80%
  - 600 days/year capacity released

**Baseline**: 35% of statistician time (time-motion studies 2024)

**Target**: ≤14% by Month 12 post-go-live (2028-05)

**Measurement Method**: Quarterly time-motion studies, workflow automation metrics, satisfaction surveys

**Dependencies**:
- Publication workflow automation
- Training completion for 500 statisticians
- Change management success

**Risks to Achievement**:
- Statistician resistance to change
- Complex edge cases requiring manual intervention
- Training effectiveness

---

### Goal G-008: Reduce Time-to-Publish to 2 Days

**Derived From Drivers**: SD-008

**Goal Owner**: S-003 Director of Statistical Production

**Goal Statement**: Reduce average time-to-publish from 4 days to 2 days for major economic indicators (GDP, CPI, Labour Market)

**Why This Matters**: Addresses Director's operational driver improving timeliness of market-sensitive releases.

**Success Metrics**:
- **Primary Metric**: Average time-to-publish for major indicators (Target: ≤2 days p50)
- **Secondary Metrics**:
  - 90% of publications ≤3 days (p90)
  - Publication schedule adherence ≥98%

**Baseline**: 4 days average (2024)

**Target**: ≤2 days by Month 6 post-go-live (2027-11)

**Measurement Method**: Publication tracking dashboard, per-series time-to-publish metrics

**Dependencies**:
- Automated validation and quality checks
- Streamlined approval workflows
- Data quality improvements upstream

**Risks to Achievement**:
- Data quality issues causing delays
- Compliance review bottlenecks
- Statistician availability

---

### Goal G-009: Reduce Publication Error Rate to <0.1%

**Derived From Drivers**: SD-009

**Goal Owner**: S-003 Director of Statistical Production

**Goal Statement**: Reduce publication error rate from 2.3% to <0.1% through automated quality controls

**Why This Matters**: Addresses Director's operational driver protecting publication quality and reducing rework.

**Success Metrics**:
- **Primary Metric**: Publication error rate (Target: <0.1%)
- **Secondary Metrics**:
  - Automated validation catches 95% of errors
  - Correction rate <4/year
  - User complaints reduced 90%

**Baseline**: 2.3% error rate (87 corrections in last 12 months)

**Target**: <0.1% by Month 6 post-go-live (2027-11)

**Measurement Method**: Publication error logs, correction tracking, automated quality validation reports

**Dependencies**:
- Automated quality validation implementation
- Pre-publication review workflows
- Version control for statistical outputs

**Risks to Achievement**:
- Complex validation rules
- Time pressure for releases
- Edge cases in methodology code

---

### Goal G-010: Deliver Programme Successfully for Service Assessment Pass

**Derived From Drivers**: SD-010

**Goal Owner**: S-003 Director of Statistical Production

**Goal Statement**: Deliver programme to Beta assessment pass and go-live on time/budget

**Why This Matters**: Addresses Director's personal driver demonstrating leadership capability through successful programme delivery.

**Success Metrics**:
- **Primary Metric**: Service Assessment outcomes (Target: PASS at Alpha, Beta, Live)
- **Secondary Metrics**:
  - Go-live on schedule (Week 78)
  - Budget within 10%
  - Benefits realization ≥75% within 12 months

**Baseline**: N/A (new programme)

**Target**: Beta Assessment PASS (Week 72), Go-live (Week 78)

**Measurement Method**: GDS Service Assessment reports, schedule variance, budget variance

**Dependencies**:
- All 14 Service Standard criteria met
- Budget management
- Stakeholder alignment

**Risks to Achievement**:
- Service Assessment failure
- Budget overrun
- Stakeholder conflicts

---

### Goal G-011: Establish TCoP Compliant Architecture

**Derived From Drivers**: SD-011

**Goal Owner**: S-004 Chief Data Architect

**Goal Statement**: Achieve Technology Code of Practice compliance across all 13 points by Beta Assessment

**Why This Matters**: Addresses Chief Architect's strategic driver ensuring government policy compliance.

**Success Metrics**:
- **Primary Metric**: TCoP criteria met (Target: 13/13)
- **Secondary Metrics**:
  - Cloud-first: 100% cloud-native
  - Open standards: SDMX, OpenAPI, DCAT compliance
  - GDS Service Assessment: TCoP confirmed

**Baseline**: 4/13 TCoP points compliant (2024)

**Target**: 13/13 by Beta Assessment Week 72

**Measurement Method**: TCoP self-assessment, GDS Service Assessment validation

**Dependencies**:
- Cloud migration completion
- Open standards adoption
- GovS 007 accreditation

**Risks to Achievement**:
- Legacy system integration challenges
- Vendor lock-in concerns
- Skills gaps

---

### Goal G-012: Achieve 99.95% Publication API Availability

**Derived From Drivers**: SD-012

**Goal Owner**: S-004 Chief Data Architect

**Goal Statement**: Achieve 99.95% monthly uptime for publication APIs (max 21.9 minutes downtime per month)

**Why This Matters**: Addresses Chief Architect's operational driver ensuring reliability for market-sensitive releases.

**Success Metrics**:
- **Primary Metric**: Monthly API uptime (Target: ≥99.95%)
- **Secondary Metrics**:
  - Zero unplanned outages during major publications
  - MTTR <30 minutes
  - Incident response SLA: acknowledge <15 min

**Baseline**: 97.8% uptime (9.6 hours downtime/month)

**Target**: ≥99.95% by Month 6 post-go-live (2027-11)

**Measurement Method**: Synthetic monitoring, incident logs, monthly SLA reports

**Dependencies**:
- Multi-AZ deployment
- Auto-scaling implementation
- Comprehensive observability

**Risks to Achievement**:
- Cloud provider outages
- Unexpected traffic spikes
- Complex failure modes

---

### Goal G-013: Avoid Vendor Lock-in

**Derived From Drivers**: SD-013

**Goal Owner**: S-004 Chief Data Architect

**Goal Statement**: Design architecture enabling cloud provider portability within 6 months if required

**Why This Matters**: Addresses Chief Architect's risk driver ensuring long-term flexibility for 30-year platform lifespan.

**Success Metrics**:
- **Primary Metric**: Vendor lock-in risk rating (Target: LOW)
- **Secondary Metrics**:
  - IaC coverage: 100% Terraform
  - Containerization: 100% of workloads
  - Data export: Open formats within 48 hours

**Baseline**: 30-year on-premises lock-in (current)

**Target**: LOW risk rating by Beta Week 72

**Measurement Method**: Architecture Review Board assessment, portability testing

**Dependencies**:
- Infrastructure as Code adoption
- Containerization of workloads
- Open standards compliance

**Risks to Achievement**:
- Cloud-specific managed services
- Proprietary features
- Data egress costs

---

### Goal G-014: Achieve GovS 007 OFFICIAL Accreditation

**Derived From Drivers**: SD-014

**Goal Owner**: S-005 Head of Cyber Security

**Goal Statement**: Pass IT Health Check (ITHC) and achieve GovS 007 OFFICIAL accreditation by Beta Week 72

**Why This Matters**: Addresses Security's compliance driver - go-live gate condition.

**Success Metrics**:
- **Primary Metric**: GovS 007 accreditation status (Target: ACCREDITED)
- **Secondary Metrics**:
  - ITHC: Zero critical/high vulnerabilities
  - Security controls: 100% coverage
  - NCSC Cyber Essentials Plus certified

**Baseline**: ITHC lapsed (2022)

**Target**: Accreditation issued by Week 73 (go-live)

**Measurement Method**: ITHC report, accreditation certificate, control audit

**Dependencies**:
- Security by design implementation
- Vulnerability remediation
- CHECK-certified ITHC testers

**Risks to Achievement**:
- ITHC failure requiring remediation
- Third-party vulnerabilities
- Timeline constraints

---

### Goal G-015: Prevent Pre-Release Data Breach

**Derived From Drivers**: SD-015

**Goal Owner**: S-005 Head of Cyber Security

**Goal Statement**: Zero security incidents involving pre-release statistics during implementation and first 12 months operation

**Why This Matters**: Addresses Security's risk driver preventing market abuse and criminal liability.

**Success Metrics**:
- **Primary Metric**: Pre-release security incidents (Target: Zero)
- **Secondary Metrics**:
  - MFA compliance: 100%
  - SIEM monitoring: 24/7
  - Quarterly pen testing: zero successful breaches

**Baseline**: Zero incidents historically (must maintain)

**Target**: Zero continuous through Month 12 post-go-live

**Measurement Method**: SIEM alerts, incident logs, pen testing reports, audit logs

**Dependencies**:
- MFA enforcement
- SIEM implementation
- Quarterly penetration testing

**Risks to Achievement**:
- Insider threat
- Social engineering
- System vulnerabilities

---

### Goal G-016: Implement Zero Trust Architecture

**Derived From Drivers**: SD-016

**Goal Owner**: S-005 Head of Cyber Security

**Goal Statement**: Implement NCSC Zero Trust principles across 100% of platform components by Beta Week 72

**Why This Matters**: Addresses Security's compliance driver meeting NCSC guidance for OFFICIAL data.

**Success Metrics**:
- **Primary Metric**: NCSC CAF principles achieved (Target: 12/14)
- **Secondary Metrics**:
  - Identity-based access: 100%
  - Encrypted communication: TLS 1.3+ 100%
  - RBAC policies: 100% coverage

**Baseline**: 10/14 CAF principles (Secure by Design assessment)

**Target**: 12/14 by Beta Week 72

**Measurement Method**: NCSC CAF self-assessment, security architecture review

**Dependencies**:
- Identity provider implementation
- Network segmentation
- Encryption infrastructure

**Risks to Achievement**:
- Legacy system integration
- User experience friction
- Operational complexity

---

### Goal G-017: Complete DPIA Before Beta

**Derived From Drivers**: SD-017

**Goal Owner**: S-006 Data Protection Officer

**Goal Statement**: DPIA approved by Alpha Week 23

**Why This Matters**: Addresses DPO's compliance driver - Beta phase blocker identified in Secure by Design assessment.

**Success Metrics**:
- **Primary Metric**: DPIA status (Target: APPROVED)
- **Secondary Metrics**:
  - ICO consultation completed (if required)
  - Privacy-by-design validated
  - DPIA published on ONS website

**Baseline**: No DPIA exists (new platform)

**Target**: Approved by Alpha Week 23 (2026-04)

**Measurement Method**: DPIA approval documentation, ICO correspondence, publication status

**Dependencies**:
- Data flow documentation
- Privacy-by-design implementation
- ICO consultation (if high residual risk)

**Risks to Achievement**:
- Processing scope complexity
- ICO consultation delays
- High residual risk requiring redesign

---

### Goal G-018: Implement Automated Data Retention

**Derived From Drivers**: SD-018

**Goal Owner**: S-006 Data Protection Officer

**Goal Statement**: Automated data retention policies implemented for 100% of datasets by Beta Week 52

**Why This Matters**: Addresses DPO's compliance driver for GDPR storage limitation compliance.

**Success Metrics**:
- **Primary Metric**: Retention policy coverage (Target: 100%)
- **Secondary Metrics**:
  - Automated deletion operational
  - Audit trail: 100% deletion logging
  - Legal hold process documented

**Baseline**: Manual retention management (inconsistent)

**Target**: 100% automated by Beta Week 52 (2026-11)

**Measurement Method**: Data catalog audit, deletion logs, DPO audit reports

**Dependencies**:
- Data catalog implementation
- Deletion workflow automation
- Legal hold process definition

**Risks to Achievement**:
- Complex retention requirements
- Legal hold exceptions
- Archive vs deletion trade-offs

---

### Goal G-019: Demonstrate BCR >2.0

**Derived From Drivers**: SD-019

**Goal Owner**: S-007 HM Treasury

**Goal Statement**: Achieve and maintain Benefit-Cost Ratio >2.0 throughout business case lifecycle

**Why This Matters**: Addresses HM Treasury's financial driver - programme approval condition.

**Success Metrics**:
- **Primary Metric**: Benefit-Cost Ratio (Target: ≥2.0)
- **Secondary Metrics**:
  - NPV positive
  - Benefits realization on track
  - HM Treasury approval maintained

**Baseline**: SOBC BCR 2.3:1

**Target**: ≥2.0 at SOBC, OBC, FBC, PIR

**Measurement Method**: Business case NPV calculations, benefits tracking, HM Treasury reviews

**Dependencies**:
- Cost management within budget
- Benefits realization on track
- No optimism bias

**Risks to Achievement**:
- Cost overruns
- Benefits shortfall
- External factors

---

### Goal G-020: Achieve £4.5M Annual Savings

**Derived From Drivers**: SD-020

**Goal Owner**: S-007 HM Treasury

**Goal Statement**: Deliver £4.5M/year cashable savings by Month 24 post-go-live

**Why This Matters**: Addresses HM Treasury's efficiency savings driver and Spending Review commitments.

**Success Metrics**:
- **Primary Metric**: Annual infrastructure savings (Target: £4.5M/year)
- **Secondary Metrics**:
  - Month 6: £2M/year savings
  - Month 12: £3.5M/year savings
  - Finance confirms cashable savings

**Baseline**: £11.2M/year infrastructure costs

**Target**: £4.5M/year savings by Month 24 (2029-04)

**Measurement Method**: FinOps reports, HM Treasury checkpoints, Spending Review reports

**Dependencies**:
- Legacy decommissioning
- Cloud cost optimization
- Dual-running period minimization

**Risks to Achievement**:
- Extended dual-running
- Cloud cost escalation
- Security cost increases

---

### Goal G-021: Achieve Service Standard 14/14 Pass

**Derived From Drivers**: SD-021

**Goal Owner**: S-008 GDS Service Assessor

**Goal Statement**: Pass GDS Service Standard assessment at Alpha, Beta, and Live

**Why This Matters**: Addresses GDS's compliance driver - go-live gate condition.

**Success Metrics**:
- **Primary Metric**: Service Assessment outcome (Target: PASS)
- **Secondary Metrics**:
  - 14/14 criteria met
  - Evidence portfolio complete
  - TCoP compliance confirmed

**Baseline**: N/A (new service)

**Target**: PASS at Alpha (Week 36), Beta (Week 72), Live (Month 12)

**Measurement Method**: GDS Service Assessment reports, evidence portfolio

**Dependencies**:
- User research complete
- Accessibility compliance
- Operational readiness

**Risks to Achievement**:
- Evidence gaps
- User research capacity
- Assessment panel concerns

---

### Goal G-022: Validate User-Centred Design

**Derived From Drivers**: SD-022

**Goal Owner**: S-008 GDS Service Assessor

**Goal Statement**: Conduct user research with ≥50 statisticians and ≥100 data consumers by Beta Assessment

**Why This Matters**: Addresses GDS's user-centred design validation requirements.

**Success Metrics**:
- **Primary Metric**: User research participants (Target: ≥150)
- **Secondary Metrics**:
  - Personas: 4 types documented
  - User journey maps: 6 workflows
  - Service Standard Point 1/2: STRONG evidence

**Baseline**: Zero user research (new platform)

**Target**: ≥150 participants by Beta Week 72

**Measurement Method**: User research reports, persona documentation, evidence portfolio

**Dependencies**:
- User researcher capacity
- Statistician availability
- Data consumer recruitment

**Risks to Achievement**:
- User availability
- Representative sample challenges
- Research capacity constraints

---

### Goal G-023: Achieve 50% API Adoption

**Derived From Drivers**: SD-023

**Goal Owner**: S-009 National Statistician

**Goal Statement**: 50% of ONS data consumption via APIs by Month 18 post-go-live

**Why This Matters**: Addresses National Statistician's customer driver fulfilling statutory accessibility duty.

**Success Metrics**:
- **Primary Metric**: API traffic % of total consumption (Target: ≥50%)
- **Secondary Metrics**:
  - Registered API users: ≥10,000
  - APIs available: 100% of series
  - Developer satisfaction: ≥85%

**Baseline**: 0% API consumption (100% file downloads)

**Target**: 50% by Month 18 (2029-11)

**Measurement Method**: API usage analytics, registered users, satisfaction surveys

**Dependencies**:
- API availability across all series
- Developer documentation
- Marketing and adoption campaigns

**Risks to Achievement**:
- User adoption slower than expected
- API discovery challenges
- Authentication friction

---

### Goal G-024: Maintain Public Trust ≥75%

**Derived From Drivers**: SD-024

**Goal Owner**: S-009 National Statistician

**Goal Statement**: Maintain/improve ONS public trust rating from 68% to ≥75% by 2029

**Why This Matters**: Addresses National Statistician's strategic driver protecting ONS institutional credibility.

**Success Metrics**:
- **Primary Metric**: Public trust rating (Target: ≥75%)
- **Secondary Metrics**:
  - Zero high-profile infrastructure failures
  - Zero Statistics Act breaches
  - Service availability: 99.95%

**Baseline**: 68% (2023 survey)

**Target**: ≥75% by 2029 survey

**Measurement Method**: ONS Public Trust Survey (biennial), media monitoring

**Dependencies**:
- Infrastructure reliability
- Publication quality
- Security incident prevention

**Risks to Achievement**:
- Infrastructure failures
- Data quality issues
- External trust factors

---

### Goal G-025: Prevent Budget Overrun

**Derived From Drivers**: SD-025

**Goal Owner**: S-010 National Audit Office

**Goal Statement**: Deliver programme within 10% of approved budget (£36.6M + 10% = £40.3M maximum)

**Why This Matters**: Addresses NAO's value for money scrutiny and prevents PAC hearings.

**Success Metrics**:
- **Primary Metric**: Budget variance (Target: ≤10%)
- **Secondary Metrics**:
  - Monthly variance <5% (amber threshold)
  - No forecast overrun >10%
  - NAO PIR: "value for money achieved"

**Baseline**: £36.6M approved budget

**Target**: ≤£40.3M final outturn

**Measurement Method**: Monthly budget reports, forecast outturn, NAO audit

**Dependencies**:
- Robust cost estimation
- Contingency management
- Scope control

**Risks to Achievement**:
- Scope creep
- Vendor cost escalation
- Unforeseen technical challenges

---

### Goal G-026: Improve Statistician Satisfaction to ≥80%

**Derived From Drivers**: SD-026

**Goal Owner**: S-011 Statisticians

**Goal Statement**: Achieve statistician satisfaction ≥80% with publication tools by Month 12 post-go-live

**Why This Matters**: Addresses statisticians' operational driver ensuring user adoption and benefits realization.

**Success Metrics**:
- **Primary Metric**: Satisfaction rating (Target: ≥80%)
- **Secondary Metrics**:
  - NPS: ≥40 (from -10)
  - Tool reliability: ≥99.5%
  - Training effectiveness: 85% confident

**Baseline**: 60% satisfaction (2024 survey)

**Target**: ≥80% by Month 12 (2028-05)

**Measurement Method**: Quarterly satisfaction surveys, NPS tracking

**Dependencies**:
- Intuitive tool design
- Comprehensive training
- Responsive support

**Risks to Achievement**:
- Change resistance
- Training effectiveness
- Tool reliability issues

---

### Goal G-027: Achieve 98% Publication Schedule Adherence

**Derived From Drivers**: SD-027

**Goal Owner**: S-011 Statisticians

**Goal Statement**: Achieve 98% publication schedule adherence by Month 6 post-go-live

**Why This Matters**: Addresses statisticians' reliability driver ensuring tools support deadline-critical work.

**Success Metrics**:
- **Primary Metric**: Schedule adherence (Target: ≥98%)
- **Secondary Metrics**:
  - Zero missed deadlines due to platform
  - Tool uptime: ≥99.9% during working hours
  - Incident impact: <2% publications

**Baseline**: 92% adherence (2024)

**Target**: ≥98% by Month 6 (2027-11)

**Measurement Method**: Publication adherence logs, uptime monitoring, incident tracking

**Dependencies**:
- Platform reliability
- Incident response capability
- User support

**Risks to Achievement**:
- Platform outages
- Performance issues
- User errors

---

### Goal G-028: Achieve ≥85% Data Consumer Satisfaction

**Derived From Drivers**: SD-028

**Goal Owner**: S-012 Data Consumers

**Goal Statement**: Achieve data consumer satisfaction ≥85% by Month 12 post-go-live

**Why This Matters**: Addresses data consumers' customer driver ensuring API meets user needs.

**Success Metrics**:
- **Primary Metric**: Satisfaction rating (Target: ≥85%)
- **Secondary Metrics**:
  - API response time: p95 <500ms
  - API reliability: 99.95%
  - Complaint rate: reduced 50%

**Baseline**: 65% satisfaction (2024 survey)

**Target**: ≥85% by Month 12 (2028-05)

**Measurement Method**: Quarterly surveys, API metrics, complaint tracking

**Dependencies**:
- API documentation quality
- Sandbox availability
- Developer support

**Risks to Achievement**:
- API performance issues
- Documentation gaps
- Support responsiveness

---

## Goal-to-Outcome Mapping

### Outcome O-001: International Statistical Leadership Demonstrated

**Supported Goals**: G-001, G-003, G-012

**Outcome Statement**: ONS ranked Top 3 in ISI Digital Capability Benchmark by 2030, demonstrating world-class statistical infrastructure

**Measurement Details**:
- **KPI**: ISI Digital Capability Benchmark Ranking
- **Current Value**: #7 (2024)
- **Target Value**: Top 3 by 2030
- **Measurement Frequency**: Biennial
- **Data Source**: International Statistical Institute benchmark survey
- **Report Owner**: Chief Data Officer

**Business Value**:
- **Financial Impact**: Enhanced international collaboration funding opportunities
- **Strategic Impact**: ONS positioned as global statistical leader, talent attraction
- **Operational Impact**: Best-practice infrastructure enabling innovation
- **Customer Impact**: World-class data services for UK users

**Timeline**:
- **Phase 1 (Months 1-12)**: Foundation capabilities, Census prototype validated
- **Phase 2 (Months 13-24)**: Full platform operational, API adoption growing
- **Phase 3 (Months 25-36)**: International recognition, conference keynotes
- **Sustainment (Year 4+)**: Maintain Top 3 ranking, continuous improvement

**Stakeholder Benefits**:
- **CDO**: Career achievement, programme success validation
- **National Statistician**: Institutional reputation enhanced
- **Statisticians**: Pride in world-class tools

**Leading Indicators**:
- Census prototype processing time <24 hours (Alpha)
- API availability reaches 99.95%
- International peer positive feedback

**Lagging Indicators**:
- ISI benchmark ranking improvement
- Conference keynote invitations
- Academic citations of ONS infrastructure

---

### Outcome O-002: Infrastructure Cost Reduction Achieved (£4.5M/year)

**Supported Goals**: G-002, G-020

**Outcome Statement**: 40% reduction in annual infrastructure costs (£11.2M → £6.7M), delivering £4.5M/year cashable savings

**Measurement Details**:
- **KPI**: Annual Infrastructure Operating Costs
- **Current Value**: £11.2M/year
- **Target Value**: £6.7M/year
- **Measurement Frequency**: Monthly
- **Data Source**: Cloud provider billing APIs, FinOps dashboard
- **Report Owner**: Chief Data Officer

**Business Value**:
- **Financial Impact**: £4.5M/year returned to Exchequer
- **Strategic Impact**: BCR >2.0 maintained, programme approval sustained
- **Operational Impact**: Modern, efficient infrastructure
- **Customer Impact**: Reinvestment potential in service improvements

**Timeline**:
- **Phase 1 (Months 1-6)**: Migration in progress, partial savings (£2M/year)
- **Phase 2 (Months 7-12)**: Majority decommissioned (£3.5M/year)
- **Phase 3 (Months 13-24)**: Full savings achieved (£4.5M/year)
- **Sustainment (Year 3+)**: Maintain savings, continuous optimization

**Stakeholder Benefits**:
- **CDO**: Business case validation, HM Treasury confidence
- **HM Treasury**: Efficiency targets met, VfM demonstrated
- **NAO**: Clean audit, no PAC concerns

**Leading Indicators**:
- Monthly cloud costs trending to target
- Legacy systems decommissioning on schedule
- FinOps optimization recommendations implemented

**Lagging Indicators**:
- Annual cost comparison vs baseline
- HM Treasury checkpoint GREEN ratings
- NAO PIR value for money rating

---

### Outcome O-003: Census-Scale Processing Validated

**Supported Goals**: G-003

**Outcome Statement**: 67 million census records processed end-to-end in <24 hours, validating Census 2031 readiness

**Measurement Details**:
- **KPI**: 67M Record Processing Time
- **Current Value**: 6 months (2021 Census)
- **Target Value**: <24 hours
- **Measurement Frequency**: Alpha (prototype), Beta (full test), Census rehearsal (2029)
- **Data Source**: Processing time logs, performance testing reports
- **Report Owner**: Chief Data Architect

**Business Value**:
- **Financial Impact**: Avoid £multi-million census recovery costs
- **Strategic Impact**: Census 2031 delivery confidence
- **Operational Impact**: Scalable processing capability
- **Customer Impact**: Timely census results publication

**Timeline**:
- **Phase 1 (Alpha Week 36)**: Prototype validates <24 hour feasibility
- **Phase 2 (Beta Week 60)**: Production capability tested, linear scaling
- **Phase 3 (2029 Rehearsal)**: Full census simulation validates capability
- **Sustainment (Census 2031)**: Successful census processing

**Stakeholder Benefits**:
- **CDO**: Census 2031 risk mitigated
- **National Statistician**: Census delivery confidence
- **HM Treasury**: Census investment justified

**Leading Indicators**:
- Alpha prototype completes <24 hours
- Beta linear scaling demonstrated
- Architecture Review Board approval

**Lagging Indicators**:
- Census 2031 rehearsal success
- Census 2031 actual processing time
- Post-census review rating

---

### Outcome O-004: Statistics Act Compliance Maintained (Zero Breaches)

**Supported Goals**: G-004

**Outcome Statement**: Zero Statistics Act compliance breaches, maintaining National Statistics designation and avoiding UK Statistics Authority sanctions

**Measurement Details**:
- **KPI**: Statistics Act Compliance Breach Count
- **Current Value**: 3 minor audit findings (2024)
- **Target Value**: Zero breaches
- **Measurement Frequency**: Quarterly self-assessment, Annual UK Statistics Authority audit
- **Data Source**: Pre-release access logs, audit reports
- **Report Owner**: Chief Statistician

**Business Value**:
- **Financial Impact**: Avoid regulatory penalties
- **Strategic Impact**: National Statistics designation protected
- **Operational Impact**: Compliant publication workflows
- **Customer Impact**: User trust in pre-release integrity

**Timeline**:
- **Phase 1 (Discovery-Alpha)**: Controls designed and implemented
- **Phase 2 (Beta)**: Controls validated through testing
- **Phase 3 (Go-live+12 months)**: Operational compliance demonstrated
- **Sustainment**: Continuous compliance monitoring

**Stakeholder Benefits**:
- **Chief Statistician**: Regulatory accountability fulfilled
- **UK Statistics Authority**: Confidence in ONS compliance
- **CDO**: Programme reputation protected

**Leading Indicators**:
- MFA compliance rate (target: 100%)
- Audit log completeness (target: 100%)
- Quarterly self-assessment PASS

**Lagging Indicators**:
- UK Statistics Authority annual audit findings
- Parliamentary questions mentioning compliance
- National Statistics designation reviews

---

### Outcome O-014: GovS 007 OFFICIAL Accreditation Certificate Issued

**Supported Goals**: G-014

**Outcome Statement**: GovS 007 OFFICIAL accreditation achieved before go-live, enabling operational use of platform

**Measurement Details**:
- **KPI**: GovS 007 Accreditation Status
- **Current Value**: Lapsed (2022)
- **Target Value**: ACCREDITED
- **Measurement Frequency**: ITHC (Week 68-72), Final certificate (Week 73)
- **Data Source**: ITHC report, accreditation certificate
- **Report Owner**: Head of Cyber Security

**Business Value**:
- **Financial Impact**: Avoid security remediation delays
- **Strategic Impact**: Go-live gate condition met
- **Operational Impact**: Security posture validated
- **Customer Impact**: User data protection assured

**Timeline**:
- **Phase 1 (Alpha)**: Security architecture approved
- **Phase 2 (Beta Week 68-72)**: ITHC performed
- **Phase 3 (Week 73)**: Accreditation certificate issued
- **Sustainment**: Annual re-accreditation

**Stakeholder Benefits**:
- **Head of Cyber Security**: Security accountability fulfilled
- **CDO**: Go-live enabled
- **GDS**: Security compliance confirmed

**Leading Indicators**:
- Quarterly internal pen testing results
- SAST/DAST findings remediation rate
- Security controls coverage %

**Lagging Indicators**:
- ITHC critical/high vulnerability count
- Accreditation certificate issued
- NCSC Cyber Essentials Plus certification

---

### Outcome O-019: Value for Money with BCR ≥2.0 Maintained

**Supported Goals**: G-019, G-025

**Outcome Statement**: Benefit-Cost Ratio ≥2.0 maintained throughout business case lifecycle, demonstrating value for money

**Measurement Details**:
- **KPI**: Benefit-Cost Ratio (BCR)
- **Current Value**: 2.3:1 (SOBC)
- **Target Value**: ≥2.0 at all stages
- **Measurement Frequency**: SOBC, OBC, FBC, PIR
- **Data Source**: Business case NPV calculations
- **Report Owner**: Chief Data Officer

**Business Value**:
- **Financial Impact**: £18.6M NPV over 10 years
- **Strategic Impact**: HM Treasury confidence, continued approval
- **Operational Impact**: Investment justified
- **Customer Impact**: Taxpayer value demonstrated

**Timeline**:
- **Phase 1 (SOBC 2025-11)**: BCR 2.3:1 - ACHIEVED
- **Phase 2 (OBC 2026-06)**: BCR ≥2.0 maintained
- **Phase 3 (FBC 2027-02)**: BCR ≥2.0 after procurement
- **Sustainment (PIR 2028-05)**: Actual BCR validated

**Stakeholder Benefits**:
- **HM Treasury**: VfM confidence, efficiency contribution
- **NAO**: Clean audit, no PAC concerns
- **CDO**: Programme approval sustained

**Leading Indicators**:
- Monthly cost variance <5%
- Benefits realization on trajectory
- HM Treasury checkpoint ratings GREEN

**Lagging Indicators**:
- Business case BCR at each stage
- HM Treasury approval status
- NAO PIR rating

---

### Outcome O-021: GDS Service Standard 14/14 Criteria Achieved

**Supported Goals**: G-021, G-022

**Outcome Statement**: GDS Service Standard PASS at Alpha, Beta, and Live assessments

**Measurement Details**:
- **KPI**: GDS Service Standard Assessment Outcome
- **Current Value**: N/A (new service)
- **Target Value**: PASS at all gates
- **Measurement Frequency**: Alpha (Week 36), Beta (Week 72), Live (Month 12)
- **Data Source**: GDS Service Assessment reports
- **Report Owner**: Director of Statistical Production

**Business Value**:
- **Financial Impact**: Digital spend control approval maintained
- **Strategic Impact**: Government assurance achieved
- **Operational Impact**: User-centred service validated
- **Customer Impact**: Service meets user needs

**Timeline**:
- **Phase 1 (Alpha Week 36)**: Problem validated, design approach approved
- **Phase 2 (Beta Week 72)**: 14/14 criteria PASS
- **Phase 3 (Live Month 12)**: Operational service validated
- **Sustainment**: Continuous assessment compliance

**Stakeholder Benefits**:
- **GDS**: Government digital standards upheld
- **Director of Statistical Production**: Service Owner success
- **Users**: User-centred service delivered

**Leading Indicators**:
- User research participation rates
- Evidence portfolio completeness
- Mock assessment results

**Lagging Indicators**:
- Alpha/Beta/Live assessment outcomes
- Criteria-by-criteria ratings
- GDS assessor feedback

---

### Outcome O-023: API Adoption 50% of Data Consumption

**Supported Goals**: G-023, G-028

**Outcome Statement**: 50% of ONS data consumption via APIs by Month 18, fulfilling Statistics Act accessibility duty

**Measurement Details**:
- **KPI**: API Traffic as % of Total Data Consumption
- **Current Value**: 0%
- **Target Value**: ≥50%
- **Measurement Frequency**: Monthly
- **Data Source**: API usage analytics, download analytics
- **Report Owner**: National Statistician

**Business Value**:
- **Financial Impact**: Reduced file hosting costs
- **Strategic Impact**: Statutory accessibility duty fulfilled
- **Operational Impact**: Modern data distribution
- **Customer Impact**: Programmatic access enabled

**Timeline**:
- **Phase 1 (Month 6)**: 10% API adoption, early adopters
- **Phase 2 (Month 12)**: 25% API adoption, mainstream growth
- **Phase 3 (Month 18)**: 50% API adoption, target achieved
- **Sustainment (Year 2+)**: Grow to >60%

**Stakeholder Benefits**:
- **National Statistician**: Statutory duty fulfilled
- **Data Consumers**: Modern data access
- **Researchers**: Machine-readable data for analysis

**Leading Indicators**:
- Registered API users growth rate
- Developer portal visits
- Sandbox usage

**Lagging Indicators**:
- API traffic % of total consumption
- User satisfaction surveys
- Research citations using API data

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder ID | Stakeholder | Driver ID | Driver Type | Intensity | Goal ID | Outcome ID | Primary KPI |
|---------------|-------------|-----------|-------------|-----------|---------|------------|-------------|
| S-001 | Chief Data Officer | SD-001 | STRATEGIC | CRITICAL | G-001 | O-001 | ISI Ranking (Top 3) |
| S-001 | Chief Data Officer | SD-002 | FINANCIAL | HIGH | G-002 | O-002 | Costs (≤£6.7M/yr) |
| S-001 | Chief Data Officer | SD-003 | RISK | HIGH | G-003 | O-003 | Processing (<24h) |
| S-002 | Chief Statistician | SD-004 | COMPLIANCE | CRITICAL | G-004 | O-004 | Breaches (Zero) |
| S-002 | Chief Statistician | SD-005 | COMPLIANCE | HIGH | G-005 | O-005 | SDC Coverage (100%) |
| S-002 | Chief Statistician | SD-006 | STRATEGIC | MEDIUM | G-006 | O-006 | Election Delays (Zero) |
| S-003 | Dir. Statistical Production | SD-007 | OPERATIONAL | CRITICAL | G-007 | O-007 | Manual Effort (≤14%) |
| S-003 | Dir. Statistical Production | SD-008 | OPERATIONAL | HIGH | G-008 | O-008 | Time-to-Publish (≤2d) |
| S-003 | Dir. Statistical Production | SD-009 | OPERATIONAL | HIGH | G-009 | O-009 | Error Rate (<0.1%) |
| S-003 | Dir. Statistical Production | SD-010 | PERSONAL | MEDIUM | G-010 | O-010 | Assessment (PASS) |
| S-004 | Chief Data Architect | SD-011 | STRATEGIC | HIGH | G-011 | O-011 | TCoP (13/13) |
| S-004 | Chief Data Architect | SD-012 | OPERATIONAL | HIGH | G-012 | O-012 | Uptime (≥99.95%) |
| S-004 | Chief Data Architect | SD-013 | RISK | HIGH | G-013 | O-013 | Lock-in Risk (LOW) |
| S-005 | Head of Cyber Security | SD-014 | COMPLIANCE | CRITICAL | G-014 | O-014 | Accreditation (ISSUED) |
| S-005 | Head of Cyber Security | SD-015 | RISK | CRITICAL | G-015 | O-015 | Breaches (Zero) |
| S-005 | Head of Cyber Security | SD-016 | COMPLIANCE | HIGH | G-016 | O-016 | CAF Score (12/14) |
| S-006 | Data Protection Officer | SD-017 | COMPLIANCE | HIGH | G-017 | O-017 | DPIA (APPROVED) |
| S-006 | Data Protection Officer | SD-018 | COMPLIANCE | MEDIUM | G-018 | O-018 | Retention (100%) |
| S-007 | HM Treasury | SD-019 | FINANCIAL | CRITICAL | G-019 | O-019 | BCR (≥2.0) |
| S-007 | HM Treasury | SD-020 | FINANCIAL | HIGH | G-020 | O-002 | Savings (£4.5M/yr) |
| S-008 | GDS Service Assessor | SD-021 | COMPLIANCE | HIGH | G-021 | O-021 | Assessment (PASS) |
| S-008 | GDS Service Assessor | SD-022 | COMPLIANCE | MEDIUM | G-022 | O-022 | Research (150+) |
| S-009 | National Statistician | SD-023 | CUSTOMER | CRITICAL | G-023 | O-023 | API Adoption (≥50%) |
| S-009 | National Statistician | SD-024 | STRATEGIC | HIGH | G-024 | O-024 | Trust Rating (≥75%) |
| S-010 | National Audit Office | SD-025 | FINANCIAL | MEDIUM | G-025 | O-025 | Budget Var (≤10%) |
| S-011 | Statisticians | SD-026 | OPERATIONAL | HIGH | G-026 | O-026 | Satisfaction (≥80%) |
| S-011 | Statisticians | SD-027 | CUSTOMER | MEDIUM | G-027 | O-027 | Adherence (≥98%) |
| S-012 | Data Consumers | SD-028 | CUSTOMER | HIGH | G-028 | O-028 | Satisfaction (≥85%) |

### Conflict Analysis

**Competing Drivers**:

- **Conflict C-001**: S-001 CDO (SD-002: cost reduction) vs S-005 Security (SD-014/SD-016: enterprise security costs)
  - **Resolution Strategy**: Risk-based segmentation - critical systems multi-region, non-critical single-region. +£400K cost within target. Approved Programme Board Week 24.

- **Conflict C-002**: S-001 CDO (SD-001: innovation speed) vs S-002 Chief Statistician (SD-004: compliance rigor)
  - **Resolution Strategy**: Two-speed architecture - publication-critical path has strict change control, non-publication features use agile sprints. Approved Programme Board Week 36.

- **Conflict C-003**: S-009 National Statistician (SD-023: open access) vs S-005 Security (SD-015: access controls)
  - **Resolution Strategy**: Tiered access model - published statistics anonymous access, pre-release requires MFA. Clear /public vs /pre-release endpoint separation. Approved Programme Board Week 24.

- **Conflict C-004**: S-001 CDO (SD-003: census investment) vs S-007 HM Treasury (SD-019: budget constraints)
  - **Resolution Strategy**: Early prototyping with gated investment - Alpha prototype (£200K) provides evidence, Beta capability (£2.8M) released only after Alpha success. Approved HM Treasury SOBC.

**Synergies**:

- **Synergy 1**: SD-001 (transformation) and SD-011 (TCoP compliance) - both drive cloud-native architecture
- **Synergy 2**: SD-007 (manual effort reduction) and SD-008 (time-to-publish) - both benefit from workflow automation
- **Synergy 3**: SD-004 (Statistics Act) and SD-015 (breach prevention) - both require strong access controls
- **Synergy 4**: SD-019 (BCR) and SD-002 (cost reduction) - both drive infrastructure optimization

---

## Communication & Engagement Plan

### Chief Data Officer (S-001) - SRO

**Primary Message**: Programme delivering transformational change with strong financial discipline - international leadership within budget

**Key Talking Points**:
- Budget on track, benefits trajectory confirmed
- International benchmarking progress
- Critical risks under active management

**Communication Frequency**: Weekly 1:1s, Monthly Programme Board

**Preferred Channel**: Executive dashboard, Slack for urgent, formal email for decisions

**Success Story**: "ONS recognized as Top 3 statistical institute globally, with £4.5M annual savings returned to Exchequer"

---

### Chief Statistician (S-002) - Regulatory Authority

**Primary Message**: Zero compliance compromises - Statistics Act requirements fully met through modern, automated controls

**Key Talking Points**:
- Pre-release access controls 100% compliant
- SDC automation validated
- Publication quality improving

**Communication Frequency**: Fortnightly compliance reviews, Monthly Programme Board

**Preferred Channel**: Formal reports, compliance dashboards

**Success Story**: "UK Statistics Authority audit confirms zero compliance issues, with publication error rate reduced 95%"

---

### Director of Statistical Production (S-003) - Product Owner

**Primary Message**: Statisticians freed from IT burden - 60% time saved for analytical work

**Key Talking Points**:
- Workflow automation progress
- Statistician satisfaction improving
- Training and change management on track

**Communication Frequency**: Daily standups (Beta), Weekly backlog refinement

**Preferred Channel**: Slack, sprint demos, workshops

**Success Story**: "Statistician satisfaction at 85%, with 600 days/year released for analytical work"

---

### HM Treasury (S-007) - Funding Authority

**Primary Message**: Strong value for money - BCR maintained, savings on trajectory

**Key Talking Points**:
- Budget variance within tolerance
- Benefits realization on track
- No cost overrun risks identified

**Communication Frequency**: Quarterly checkpoint meetings

**Preferred Channel**: Formal checkpoint reports, business case submissions

**Success Story**: "£4.5M annual savings delivered ahead of schedule, BCR 2.3:1 validated in PIR"

---

### Statisticians (S-011) - Internal Users

**Primary Message**: Modern tools that let you focus on statistics, not IT

**Key Talking Points**:
- 60% time savings on publication mechanics
- Reliable tools meeting 9:30 AM deadlines
- Comprehensive training and support available

**Communication Frequency**: Monthly workshops, Quarterly surveys

**Preferred Channel**: Intranet, email newsletters, demos

**Success Story**: "95% of statisticians say new tools let them focus on what matters - producing world-class statistics"

---

### Data Consumers (S-012) - External Users

**Primary Message**: ONS data at your fingertips - modern APIs for programmatic access

**Key Talking Points**:
- 100% of statistics available via API
- Developer-friendly documentation
- Fast, reliable access (99.95% uptime)

**Communication Frequency**: Quarterly webinars

**Preferred Channel**: Developer portal, email updates

**Success Story**: "Over 10,000 organizations now access ONS data via API, powering research, policy, and business decisions"

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Statisticians (S-011) | Manual publication workflows, file-based | Automated workflows, API-first | HIGH | MEDIUM | Change champions, extended training, 6-week hypercare |
| Data Consumers (S-012) | File downloads only | API access primary channel | HIGH | LOW | Developer documentation, sandbox, webinars |
| Chief Statistician (S-002) | Manual compliance reviews | Automated compliance controls | MEDIUM | LOW | Compliance dashboard, continuous validation reporting |
| Security (S-005) | Perimeter security | Zero Trust architecture | MEDIUM | LOW | Phased implementation, NCSC alignment |
| IT Operations | On-premises infrastructure | Cloud-native managed services | HIGH | MEDIUM | Retraining, DevOps transition support |

### Change Readiness

**Champions** (Enthusiastic supporters):
- S-001 CDO - Programme sponsor, career stake
- S-003 Director of Statistical Production - Benefits owner, career progression
- S-004 Chief Data Architect - Modern architecture advocate

**Fence-sitters** (Neutral, need convincing):
- S-011 Statisticians (subset) - Need to see tools work before committing
- S-006 DPO - Focused on compliance, neutral on change itself

**Resisters** (Opposed or skeptical):
- S-011 Statisticians (subset) - Fear of job changes, learning curve concerns
  - **Strategy**: Extended training, hypercare support, demonstrate time savings

---

## Risk Register (Stakeholder-Related)

### Risk SR-001: Statistician Change Resistance

**Related Stakeholders**: S-003, S-011

**Risk Description**: Statistician resistance to change leads to <80% adoption, preventing efficiency benefits realization

**Impact on Goals**: G-007, G-026, O-007

**Probability**: POSSIBLE | **Impact**: HIGH

**Mitigation Strategy**: Change champions network (5 statisticians), extended training (4 hours), 6-week hypercare, quarterly satisfaction surveys

**Contingency Plan**: Extended parallel running, additional training, targeted support for resistant groups

---

### Risk SR-002: Statistics Act Compliance Breach

**Related Stakeholders**: S-002, S-009

**Risk Description**: Statistics Act compliance breach during implementation damages ONS reputation and triggers UK Statistics Authority sanctions

**Impact on Goals**: G-004, O-004

**Probability**: UNLIKELY | **Impact**: CRITICAL

**Mitigation Strategy**: MFA enforced 100%, audit logs monitored 24/7, quarterly compliance reviews, UK Statistics Authority validation in Alpha

**Contingency Plan**: Immediate remediation, UK Statistics Authority notification, root cause analysis

---

### Risk SR-003: Budget Overrun

**Related Stakeholders**: S-001, S-007

**Risk Description**: Budget overrun >10% triggers HM Treasury funding withdrawal and programme cancellation

**Impact on Goals**: G-019, G-025, O-019

**Probability**: POSSIBLE | **Impact**: CRITICAL

**Mitigation Strategy**: 10% contingency (£1.8M), monthly budget variance monitoring, early escalation at >5% variance

**Contingency Plan**: Scope reduction, timeline extension, re-baselining business case

---

### Risk SR-004: Service Standard Assessment Failure

**Related Stakeholders**: S-003, S-008

**Risk Description**: Service Standard Beta assessment fails, delaying go-live and damaging credibility

**Impact on Goals**: G-010, G-021, O-021

**Probability**: UNLIKELY | **Impact**: HIGH

**Mitigation Strategy**: Mock assessment in Alpha Week 36, continuous evidence portfolio, GDS engagement quarterly

**Contingency Plan**: Conditional pass remediation, timeline extension, additional GDS coaching

---

### Risk SR-005: ITHC Failure

**Related Stakeholders**: S-005

**Risk Description**: ITHC failure prevents go-live, requires 3-month remediation, delays programme 12 weeks

**Impact on Goals**: G-014, O-014

**Probability**: POSSIBLE | **Impact**: HIGH

**Mitigation Strategy**: Security by design, SAST/DAST in CI/CD, quarterly internal pen testing, CHECK testers engaged Week 68

**Contingency Plan**: Rapid remediation sprint, re-test within 4 weeks, timeline extension if needed

---

### Risk SR-006: API Adoption Failure

**Related Stakeholders**: S-009, S-012

**Risk Description**: API adoption fails (<25% vs 50% target), wasting investment and failing statutory accessibility duty

**Impact on Goals**: G-023, O-023

**Probability**: POSSIBLE | **Impact**: HIGH

**Mitigation Strategy**: User research (100+ data consumers), developer webinars, sandbox, generous rate limits, marketing campaign

**Contingency Plan**: Enhanced marketing, user research to identify barriers, feature improvements

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Programme strategic direction | Dir. of Production | CDO (SRO) | Chief Statistician, Chief Architect | All stakeholders |
| Budget allocation | CDO (SRO) | Permanent Secretary | HM Treasury | Programme Board |
| Architecture decisions | Chief Data Architect | Architecture Review Board | Security, DPO | Programme Board |
| Requirements prioritization | Dir. of Production | Programme Board | Statisticians, Chief Statistician | Delivery Team |
| Go/No-go gate decisions | Programme Board | CDO (SRO) | GDS Assessor, UK Statistics Authority | HM Treasury |
| Statistics Act compliance | Chief Statistician | UK Statistics Authority | DPO, Security | Programme Board |
| Security accreditation | Head of Cyber Security | SIRO | Chief Architect | Programme Board |
| DPIA approval | Data Protection Officer | ICO (if consulted) | Security, Chief Statistician | Programme Board |
| Service Standard assessment | Dir. of Production | GDS Service Assessor | Delivery Team | Programme Board |
| Benefits realization | Dir. of Production | CDO (SRO) | Finance, HM Treasury | Programme Board |

### Escalation Path

1. **Level 1**: Project Manager / Product Owner - Day-to-day decisions, sprint scope
2. **Level 2**: Programme Board (monthly) - Scope, timeline, budget variances >5%
3. **Level 3**: CDO (SRO) - Strategic direction, major conflicts, exceptions
4. **Level 4**: HM Treasury / UK Statistics Authority - Funding, regulatory escalations

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| Chief Data Officer (S-001) | PENDING | | PENDING |
| Chief Statistician (S-002) | PENDING | | PENDING |
| Director of Statistical Production (S-003) | PENDING | | PENDING |
| Chief Data Architect (S-004) | PENDING | | PENDING |
| Head of Cyber Security (S-005) | PENDING | | PENDING |
| Data Protection Officer (S-006) | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor | CDO | | |
| Business Owner | Dir. of Statistical Production | | |
| Enterprise Architect | Chief Data Architect | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

#### Interview with Director of Statistical Production - 2025-11-02

**Key Points**:
- Frustrated with 35% time on publication mechanics
- Keen on modern tools to attract talent
- Concerned about statistician change resistance

**Quotes**:
- "Our statisticians want to do statistics, not wrestle with spreadsheets and FTP uploads"
- "If we can save 60% of publication time, we can finally invest in new analytical capabilities"

**Follow-up Actions**:
- Include statistician workshops in Discovery
- Design change management programme

---

#### Interview with Head of Cyber Security - 2025-11-03

**Key Points**:
- GovS 007 accreditation non-negotiable
- Zero tolerance for pre-release data breaches
- Supportive of Zero Trust approach

**Quotes**:
- "Pre-release GDP data is market-sensitive. A breach would be catastrophic - potentially criminal"
- "We need identity-based access, not network perimeters. Zero Trust is the only way"

**Follow-up Actions**:
- Early security architecture engagement
- Quarterly internal pen testing

---

### Appendix B: Driver Type Summary

| Driver Type | Count | % of Total | Critical Intensity |
|-------------|-------|------------|-------------------|
| COMPLIANCE | 9 | 32% | 3 (33%) |
| OPERATIONAL | 6 | 21% | 1 (17%) |
| STRATEGIC | 5 | 18% | 1 (20%) |
| FINANCIAL | 4 | 14% | 1 (25%) |
| CUSTOMER | 3 | 11% | 1 (33%) |
| RISK | 3 | 11% | 1 (33%) |
| PERSONAL | 1 | 4% | 0 (0%) |
| **Total** | **28** | **100%** | **8 (29%)** |

---

### Appendix C: References

- Architecture Principles document (ARC-001-PRIN-v1.1)
- Strategic Outline Business Case (SOBC)
- Risk Register (ARC-001-RISK-v1.0)
- Requirements document (ARC-001-REQ-v1.0)
- UK Statistics Act 2007
- GDS Service Standard
- Technology Code of Practice
- NCSC Zero Trust Architecture guidance

---

## Document Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial stakeholder analysis |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2 |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-01-26
**ArcKit Version**: 0.11.2
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-opus-4-5-20251101
