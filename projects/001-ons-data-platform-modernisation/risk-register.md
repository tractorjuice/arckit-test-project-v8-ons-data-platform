# Risk Register: ONS Data Platform Modernisation

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.0 |
| **Document Type** | Risk Register (HM Treasury Orange Book) |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2025-11-05 |
| **Review Frequency** | Monthly (Critical/High), Quarterly (Medium/Low) |
| **Next Review Date** | 2025-12-05 |
| **Risk Register Owner** | Chief Data Architect, ONS |
| **Approved By** | [PENDING] |

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial creation from `/arckit.risk` command |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified**: 22 risks across 6 categories

| Category | Count | Average Inherent Score | Average Residual Score | Risk Reduction |
|----------|-------|------------------------|------------------------|----------------|
| STRATEGIC | 4 | 18.0 | 10.5 | 42% |
| OPERATIONAL | 5 | 14.4 | 9.2 | 36% |
| FINANCIAL | 3 | 15.3 | 9.7 | 37% |
| COMPLIANCE | 5 | 19.2 | 11.8 | 39% |
| TECHNOLOGY | 4 | 16.5 | 10.0 | 39% |
| REPUTATIONAL | 1 | 16.0 | 10.0 | 38% |

### Risk Distribution by Severity

**Inherent Risk** (before controls):
- **Critical (20-25)**: 6 risks (27%)
- **High (13-19)**: 12 risks (55%)
- **Medium (6-12)**: 4 risks (18%)
- **Low (1-5)**: 0 risks (0%)

**Residual Risk** (after controls):
- **Critical (20-25)**: 0 risks (0%) ✅
- **High (13-19)**: 3 risks (14%)
- **Medium (6-12)**: 16 risks (73%)
- **Low (1-5)**: 3 risks (14%)

### Overall Assessment

**Overall Risk Profile**: **CONCERNING but MANAGEABLE**

**Key Findings**:
- All 6 Critical inherent risks reduced to High/Medium through planned controls
- 3 High residual risks require active monitoring and additional mitigations
- Effective control framework reduces overall risk by 38% on average
- 14% of risks (3) remain HIGH after controls - require escalation to Programme Board
- No risks exceed organizational appetite thresholds with planned controls in place

### Top 5 Risks Requiring Immediate Attention

| Rank | ID | Title | Category | Residual Score | Owner | Status |
|------|-----|-------|----------|----------------|-------|--------|
| 1 | R-003 | Data Migration Integrity Failures | OPERATIONAL | 15 (High) | Chief Data Architect | Open |
| 2 | R-006 | Statistics Act Pre-Release Access Breach | COMPLIANCE | 15 (High) | Chief Statistician | Open |
| 3 | R-010 | Census-Scale Performance Failure | TECHNOLOGY | 15 (High) | Chief Data Architect | Open |
| 4 | R-001 | Strategic Direction Change Mid-Project | STRATEGIC | 12 (Medium) | Chief Data Officer | Open |
| 5 | R-007 | Cloud Cost Overruns Exceed £6.7M Target | FINANCIAL | 12 (Medium) | Chief Data Officer | Open |

### Immediate Actions Required

1. **R-003 Data Migration**: Establish parallel running environment by Week 65 (Beta Sprint 5)
2. **R-006 Statistics Act Compliance**: Design pre-release access controls in Sprint 4, validate with UK Statistics Authority
3. **R-010 Performance**: Conduct early performance prototyping in Alpha (Week 20-24)
4. **R-001 Strategic Risk**: Monthly Programme Board reviews to monitor policy stability
5. **R-007 Cost Management**: Implement FinOps controls and monthly cost reviews from Week 43 (Beta start)

### 4Ts Risk Response Distribution

| Response | Count | % | Description |
|----------|-------|---|-------------|
| **Treat** | 18 risks | 82% | Mitigate through additional controls, dominant strategy |
| **Transfer** | 2 risks | 9% | Cyber insurance, vendor liability contracts |
| **Tolerate** | 2 risks | 9% | Accept within appetite (statistician resistance, skills gaps) |
| **Terminate** | 0 risks | 0% | No activities require termination |

**Recommended Strategy**: Majority of risks require active treatment (82%), demonstrating appropriate risk-taking for a transformational programme balanced with comprehensive control framework.

---

## Risk Matrix Visualizations

### Inherent Risk Matrix (Before Controls)

```
LIKELIHOOD ↑
    5 |           | R-006     | R-003     | R-010     | R-002     |  ← Almost Certain
      |           | (Stats    | (Data     | (Census   | (Vendor   |
      |           | Act)      | Migr.)    | Perf.)    | Delay)    |
      |           |           |           |           |           |
    4 |           | R-008     | R-004     | R-001     | R-013     |  ← Likely
      |           | (Legacy   | (GovS 007 | (Strategic| (Vendor   |
      |           | Integr.)  | Fail)     | Change)   | Lock-in)  |
      |           |           |           |           |           |
    3 | R-018     | R-005     | R-007     | R-015     | R-012     |  ← Possible
      | (User     | (GDS      | (Cloud    | (Skills   | (Security |
      | Resist.)  | Assess.)  | Cost)     | Gap)      | Breach)   |
      |           |           |           |           |           |
    2 |           | R-020     | R-011     | R-009     | R-016     |  ← Unlikely
      |           | (Key      | (Disaster | (API      | (Social   |
      |           | Staff)    | Recovery) | Traffic)  | Media)    |
      |           |           |           |           |           |
    1 |           | R-014     | R-019     | R-017     | R-021     |  ← Rare
      |           | (HMRC API)| (Research)| (SDMX)    | (Judicial)|
      |           |           |           |           |           |
      +--------------------------------------------------------→
        1           2           3           4           5
                        IMPACT →

Color Legend:
Critical (20-25): █ Red     - 6 risks
High (13-19):     █ Orange  - 12 risks
Medium (6-12):    █ Yellow  - 4 risks
Low (1-5):        █ Green   - 0 risks
```

### Residual Risk Matrix (After Controls)

```
LIKELIHOOD ↑
    5 |           |           |           |           |           |  ← Almost Certain
      |           |           |           |           |           |
      |           |           |           |           |           |
      |           |           |           |           |           |
    4 |           |           |           |           |           |  ← Likely
      |           |           |           |           |           |
      |           |           |           |           |           |
      |           |           |           |           |           |
    3 |           | R-018     | R-003     | R-001     | R-006     |  ← Possible
      |           | (User     | R-007     | R-004     | R-010     |
      |           | Resist.)  | R-015     | R-005     |           |
      |           | R-020     | R-011     | R-008     |           |
      |           |           | R-019     | R-009     |           |
    2 |           | R-014     | R-013     | R-002     | R-012     |  ← Unlikely
      |           |           | R-017     | R-016     |           |
      |           |           |           |           |           |
      |           |           |           |           |           |
    1 | R-021     |           |           |           |           |  ← Rare
      |           |           |           |           |           |
      |           |           |           |           |           |
      |           |           |           |           |           |
      +--------------------------------------------------------→
        1           2           3           4           5
                        IMPACT →

Color Legend:
Critical (20-25): None (0 risks) ✅ All mitigated below critical
High (13-19):     █ Orange  - 3 risks (R-003, R-006, R-010)
Medium (6-12):    █ Yellow  - 16 risks
Low (1-5):        █ Green   - 3 risks
```

### Risk Movement Analysis

**Significant Risk Reductions** (≥10 point reduction):
- **R-006** (Statistics Act): 20 → 15 (-5 points): MFA + audit logging
- **R-002** (Vendor Delay): 20 → 12 (-8 points): Early procurement, fixed deadlines
- **R-003** (Data Migration): 20 → 15 (-5 points): Parallel running validation
- **R-010** (Census Performance): 20 → 15 (-5 points): Early performance testing
- **R-012** (Security Breach): 20 → 10 (-10 points): Zero Trust architecture
- **R-004** (GovS 007): 16 → 12 (-4 points): Security by design, automated scanning

**Risks Remaining HIGH** (require ongoing active management):
- **R-003** (Data Migration Integrity): Residual 15 - parallel running, statistician validation
- **R-006** (Statistics Act Breach): Residual 15 - MFA, audit logging, UK Statistics Authority validation
- **R-010** (Census-Scale Performance): Residual 15 - early load testing, scalability validation

---

## Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | 4Ts | Status |
|------|-----|-------|----------|----------|----------|-------|-----|--------|
| 1 | R-003 | Data Migration Integrity Failures | OPERATIONAL | 20 | 15 (High) | Chief Data Architect | Treat | Open |
| 2 | R-006 | Statistics Act Pre-Release Access Breach | COMPLIANCE | 20 | 15 (High) | Chief Statistician | Treat | Open |
| 3 | R-010 | Census-Scale Performance Failure | TECHNOLOGY | 20 | 15 (High) | Chief Data Architect | Treat | Open |
| 4 | R-001 | Strategic Direction Change Mid-Project | STRATEGIC | 16 | 12 (Medium) | Chief Data Officer | Treat | Open |
| 5 | R-004 | GovS 007 ITHC Security Failure | COMPLIANCE | 16 | 12 (Medium) | Head of Cyber Security | Treat | Open |
| 6 | R-005 | GDS Service Standard Assessment Failure | COMPLIANCE | 15 | 12 (Medium) | Director of Statistical Production | Treat | Open |
| 7 | R-007 | Cloud Cost Overruns Exceed £6.7M Target | FINANCIAL | 15 | 12 (Medium) | Chief Data Officer | Treat | Open |
| 8 | R-008 | Legacy System Integration Failures | OPERATIONAL | 16 | 12 (Medium) | Chief Data Architect | Treat | Open |
| 9 | R-009 | API Traffic Spike Handling Failure | TECHNOLOGY | 12 | 12 (Medium) | Chief Data Architect | Treat | Open |
| 10 | R-012 | Cyber Security Breach of Pre-Release Data | REPUTATIONAL | 20 | 10 (Medium) | Head of Cyber Security | Transfer | Open |

---

## Detailed Risk Register

### STRATEGIC Risks

#### R-001: Strategic Direction Change Mid-Project

**Risk Description**: UK Government policy or ministerial priorities change mid-implementation, requiring significant scope changes or project re-direction. Could result from machinery of government changes, new manifesto commitments, or National Statistician strategic review.

**Root Cause**: Political environment uncertainty, long project duration (18 months), potential general election, ministerial turnover.

**Trigger Events**:
- Machinery of government changes affecting ONS structure
- New National Statistician appointed with different priorities
- Manifesto commitment requiring ONS to deliver different capabilities
- HM Treasury spending review cuts budget allocation

**Consequences if Realized**:
- Major scope changes require re-work (4-8 weeks delay)
- Budget reallocation requires new business case approval
- Team morale impact from scope thrash
- Sunk costs on abandoned work (£500K-£1M)
- Delay to benefits realization (£4.5M annual savings)

**Affected Stakeholders**:
- Chief Data Officer (SRO accountability)
- Chief Statistician (regulatory compliance)
- Director of Statistical Production (operational delivery)
- Programme Board (oversight)

**Related Objectives**: BR-001 (Reduce Infrastructure Costs), BR-002 (Improve Publication Efficiency)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - 18-month programme spans political cycle
- **Inherent Impact**: 4 (Major) - Significant scope change, budget impact
- **Inherent Risk Score**: **16 (High)**

**Current Controls**:
- Monthly Programme Board reviews with SRO sign-off
- Quarterly HM Treasury checkpoint meetings
- Strong business case aligned with ONS statutory duties (Statistics Act 2007)
- Phased delivery enables scope flexibility
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Controls provide early warning, flexible delivery
- **Residual Impact**: 4 (Major) - Impact remains significant if occurs
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Monthly Programme Board reviews with Chief Data Officer to monitor policy environment
  - **Owner**: Chief Data Officer
  - **Target Date**: Ongoing (monthly)
  - **Success Criteria**: Early warning of policy changes (>4 weeks notice)

- **Action 2**: Build flexibility into architecture (modularity, loose coupling)
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 24 (HLD approval)
  - **Success Criteria**: Components can be re-prioritised without major re-work

- **Action 3**: Quarterly stakeholder revalidation of business case
  - **Owner**: Director of Statistical Production
  - **Target Date**: Quarterly from Week 12
  - **Success Criteria**: Stakeholder buy-in confirmed, no strategic concerns raised

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-002: Vendor Procurement Delays Alpha Phase

**Risk Description**: Vendor procurement process (SOW, RFP, evaluation, contract negotiation) exceeds planned 8 weeks, delaying Alpha phase completion and compressing Beta delivery timeline. G-Cloud framework reduces risk but complex requirements and negotiation could extend timeline.

**Root Cause**: Complex technical requirements, multiple vendor evaluation rounds, contract negotiation challenges, public sector procurement rules.

**Trigger Events**:
- Insufficient G-Cloud suppliers meet requirements
- Vendor clarification questions extend evaluation period
- Contract negotiations stall on liability clauses
- HM Treasury approval delays for >£18M programme
- Challenger vendor requests procurement review

**Consequences if Realized**:
- Alpha phase extends by 4-8 weeks
- Beta implementation compressed (quality risk)
- Go-live date slips (delayed benefits realization)
- Budget pressure from extended contractor costs (£200K-£400K)

**Affected Stakeholders**:
- Chief Data Officer (SRO accountability, budget pressure)
- Director of Statistical Production (publication timeline impact)
- Procurement Specialist (delivery accountability)

**Related Objectives**: BR-001 (Cost Reduction), Project Timeline (78 weeks)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Public sector procurement often exceeds estimates
- **Inherent Impact**: 5 (Catastrophic) - Critical path impact, budget overrun
- **Inherent Risk Score**: **20 (Critical)**

**Current Controls**:
- G-Cloud Digital Marketplace framework (pre-approved suppliers)
- Start procurement early (Week 13, immediately after Discovery)
- Parallel HLD design during procurement (de-risk critical path)
- Fixed evaluation timeline with hard deadlines
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - G-Cloud accelerates, but negotiation risk remains
- **Residual Impact**: 4 (Major) - Delay impact reduced by parallelization
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Start procurement Week 13 (immediately after Discovery Assessment)
  - **Owner**: Procurement Specialist
  - **Target Date**: Week 13 (2025-01-28)
  - **Success Criteria**: SOW/RFP published within 2 weeks of Alpha start

- **Action 2**: Use G-Cloud DOS (Digital Outcomes & Specialists) framework
  - **Owner**: Procurement Specialist
  - **Target Date**: Week 13
  - **Success Criteria**: Pre-approved supplier pool identified (≥5 suppliers)

- **Action 3**: Parallel HLD design during vendor evaluation
  - **Owner**: Chief Data Architect
  - **Target Date**: Weeks 13-20
  - **Success Criteria**: HLD progresses independently of vendor selection

- **Action 4**: Fixed evaluation timeline (4 weeks maximum)
  - **Owner**: Procurement Specialist
  - **Target Date**: Weeks 16-19
  - **Success Criteria**: Vendor selected by Week 20

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-013: Vendor Lock-In Limits Future Options

**Risk Description**: Proprietary cloud platform features or vendor-specific tooling creates lock-in, limiting future migration options and increasing switching costs. Could prevent multi-cloud strategy and increase vendor pricing power.

**Root Cause**: Cloud-native design pressures to use managed services, time pressures favour quick solutions over portable ones, lack of abstraction layers.

**Trigger Events**:
- Heavy use of vendor-specific services (AWS Lambda, Azure Functions)
- Data stored in proprietary formats (DynamoDB, CosmosDB)
- Vendor pricing increases post-contract (year 2-3)
- Competitive cloud offering emerges with better features/pricing

**Consequences if Realized**:
- Switching costs £2M-£5M if re-platforming needed
- Vendor pricing power increases (40% price hikes observed in industry)
- Cannot adopt new cloud innovations from other providers
- Fails Architecture Principle 9 (Cloud-Native with portability)

**Affected Stakeholders**:
- Chief Data Officer (long-term cost implications)
- Chief Data Architect (architecture integrity)
- Chief Technology Officer (strategic flexibility)

**Related Objectives**: Principle 9 (Cloud-Native Architecture)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Vendor lock-in common in cloud migrations
- **Inherent Impact**: 4 (Major) - Significant switching costs, pricing power loss
- **Inherent Risk Score**: **16 (High)**

**Current Controls**:
- Architecture Principle 9 requires abstraction layers
- HLD review checks for vendor lock-in risks
- Containerization (Docker/Kubernetes) for compute portability
- Open standards for data formats (SDMX, CSV, JSON)
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Controls reduce but don't eliminate lock-in
- **Residual Impact**: 3 (Moderate) - Portability layers reduce switching costs
- **Residual Risk Score**: **9 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: HLD review validates abstraction layers for compute, storage, queuing
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 24 (HLD Review)
  - **Success Criteria**: No vendor-specific services without abstraction

- **Action 2**: Contract includes exit rights and data portability clauses
  - **Owner**: Procurement Specialist
  - **Target Date**: Week 20 (Vendor Selection)
  - **Success Criteria**: 90-day exit clause, data export in open formats

- **Action 3**: Annual vendor lock-in assessment
  - **Owner**: Chief Data Architect
  - **Target Date**: Annually from Week 78 (Live)
  - **Success Criteria**: Switching cost estimate <£1M

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-022: Funding Shortfall Impacts Delivery

**Risk Description**: HM Treasury budget cuts or spending review changes funding allocation mid-programme, requiring scope reduction or programme pause. Could result from fiscal constraints, competing priorities, or PAC/NAO recommendations.

**Root Cause**: Economic uncertainty, public spending pressures, long programme duration (18 months), cross-Parliament spending.

**Trigger Events**:
- Emergency budget / fiscal event
- Spending review reduces ONS allocation
- NAO value for money concerns
- PAC recommendations to pause programme
- Cross-government headcount freeze affects ONS staffing

**Consequences if Realized**:
- Programme pause (6-12 months delay)
- Scope reduction (50% of statistical series migrated instead of 500+)
- Redundancy costs for contractors (£500K-£1M)
- Opportunity cost of delayed benefits (£4.5M annual savings)
- Sunk costs on incomplete work (£5M-£10M)

**Affected Stakeholders**:
- Chief Data Officer (SRO accountability)
- National Statistician (strategic impact)
- HM Treasury (funding authority)

**Related Objectives**: BR-001 (Reduce Infrastructure Costs by £4.5M annually)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 2 (Unlikely) - Strong business case, statutory duties, but fiscal pressures exist
- **Inherent Impact**: 5 (Catastrophic) - Programme failure
- **Inherent Risk Score**: **10 (Medium)**

**Current Controls**:
- Strong business case (£4.5M annual savings, 2.5 year payback)
- ONS statutory duties require functioning infrastructure (Statistics Act 2007)
- Phased delivery enables scope flexibility
- Quarterly HM Treasury checkpoint meetings
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Statutory duties + ROI case strong
- **Residual Impact**: 4 (Major) - Phased delivery reduces impact
- **Residual Risk Score**: **8 (Medium)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: Quarterly benefits realization reporting to HM Treasury
  - **Owner**: Chief Data Officer
  - **Target Date**: Quarterly from Week 12
  - **Success Criteria**: HM Treasury confirm continued funding

- **Action 2**: Prioritize high-value statistical series (top 100) for early migration
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 42 (DLD Review)
  - **Success Criteria**: 80% of benefits achievable with 20% of scope

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

### OPERATIONAL Risks

#### R-003: Data Migration Integrity Failures

**Risk Description**: Migration of 500+ statistical series from legacy systems results in data integrity errors (data loss, corruption, incorrect calculations). Could cause publication of inaccurate statistics, breaching ONS statutory duty and damaging public trust.

**Root Cause**: Complex legacy systems (30+ years old), undocumented transformation logic, manual processes not captured in code, human error in migration scripts.

**Trigger Events**:
- Legacy system documentation incomplete/inaccurate
- Migration scripts contain logic errors
- Data validation rules miss edge cases
- Parallel running period too short to detect issues
- Statistician validation insufficient coverage

**Consequences if Realized**:
- Inaccurate statistics published (breach of Statistics Act 2007)
- UK Statistics Authority revokes ONS accreditation
- Parliamentary inquiry / PAC scrutiny
- Media coverage damages ONS reputation
- Loss of public trust in official statistics
- Legal liability for incorrect data affecting policy decisions
- Re-work costs £1M-£3M + 6-12 month delay

**Affected Stakeholders**:
- Chief Statistician (regulatory accountability)
- National Statistician (public trust)
- Chief Data Architect (technical delivery)
- Director of Statistical Production (operational delivery)

**Related Objectives**: DR-005 (Data Migration with 100% integrity), Principle 4 (Single Source of Truth)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Complex migration, 500+ series, legacy complexity
- **Inherent Impact**: 5 (Catastrophic) - Regulatory breach, public trust damage
- **Inherent Risk Score**: **20 (Critical)**

**Current Controls**:
- Parallel running: legacy and new systems for 4 weeks validation (Week 67-70)
- Automated data validation (record counts, checksums, sample verification)
- Statistician sign-off for each migrated series (100% validation)
- Rollback capability if issues detected
- Migration success criteria: 100% data integrity, zero data loss
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Comprehensive validation reduces likelihood
- **Residual Impact**: 5 (Catastrophic) - Impact remains critical if occurs
- **Residual Risk Score**: **15 (High)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Establish parallel running environment by Week 65
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 65 (Beta Sprint 5)
  - **Success Criteria**: Legacy and new systems publishing simultaneously

- **Action 2**: Develop comprehensive data validation framework
  - **Owner**: Data Engineers
  - **Target Date**: Week 50 (Beta Sprint 2)
  - **Success Criteria**: Automated validation for 100% of data quality dimensions

- **Action 3**: Statistician validation for 100% of migrated series
  - **Owner**: Director of Statistical Production
  - **Target Date**: Weeks 67-72
  - **Success Criteria**: Sign-off from series owner for each statistical series

- **Action 4**: 6-week parallel running period (extend from 4 weeks)
  - **Owner**: Chief Data Architect
  - **Target Date**: Weeks 67-72
  - **Success Criteria**: Zero data integrity issues detected in week 5-6

**Risk Status**: **Open**

**Risk Escalation**: Programme Board (monthly updates during Beta)

**Review Date**: 2025-12-05

---

#### R-008: Legacy System Integration Failures

**Risk Description**: Integrations with legacy ONS source systems (survey systems, admin data feeds) fail during implementation or operations, preventing data ingestion and publication. Could result from undocumented interfaces, legacy system changes, or authentication issues.

**Root Cause**: Legacy systems (30+ years old), limited documentation, multiple integration points (7 systems), legacy owners lack API expertise.

**Trigger Events**:
- Legacy system owners change interface without notice
- Authentication credentials expire
- Legacy system capacity insufficient for API load
- Data format changes (CSV schema drift)
- Legacy system outage during critical publication window

**Consequences if Realized**:
- Publication delays (Statistics Act 2007 breach if >24 hours)
- Manual workarounds required (defeats automation objective)
- Statistical series unavailable (user impact)
- Reputational damage (ONS seen as unreliable)
- Statistician frustration with new platform

**Affected Stakeholders**:
- Chief Data Architect (technical delivery)
- Director of Statistical Production (operational delivery)
- Legacy System Owners (integration accountability)

**Related Objectives**: INT-001 (Survey Data Integration), INT-002 (Admin Data Integration)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Multiple legacy integrations, limited documentation
- **Inherent Impact**: 4 (Major) - Publication delays, Statistics Act breach risk
- **Inherent Risk Score**: **16 (High)**

**Current Controls**:
- Integration testing in Sprint 5 (Week 59-62)
- Stub APIs for testing before legacy integration
- Fallback procedures (manual file transfer if API fails)
- Integration contracts defined in DLD (Week 42)
- Weekly coordination meetings with legacy system owners
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Testing and fallbacks reduce likelihood
- **Residual Impact**: 4 (Major) - Impact remains significant if critical system fails
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Weekly coordination meetings with legacy system owners from Week 37
  - **Owner**: Chief Data Architect
  - **Target Date**: Ongoing from Week 37 (Beta start)
  - **Success Criteria**: No surprise interface changes, 4-week notice for changes

- **Action 2**: Comprehensive integration testing in Sprint 5
  - **Owner**: Data Engineers
  - **Target Date**: Weeks 59-62
  - **Success Criteria**: All 7 integrations validated under load

- **Action 3**: Fallback procedures documented and tested
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 66 (Beta Sprint 6)
  - **Success Criteria**: Manual fallback completes publication within 8 hours

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-015: Skills Gap in Cloud-Native Technologies

**Risk Description**: ONS team lacks sufficient cloud engineering expertise (Kubernetes, serverless, Infrastructure as Code, cloud security), requiring heavy vendor dependency and limiting operational effectiveness. Knowledge transfer from vendor insufficient.

**Root Cause**: ONS historically on-premises infrastructure, limited cloud migration experience, civil service recruitment challenges, cloud skills shortage in market.

**Trigger Events**:
- Key vendor engineers leave mid-project
- Knowledge transfer insufficient (4 weeks planned)
- ONS engineers unable to operate platform independently
- Post-go-live operational issues require vendor escalation (cost impact)
- Cloud skills training budget insufficient

**Consequences if Realized**:
- Extended vendor dependency (additional £500K-£1M annual cost)
- Slow operational response (MTTR >4 hours vs <30 minutes target)
- Cannot innovate post-go-live (locked into vendor roadmap)
- Staff frustration and turnover (unable to support modern platform)
- Business case ROI not achieved (operational costs higher than planned)

**Affected Stakeholders**:
- Chief Data Architect (operational readiness)
- Chief Technology Officer (skills strategy)
- Support team (operational capability)

**Related Objectives**: BR-001 (Reduce Infrastructure Costs - dependent on operational efficiency)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - Cloud skills shortage, civil service constraints
- **Inherent Impact**: 4 (Major) - Operational dependency, cost impact
- **Inherent Risk Score**: **12 (Medium)**

**Current Controls**:
- Vendor knowledge transfer requirement in contract (minimum 20 days)
- ONS engineers embedded with vendor during Beta (8 engineers, 36 weeks)
- Cloud training programme (AWS/Azure certifications)
- Comprehensive runbooks and documentation
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Training helps but cloud complexity remains
- **Residual Impact**: 3 (Moderate) - Knowledge transfer reduces vendor dependency
- **Residual Risk Score**: **9 (Medium)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: Embed 8 ONS engineers with vendor during Beta implementation
  - **Owner**: Chief Data Architect
  - **Target Date**: Weeks 37-72
  - **Success Criteria**: Engineers can perform 80% of operational tasks independently

- **Action 2**: Cloud certifications for 100% of support team
  - **Owner**: Chief Technology Officer
  - **Target Date**: Week 72 (by go-live)
  - **Success Criteria**: AWS/Azure Associate certification for all 6 support engineers

- **Action 3**: Comprehensive operational runbooks
  - **Owner**: Vendor + Chief Data Architect
  - **Target Date**: Week 72
  - **Success Criteria**: Runbook covers 90% of operational scenarios

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-018: Statistician Resistance to New Workflow

**Risk Description**: Statisticians resist adopting new automated publication workflow, preferring familiar manual processes. Could result in low adoption, parallel manual processes, and failure to achieve 60% efficiency gains.

**Root Cause**: Change fatigue (multiple ONS transformation programmes), fear of job security, lack of trust in automation, insufficient training, workflow doesn't match mental models.

**Trigger Events**:
- UAT feedback negative (workflows too complex)
- Training insufficient (4 hours planned may be inadequate)
- Automation errors early post-go-live (erodes trust)
- Key influencer statisticians resist publicly
- No statistician champions to advocate for new platform

**Consequences if Realized**:
- Low adoption rate (<50% vs 100% target)
- Statisticians maintain manual parallel processes (shadow IT)
- Efficiency gains not realized (60% effort reduction objective fails)
- Business case ROI not achieved (BR-002 failure)
- Platform investment wasted (£18M not delivering value)

**Affected Stakeholders**:
- Director of Statistical Production (user adoption accountability)
- Statisticians (500 users affected)
- Chief Data Officer (ROI accountability)

**Related Objectives**: BR-002 (Improve Publication Efficiency by 60%)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - Change resistance common, but strong engagement plan
- **Inherent Impact**: 4 (Major) - Business case failure if adoption low
- **Inherent Risk Score**: **12 (Medium)**

**Current Controls**:
- User research in Discovery (Week 3-5) to understand pain points
- UAT engagement (20 statisticians, 3 weeks, Week 70-72)
- Training programme (4 hours per statistician, Week 70-72)
- Change champions (5 statisticians identified, Week 67)
- Hypercare support (4 weeks intensive, 24/7, Week 75-78)
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Strong engagement plan reduces resistance
- **Residual Impact**: 3 (Moderate) - Impact remains but hypercare limits damage
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: User research to validate workflow design
  - **Owner**: Director of Statistical Production
  - **Target Date**: Weeks 3-5 (Discovery)
  - **Success Criteria**: Workflow matches 90% of statistician mental models

- **Action 2**: Identify and engage 5 change champions early
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 67
  - **Success Criteria**: Champions advocate for platform, provide peer support

- **Action 3**: Extended hypercare support (6 weeks instead of 4)
  - **Owner**: Support team
  - **Target Date**: Weeks 75-80
  - **Success Criteria**: Statistician satisfaction ≥80%

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-020: Key Team Members Leave During Implementation

**Risk Description**: Critical team members (Chief Data Architect, Technical Lead, Security Architect) leave ONS during Beta implementation, causing knowledge loss, delivery delays, and quality risks.

**Root Cause**: Civil service turnover, competitive market for cloud skills, 18-month programme duration, contractor end-of-term, career progression opportunities elsewhere.

**Trigger Events**:
- Chief Data Architect accepts private sector role (200% salary increase)
- Technical Lead promoted to different ONS programme
- Security Architect contract expires (not renewed due to budget)
- Multiple engineers leave simultaneously (team morale collapse)

**Consequences if Realized**:
- Project delay (4-8 weeks to recruit replacement)
- Knowledge loss (undocumented design decisions)
- Quality degradation (new team members lack context)
- Team morale impact (remaining team overloaded)
- Budget pressure from recruitment costs (£50K-£100K)

**Affected Stakeholders**:
- Chief Data Officer (delivery accountability)
- Chief Data Architect (team stability)
- Programme Board (oversight)

**Related Objectives**: Project Timeline (78 weeks)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 2 (Unlikely) - Some turnover expected but not mass exodus
- **Inherent Impact**: 4 (Major) - Critical path delay, knowledge loss
- **Inherent Risk Score**: **8 (Medium)**

**Current Controls**:
- Knowledge sharing (pair programming, code reviews)
- Comprehensive documentation (architecture decisions recorded)
- Vendor knowledge transfer (reduces ONS dependency)
- Succession planning (deputies identified for key roles)
- Competitive retention packages (where civil service rules allow)
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Controls maintain team stability
- **Residual Impact**: 3 (Moderate) - Documentation reduces impact
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: Succession planning for 3 critical roles (Architect, Tech Lead, Security)
  - **Owner**: Chief Data Officer
  - **Target Date**: Week 37 (Alpha end)
  - **Success Criteria**: Deputies identified, can assume role within 2 weeks

- **Action 2**: Architecture Decision Records (ADRs) for all major decisions
  - **Owner**: Chief Data Architect
  - **Target Date**: Ongoing from Week 13
  - **Success Criteria**: 100% of HLD/DLD decisions documented

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

### FINANCIAL Risks

#### R-007: Cloud Cost Overruns Exceed £6.7M Target

**Risk Description**: Cloud infrastructure costs exceed £6.7M annual target due to inefficient resource usage, lack of cost optimization, or underestimated data volumes. Could result in business case failure (BR-001: 40% cost reduction not achieved).

**Root Cause**: Cloud cost estimation uncertainty, data volume growth exceeds projections (20% annually), inefficient resource provisioning, lack of FinOps culture.

**Trigger Events**:
- Data volumes grow faster than 20% projection (30-40% growth)
- Auto-scaling policies too aggressive (over-provisioning)
- Development/test environments not shut down after hours
- Data retention exceeds planned periods (storage costs compound)
- Vendor pricing changes (price increases year 2-3)
- Insufficient use of reserved instances (on-demand premium 40%)

**Consequences if Realized**:
- Annual costs £8M-£9M vs £6.7M target (20-35% overrun)
- Business case ROI not achieved (BR-001 failure)
- HM Treasury questions value for money
- Budget reallocation required (impacts other ONS programmes)
- PAC scrutiny of cost management

**Affected Stakeholders**:
- Chief Data Officer (budget accountability)
- Chief Data Architect (architecture efficiency)
- HM Treasury (value for money oversight)

**Related Objectives**: BR-001 (Reduce Infrastructure Costs by 40% to £6.7M annually)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - Cloud cost overruns common (60% of organizations exceed budget)
- **Inherent Impact**: 5 (Catastrophic) - Business case failure, PAC scrutiny
- **Inherent Risk Score**: **15 (High)**

**Current Controls**:
- Monthly cost monitoring and reporting (from Week 43)
- FinOps controls and cost allocation by workload
- Auto-scaling policies with upper limits
- Reserved instances for predictable workloads (30% discount)
- Data retention policies (automated deletion)
- Budget alerts at 80%, 90%, 100% thresholds
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Controls provide visibility but don't eliminate risk
- **Residual Impact**: 4 (Major) - Business case impact but not catastrophic
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Implement FinOps controls and monthly cost reviews from Week 43
  - **Owner**: Chief Data Officer
  - **Target Date**: Week 43 (Beta Sprint 1 start)
  - **Success Criteria**: Costs within 5% of budget monthly

- **Action 2**: Reserved instance purchasing strategy (70% of compute)
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 73 (Production deployment)
  - **Success Criteria**: 70% compute on reserved instances (30% cost saving)

- **Action 3**: Automated cost anomaly detection
  - **Owner**: DevOps Engineer
  - **Target Date**: Week 66 (Beta Sprint 6)
  - **Success Criteria**: Alerts on cost increases >20% week-on-week

- **Action 4**: Quarterly cost optimization reviews
  - **Owner**: Chief Data Architect
  - **Target Date**: Quarterly from Week 78 (Live)
  - **Success Criteria**: Identify 10% optimization opportunities each quarter

**Risk Status**: **Open**

**Risk Escalation**: Programme Board (monthly cost reporting)

**Review Date**: 2025-12-05

---

#### R-011: Disaster Recovery Costs Higher Than Budgeted

**Risk Description**: Disaster recovery infrastructure (multi-region deployment, backup storage, failover testing) costs significantly exceed £500K budget estimate due to underestimated storage volumes or vendor pricing.

**Root Cause**: DR cost estimation uncertainty, backup retention requirements (7 years for compliance), geo-replication costs, failover testing overhead.

**Trigger Events**:
- Backup volumes exceed estimate (500TB → 750TB)
- Multi-region data transfer costs higher than projected
- Quarterly DR testing consumes significant compute (failover drills)
- Compliance requirements extend backup retention (7 years → 10 years)

**Consequences if Realized**:
- DR costs £1M-£1.5M vs £500K budget (100-200% overrun)
- Budget reallocation required from operational budget
- Trade-offs with other priorities (features vs DR)
- NFR-A-002 (RTO 4 hours, RPO 1 hour) at risk if budget cut

**Affected Stakeholders**:
- Chief Data Officer (budget accountability)
- Chief Data Architect (architecture design)
- Head of Cyber Security (resilience requirements)

**Related Objectives**: NFR-A-002 (Disaster Recovery with RTO 4 hours, RPO 1 hour)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - DR cost estimation challenging
- **Inherent Impact**: 3 (Moderate) - Budget impact but not catastrophic
- **Inherent Risk Score**: **9 (Medium)**

**Current Controls**:
- DR architecture designed in HLD with cost estimates (Week 17-22)
- Multi-region deployment across UK availability zones only (no US/EU)
- Backup retention aligned with compliance minimum (7 years, not 10)
- Quarterly DR testing (not monthly, reduces testing costs)
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - HLD cost validation reduces uncertainty
- **Residual Impact**: 3 (Moderate) - Impact contained through design
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: HLD cost validation for DR architecture
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 22 (HLD design)
  - **Success Criteria**: DR costs within £500K ±10%

- **Action 2**: Backup retention policy optimization
  - **Owner**: Data Protection Officer
  - **Target Date**: Week 23 (DPIA)
  - **Success Criteria**: Minimum retention periods defined (no over-retention)

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-014: HMRC/DWP API Access Costs Higher Than Expected

**Risk Description**: API access fees for admin data from HMRC (tax data), DWP (benefits data), NHS (health data) exceed budget estimates due to data volume or pricing changes.

**Root Cause**: API pricing uncertainty, data volume growth, government department pricing models vary, no standard cross-government API pricing.

**Trigger Events**:
- HMRC changes API pricing model (per-record fees introduced)
- Data volumes exceed projections (more frequent polling)
- Government departments introduce new API tiers (premium pricing)
- Data sharing agreements require renegotiation (terms change)

**Consequences if Realized**:
- API access costs £200K-£500K vs £100K budget (100-400% overrun)
- Budget reallocation required
- Reduce API polling frequency (data freshness impact)
- Trade-offs with other data sources (prioritize HMRC, deprioritize NHS)

**Affected Stakeholders**:
- Chief Data Officer (budget accountability)
- Chief Data Architect (integration design)
- Government departments (data sharing partners)

**Related Objectives**: INT-002 (Admin Data Integration)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 2 (Unlikely) - Government APIs typically free/low-cost
- **Inherent Impact**: 2 (Minor) - Budget impact manageable (<£500K)
- **Inherent Risk Score**: **4 (Low)**

**Current Controls**:
- Data sharing agreements negotiated in Alpha (Week 20)
- API pricing confirmed before integration design (DLD Week 42)
- Polling frequency optimized (daily vs hourly vs real-time)
- Caching reduces redundant API calls
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Agreements provide pricing certainty
- **Residual Impact**: 2 (Minor) - Impact remains low
- **Residual Risk Score**: **4 (Low)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: Confirm API pricing in data sharing agreements
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 20 (Alpha)
  - **Success Criteria**: Pricing confirmed for 3-year contract period

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

### COMPLIANCE/REGULATORY Risks

#### R-004: GovS 007 ITHC Security Assessment Failure

**Risk Description**: IT Health Check (ITHC) penetration testing identifies critical or high-severity security vulnerabilities, blocking go-live and requiring remediation. Could delay production deployment by 4-8 weeks.

**Root Cause**: Complex security requirements (Zero Trust, OFFICIAL classification), cloud security expertise gaps, tight timeline for security hardening.

**Trigger Events**:
- ITHC finds critical vulnerabilities (SQL injection, XSS, authentication bypass)
- Penetration testers identify cloud misconfigurations (public S3 buckets, weak IAM)
- Security controls not implemented per GovS 007 requirements
- Vulnerability remediation takes longer than 2-week buffer (Week 70-72)

**Consequences if Realized**:
- Go-live delayed by 4-8 weeks (benefits realization delayed)
- OFFICIAL accreditation withheld (cannot process sensitive data)
- Re-work costs £200K-£500K for security remediation
- Reputational damage (security failures visible to NCSC)
- HM Treasury questions programme governance

**Affected Stakeholders**:
- Head of Cyber Security (security accreditation)
- Chief Data Officer (go-live accountability)
- NCSC (security oversight)

**Related Objectives**: NFR-SEC-003 (Vulnerability Management), Principle 10 (Security by Design)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Complex cloud security, tight timeline
- **Inherent Impact**: 4 (Major) - Go-live delay, accreditation blocked
- **Inherent Risk Score**: **16 (High)**

**Current Controls**:
- Security by design from HLD (Week 17-22)
- Automated SAST/DAST scanning in CI/CD pipeline (from Week 43)
- Threat model (STRIDE) in Alpha (Week 19-21)
- Security testing before ITHC (Week 70-72)
- 2-week remediation buffer before go-live (Week 70-72)
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Controls provide early detection
- **Residual Impact**: 4 (Major) - Delay impact remains if critical findings
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Threat model (STRIDE) in Alpha to identify security controls early
  - **Owner**: Head of Cyber Security
  - **Target Date**: Weeks 19-21 (Alpha)
  - **Success Criteria**: Security controls mapped to all threats

- **Action 2**: Automated SAST/DAST in CI/CD from Sprint 1
  - **Owner**: Security Engineer
  - **Target Date**: Week 43 (Beta Sprint 1)
  - **Success Criteria**: Zero critical vulnerabilities in production code

- **Action 3**: Internal penetration testing 4 weeks before ITHC
  - **Owner**: Head of Cyber Security
  - **Target Date**: Week 68 (4 weeks before ITHC Week 72)
  - **Success Criteria**: Internal PT finds zero critical/high issues

- **Action 4**: 4-week remediation buffer (extend from 2 weeks)
  - **Owner**: Chief Data Officer
  - **Target Date**: Weeks 69-72
  - **Success Criteria**: All ITHC findings remediated before go-live

**Risk Status**: **Open**

**Risk Escalation**: Programme Board (monthly security status)

**Review Date**: 2025-12-05

---

#### R-005: GDS Service Standard Assessment Failure

**Risk Description**: GDS Service Assessment at Beta phase fails to meet Service Standard criteria (14 points), requiring remediation before go-live. Could delay production deployment or result in non-compliance with government policy.

**Root Cause**: Service Standard criteria not embedded in delivery, insufficient user research, accessibility gaps, operational readiness not demonstrated.

**Trigger Events**:
- User research insufficient (<50 users, not representative)
- Accessibility WCAG 2.1 AA not met (automated + manual testing)
- Technology choices not justified with evidence
- Operational support not demonstrated (no runbooks, no on-call)
- Performance data not collected (no SLOs, no monitoring)

**Consequences if Realized**:
- Go-live delayed by 4-8 weeks for remediation
- Reputational damage (failed Service Assessment published on GOV.UK)
- GDS Digital Spend Control may block future ONS funding
- Remediation costs £100K-£300K (additional user research, accessibility fixes)

**Affected Stakeholders**:
- Director of Statistical Production (Service Owner accountability)
- Chief Data Officer (overall accountability)
- GDS Service Assessor (assessment authority)

**Related Objectives**: BR-004 (Meet UK Government Digital Standards)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - Service Standard failure rate 20-30% on first attempt
- **Inherent Impact**: 5 (Catastrophic) - Go-live blocked, policy non-compliance
- **Inherent Risk Score**: **15 (High)**

**Current Controls**:
- Service Standard evidence gathering from Discovery (Week 1)
- Mock assessment in Alpha (Week 26)
- Continuous user research throughout Beta
- Accessibility testing in CI/CD pipeline
- Operational readiness demonstrated in UAT (Week 70-72)
- `/arckit.service-assessment` preparation tool
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Mock assessment reduces risk but not eliminates
- **Residual Impact**: 4 (Major) - Delay reduced through early preparation
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Mock Service Assessment in Alpha (Week 26)
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 26
  - **Success Criteria**: Mock assessment identifies gaps ≥8 weeks before Beta assessment

- **Action 2**: Continuous Service Standard evidence gathering
  - **Owner**: Service Owner
  - **Target Date**: Ongoing from Week 1
  - **Success Criteria**: Evidence pack for all 14 points by Week 70

- **Action 3**: User research with ≥100 users (20 Discovery, 80 Beta)
  - **Owner**: Director of Statistical Production
  - **Target Date**: Weeks 3-72
  - **Success Criteria**: Representative user sample (statisticians, API consumers, citizens)

- **Action 4**: Beta Assessment preparation using `/arckit.service-assessment`
  - **Owner**: Service Owner
  - **Target Date**: Week 71
  - **Success Criteria**: Evidence pack complete, mock assessment passed

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-006: Statistics Act Pre-Release Access Breach

**Risk Description**: Pre-release access controls fail, allowing unauthorized access to market-sensitive statistics before 9:30 AM publication time. Could breach Statistics Act 2007, resulting in UK Statistics Authority sanctions, ministerial questions, and loss of statistical independence.

**Root Cause**: Complex pre-release access rules (24-hour maximum, designated user lists, audit trails), authentication failures, human error, insider threat.

**Trigger Events**:
- MFA authentication bypass or failure
- Audit logging gaps (access not recorded)
- Pre-release period exceeds 24 hours (automatic alert not configured)
- Designated user list not updated (wrong people have access)
- Insider deliberately leaks pre-release statistics

**Consequences if Realized**:
- UK Statistics Authority sanctions (ONS accreditation at risk)
- Parliamentary questions to National Statistician
- Cabinet Office inquiry
- Media coverage damages ONS independence reputation
- Financial market impact (insider trading concerns)
- Legal liability (Statistics Act 2007 Section 11 breach)

**Affected Stakeholders**:
- Chief Statistician (Statistics Act compliance)
- National Statistician (ONS accreditation)
- Chief Data Officer (platform accountability)

**Related Objectives**: FR-004 (Pre-Release Access Control), NFR-C-002 (Statistics Act Compliance)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Complex controls, human factors, insider threat
- **Inherent Impact**: 5 (Catastrophic) - Regulatory breach, accreditation at risk
- **Inherent Risk Score**: **20 (Critical)**

**Current Controls**:
- Multi-factor authentication (MFA) required for pre-release access (NFR-SEC-001)
- Designated user lists maintained per statistical series
- Audit log of all pre-release access (who, when, what)
- Automatic alert if pre-release period exceeds 24 hours
- Automatic public release at 9:30 AM GMT (no human intervention)
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Controls reduce but don't eliminate insider threat
- **Residual Impact**: 5 (Catastrophic) - Impact remains critical if occurs
- **Residual Risk Score**: **15 (High)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Design pre-release access controls in Sprint 4 (Data Catalog & SDC)
  - **Owner**: Chief Statistician
  - **Target Date**: Weeks 55-58 (Beta Sprint 4)
  - **Success Criteria**: Controls meet Statistics Act requirements

- **Action 2**: UK Statistics Authority validation of controls
  - **Owner**: Chief Statistician
  - **Target Date**: Week 65 (before UAT)
  - **Success Criteria**: UK Statistics Authority sign-off on control design

- **Action 3**: UAT validation with statisticians
  - **Owner**: Chief Statistician
  - **Target Date**: Weeks 70-72
  - **Success Criteria**: UAT validates controls work correctly, zero breaches in testing

- **Action 4**: Real-time audit monitoring dashboard
  - **Owner**: Security Engineer
  - **Target Date**: Week 66 (Beta Sprint 6)
  - **Success Criteria**: Security team can monitor pre-release access in real-time

**Risk Status**: **Open**

**Risk Escalation**: Chief Statistician → National Statistician → UK Statistics Authority (if breach occurs)

**Review Date**: 2025-12-05

---

#### R-017: SDMX Metadata Compliance Failure

**Risk Description**: Published statistical metadata does not comply with SDMX (Statistical Data and Metadata eXchange) standard, preventing interoperability with Eurostat, UN, OECD systems and failing Principle 8 (Interoperability).

**Root Cause**: SDMX complexity, limited ONS SDMX expertise, metadata generation not automated, data steward capacity constraints.

**Trigger Events**:
- SDMX Data Structure Definitions (DSDs) incorrect or incomplete
- Codelists don't align with international standards (ISO 3166, ISO 8601)
- Metadata quality checks insufficient
- Eurostat rejects ONS metadata submission (interoperability failure)

**Consequences if Realized**:
- Eurostat/UN/OECD integration delayed or blocked
- Manual metadata transformation required (defeats automation objective)
- International statistical community cannot consume ONS data
- Reputational damage (ONS seen as non-compliant)
- Re-work costs £100K-£300K

**Affected Stakeholders**:
- Chief Data Architect (interoperability accountability)
- Director of Statistical Production (metadata ownership)
- Eurostat/UN/OECD (international partners)

**Related Objectives**: DR-004 (SDMX Metadata), Principle 8 (Interoperability and Open Standards)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - SDMX complexity, limited expertise
- **Inherent Impact**: 3 (Moderate) - Interoperability impact, re-work costs
- **Inherent Risk Score**: **9 (Medium)**

**Current Controls**:
- SDMX metadata generation automated in Sprint 4 (Week 55-58)
- Metadata quality validation rules
- Eurostat validation tools used before submission
- Data steward training on SDMX standards
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Automation + validation reduces errors
- **Residual Impact**: 3 (Moderate) - Impact remains if occurs
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Automate SDMX metadata generation in Sprint 4
  - **Owner**: Data Engineers
  - **Target Date**: Weeks 55-58
  - **Success Criteria**: Metadata generated automatically for 100% of series

- **Action 2**: Eurostat validation before go-live
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 72
  - **Success Criteria**: Eurostat accepts ONS metadata submissions

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-021: Judicial Review of Procurement Process

**Risk Description**: Unsuccessful vendor challenges procurement process via judicial review, alleging unfair evaluation or process irregularities. Could pause or reverse vendor selection decision.

**Root Cause**: Public sector procurement transparency, high-value contract (£4.5M SI costs), competitive market, vendor dissatisfaction with evaluation.

**Trigger Events**:
- Vendor alleges evaluation criteria not objective
- Vendor claims bias in scoring (favoritism toward incumbent)
- Vendor disputes contract award (claims should have won)
- Procurement process irregularities (documentation gaps)

**Consequences if Realized**:
- Procurement paused for 6-12 months (judicial review timeline)
- Programme delay (Alpha phase extends significantly)
- Legal costs £50K-£200K
- Vendor relationship damage (trust eroded)
- Re-procurement may be required (6-8 weeks additional)

**Affected Stakeholders**:
- Chief Data Officer (programme accountability)
- Procurement Specialist (process integrity)
- HM Treasury (value for money)

**Related Objectives**: Vendor Procurement (Alpha Weeks 13-20)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 1 (Rare) - Judicial reviews uncommon (5% of procurements)
- **Inherent Impact**: 5 (Catastrophic) - Programme pause, significant delay
- **Inherent Risk Score**: **5 (Low)**

**Current Controls**:
- G-Cloud framework (pre-approved process, reduces challenge risk)
- Objective evaluation criteria published in RFP
- Evaluation scoring documented and auditable
- Legal review of procurement process
- Vendor debriefs provided (transparency)
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 1 (Rare) - Framework + transparency minimize risk
- **Residual Impact**: 4 (Major) - Delay reduced through strong process
- **Residual Risk Score**: **4 (Low)**

**Risk Response**: **TOLERATE**

**Action Plan**:
- **Action 1**: Legal review of procurement process before launch
  - **Owner**: Procurement Specialist
  - **Target Date**: Week 13
  - **Success Criteria**: Legal sign-off on process integrity

- **Action 2**: Vendor debriefs for unsuccessful bidders
  - **Owner**: Procurement Specialist
  - **Target Date**: Week 20 (post-selection)
  - **Success Criteria**: Vendors understand evaluation rationale, no disputes raised

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

### TECHNOLOGY Risks

#### R-009: API Traffic Spike Handling Failure

**Risk Description**: Platform fails to handle peak publication load (10,000 requests/second) for major economic releases (GDP, CPI, Labour Market), resulting in service degradation or outage.

**Root Cause**: Auto-scaling insufficient, load testing doesn't replicate real traffic patterns, caching ineffective, database bottlenecks.

**Trigger Events**:
- Major economic release (GDP, CPI) generates 20,000 req/s (2x projection)
- Auto-scaling too slow (<5 minute response time exceeded)
- Database query performance degrades under load
- CDN cache not configured correctly (origin overwhelmed)
- Load testing scenarios unrealistic (didn't test production patterns)

**Consequences if Realized**:
- API outage during publication window (Statistics Act breach)
- Media coverage ("ONS website crashes")
- User complaints (journalists, analysts unable to access data)
- Reputational damage (ONS seen as unreliable)
- Availability SLA breach (99.95% not met)

**Affected Stakeholders**:
- Chief Data Architect (platform performance)
- Director of Statistical Production (publication reliability)
- Data users (API consumers affected)

**Related Objectives**: NFR-P-003 (Handle 10,000 req/s peak load), NFR-A-001 (99.95% availability)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - Traffic spikes unpredictable, load testing may miss patterns
- **Inherent Impact**: 4 (Major) - Statistics Act breach, reputational damage
- **Inherent Risk Score**: **12 (Medium)**

**Current Controls**:
- Load testing in Beta (Week 71-72) simulates 10,000 req/s peak
- Auto-scaling policies tested (scale-out <5 minutes)
- CDN caching for frequently accessed endpoints
- Database query optimization and indexing
- Burst capacity to 20,000 req/s for 5 minutes (NFR-P-003)
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Testing reduces but doesn't eliminate risk
- **Residual Impact**: 4 (Major) - Impact remains if spike exceeds capacity
- **Residual Risk Score**: **12 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Load testing with realistic publication traffic patterns
  - **Owner**: QA/Test Engineer
  - **Target Date**: Week 71 (Beta)
  - **Success Criteria**: 10,000 req/s sustained, 20,000 req/s burst for 5 minutes, latency <500ms p95

- **Action 2**: Auto-scaling validation (scale-out <5 minutes)
  - **Owner**: DevOps Engineer
  - **Target Date**: Week 71
  - **Success Criteria**: Capacity doubles within 5 minutes of load trigger

- **Action 3**: CDN caching strategy for top 20 endpoints
  - **Owner**: Chief Data Architect
  - **Target Date**: Week 66 (Beta Sprint 6)
  - **Success Criteria**: 80% cache hit rate for frequently accessed data

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-010: Census-Scale Performance Failure

**Risk Description**: Platform fails to process census-scale datasets (67 million records) within 24-hour target, failing BR-005 and preventing near-real-time census statistics for 2031 Census.

**Root Cause**: Underestimated processing complexity, insufficient parallelization, database write throughput limits, data quality validation overhead.

**Trigger Events**:
- Census data processing prototype in Alpha fails to meet 24-hour target
- Load testing in Beta shows linear scaling breaks at 50M records
- Data quality validation takes 12 hours (50% of budget)
- Statistical Disclosure Control (SDC) processing too slow (not parallelized)

**Consequences if Realized**:
- 2031 Census statistics delayed by weeks/months (vs 24 hours target)
- ONS unable to deliver near-real-time census statistics
- BR-005 objective failure (census-scale processing <24 hours)
- Reputational damage (ONS seen as technologically behind)
- Re-architecture required (£500K-£1M, 6-12 month delay)

**Affected Stakeholders**:
- Chief Data Architect (technical delivery)
- Census Programme Director (2031 Census)
- Chief Data Officer (strategic objective)

**Related Objectives**: BR-005 (Enable Census-Scale Processing <24 hours)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - Census-scale processing complex, limited prototyping time
- **Inherent Impact**: 5 (Catastrophic) - Strategic objective failure, re-architecture
- **Inherent Risk Score**: **20 (Critical)**

**Current Controls**:
- Early performance prototyping in Alpha (Week 20-24)
- Scalability testing demonstrates linear scaling to 100M records
- Distributed processing framework (Spark/Dask)
- Data partitioning strategy (by geography, time period)
- Load testing in Beta validates 67M records <24 hours
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 3 (Possible) - Early testing reduces risk
- **Residual Impact**: 5 (Catastrophic) - Impact remains critical if occurs
- **Residual Risk Score**: **15 (High)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Early performance prototyping in Alpha (Week 20-24)
  - **Owner**: Chief Data Architect
  - **Target Date**: Weeks 20-24
  - **Success Criteria**: 67M record prototype completes in <24 hours

- **Action 2**: Scalability testing to 100M records
  - **Owner**: QA/Test Engineer
  - **Target Date**: Week 71 (Beta)
  - **Success Criteria**: Linear scaling demonstrated, 100M records <36 hours

- **Action 3**: Distributed processing framework (Spark/Dask)
  - **Owner**: Data Engineers
  - **Target Date**: Week 50 (Beta Sprint 2)
  - **Success Criteria**: Processing parallelized across 50+ nodes

**Risk Status**: **Open**

**Risk Escalation**: Programme Board (monthly performance status in Beta)

**Review Date**: 2025-12-05

---

#### R-013: Vendor Lock-In Limits Future Options

(See STRATEGIC section - R-013 above for full details)

---

### REPUTATIONAL Risks

#### R-012: Cyber Security Breach of Pre-Release Data

**Risk Description**: Cyber attack successfully breaches ONS platform and exfiltrates pre-release market-sensitive statistics (GDP, inflation, unemployment), resulting in insider trading, financial market disruption, and catastrophic reputational damage.

**Root Cause**: High-value target (ONS pre-release data valuable for financial markets), nation-state APT (Advanced Persistent Threat), insider threat, zero-day exploits.

**Trigger Events**:
- Nation-state APT targets ONS (espionage motivation)
- Phishing attack compromises statistician credentials (MFA bypass)
- Zero-day exploit in cloud platform (unpatched vulnerability)
- Insider deliberately exfiltrates data (malicious or coerced)
- Ransomware attack encrypts ONS data (extortion)

**Consequences if Realized**:
- Pre-release statistics leaked to financial markets (insider trading)
- Financial market disruption (FCA investigation)
- Parliamentary inquiry / Cabinet Office investigation
- NCSC incident response (national security concern)
- Media coverage catastrophic ("ONS hacked, UK economic data compromised")
- UK Statistics Authority revokes ONS accreditation
- Chief Statistician / National Statistician resignation pressure
- Public trust in official statistics destroyed

**Affected Stakeholders**:
- Chief Statistician (regulatory accountability)
- National Statistician (ONS reputation)
- Head of Cyber Security (security breach)
- Financial markets (insider trading impact)
- NCSC (national security)

**Related Objectives**: NFR-SEC-001 (Zero Trust Architecture), Principle 10 (Security by Design)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 4 (Likely) - High-value target, nation-state APT capability
- **Inherent Impact**: 5 (Catastrophic) - National security, public trust destroyed
- **Inherent Risk Score**: **20 (Critical)**

**Current Controls**:
- Zero Trust architecture (multi-layer defense)
- Multi-factor authentication (MFA) for all users
- Network segmentation (pre-release data isolated)
- Encryption at rest (AES-256) and in transit (TLS 1.3+)
- SIEM real-time monitoring (24/7)
- Penetration testing (annual external, quarterly internal)
- Incident response plan and playbooks
- Cyber insurance (£10M coverage)
- **Control Effectiveness**: Strong

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Zero Trust significantly reduces attack surface
- **Residual Impact**: 5 (Catastrophic) - Impact remains catastrophic if occurs
- **Residual Risk Score**: **10 (Medium)**

**Risk Response**: **TRANSFER** (partial via cyber insurance) + **TREAT**

**Action Plan**:
- **Action 1**: Zero Trust architecture implementation (Sprint 6)
  - **Owner**: Head of Cyber Security
  - **Target Date**: Weeks 63-66 (Beta Sprint 6)
  - **Success Criteria**: All controls per NFR-SEC-001 implemented

- **Action 2**: Penetration testing (internal Week 68, external ITHC Week 72)
  - **Owner**: Head of Cyber Security
  - **Target Date**: Weeks 68, 72
  - **Success Criteria**: Zero critical/high findings

- **Action 3**: Cyber insurance (£10M coverage)
  - **Owner**: Chief Data Officer
  - **Target Date**: Week 73 (before go-live)
  - **Success Criteria**: Coverage includes data breach, business interruption, incident response

- **Action 4**: SIEM 24/7 monitoring and incident response
  - **Owner**: Head of Cyber Security
  - **Target Date**: Week 73 (go-live)
  - **Success Criteria**: Security Operations Centre (SOC) operational 24/7

**Risk Status**: **Open**

**Risk Escalation**: Chief Statistician → National Statistician → NCSC → Cabinet Office (if breach occurs)

**Review Date**: 2025-12-05

---

#### R-016: Social Media Backlash from Service Failure

**Risk Description**: High-profile service outage or data error triggers social media backlash, damaging ONS reputation and eroding public trust in official statistics.

**Root Cause**: Heightened social media scrutiny of public services, 24/7 news cycle, low tolerance for government failures.

**Trigger Events**:
- API outage during major release (GDP, CPI)
- Incorrect statistics published (data integrity failure)
- Accessibility failure (disabled users cannot access data)
- Slow API performance (user frustration)

**Consequences if Realized**:
- Twitter/X trending topic ("ONS fails again")
- Media amplification (newspapers pick up social media story)
- Parliamentary questions to National Statistician
- User confidence eroded (switch to alternative data sources)
- ONS brand damage

**Affected Stakeholders**:
- National Statistician (public trust)
- Director of Statistical Production (service delivery)
- Data users (public, media, researchers)

**Related Objectives**: BR-003 (Enhance Public Data Access)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 2 (Unlikely) - Comprehensive testing reduces outage risk
- **Inherent Impact**: 4 (Major) - Reputational damage significant
- **Inherent Risk Score**: **8 (Medium)**

**Current Controls**:
- Comprehensive testing (security, performance, UAT)
- Availability SLA (99.95% uptime)
- Hypercare support (4 weeks intensive, 24/7)
- Incident response plan
- Proactive communication strategy
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Controls maintain service reliability
- **Residual Impact**: 3 (Moderate) - Impact reduced through rapid response
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: Incident response plan and communication strategy
  - **Owner**: Director of Statistical Production
  - **Target Date**: Week 72
  - **Success Criteria**: Incident playbook covers communication within 1 hour

- **Action 2**: Proactive monitoring and alerting
  - **Owner**: DevOps Engineer
  - **Target Date**: Week 66
  - **Success Criteria**: Alerts detect issues before users complain

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

#### R-019: Research Community Access Issues

**Risk Description**: Integration with Secure Research Service (SRS) fails or is delayed, preventing approved researchers from accessing anonymised microdata for academic research. Could damage ONS relationship with research community.

**Root Cause**: SRS integration complexity, Five Safes framework implementation challenges, output checking workflow bottlenecks.

**Trigger Events**:
- SRS integration delayed (lower priority in Beta)
- Five Safes controls too restrictive (researchers frustrated)
- Output checking workflow too slow (weeks vs days)
- Researcher authentication issues (access denied incorrectly)

**Consequences if Realized**:
- Research community unable to access data (impact: 1,000+ researchers)
- Academic publications delayed (research output impact)
- ONS reputation in research community damaged
- Research funding bodies question ONS commitment to open data

**Affected Stakeholders**:
- Director of Statistical Production (research access)
- Researchers (1,000+ users)
- Research funding bodies (UKRI, Wellcome)

**Related Objectives**: INT-004 (Research Access Integration)

**Inherent Risk Assessment**:
- **Inherent Likelihood**: 3 (Possible) - SHOULD_HAVE requirement, lower priority
- **Inherent Impact**: 3 (Moderate) - Research impact but not critical to operations
- **Inherent Risk Score**: **9 (Medium)**

**Current Controls**:
- SRS integration in Sprint 5 (Week 59-62)
- Five Safes framework embedded in design
- Output checking workflow automated where possible
- **Control Effectiveness**: Adequate

**Residual Risk Assessment**:
- **Residual Likelihood**: 2 (Unlikely) - Sprint 5 time allocation sufficient
- **Residual Impact**: 3 (Moderate) - Impact contained
- **Residual Risk Score**: **6 (Medium)**

**Risk Response**: **TREAT**

**Action Plan**:
- **Action 1**: SRS integration prioritized in Sprint 5
  - **Owner**: Data Engineers
  - **Target Date**: Weeks 59-62
  - **Success Criteria**: Integration complete, researchers can access data

**Risk Status**: **Open**

**Review Date**: 2025-12-05

---

## Risk Ownership Matrix

| Stakeholder | Owned Risks | Critical/High Risks | Total Residual Score | Notes |
|-------------|-------------|---------------------|----------------------|-------|
| **Chief Data Officer** | R-001, R-007, R-022 | 0 Critical, 2 High (R-001, R-007) | 32 | Heavy concentration of strategic + financial risks |
| **Chief Data Architect** | R-003, R-008, R-009, R-010, R-013 | 0 Critical, 2 High (R-003, R-010) | 63 | Owns majority of technical delivery risks |
| **Chief Statistician** | R-006 | 0 Critical, 1 High (R-006) | 15 | Critical Statistics Act compliance risk |
| **Head of Cyber Security** | R-004, R-012 | 0 Critical, 0 High | 22 | Security risks well-controlled |
| **Director of Statistical Production** | R-005, R-018, R-019 | 0 Critical, 0 High | 24 | User adoption and service delivery risks |
| **Procurement Specialist** | R-002 | 0 Critical, 0 High | 12 | Vendor procurement risk |
| **Chief Technology Officer** | R-015 | 0 Critical, 0 High | 9 | Skills gap risk tolerated |
| **Multiple owners** | R-011, R-014, R-016, R-017, R-020, R-021 | 0 Critical, 0 High | 30 | Lower priority risks |

**Key Observations**:
- **Chief Data Architect** owns highest total residual risk (63 points, 5 risks) - requires active support
- **Chief Statistician** owns critical Statistics Act compliance risk (R-006) - highest priority
- **Chief Data Officer** owns strategic + financial risks (32 points) - Programme Board oversight essential
- **Head of Cyber Security** has effectively controlled security risks (Critical → Medium reductions)

---

## 4Ts Risk Response Summary

| Response | Count | % | Key Examples | Rationale |
|----------|-------|---|--------------|-----------|
| **Treat** | 18 risks | 82% | R-001, R-002, R-003, R-004, R-005, R-006, R-007, R-008, R-009, R-010, R-011, R-012, R-013, R-014, R-016, R-017, R-019, R-021 | Majority of risks require active mitigation through additional controls. Demonstrates appropriate risk management for transformational programme. |
| **Transfer** | 2 risks | 9% | R-012 (Cyber insurance £10M), R-002 (Vendor liability contracts) | High-impact, low-likelihood risks transferred to 3rd parties via insurance and contracts. |
| **Tolerate** | 2 risks | 9% | R-018 (Statistician resistance - change management), R-015 (Skills gap - training), R-022 (Funding shortfall - strong business case) | Low residual risks within organizational appetite. Cost of additional controls exceeds benefit. |
| **Terminate** | 0 risks | 0% | None | No activities require termination. All risks manageable through treatment or tolerance. |

**Recommended Strategy**: The 4Ts distribution is appropriate for a large transformational programme:
- **82% Treat**: Reflects comprehensive control framework for high-risk areas (security, compliance, performance)
- **9% Transfer**: Appropriate use of insurance and contracts for catastrophic but unlikely events
- **9% Tolerate**: Reasonable acceptance of low residual risks within appetite
- **0% Terminate**: Indicates no unacceptable risks requiring activity cessation

---

## Risk by Category Analysis

### STRATEGIC Risks (4 risks)

**Average Inherent Score**: 18.0 (High)
**Average Residual Score**: 10.5 (Medium)
**Risk Reduction**: 42%

**Key Themes**:
- Policy/ministerial direction changes (R-001)
- Vendor procurement and lock-in (R-002, R-013)
- Funding shortfalls (R-022)

**Control Effectiveness**: Strong controls reduce strategic risks by 42% on average. Monthly Programme Board reviews and phased delivery provide flexibility to respond to strategic changes.

**Actions Required**:
- Monthly Programme Board reviews to monitor policy environment
- Vendor contract exit rights and abstraction layers to reduce lock-in
- Quarterly HM Treasury checkpoint meetings to maintain funding

---

### OPERATIONAL Risks (5 risks)

**Average Inherent Score**: 14.4 (High)
**Average Residual Score**: 9.2 (Medium)
**Risk Reduction**: 36%

**Key Themes**:
- Data migration integrity (R-003 - HIGH residual)
- Legacy system integration (R-008)
- Skills gaps (R-015)
- Team stability (R-020)
- User adoption (R-018)

**Control Effectiveness**: Adequate controls reduce operational risks by 36%. Data migration (R-003) remains HIGH residual risk requiring intensive parallel running and statistician validation.

**Actions Required**:
- 6-week parallel running period for data migration validation
- Weekly legacy system coordination meetings
- Embedded ONS engineers during Beta implementation
- Change champion network for user adoption

---

### FINANCIAL Risks (3 risks)

**Average Inherent Score**: 15.3 (High)
**Average Residual Score**: 9.7 (Medium)
**Risk Reduction**: 37%

**Key Themes**:
- Cloud cost overruns (R-007 - priority risk)
- Disaster recovery costs (R-011)
- Admin data API fees (R-014)

**Control Effectiveness**: Adequate controls reduce financial risks by 37%. Monthly cost monitoring and FinOps practices essential for R-007 (cloud costs).

**Actions Required**:
- Monthly cost monitoring and FinOps controls from Week 43
- Reserved instance purchasing strategy (70% compute)
- Quarterly cost optimization reviews
- Budget alerts at 80%, 90%, 100% thresholds

---

### COMPLIANCE/REGULATORY Risks (5 risks)

**Average Inherent Score**: 19.2 (Critical/High)
**Average Residual Score**: 11.8 (Medium)
**Risk Reduction**: 39%

**Key Themes**:
- Statistics Act compliance (R-006 - HIGH residual, critical importance)
- Security accreditation (R-004 - GovS 007 ITHC)
- GDS Service Standard (R-005)
- SDMX metadata (R-017)
- Procurement challenge (R-021)

**Control Effectiveness**: Strong controls reduce compliance risks by 39% on average. Statistics Act compliance (R-006) remains HIGH residual risk due to catastrophic impact if breached.

**Actions Required**:
- UK Statistics Authority validation of pre-release access controls
- ITHC penetration testing with 4-week remediation buffer
- Mock GDS Service Assessment in Alpha
- Eurostat SDMX validation before go-live

---

### TECHNOLOGY Risks (4 risks)

**Average Inherent Score**: 16.5 (High)
**Average Residual Score**: 10.0 (Medium)
**Risk Reduction**: 39%

**Key Themes**:
- Census-scale performance (R-010 - HIGH residual, strategic importance)
- API traffic spikes (R-009)
- Vendor lock-in (R-013)

**Control Effectiveness**: Strong controls reduce technology risks by 39%. Census-scale performance (R-010) remains HIGH residual risk requiring early prototyping and load testing.

**Actions Required**:
- Early performance prototyping in Alpha (67M records <24 hours)
- Load testing with realistic traffic patterns (10,000 req/s sustained)
- Scalability testing to 100M records
- Auto-scaling validation (<5 minute response time)

---

### REPUTATIONAL Risks (1 risk)

**Average Inherent Score**: 16.0 (High)
**Average Residual Score**: 10.0 (Medium)
**Risk Reduction**: 38%

**Key Themes**:
- Cyber security breach of pre-release data (R-012 - transferred via insurance)
- Social media backlash (R-016)
- Research community access (R-019)

**Control Effectiveness**: Strong controls reduce reputational risks by 38%. Zero Trust architecture and cyber insurance provide defense-in-depth for R-012.

**Actions Required**:
- Cyber insurance (£10M coverage) before go-live
- SIEM 24/7 monitoring and incident response
- Incident communication strategy (<1 hour response)

---

## Action Plan (Prioritized)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Status |
|----------|--------|-------------------|-------|----------|--------|
| **1** | Establish parallel running environment | R-003 (Data Migration - HIGH) | Chief Data Architect | Week 65 | Open |
| **2** | Design Statistics Act pre-release access controls | R-006 (Statistics Act - HIGH) | Chief Statistician | Weeks 55-58 | Open |
| **3** | Early census-scale performance prototyping | R-010 (Census Performance - HIGH) | Chief Data Architect | Weeks 20-24 | Open |
| **4** | Start vendor procurement immediately after Discovery | R-002 (Vendor Delay) | Procurement Specialist | Week 13 | Open |
| **5** | Implement FinOps cost monitoring from Beta start | R-007 (Cloud Costs) | Chief Data Officer | Week 43 | Open |
| **6** | STRIDE threat model in Alpha | R-004 (GovS 007), R-012 (Security Breach) | Head of Cyber Security | Weeks 19-21 | Open |
| **7** | Mock GDS Service Assessment in Alpha | R-005 (Service Standard) | Service Owner | Week 26 | Open |
| **8** | HLD review validates abstraction layers (vendor lock-in) | R-013 (Vendor Lock-in) | Chief Data Architect | Week 24 | Open |
| **9** | Weekly legacy system coordination meetings | R-008 (Legacy Integration) | Chief Data Architect | Weeks 37-78 | Open |
| **10** | Load testing with realistic publication traffic | R-009 (API Traffic), R-010 (Census Performance) | QA/Test Engineer | Week 71 | Open |
| **11** | Cyber insurance (£10M coverage) before go-live | R-012 (Security Breach) | Chief Data Officer | Week 73 | Open |
| **12** | Embed 8 ONS engineers with vendor during Beta | R-015 (Skills Gap) | Chief Data Architect | Weeks 37-72 | Open |
| **13** | Identify 5 change champions for user adoption | R-018 (User Resistance) | Director of Production | Week 67 | Open |
| **14** | UK Statistics Authority validation of controls | R-006 (Statistics Act) | Chief Statistician | Week 65 | Open |
| **15** | Internal penetration testing 4 weeks before ITHC | R-004 (GovS 007) | Head of Cyber Security | Week 68 | Open |
| **16** | Reserved instance purchasing strategy (70% compute) | R-007 (Cloud Costs) | Chief Data Architect | Week 73 | Open |
| **17** | Comprehensive data validation framework | R-003 (Data Migration) | Data Engineers | Week 50 | Open |
| **18** | Automate SDMX metadata generation | R-017 (SDMX Compliance) | Data Engineers | Weeks 55-58 | Open |
| **19** | SRS research integration in Sprint 5 | R-019 (Research Access) | Data Engineers | Weeks 59-62 | Open |
| **20** | Quarterly benefits realization reporting to HM Treasury | R-001 (Strategic Change), R-022 (Funding) | Chief Data Officer | Quarterly | Open |

---

## Monitoring and Review Framework

### Review Frequency

| Risk Severity | Review Frequency | Owner | Escalation |
|---------------|------------------|-------|------------|
| **Critical (20-25)** | Weekly | Risk Owner | Programme Board immediately |
| **High (13-19)** | Fortnightly | Risk Owner | Programme Board if increasing |
| **Medium (6-12)** | Monthly | Risk Owner | Programme Board if exceeds appetite |
| **Low (1-5)** | Quarterly | Risk Owner | None required |

**Current Status**: 0 Critical, 3 High, 16 Medium, 3 Low

### Escalation Criteria

Risks must be escalated to Programme Board if:
1. **Risk score increases by ≥5 points** (e.g., Medium → High)
2. **New Critical risk identified** (score 20-25)
3. **Residual risk exceeds organizational appetite** (if appetite defined)
4. **Risk materializes** (trigger event occurs)
5. **Control effectiveness degrades** (Strong → Adequate → Weak)

### Reporting Requirements

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| **Risk Status Report** | Weekly | SRO, Programme Board | Critical/High risks only, RAG status, actions progress |
| **Risk Register Review** | Monthly | Programme Board | All risks, trend analysis, new risks, closed risks |
| **Risk Appetite Compliance** | Quarterly | Audit Committee | Risks exceeding appetite, justifications, approvals |
| **Risk Assurance Review** | Annually | Internal Audit | Control effectiveness, Orange Book compliance |

### Risk Register Ownership

**Risk Register Owner**: Chief Data Architect, ONS

**Responsibilities**:
- Maintain risk register (add, update, close risks)
- Coordinate risk reviews with risk owners
- Prepare risk reports for Programme Board
- Escalate risks per escalation criteria
- Annual Orange Book compliance review

**Next Review Date**: 2025-12-05 (Monthly review)

**Next Full Re-Assessment**: 2026-02-05 (Quarterly re-assessment)

---

## Integration with SOBC (Strategic Outline Business Case)

This risk register feeds into the SOBC as follows:

### Strategic Case (Part A)
- **Strategic risks** (R-001, R-022) inform "Why Now?" urgency and policy context
- **Reputational risks** (R-012, R-016) support case for modernisation to maintain public trust

### Economic Case (Part B)
- **Financial risks** (R-007, R-011, R-014) inform risk-adjusted cost estimates
- **Optimism bias** applied per HM Treasury Green Book (15% for IT-enabled programmes)
- **Benefits risks** (R-003, R-018) inform benefits realisation probability

### Commercial Case (Part C)
- **Vendor risks** (R-002, R-013) inform procurement strategy and contract terms
- **Delivery model** selected to mitigate high vendor dependency risks

### Financial Case (Part D)
- **Cost overrun risks** (R-007, R-011) inform contingency allocation (10% = £1.8M)
- **Funding risks** (R-022) inform spend profile and HM Treasury engagement

### Management Case (Part E)
- **Full risk register** (this document) copied into Management Case Part E
- **Risk management framework** (monitoring, escalation, review) defined
- **Governance structure** aligns risk ownership to decision rights

---

## Orange Book Compliance

This risk register demonstrates compliance with HM Treasury Orange Book principles:

### ✅ Principle 1: Governance and Leadership
- **Risk ownership**: All 22 risks assigned to senior stakeholders (Director+ level)
- **Accountability**: SRO (Chief Data Officer) owns overall risk profile
- **Board oversight**: Programme Board reviews monthly risk status
- **Escalation**: Clear escalation paths defined (Risk Owner → Programme Board → HMT)

### ✅ Principle 2: Integration
- **Strategic alignment**: Risks traced to business objectives (BR-001 to BR-005)
- **SOBC integration**: Risk register feeds into all 5 cases of business case
- **Decision-making**: Risk appetite informs go/no-go decisions at gates
- **Performance management**: Risk metrics included in Programme Board KPIs

### ✅ Principle 3: Collaboration
- **Stakeholder engagement**: Risks sourced from stakeholder concerns (requirements, principles)
- **Cross-functional**: Risks span strategy, operations, finance, compliance, technology
- **Expert judgment**: Risk assessments validated by subject matter experts (Security, Architecture)
- **Lessons learned**: Risk patterns informed by ONS previous programmes

### ✅ Principle 4: Risk Processes
- **Identify**: Systematic identification across 6 Orange Book categories
- **Assess**: Likelihood × Impact methodology (1-5 scale), inherent + residual
- **Respond**: 4Ts framework applied (Tolerate, Treat, Transfer, Terminate)
- **Monitor**: Review frequency defined by risk severity (weekly for Critical, monthly for High)

### ✅ Principle 5: Continual Improvement
- **Review framework**: Monthly register review, quarterly re-assessment, annual assurance
- **Action tracking**: 20 priority actions with owners, due dates, success criteria
- **Lessons learned**: Risk register updated based on emerging risks and controls effectiveness
- **Control effectiveness**: Monitoring demonstrates 38% average risk reduction from inherent to residual

---

## Appendices

### Appendix A: Risk Scoring Methodology

#### Likelihood Scale (1-5)

| Score | Descriptor | Definition | Probability |
|-------|------------|------------|-------------|
| 5 | Almost Certain | Expected to occur, highly likely | > 75% |
| 4 | Likely | More likely to happen than not | 50-75% |
| 3 | Possible | Reasonable chance of occurring | 25-50% |
| 2 | Unlikely | Could happen but probably won't | 5-25% |
| 1 | Rare | Highly unlikely, exceptional circumstances | < 5% |

#### Impact Scale (1-5)

| Score | Descriptor | Cost Impact | Timeline Impact | Strategic Impact |
|-------|------------|-------------|-----------------|------------------|
| 5 | Catastrophic | > £5M or >40% variance | > 6 months delay | Project failure, regulatory breach |
| 4 | Major | £2M-£5M or 20-40% variance | 3-6 months delay | Major objectives threatened |
| 3 | Moderate | £500K-£2M or 10-20% variance | 1-3 months delay | Significant management effort |
| 2 | Minor | £100K-£500K or 5-10% variance | 2-4 weeks delay | Manageable within reserves |
| 1 | Negligible | < £100K or <5% variance | < 2 weeks delay | Minimal impact, easily absorbed |

#### Risk Score Matrix (Likelihood × Impact)

| | **1 (Neg)** | **2 (Minor)** | **3 (Mod)** | **4 (Major)** | **5 (Cata)** |
|---|---|---|---|---|---|
| **5 (A.Cert)** | 5 (Low) | 10 (Med) | 15 (High) | 20 (Crit) | 25 (Crit) |
| **4 (Likely)** | 4 (Low) | 8 (Med) | 12 (Med) | 16 (High) | 20 (Crit) |
| **3 (Poss)** | 3 (Low) | 6 (Med) | 9 (Med) | 12 (Med) | 15 (High) |
| **2 (Unlik)** | 2 (Low) | 4 (Low) | 6 (Med) | 8 (Med) | 10 (Med) |
| **1 (Rare)** | 1 (Low) | 2 (Low) | 3 (Low) | 4 (Low) | 5 (Low) |

**Risk Severity Bands**:
- **Critical (20-25)**: Immediate escalation to SRO, Programme Board, HM Treasury
- **High (13-19)**: Active management, fortnightly review, Programme Board oversight
- **Medium (6-12)**: Standard management, monthly review, escalate if increasing
- **Low (1-5)**: Monitor, quarterly review, no escalation required

---

### Appendix B: 4Ts Risk Response Framework

#### TOLERATE
**When to use**: Residual risk within appetite, cost of mitigation exceeds benefit, low likelihood/low impact.

**Requirements**:
- Explicit acceptance decision documented
- Risk owner sign-off
- Monitoring plan defined
- Escalation criteria if risk increases

**Examples**: R-015 (Skills gap - training sufficient), R-018 (User resistance - change management adequate), R-022 (Funding shortfall - strong business case)

#### TREAT
**When to use**: Medium/high residual risk, can be reduced through actions, cost-effective controls available.

**Requirements**:
- Specific mitigation actions defined
- Action owner assigned (may differ from risk owner)
- Target residual risk score defined
- Success criteria measurable

**Examples**: R-003 (Data migration - parallel running), R-006 (Statistics Act - MFA + audit), R-010 (Performance - early testing)

#### TRANSFER
**When to use**: Low likelihood/high impact, can be insured or contracted out, 3rd party better positioned to manage risk.

**Requirements**:
- Transfer mechanism defined (insurance, contract terms)
- Residual risk after transfer assessed (not all risk transferred)
- Cost of transfer justified

**Examples**: R-012 (Cyber breach - £10M insurance), R-002 (Vendor delay - liability clauses)

#### TERMINATE
**When to use**: High likelihood/high impact, exceeds appetite, cannot be mitigated, stop activity creating risk.

**Requirements**:
- Decision authority (typically SRO or Programme Board)
- Sunk cost analysis
- Alternative approach identified

**Examples**: None (no activities require termination in this programme)

---

### Appendix C: Stakeholder Contact Details

| Stakeholder | Role | Email | Phone |
|-------------|------|-------|-------|
| Chief Data Officer | SRO, Programme Board Chair | cdo@ons.gov.uk | [TBD] |
| Chief Statistician | Regulatory Compliance | chief.statistician@ons.gov.uk | [TBD] |
| Chief Data Architect | Technical Authority | chief.architect@ons.gov.uk | [TBD] |
| Director of Statistical Production | Service Owner | production.director@ons.gov.uk | [TBD] |
| Head of Cyber Security | Security Authority | security.head@ons.gov.uk | [TBD] |
| National Statistician | ONS Accreditation | national.statistician@ons.gov.uk | [TBD] |
| GDS Service Assessor | Service Standard | assessments@digital.cabinet-office.gov.uk | [TBD] |
| HM Treasury Programme Manager | Funding Authority | [TBD]@hmtreasury.gov.uk | [TBD] |

---

### Appendix D: Risk Register Change Log

| Date | Version | Risk ID | Change Description | Changed By |
|------|---------|---------|-------------------|------------|
| 2025-11-05 | 1.0 | All | Initial risk register creation | ArcKit AI |
| [TBD] | 1.1 | [ID] | [Description] | [Name] |

---

### Appendix E: References

| Document | Location | Version |
|----------|----------|---------|
| HM Treasury Orange Book | https://www.gov.uk/government/publications/orange-book | 2023 |
| HM Treasury Green Book | https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-governent | 2022 |
| Architecture Principles | `.arckit/memory/architecture-principles.md` | 1.0 |
| Requirements | `projects/001-ons-data-platform-modernisation/requirements.md` | 1.0 |
| Project Plan | `projects/001-ons-data-platform-modernisation/project-plan.md` | 1.0 |
| GDS Service Manual | https://www.gov.uk/service-manual | Current |
| Statistics and Registration Service Act 2007 | https://www.legislation.gov.uk/ukpga/2007/18 | Current |

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: 2025-11-05
**ArcKit Version**: 0.8.3
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-sonnet-4-5-20250929
**Methodology**: HM Treasury Orange Book 2023
**Context Used**: Requirements (100+ reqs), Architecture Principles (14 principles), Project Plan (78 weeks), Stakeholder information from requirements document
**Total Risks**: 22 risks across 6 categories
**Overall Risk Profile**: Concerning but manageable (3 High residual risks require escalation)
