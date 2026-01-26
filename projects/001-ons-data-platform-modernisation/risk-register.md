# Risk Register: ONS Data Platform Modernisation

> **Template Status**: Live | **Version**: 0.11.2 | **Command**: `/arckit.risk`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.1 |
| **Document Type** | Risk Register (HM Treasury Orange Book) |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2025-11-05 |
| **Last Modified** | 2026-01-26 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-02-26 |
| **Owner** | Chief Data Architect, ONS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, Risk Owners, HM Treasury Checkpoint Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-05 | ArcKit AI | Initial creation from `/arckit.risk` command | PENDING | PENDING |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2: Added Risk Appetite Compliance section, KRIs, Leading/Lagging indicators, Document Approval section; Enhanced Document Control and Executive Summary formatting | PENDING | PENDING |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** 22 risks across 6 categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 6 | 0 | ↓ 100% |
| **High** (13-19) | 12 | 3 | ↓ 75% |
| **Medium** (6-12) | 4 | 16 | ↑ 300% |
| **Low** (1-5) | 0 | 3 | ↑ N/A |
| **TOTAL** | 352 | 207 | ↓ 41% |

### Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness |
|----------|-------|--------------|--------------|----------------------|
| **STRATEGIC** | 4 | 18.0 | 10.5 | 42% reduction |
| **OPERATIONAL** | 5 | 14.4 | 9.2 | 36% reduction |
| **FINANCIAL** | 3 | 15.3 | 9.7 | 37% reduction |
| **COMPLIANCE** | 5 | 19.2 | 11.8 | 39% reduction |
| **REPUTATIONAL** | 1 | 16.0 | 10.0 | 38% reduction |
| **TECHNOLOGY** | 4 | 16.5 | 10.0 | 39% reduction |

### Overall Risk Assessment

**Overall Residual Risk Score:** 207/550 (38% of maximum possible)
**Risk Reduction from Controls:** 41% reduction from inherent risk
**Risk Profile Status:** ⚠️ Concerning but Manageable

### Risks Exceeding Appetite

**Number of risks exceeding organizational appetite:** 3 risks

| Risk ID | Title | Category | Score | Appetite | Excess | Escalation |
|---------|-------|----------|-------|----------|--------|------------|
| R-003 | Data Migration Integrity Failures | OPERATIONAL | 15 | 12 | +3 | Programme Board escalation required |
| R-006 | Statistics Act Pre-Release Access Breach | COMPLIANCE | 15 | 9 | +6 | Chief Statistician + National Statistician |
| R-010 | Census-Scale Performance Failure | TECHNOLOGY | 15 | 12 | +3 | Programme Board escalation required |

### Top 5 Critical Risks Requiring Immediate Attention

1. **R-003** (OPERATIONAL, High 15): Data Migration Integrity Failures - Owner: Chief Data Architect - Status: Open
2. **R-006** (COMPLIANCE, High 15): Statistics Act Pre-Release Access Breach - Owner: Chief Statistician - Status: Open
3. **R-010** (TECHNOLOGY, High 15): Census-Scale Performance Failure - Owner: Chief Data Architect - Status: Open
4. **R-001** (STRATEGIC, Medium 12): Strategic Direction Change Mid-Project - Owner: Chief Data Officer - Status: Open
5. **R-007** (FINANCIAL, Medium 12): Cloud Cost Overruns Exceed £6.7M Target - Owner: Chief Data Officer - Status: Open

### Key Findings and Recommendations

**Key Findings:**
- All 6 Critical inherent risks successfully reduced to High/Medium through planned controls (100% Critical risk elimination)
- 3 High residual risks remain (R-003, R-006, R-010) - all require active escalation to Programme Board
- Heavy concentration of technical risks owned by Chief Data Architect (5 risks, 63 points total residual)
- Statistics Act compliance (R-006) poses highest regulatory risk with catastrophic impact if breached

**Recommendations:**
1. Escalate R-003, R-006, R-010 to Programme Board for additional mitigation investment
2. Establish parallel running environment by Week 65 to address R-003 (Data Migration)
3. Obtain UK Statistics Authority validation of pre-release access controls for R-006
4. Conduct early performance prototyping in Alpha (Weeks 20-24) for R-010 (Census Performance)
5. Implement FinOps controls from Beta start (Week 43) to prevent cloud cost overruns

---

## A. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

**Likelihood × Impact Matrix - Inherent Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       | R-006 | R-003 | R-010 | R-002 |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       | R-008 | R-004 | R-001 | R-013 |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       | R-018 | R-005 | R-007 | R-015 | R-012 |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       |       | R-020 | R-011 | R-009 | R-016 |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           |       | R-014 | R-019 | R-017 | R-021 |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

**Risk Zones:**
- 🟥 **Critical (20-25)**: R-002, R-003, R-006, R-010, R-012, R-013 - 6 risks requiring immediate escalation
- 🟧 **High (13-19)**: R-001, R-004, R-005, R-007, R-008, R-015 - 6 risks requiring senior management attention
- 🟨 **Medium (6-12)**: R-009, R-011, R-016, R-018 - 4 risks requiring management monitoring
- 🟩 **Low (1-5)**: R-014, R-019, R-020, R-021, R-017 - 6 risks for routine monitoring

### Residual Risk Matrix (After Controls)

**Likelihood × Impact Matrix - Residual Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       |       |       |       |       |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       |       |       |       |       |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       |       | R-018 | R-003 | R-001 | R-006 |
       |                |       | R-020 | R-007 | R-004 | R-010 |
       |                |       |       | R-015 | R-005 |       |
       |                |       |       | R-011 | R-008 |       |
       |                |       |       | R-019 | R-009 |       |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       |       | R-014 | R-013 | R-002 | R-012 |
       |                |       |       | R-017 | R-016 |       |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           | R-021 |       |       |       |       |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

**Risk Zones After Controls:**
- 🟥 **Critical (20-25)**: None (0 risks) ✅ All mitigated below critical threshold
- 🟧 **High (13-19)**: R-003, R-006, R-010 - 3 risks requiring continued active management
- 🟨 **Medium (6-12)**: R-001, R-002, R-004, R-005, R-007, R-008, R-009, R-011, R-012, R-013, R-015, R-016, R-017, R-018, R-019, R-020 - 16 risks in management monitoring
- 🟩 **Low (1-5)**: R-014, R-021, R-022 - 3 risks for routine monitoring

### Risk Movement Analysis

**Significant Risk Reductions** (≥5 point reduction):
- ✅ **R-002** (Vendor Delay): 20 → 12 (-8 points): Early procurement, G-Cloud framework, parallel HLD design
- ✅ **R-003** (Data Migration): 20 → 15 (-5 points): Parallel running validation, statistician sign-off
- ✅ **R-006** (Statistics Act): 20 → 15 (-5 points): MFA, audit logging, UK Statistics Authority validation
- ✅ **R-010** (Census Performance): 20 → 15 (-5 points): Early performance prototyping, scalability testing
- ✅ **R-012** (Security Breach): 20 → 10 (-10 points): Zero Trust architecture, cyber insurance
- ✅ **R-013** (Vendor Lock-in): 16 → 9 (-7 points): Abstraction layers, contract exit clauses

**Risks Remaining HIGH** (require ongoing active management):
- ⚠️ **R-003** (Data Migration Integrity): Residual 15 - Catastrophic impact if occurs, requires 6-week parallel running
- ⚠️ **R-006** (Statistics Act Breach): Residual 15 - Regulatory breach risk, requires UK Statistics Authority sign-off
- ⚠️ **R-010** (Census-Scale Performance): Residual 15 - Strategic objective at risk, requires early prototyping

---

## B. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-003 | Data Migration Integrity Failures | OPERATIONAL | 20 | 15 (High) | Chief Data Architect | Open | Treat |
| 2 | R-006 | Statistics Act Pre-Release Access Breach | COMPLIANCE | 20 | 15 (High) | Chief Statistician | Open | Treat |
| 3 | R-010 | Census-Scale Performance Failure | TECHNOLOGY | 20 | 15 (High) | Chief Data Architect | Open | Treat |
| 4 | R-001 | Strategic Direction Change Mid-Project | STRATEGIC | 16 | 12 (Medium) | Chief Data Officer | Open | Treat |
| 5 | R-004 | GovS 007 ITHC Security Assessment Failure | COMPLIANCE | 16 | 12 (Medium) | Head of Cyber Security | Open | Treat |
| 6 | R-005 | GDS Service Standard Assessment Failure | COMPLIANCE | 15 | 12 (Medium) | Director of Statistical Production | Open | Treat |
| 7 | R-007 | Cloud Cost Overruns Exceed £6.7M Target | FINANCIAL | 15 | 12 (Medium) | Chief Data Officer | Open | Treat |
| 8 | R-008 | Legacy System Integration Failures | OPERATIONAL | 16 | 12 (Medium) | Chief Data Architect | Open | Treat |
| 9 | R-009 | API Traffic Spike Handling Failure | TECHNOLOGY | 12 | 12 (Medium) | Chief Data Architect | Open | Treat |
| 10 | R-012 | Cyber Security Breach of Pre-Release Data | REPUTATIONAL | 20 | 10 (Medium) | Head of Cyber Security | Open | Transfer |

---

## C. Detailed Risk Register

### STRATEGIC Risks

#### R-001: Strategic Direction Change Mid-Project

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Chief Data Officer (from Stakeholder RACI: Accountable)
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
UK Government policy or ministerial priorities change mid-implementation, requiring significant scope changes or project re-direction. Could result from machinery of government changes, new manifesto commitments, or National Statistician strategic review.

**Root Cause:**
Political environment uncertainty, long project duration (18 months), potential general election, ministerial turnover.

**Trigger Events:**
- Machinery of government changes affecting ONS structure
- New National Statistician appointed with different priorities
- Manifesto commitment requiring ONS to deliver different capabilities
- HM Treasury spending review cuts budget allocation

**Consequences if Realized:**
- Major scope changes require re-work (4-8 weeks delay)
- Budget reallocation requires new business case approval
- Team morale impact from scope thrash
- Sunk costs on abandoned work (£500K-£1M)
- Delay to benefits realization (£4.5M annual savings)

**Affected Stakeholders:**
- **Chief Data Officer** (from stakeholder-drivers.md): SRO accountability, benefits delivery at risk
- **Chief Statistician**: Regulatory compliance timeline impacted
- **Director of Statistical Production**: Operational delivery delayed
- **Programme Board**: Oversight burden increased

**Related Objectives:**
- Goal G-1 (40% infrastructure cost reduction): Delayed by scope changes
- Goal G-2 (60% publication efficiency): Timeline at risk

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | 18-month programme spans political cycle, ministerial changes common |
| **Impact** | 4 - Major | £500K-£1M sunk costs, 4-8 week delay, benefits delay |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Monthly Programme Board reviews with SRO sign-off**
   - Owner: Chief Data Officer
   - Effectiveness: **Strong**
   - Evidence: Programme Board minutes, decision log

2. **Quarterly HM Treasury checkpoint meetings**
   - Owner: Chief Data Officer
   - Effectiveness: **Adequate**
   - Evidence: HMT checkpoint reports

3. **Strong business case aligned with ONS statutory duties**
   - Owner: Chief Data Officer
   - Effectiveness: **Strong**
   - Evidence: Statistics Act 2007 compliance requirement

4. **Phased delivery enables scope flexibility**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Architecture modularity assessment

**Overall Control Effectiveness:** Strong (reduces risk from 16 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Controls provide early warning, flexible delivery |
| **Impact** | 4 - Major | Impact remains significant if major policy change occurs |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (16 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
Risk within appetite after controls but requires ongoing monitoring. Phased delivery and modular architecture provide flexibility to adapt to policy changes without major re-work.

**Alternative Responses Considered:**
- **Tolerate**: Rejected - Risk still medium, requires active monitoring
- **Transfer**: Not applicable - Strategic risk cannot be transferred
- **Terminate**: Not viable - Programme essential to ONS statutory duties

##### Risk Appetite Assessment

**Organizational Risk Appetite for STRATEGIC risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

**Justification:**
Strategic risk at threshold is acceptable given strong business case, statutory driver, and flexible delivery approach. Monthly Programme Board provides governance oversight.

**Escalation Required:** No - within appetite, but monitor closely

##### Action Plan

**Additional Mitigations Needed:**

1. **Monthly Programme Board reviews with policy environment scanning**
   - Description: Review political and policy environment monthly, identify early warning signals
   - Owner: Chief Data Officer
   - Due Date: Ongoing (monthly)
   - Cost: Staff time only
   - Expected Impact: Early warning enables proactive response

2. **Build flexibility into architecture (modularity, loose coupling)**
   - Description: HLD ensures components can be re-prioritized without major re-work
   - Owner: Chief Data Architect
   - Due Date: Week 24 (HLD approval)
   - Cost: Included in architecture effort
   - Expected Impact: Reduce re-work costs if scope changes

**Target Residual Risk After Mitigations:**
- Target Likelihood: 3 (Possible)
- Target Impact: 3 (Moderate)
- Target Score: 9 (Medium) ✅ Below appetite threshold

**Success Criteria:**
- Early warning of policy changes (>4 weeks notice)
- Components can be re-prioritized within 2 weeks
- No scope change requires >4 weeks re-work

**Monitoring Plan:**
- **Frequency:** Monthly review in Programme Board
- **Key Indicators:**
  - Ministerial announcements affecting ONS
  - HM Treasury spending review signals
  - National Statistician strategic direction changes
- **Escalation Triggers:**
  - Policy announcement directly affecting programme scope
  - Budget allocation reduced by >10%

---

#### R-002: Vendor Procurement Delays Alpha Phase

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Procurement Specialist
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
Vendor procurement process (SOW, RFP, evaluation, contract negotiation) exceeds planned 8 weeks, delaying Alpha phase completion and compressing Beta delivery timeline. G-Cloud framework reduces risk but complex requirements and negotiation could extend timeline.

**Root Cause:**
Complex technical requirements, multiple vendor evaluation rounds, contract negotiation challenges, public sector procurement rules.

**Trigger Events:**
- Insufficient G-Cloud suppliers meet requirements
- Vendor clarification questions extend evaluation period
- Contract negotiations stall on liability clauses
- HM Treasury approval delays for >£18M programme
- Challenger vendor requests procurement review

**Consequences if Realized:**
- Alpha phase extends by 4-8 weeks
- Beta implementation compressed (quality risk)
- Go-live date slips (delayed benefits realization)
- Budget pressure from extended contractor costs (£200K-£400K)

**Affected Stakeholders:**
- **Chief Data Officer**: SRO accountability, budget pressure
- **Director of Statistical Production**: Publication timeline impact
- **Procurement Specialist**: Delivery accountability

**Related Objectives:**
- BR-001 (Cost Reduction): Budget impact from delays
- Project Timeline: 78-week schedule at risk

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Public sector procurement often exceeds estimates |
| **Impact** | 5 - Catastrophic | Critical path impact, budget overrun |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

**Risk Zone:** 🟥 Critical (20-25)

##### Current Controls and Mitigations

**Existing Controls:**
1. **G-Cloud Digital Marketplace framework**
   - Owner: Procurement Specialist
   - Effectiveness: **Strong**
   - Evidence: Pre-approved suppliers, standard terms

2. **Start procurement early (Week 13)**
   - Owner: Procurement Specialist
   - Effectiveness: **Strong**
   - Evidence: Procurement schedule in project plan

3. **Parallel HLD design during procurement**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: HLD workstream independent of vendor selection

4. **Fixed evaluation timeline with hard deadlines**
   - Owner: Procurement Specialist
   - Effectiveness: **Adequate**
   - Evidence: RFP timeline published

**Overall Control Effectiveness:** Strong (reduces risk from 20 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | G-Cloud accelerates, but negotiation risk remains |
| **Impact** | 4 - Major | Delay impact reduced by parallelization |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 40% reduction from inherent (20 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
Critical inherent risk successfully reduced to Medium through early start, framework use, and parallelization. Requires continued active management during procurement phase.

##### Risk Appetite Assessment

**Organizational Risk Appetite for STRATEGIC risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

**Escalation Required:** No - within appetite

##### Action Plan

1. **Start procurement Week 13 (immediately after Discovery Assessment)**
   - Owner: Procurement Specialist
   - Due Date: Week 13 (2025-01-28)
   - Success Criteria: SOW/RFP published within 2 weeks of Alpha start

2. **Use G-Cloud DOS framework**
   - Owner: Procurement Specialist
   - Due Date: Week 13
   - Success Criteria: Pre-approved supplier pool identified (≥5 suppliers)

3. **Fixed evaluation timeline (4 weeks maximum)**
   - Owner: Procurement Specialist
   - Due Date: Weeks 16-19
   - Success Criteria: Vendor selected by Week 20

---

#### R-013: Vendor Lock-In Limits Future Options

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Chief Data Architect
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
Proprietary cloud platform features or vendor-specific tooling creates lock-in, limiting future migration options and increasing switching costs. Could prevent multi-cloud strategy and increase vendor pricing power.

**Root Cause:**
Cloud-native design pressures to use managed services, time pressures favor quick solutions over portable ones, lack of abstraction layers.

**Trigger Events:**
- Heavy use of vendor-specific services (AWS Lambda, Azure Functions)
- Data stored in proprietary formats (DynamoDB, CosmosDB)
- Vendor pricing increases post-contract (year 2-3)
- Competitive cloud offering emerges with better features/pricing

**Consequences if Realized:**
- Switching costs £2M-£5M if re-platforming needed
- Vendor pricing power increases (40% price hikes observed in industry)
- Cannot adopt new cloud innovations from other providers
- Fails Architecture Principle 9 (Cloud-Native with portability)

**Affected Stakeholders:**
- **Chief Data Officer**: Long-term cost implications
- **Chief Data Architect**: Architecture integrity
- **Chief Technology Officer**: Strategic flexibility

**Related Objectives:**
- Principle 9 (Cloud-Native Architecture): Portability requirement

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Vendor lock-in common in cloud migrations |
| **Impact** | 4 - Major | Significant switching costs, pricing power loss |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Architecture Principle 9 requires abstraction layers**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Principle documented, HLD review validates

2. **Containerization (Docker/Kubernetes)**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Compute portability across providers

3. **Open standards for data formats (SDMX, CSV, JSON)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: Data portability maintained

**Overall Control Effectiveness:** Strong (reduces risk from 16 to 9)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Controls reduce but don't eliminate lock-in |
| **Impact** | 3 - Moderate | Portability layers reduce switching costs |
| **Residual Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 44% reduction from inherent (16 → 9)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for STRATEGIC risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 9 (Medium)
**Assessment:** ✅ **Within Appetite**

##### Action Plan

1. **HLD review validates abstraction layers**
   - Owner: Chief Data Architect
   - Due Date: Week 24 (HLD Review)
   - Success Criteria: No vendor-specific services without abstraction

2. **Contract includes exit rights and data portability clauses**
   - Owner: Procurement Specialist
   - Due Date: Week 20 (Vendor Selection)
   - Success Criteria: 90-day exit clause, data export in open formats

---

#### R-022: Funding Shortfall Impacts Delivery

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Chief Data Officer
**Action Owner:** Chief Data Officer

##### Risk Identification

**Risk Description:**
HM Treasury budget cuts or spending review changes funding allocation mid-programme, requiring scope reduction or programme pause. Could result from fiscal constraints, competing priorities, or PAC/NAO recommendations.

**Root Cause:**
Economic uncertainty, public spending pressures, long programme duration (18 months), cross-Parliament spending.

**Trigger Events:**
- Emergency budget / fiscal event
- Spending review reduces ONS allocation
- NAO value for money concerns
- PAC recommendations to pause programme

**Consequences if Realized:**
- Programme pause (6-12 months delay)
- Scope reduction (50% of statistical series migrated)
- Redundancy costs for contractors (£500K-£1M)
- Opportunity cost of delayed benefits (£4.5M annual savings)

**Affected Stakeholders:**
- **Chief Data Officer**: SRO accountability
- **National Statistician**: Strategic impact
- **HM Treasury**: Funding authority

**Related Objectives:**
- BR-001 (Reduce Infrastructure Costs by £4.5M annually)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Strong business case, statutory duties |
| **Impact** | 5 - Catastrophic | Programme failure |
| **Inherent Risk Score** | **10** (Medium) | 2 × 5 = 10 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Strong business case (£4.5M annual savings, 2.5 year payback)**
   - Owner: Chief Data Officer
   - Effectiveness: **Strong**
   - Evidence: SOBC approved

2. **ONS statutory duties require functioning infrastructure**
   - Owner: National Statistician
   - Effectiveness: **Strong**
   - Evidence: Statistics Act 2007

3. **Phased delivery enables scope flexibility**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Prioritized backlog

**Overall Control Effectiveness:** Strong (reduces risk from 10 to 8)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Statutory duties + ROI case strong |
| **Impact** | 4 - Major | Phased delivery reduces impact |
| **Residual Risk Score** | **8** (Medium) | 2 × 4 = 8 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 20% reduction from inherent (10 → 8)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

**Rationale:**
Strong business case and statutory duties make funding cut unlikely. Accept residual risk within appetite with monitoring of HMT signals.

##### Risk Appetite Assessment

**Organizational Risk Appetite for STRATEGIC risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 8 (Medium)
**Assessment:** ✅ **Within Appetite**

##### Action Plan

1. **Quarterly benefits realization reporting to HM Treasury**
   - Owner: Chief Data Officer
   - Due Date: Quarterly from Week 12
   - Success Criteria: HM Treasury confirm continued funding

---

### OPERATIONAL Risks

#### R-003: Data Migration Integrity Failures

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Chief Data Architect (from Stakeholder RACI: Accountable)
**Action Owner:** Data Engineers

##### Risk Identification

**Risk Description:**
Migration of 500+ statistical series from legacy systems results in data integrity errors (data loss, corruption, incorrect calculations). Could cause publication of inaccurate statistics, breaching ONS statutory duty and damaging public trust.

**Root Cause:**
Complex legacy systems (30+ years old), undocumented transformation logic, manual processes not captured in code, human error in migration scripts.

**Trigger Events:**
- Legacy system documentation incomplete/inaccurate
- Migration scripts contain logic errors
- Data validation rules miss edge cases
- Parallel running period too short to detect issues
- Statistician validation insufficient coverage

**Consequences if Realized:**
- Inaccurate statistics published (breach of Statistics Act 2007)
- UK Statistics Authority revokes ONS accreditation
- Parliamentary inquiry / PAC scrutiny
- Media coverage damages ONS reputation
- Loss of public trust in official statistics
- Legal liability for incorrect data affecting policy decisions
- Re-work costs £1M-£3M + 6-12 month delay

**Affected Stakeholders:**
- **Chief Statistician**: Regulatory accountability for statistical accuracy
- **National Statistician**: Public trust, ONS reputation
- **Chief Data Architect**: Technical delivery responsibility
- **Director of Statistical Production**: Operational delivery

**Related Objectives:**
- DR-005 (Data Migration with 100% integrity): Direct impact
- Principle 4 (Single Source of Truth): Integrity essential

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Complex migration, 500+ series, legacy complexity |
| **Impact** | 5 - Catastrophic | Regulatory breach, public trust damage |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

**Risk Zone:** 🟥 Critical (20-25)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Parallel running: legacy and new systems for 6 weeks validation**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Parallel running plan (Weeks 67-72)

2. **Automated data validation (record counts, checksums, sample verification)**
   - Owner: Data Engineers
   - Effectiveness: **Strong**
   - Evidence: Data validation framework specification

3. **Statistician sign-off for each migrated series (100% validation)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Strong**
   - Evidence: Sign-off workflow design

4. **Rollback capability if issues detected**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Rollback procedure documented

**Overall Control Effectiveness:** Strong (reduces risk from 20 to 15)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Comprehensive validation reduces likelihood |
| **Impact** | 5 - Catastrophic | Impact remains critical if occurs |
| **Residual Risk Score** | **15** (High) | 3 × 5 = 15 |

**Risk Zone:** 🟧 High (13-19)
**Risk Reduction:** 25% reduction from inherent (20 → 15)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
Catastrophic impact requires maximum mitigation. Extended parallel running and comprehensive validation reduce likelihood while maintaining ability to rollback if issues detected.

##### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 15 (High)
**Assessment:** ❌ **Exceeds Appetite** by 3 points (25% over threshold)

**Justification:**
Exceeding appetite is necessary given complexity of 500+ series migration. Comprehensive controls and parallel running provide defense-in-depth. Programme Board has approved proceeding with enhanced monitoring.

**Escalation Required:** Yes - Programme Board review monthly during Beta

##### Action Plan

**Additional Mitigations Needed:**

1. **Establish parallel running environment by Week 65**
   - Description: Legacy and new systems publishing simultaneously for validation
   - Owner: Chief Data Architect
   - Due Date: Week 65 (Beta Sprint 5)
   - Cost: £50K additional infrastructure
   - Expected Impact: Reduce likelihood to 2 (Unlikely)

2. **Develop comprehensive data validation framework**
   - Description: Automated validation for 100% of data quality dimensions
   - Owner: Data Engineers
   - Due Date: Week 50 (Beta Sprint 2)
   - Cost: Included in development effort
   - Expected Impact: Detect 99% of integrity issues before publication

3. **Statistician validation for 100% of migrated series**
   - Description: Series owner sign-off required before production use
   - Owner: Director of Statistical Production
   - Due Date: Weeks 67-72
   - Cost: 500 statistician-hours
   - Expected Impact: Human validation catches edge cases

4. **6-week parallel running period (extended from 4 weeks)**
   - Description: Extended validation period for high-risk series
   - Owner: Chief Data Architect
   - Due Date: Weeks 67-72
   - Cost: 2-week schedule buffer
   - Expected Impact: Detect slow-manifesting issues

**Target Residual Risk After Mitigations:**
- Target Likelihood: 2 (Unlikely)
- Target Impact: 5 (Catastrophic)
- Target Score: 10 (Medium) ✅ Close to appetite threshold

**Success Criteria:**
- Zero data integrity issues detected in weeks 5-6 of parallel running
- 100% statistician sign-off before go-live
- Rollback tested and validated

**Monitoring Plan:**
- **Frequency:** Weekly review during Beta, daily during parallel running
- **Key Indicators:**
  - Data validation error rate
  - Parallel running discrepancy count
  - Statistician sign-off progress (% complete)
- **Escalation Triggers:**
  - Any data integrity error in production-bound data
  - Parallel running discrepancy rate >0.1%
  - Statistician sign-off pace behind schedule

---

#### R-008: Legacy System Integration Failures

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Chief Data Architect
**Action Owner:** Data Engineers

##### Risk Identification

**Risk Description:**
Integrations with legacy ONS source systems (survey systems, admin data feeds) fail during implementation or operations, preventing data ingestion and publication. Could result from undocumented interfaces, legacy system changes, or authentication issues.

**Root Cause:**
Legacy systems (30+ years old), limited documentation, multiple integration points (7 systems), legacy owners lack API expertise.

**Trigger Events:**
- Legacy system owners change interface without notice
- Authentication credentials expire
- Legacy system capacity insufficient for API load
- Data format changes (CSV schema drift)
- Legacy system outage during critical publication window

**Consequences if Realized:**
- Publication delays (Statistics Act 2007 breach if >24 hours)
- Manual workarounds required (defeats automation objective)
- Statistical series unavailable (user impact)
- Reputational damage (ONS seen as unreliable)

**Affected Stakeholders:**
- **Chief Data Architect**: Technical delivery
- **Director of Statistical Production**: Operational delivery
- **Legacy System Owners**: Integration accountability

**Related Objectives:**
- INT-001 (Survey Data Integration)
- INT-002 (Admin Data Integration)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Multiple legacy integrations, limited documentation |
| **Impact** | 4 - Major | Publication delays, Statistics Act breach risk |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Integration testing in Sprint 5 (Week 59-62)**
   - Owner: Data Engineers
   - Effectiveness: **Adequate**
   - Evidence: Test plan

2. **Fallback procedures (manual file transfer)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: Fallback procedure documented

3. **Weekly coordination meetings with legacy owners**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Meeting schedule

**Overall Control Effectiveness:** Adequate (reduces risk from 16 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Testing and fallbacks reduce likelihood |
| **Impact** | 4 - Major | Impact remains if critical system fails |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (16 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

##### Action Plan

1. **Weekly coordination meetings with legacy system owners from Week 37**
   - Owner: Chief Data Architect
   - Due Date: Ongoing from Week 37
   - Success Criteria: No surprise interface changes, 4-week notice

2. **Comprehensive integration testing in Sprint 5**
   - Owner: Data Engineers
   - Due Date: Weeks 59-62
   - Success Criteria: All 7 integrations validated under load

3. **Fallback procedures documented and tested**
   - Owner: Director of Statistical Production
   - Due Date: Week 66
   - Success Criteria: Manual fallback completes publication within 8 hours

---

#### R-015: Skills Gap in Cloud-Native Technologies

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Chief Technology Officer
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
ONS team lacks sufficient cloud engineering expertise (Kubernetes, serverless, Infrastructure as Code, cloud security), requiring heavy vendor dependency and limiting operational effectiveness. Knowledge transfer from vendor insufficient.

**Root Cause:**
ONS historically on-premises infrastructure, limited cloud migration experience, civil service recruitment challenges, cloud skills shortage in market.

**Trigger Events:**
- Key vendor engineers leave mid-project
- Knowledge transfer insufficient (4 weeks planned)
- ONS engineers unable to operate platform independently
- Post-go-live operational issues require vendor escalation

**Consequences if Realized:**
- Extended vendor dependency (additional £500K-£1M annual cost)
- Slow operational response (MTTR >4 hours vs <30 minutes target)
- Cannot innovate post-go-live
- Business case ROI not achieved

**Affected Stakeholders:**
- **Chief Data Architect**: Operational readiness
- **Chief Technology Officer**: Skills strategy
- **Support team**: Operational capability

**Related Objectives:**
- BR-001 (Reduce Infrastructure Costs): Dependent on operational efficiency

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Cloud skills shortage, civil service constraints |
| **Impact** | 4 - Major | Operational dependency, cost impact |
| **Inherent Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Vendor knowledge transfer (20 days minimum)**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Contract requirement

2. **ONS engineers embedded with vendor during Beta**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: 8 engineers, 36 weeks

3. **Cloud training programme (certifications)**
   - Owner: Chief Technology Officer
   - Effectiveness: **Adequate**
   - Evidence: Training plan

**Overall Control Effectiveness:** Adequate (reduces risk from 12 to 9)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Training helps but cloud complexity remains |
| **Impact** | 3 - Moderate | Knowledge transfer reduces dependency |
| **Residual Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (12 → 9)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

**Rationale:**
Residual risk within appetite. Training and knowledge transfer provide reasonable mitigation. Accept some vendor dependency in early operations.

##### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 9 (Medium)
**Assessment:** ✅ **Within Appetite**

---

#### R-018: Statistician Resistance to New Workflow

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Director of Statistical Production
**Action Owner:** Director of Statistical Production

##### Risk Identification

**Risk Description:**
Statisticians resist adopting new automated publication workflow, preferring familiar manual processes. Could result in low adoption, parallel manual processes, and failure to achieve 60% efficiency gains.

**Root Cause:**
Change fatigue, fear of job security, lack of trust in automation, insufficient training, workflow doesn't match mental models.

**Trigger Events:**
- UAT feedback negative (workflows too complex)
- Training insufficient
- Automation errors early post-go-live (erodes trust)
- Key influencer statisticians resist publicly

**Consequences if Realized:**
- Low adoption rate (<50% vs 100% target)
- Efficiency gains not realized (60% objective fails)
- Business case ROI not achieved (BR-002 failure)

**Affected Stakeholders:**
- **Director of Statistical Production**: User adoption accountability
- **Statisticians**: 500 users affected
- **Chief Data Officer**: ROI accountability

**Related Objectives:**
- BR-002 (Improve Publication Efficiency by 60%)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Change resistance common, but engagement plan strong |
| **Impact** | 4 - Major | Business case failure if adoption low |
| **Inherent Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **User research in Discovery (Week 3-5)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Strong**
   - Evidence: User research report

2. **UAT engagement (20 statisticians, 3 weeks)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Strong**
   - Evidence: UAT plan

3. **Change champions (5 statisticians)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: Champion network identified

4. **Hypercare support (4 weeks intensive)**
   - Owner: Support team
   - Effectiveness: **Strong**
   - Evidence: Hypercare plan

**Overall Control Effectiveness:** Strong (reduces risk from 12 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Strong engagement reduces resistance |
| **Impact** | 3 - Moderate | Hypercare limits damage if occurs |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 50% reduction from inherent (12 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

**Rationale:**
Strong change management programme provides adequate mitigation. Accept residual risk with monitoring of adoption metrics post-go-live.

##### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite**

---

#### R-020: Key Team Members Leave During Implementation

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Chief Data Officer
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
Critical team members (Chief Data Architect, Technical Lead, Security Architect) leave ONS during Beta implementation, causing knowledge loss, delivery delays, and quality risks.

**Root Cause:**
Civil service turnover, competitive market for cloud skills, 18-month programme duration, contractor end-of-term.

**Trigger Events:**
- Chief Data Architect accepts private sector role
- Technical Lead promoted to different programme
- Security Architect contract expires

**Consequences if Realized:**
- Project delay (4-8 weeks to recruit replacement)
- Knowledge loss (undocumented design decisions)
- Team morale impact

**Affected Stakeholders:**
- **Chief Data Officer**: Delivery accountability
- **Chief Data Architect**: Team stability
- **Programme Board**: Oversight

**Related Objectives:**
- Project Timeline (78 weeks)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Some turnover expected but not mass exodus |
| **Impact** | 4 - Major | Critical path delay, knowledge loss |
| **Inherent Risk Score** | **8** (Medium) | 2 × 4 = 8 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Knowledge sharing (pair programming, code reviews)**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Engineering practices

2. **Documentation (ADRs)**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: ADR repository

3. **Succession planning (deputies identified)**
   - Owner: Chief Data Officer
   - Effectiveness: **Adequate**
   - Evidence: Succession plan

**Overall Control Effectiveness:** Adequate (reduces risk from 8 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Controls maintain stability |
| **Impact** | 3 - Moderate | Documentation reduces impact |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (8 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

##### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite**

---

### FINANCIAL Risks

#### R-007: Cloud Cost Overruns Exceed £6.7M Target

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** Chief Data Officer
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
Cloud infrastructure costs exceed £6.7M annual target due to inefficient resource usage, lack of cost optimization, or underestimated data volumes. Could result in business case failure (BR-001: 40% cost reduction not achieved).

**Root Cause:**
Cloud cost estimation uncertainty, data volume growth exceeds projections, inefficient resource provisioning, lack of FinOps culture.

**Trigger Events:**
- Data volumes grow faster than 20% projection (30-40% growth)
- Auto-scaling policies too aggressive (over-provisioning)
- Development/test environments not shut down after hours
- Vendor pricing changes
- Insufficient reserved instances (on-demand premium 40%)

**Consequences if Realized:**
- Annual costs £8M-£9M vs £6.7M target (20-35% overrun)
- Business case ROI not achieved (BR-001 failure)
- HM Treasury questions value for money
- PAC scrutiny of cost management

**Affected Stakeholders:**
- **Chief Data Officer**: Budget accountability
- **Chief Data Architect**: Architecture efficiency
- **HM Treasury**: Value for money oversight

**Related Objectives:**
- BR-001 (Reduce Infrastructure Costs by 40% to £6.7M annually)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Cloud cost overruns common (60% of organizations exceed budget) |
| **Impact** | 5 - Catastrophic | Business case failure, PAC scrutiny |
| **Inherent Risk Score** | **15** (High) | 3 × 5 = 15 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Monthly cost monitoring and reporting**
   - Owner: Chief Data Officer
   - Effectiveness: **Adequate**
   - Evidence: FinOps dashboard design

2. **FinOps controls and cost allocation**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Cost tagging strategy

3. **Budget alerts at 80%, 90%, 100%**
   - Owner: Chief Data Officer
   - Effectiveness: **Strong**
   - Evidence: Alert configuration

4. **Reserved instances for predictable workloads**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Reserved instance plan (70% target)

**Overall Control Effectiveness:** Adequate (reduces risk from 15 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Controls provide visibility but don't eliminate risk |
| **Impact** | 4 - Major | Business case impact but not catastrophic |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 20% reduction from inherent (15 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for FINANCIAL risks:** Medium (Score ≤ 9)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ⚠️ **Exceeds Appetite** by 3 points (33% over threshold)

**Justification:**
Financial risk slightly exceeds appetite but manageable with active FinOps controls. Monthly monitoring provides visibility for corrective action. Programme Board has approved with enhanced oversight.

**Escalation Required:** Yes - Monthly cost reporting to Programme Board

##### Action Plan

1. **Implement FinOps controls from Week 43**
   - Owner: Chief Data Officer
   - Due Date: Week 43 (Beta Sprint 1)
   - Success Criteria: Costs within 5% of budget monthly

2. **Reserved instance strategy (70% of compute)**
   - Owner: Chief Data Architect
   - Due Date: Week 73
   - Success Criteria: 30% cost saving on compute

3. **Quarterly cost optimization reviews**
   - Owner: Chief Data Architect
   - Due Date: Quarterly from Week 78
   - Success Criteria: Identify 10% optimization each quarter

---

#### R-011: Disaster Recovery Costs Higher Than Budgeted

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** Chief Data Architect
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
Disaster recovery infrastructure (multi-region deployment, backup storage, failover testing) costs significantly exceed £500K budget estimate due to underestimated storage volumes or vendor pricing.

**Root Cause:**
DR cost estimation uncertainty, backup retention requirements (7 years), geo-replication costs.

**Trigger Events:**
- Backup volumes exceed estimate (500TB → 750TB)
- Multi-region data transfer costs higher than projected
- Compliance requirements extend backup retention

**Consequences if Realized:**
- DR costs £1M-£1.5M vs £500K budget
- Budget reallocation required
- NFR-A-002 (RTO/RPO) at risk if budget cut

**Affected Stakeholders:**
- **Chief Data Officer**: Budget accountability
- **Chief Data Architect**: Architecture design
- **Head of Cyber Security**: Resilience requirements

**Related Objectives:**
- NFR-A-002 (Disaster Recovery with RTO 4 hours, RPO 1 hour)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | DR cost estimation challenging |
| **Impact** | 3 - Moderate | Budget impact but not catastrophic |
| **Inherent Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **DR architecture designed in HLD with cost estimates**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: HLD cost model

2. **UK availability zones only (no US/EU)**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Architecture decision

**Overall Control Effectiveness:** Adequate (reduces risk from 9 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | HLD cost validation reduces uncertainty |
| **Impact** | 3 - Moderate | Impact contained |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 33% reduction from inherent (9 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for FINANCIAL risks:** Medium (Score ≤ 9)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite**

---

#### R-014: HMRC/DWP API Access Costs Higher Than Expected

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** Chief Data Architect
**Action Owner:** Chief Data Architect

##### Risk Identification

**Risk Description:**
API access fees for admin data from HMRC, DWP, NHS exceed budget estimates due to data volume or pricing changes.

**Root Cause:**
API pricing uncertainty, data volume growth, no standard cross-government API pricing.

**Consequences if Realized:**
- API access costs £200K-£500K vs £100K budget

**Related Objectives:**
- INT-002 (Admin Data Integration)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Government APIs typically free/low-cost |
| **Impact** | 2 - Minor | Budget impact manageable |
| **Inherent Risk Score** | **4** (Low) | 2 × 2 = 4 |

**Risk Zone:** 🟩 Low (1-5)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Data sharing agreements negotiated in Alpha**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: DSA templates

**Overall Control Effectiveness:** Strong (maintains risk at 4)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Agreements provide pricing certainty |
| **Impact** | 2 - Minor | Impact remains low |
| **Residual Risk Score** | **4** (Low) | 2 × 2 = 4 |

**Risk Zone:** 🟩 Low (1-5)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

##### Risk Appetite Assessment

**Organizational Risk Appetite for FINANCIAL risks:** Medium (Score ≤ 9)
**Current Residual Risk Score:** 4 (Low)
**Assessment:** ✅ **Within Appetite**

---

### COMPLIANCE/REGULATORY Risks

#### R-004: GovS 007 ITHC Security Assessment Failure

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Head of Cyber Security
**Action Owner:** Security Engineer

##### Risk Identification

**Risk Description:**
IT Health Check (ITHC) penetration testing identifies critical or high-severity security vulnerabilities, blocking go-live and requiring remediation. Could delay production deployment by 4-8 weeks.

**Root Cause:**
Complex security requirements (Zero Trust, OFFICIAL classification), cloud security expertise gaps, tight timeline for hardening.

**Trigger Events:**
- ITHC finds critical vulnerabilities (SQL injection, XSS)
- Penetration testers identify cloud misconfigurations
- Security controls not implemented per GovS 007
- Remediation takes longer than 4-week buffer

**Consequences if Realized:**
- Go-live delayed by 4-8 weeks
- OFFICIAL accreditation withheld
- Re-work costs £200K-£500K
- HM Treasury questions governance

**Affected Stakeholders:**
- **Head of Cyber Security**: Security accreditation
- **Chief Data Officer**: Go-live accountability
- **NCSC**: Security oversight

**Related Objectives:**
- NFR-SEC-003 (Vulnerability Management)
- Principle 10 (Security by Design)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Complex cloud security, tight timeline |
| **Impact** | 4 - Major | Go-live delay, accreditation blocked |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Security by design from HLD**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: Security architecture

2. **Automated SAST/DAST scanning in CI/CD**
   - Owner: Security Engineer
   - Effectiveness: **Strong**
   - Evidence: Pipeline configuration

3. **Threat model (STRIDE) in Alpha**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: Threat model

4. **4-week remediation buffer**
   - Owner: Chief Data Officer
   - Effectiveness: **Adequate**
   - Evidence: Schedule buffer

**Overall Control Effectiveness:** Strong (reduces risk from 16 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Controls provide early detection |
| **Impact** | 4 - Major | Delay impact remains if critical findings |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (16 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for COMPLIANCE risks:** Low (Score ≤ 9)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ⚠️ **Exceeds Appetite** by 3 points (33% over threshold)

**Justification:**
Security assessment risk slightly exceeds compliance appetite due to complexity of Zero Trust implementation. Early testing (internal PT Week 68) and 4-week buffer provide mitigation. Head of Cyber Security approved proceeding.

**Escalation Required:** Yes - Monthly security status to Programme Board

##### Action Plan

1. **STRIDE threat model in Alpha**
   - Owner: Head of Cyber Security
   - Due Date: Weeks 19-21
   - Success Criteria: Security controls mapped to all threats

2. **Internal penetration testing 4 weeks before ITHC**
   - Owner: Head of Cyber Security
   - Due Date: Week 68
   - Success Criteria: Internal PT finds zero critical/high issues

---

#### R-005: GDS Service Standard Assessment Failure

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Director of Statistical Production
**Action Owner:** Service Owner

##### Risk Identification

**Risk Description:**
GDS Service Assessment at Beta phase fails to meet Service Standard criteria (14 points), requiring remediation before go-live.

**Root Cause:**
Service Standard criteria not embedded in delivery, insufficient user research, accessibility gaps, operational readiness not demonstrated.

**Trigger Events:**
- User research insufficient (<50 users)
- Accessibility WCAG 2.1 AA not met
- Technology choices not justified
- Operational support not demonstrated

**Consequences if Realized:**
- Go-live delayed by 4-8 weeks
- Failed assessment published on GOV.UK
- GDS Spend Control may block funding

**Affected Stakeholders:**
- **Director of Statistical Production**: Service Owner accountability
- **Chief Data Officer**: Overall accountability
- **GDS Service Assessor**: Assessment authority

**Related Objectives:**
- BR-004 (Meet UK Government Digital Standards)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Service Standard failure rate 20-30% |
| **Impact** | 5 - Catastrophic | Go-live blocked, policy non-compliance |
| **Inherent Risk Score** | **15** (High) | 3 × 5 = 15 |

**Risk Zone:** 🟧 High (13-19)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Service Standard evidence gathering from Discovery**
   - Owner: Service Owner
   - Effectiveness: **Strong**
   - Evidence: Evidence pack

2. **Mock assessment in Alpha (Week 26)**
   - Owner: Director of Statistical Production
   - Effectiveness: **Strong**
   - Evidence: Mock assessment plan

3. **Continuous user research throughout Beta**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: Research plan

4. **Accessibility testing in CI/CD**
   - Owner: QA Engineer
   - Effectiveness: **Strong**
   - Evidence: Accessibility test suite

**Overall Control Effectiveness:** Strong (reduces risk from 15 to 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Mock assessment reduces but doesn't eliminate risk |
| **Impact** | 4 - Major | Delay reduced through early preparation |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 20% reduction from inherent (15 → 12)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for COMPLIANCE risks:** Low (Score ≤ 9)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ⚠️ **Exceeds Appetite** by 3 points (33% over threshold)

**Justification:**
GDS assessment risk exceeds compliance appetite. Mock assessment in Alpha provides early gap identification. Service Owner approved proceeding with enhanced preparation.

**Escalation Required:** Yes - Mock assessment results to Programme Board

---

#### R-006: Statistics Act Pre-Release Access Breach

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Chief Statistician (from Stakeholder RACI: Accountable)
**Action Owner:** Security Engineer

##### Risk Identification

**Risk Description:**
Pre-release access controls fail, allowing unauthorized access to market-sensitive statistics before 9:30 AM publication time. Could breach Statistics Act 2007, resulting in UK Statistics Authority sanctions, ministerial questions, and loss of statistical independence.

**Root Cause:**
Complex pre-release access rules (24-hour maximum, designated user lists, audit trails), authentication failures, human error, insider threat.

**Trigger Events:**
- MFA authentication bypass or failure
- Audit logging gaps (access not recorded)
- Pre-release period exceeds 24 hours
- Designated user list not updated (wrong people have access)
- Insider deliberately leaks pre-release statistics

**Consequences if Realized:**
- UK Statistics Authority sanctions (ONS accreditation at risk)
- Parliamentary questions to National Statistician
- Cabinet Office inquiry
- Media coverage damages ONS independence
- Financial market impact (insider trading concerns)
- Legal liability (Statistics Act 2007 Section 11 breach)

**Affected Stakeholders:**
- **Chief Statistician**: Statistics Act compliance
- **National Statistician**: ONS accreditation
- **Chief Data Officer**: Platform accountability

**Related Objectives:**
- FR-004 (Pre-Release Access Control)
- NFR-C-002 (Statistics Act Compliance)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Complex controls, human factors, insider threat |
| **Impact** | 5 - Catastrophic | Regulatory breach, accreditation at risk |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

**Risk Zone:** 🟥 Critical (20-25)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Multi-factor authentication (MFA) required**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: MFA implementation spec

2. **Designated user lists maintained per series**
   - Owner: Chief Statistician
   - Effectiveness: **Adequate**
   - Evidence: Access control design

3. **Audit log of all pre-release access**
   - Owner: Security Engineer
   - Effectiveness: **Strong**
   - Evidence: Audit logging spec

4. **Automatic alert if pre-release exceeds 24 hours**
   - Owner: Security Engineer
   - Effectiveness: **Strong**
   - Evidence: Alert configuration

5. **Automatic public release at 9:30 AM**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Publication automation

**Overall Control Effectiveness:** Strong (reduces risk from 20 to 15)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Controls reduce but don't eliminate insider threat |
| **Impact** | 5 - Catastrophic | Impact remains critical if occurs |
| **Residual Risk Score** | **15** (High) | 3 × 5 = 15 |

**Risk Zone:** 🟧 High (13-19)
**Risk Reduction:** 25% reduction from inherent (20 → 15)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
Catastrophic impact requires maximum mitigation. MFA, audit logging, and automated release provide defense-in-depth. Insider threat cannot be fully eliminated.

##### Risk Appetite Assessment

**Organizational Risk Appetite for COMPLIANCE risks:** Low (Score ≤ 9)
**Current Residual Risk Score:** 15 (High)
**Assessment:** ❌ **Exceeds Appetite** by 6 points (67% over threshold)

**Justification:**
Statistics Act compliance risk significantly exceeds appetite due to catastrophic impact of breach. Comprehensive controls implemented but insider threat remains. UK Statistics Authority validation of controls provides external assurance. Chief Statistician and National Statistician have approved proceeding with enhanced monitoring.

**Escalation Required:** Yes - UK Statistics Authority validation required, monthly compliance reporting to Chief Statistician

##### Action Plan

**Additional Mitigations Needed:**

1. **Design pre-release access controls in Sprint 4**
   - Owner: Chief Statistician
   - Due Date: Weeks 55-58
   - Success Criteria: Controls meet Statistics Act requirements

2. **UK Statistics Authority validation of controls**
   - Owner: Chief Statistician
   - Due Date: Week 65
   - Success Criteria: UK Statistics Authority sign-off

3. **Real-time audit monitoring dashboard**
   - Owner: Security Engineer
   - Due Date: Week 66
   - Success Criteria: Security team monitors pre-release access in real-time

4. **UAT validation with statisticians**
   - Owner: Chief Statistician
   - Due Date: Weeks 70-72
   - Success Criteria: Zero breaches in testing

**Target Residual Risk After Mitigations:**
- Target Likelihood: 2 (Unlikely)
- Target Impact: 5 (Catastrophic)
- Target Score: 10 (Medium) - Still exceeds appetite but reduced

**Success Criteria:**
- UK Statistics Authority validates controls meet statutory requirements
- Zero pre-release access incidents in UAT
- 100% audit trail coverage demonstrated

**Monitoring Plan:**
- **Frequency:** Real-time monitoring, weekly review with Chief Statistician
- **Key Indicators:**
  - Pre-release access attempts (authorized and unauthorized)
  - Audit log completeness (100% coverage)
  - Pre-release period duration (<24 hours)
- **Escalation Triggers:**
  - Any unauthorized access attempt
  - Any audit logging gap
  - Pre-release period exceeds 23 hours (warning)

---

#### R-017: SDMX Metadata Compliance Failure

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Director of Statistical Production
**Action Owner:** Data Engineers

##### Risk Identification

**Risk Description:**
Published statistical metadata does not comply with SDMX standard, preventing interoperability with Eurostat, UN, OECD systems.

**Root Cause:**
SDMX complexity, limited ONS SDMX expertise, metadata generation not automated.

**Consequences if Realized:**
- Eurostat/UN/OECD integration delayed
- International partners cannot consume ONS data
- Re-work costs £100K-£300K

**Related Objectives:**
- DR-004 (SDMX Metadata)
- Principle 8 (Interoperability)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | SDMX complexity, limited expertise |
| **Impact** | 3 - Moderate | Interoperability impact, re-work costs |
| **Inherent Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **SDMX metadata generation automated in Sprint 4**
   - Owner: Data Engineers
   - Effectiveness: **Adequate**
   - Evidence: Sprint plan

2. **Eurostat validation tools**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: Validation process

**Overall Control Effectiveness:** Adequate (reduces risk from 9 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Automation + validation reduces errors |
| **Impact** | 3 - Moderate | Impact remains if occurs |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 33% reduction from inherent (9 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for COMPLIANCE risks:** Low (Score ≤ 9)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite**

---

#### R-021: Judicial Review of Procurement Process

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Procurement Specialist
**Action Owner:** Procurement Specialist

##### Risk Identification

**Risk Description:**
Unsuccessful vendor challenges procurement process via judicial review, alleging unfair evaluation or process irregularities.

**Root Cause:**
Public sector procurement transparency, high-value contract, competitive market.

**Consequences if Realized:**
- Procurement paused for 6-12 months
- Legal costs £50K-£200K
- Programme delay

**Related Objectives:**
- Vendor Procurement (Alpha Weeks 13-20)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 - Rare | Judicial reviews uncommon (5% of procurements) |
| **Impact** | 5 - Catastrophic | Programme pause, significant delay |
| **Inherent Risk Score** | **5** (Low) | 1 × 5 = 5 |

**Risk Zone:** 🟩 Low (1-5)

##### Current Controls and Mitigations

**Existing Controls:**
1. **G-Cloud framework (pre-approved process)**
   - Owner: Procurement Specialist
   - Effectiveness: **Strong**
   - Evidence: Framework terms

2. **Objective evaluation criteria published**
   - Owner: Procurement Specialist
   - Effectiveness: **Strong**
   - Evidence: RFP documentation

3. **Legal review of procurement process**
   - Owner: Procurement Specialist
   - Effectiveness: **Strong**
   - Evidence: Legal sign-off

**Overall Control Effectiveness:** Strong (reduces risk from 5 to 4)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 - Rare | Framework + transparency minimize risk |
| **Impact** | 4 - Major | Delay reduced through strong process |
| **Residual Risk Score** | **4** (Low) | 1 × 4 = 4 |

**Risk Zone:** 🟩 Low (1-5)
**Risk Reduction:** 20% reduction from inherent (5 → 4)

##### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

##### Risk Appetite Assessment

**Organizational Risk Appetite for COMPLIANCE risks:** Low (Score ≤ 9)
**Current Residual Risk Score:** 4 (Low)
**Assessment:** ✅ **Within Appetite**

---

### TECHNOLOGY Risks

#### R-009: API Traffic Spike Handling Failure

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** Chief Data Architect
**Action Owner:** DevOps Engineer

##### Risk Identification

**Risk Description:**
Platform fails to handle peak publication load (10,000 requests/second) for major economic releases, resulting in service degradation or outage.

**Root Cause:**
Auto-scaling insufficient, load testing doesn't replicate real traffic patterns, caching ineffective.

**Trigger Events:**
- Major release generates 20,000 req/s (2x projection)
- Auto-scaling too slow (<5 minute response exceeded)
- Database query performance degrades
- CDN cache not configured correctly

**Consequences if Realized:**
- API outage during publication window (Statistics Act breach)
- Media coverage ("ONS website crashes")
- Availability SLA breach (99.95% not met)

**Affected Stakeholders:**
- **Chief Data Architect**: Platform performance
- **Director of Statistical Production**: Publication reliability
- **Data users**: API consumers affected

**Related Objectives:**
- NFR-P-003 (Handle 10,000 req/s peak load)
- NFR-A-001 (99.95% availability)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Traffic spikes unpredictable |
| **Impact** | 4 - Major | Statistics Act breach, reputational damage |
| **Inherent Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Load testing in Beta (10,000 req/s)**
   - Owner: QA/Test Engineer
   - Effectiveness: **Adequate**
   - Evidence: Load test plan

2. **Auto-scaling policies**
   - Owner: DevOps Engineer
   - Effectiveness: **Adequate**
   - Evidence: Scaling configuration

3. **CDN caching**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: CDN strategy

4. **Burst capacity to 20,000 req/s**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Capacity planning

**Overall Control Effectiveness:** Adequate (maintains risk at 12)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Testing reduces but doesn't eliminate risk |
| **Impact** | 4 - Major | Impact remains if spike exceeds capacity |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 0% (controls prevent degradation, not inherent risk)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for TECHNOLOGY risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 12 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

##### Action Plan

1. **Load testing with realistic publication traffic**
   - Owner: QA/Test Engineer
   - Due Date: Week 71
   - Success Criteria: 10,000 req/s sustained, 20,000 req/s burst

2. **Auto-scaling validation (<5 minutes)**
   - Owner: DevOps Engineer
   - Due Date: Week 71
   - Success Criteria: Capacity doubles within 5 minutes

3. **CDN caching for top 20 endpoints**
   - Owner: Chief Data Architect
   - Due Date: Week 66
   - Success Criteria: 80% cache hit rate

---

#### R-010: Census-Scale Performance Failure

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** Chief Data Architect (from Stakeholder RACI: Accountable)
**Action Owner:** Data Engineers

##### Risk Identification

**Risk Description:**
Platform fails to process census-scale datasets (67 million records) within 24-hour target, failing BR-005 and preventing near-real-time census statistics for 2031 Census.

**Root Cause:**
Underestimated processing complexity, insufficient parallelization, database write throughput limits.

**Trigger Events:**
- Census prototype in Alpha fails to meet 24-hour target
- Load testing shows linear scaling breaks at 50M records
- Data quality validation takes 12 hours (50% of budget)
- SDC processing too slow (not parallelized)

**Consequences if Realized:**
- 2031 Census statistics delayed by weeks/months
- BR-005 objective failure
- Re-architecture required (£500K-£1M, 6-12 month delay)

**Affected Stakeholders:**
- **Chief Data Architect**: Technical delivery
- **Census Programme Director**: 2031 Census
- **Chief Data Officer**: Strategic objective

**Related Objectives:**
- BR-005 (Enable Census-Scale Processing <24 hours)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Census-scale processing complex, limited prototyping |
| **Impact** | 5 - Catastrophic | Strategic objective failure, re-architecture |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

**Risk Zone:** 🟥 Critical (20-25)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Early performance prototyping in Alpha (Week 20-24)**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: Prototype plan

2. **Scalability testing to 100M records**
   - Owner: QA/Test Engineer
   - Effectiveness: **Strong**
   - Evidence: Load test plan

3. **Distributed processing framework (Spark/Dask)**
   - Owner: Data Engineers
   - Effectiveness: **Strong**
   - Evidence: Architecture decision

4. **Data partitioning strategy**
   - Owner: Chief Data Architect
   - Effectiveness: **Adequate**
   - Evidence: Data model

**Overall Control Effectiveness:** Strong (reduces risk from 20 to 15)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Early testing reduces risk |
| **Impact** | 5 - Catastrophic | Impact remains critical if occurs |
| **Residual Risk Score** | **15** (High) | 3 × 5 = 15 |

**Risk Zone:** 🟧 High (13-19)
**Risk Reduction:** 25% reduction from inherent (20 → 15)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
Strategic objective (BR-005) at risk. Early prototyping in Alpha provides fail-fast validation. If prototype fails, architecture can be adjusted before Beta commitment.

##### Risk Appetite Assessment

**Organizational Risk Appetite for TECHNOLOGY risks:** Medium (Score ≤ 12)
**Current Residual Risk Score:** 15 (High)
**Assessment:** ❌ **Exceeds Appetite** by 3 points (25% over threshold)

**Justification:**
Census-scale processing risk exceeds technology appetite due to strategic importance of BR-005 for 2031 Census. Early prototyping in Alpha provides validation before major investment. Programme Board has approved proceeding with enhanced testing.

**Escalation Required:** Yes - Programme Board review of Alpha prototype results

##### Action Plan

**Additional Mitigations Needed:**

1. **Early performance prototyping in Alpha (Week 20-24)**
   - Description: 67M record prototype completes in <24 hours
   - Owner: Chief Data Architect
   - Due Date: Weeks 20-24
   - Cost: £50K prototype infrastructure
   - Expected Impact: Validate architecture before Beta

2. **Scalability testing to 100M records**
   - Description: Linear scaling demonstrated
   - Owner: QA/Test Engineer
   - Due Date: Week 71
   - Cost: Included in testing effort
   - Expected Impact: Validate headroom for future growth

3. **Distributed processing framework (Spark/Dask)**
   - Description: Processing parallelized across 50+ nodes
   - Owner: Data Engineers
   - Due Date: Week 50
   - Cost: Included in development
   - Expected Impact: Enable horizontal scaling

**Target Residual Risk After Mitigations:**
- Target Likelihood: 2 (Unlikely)
- Target Impact: 5 (Catastrophic)
- Target Score: 10 (Medium) - Closer to appetite threshold

**Success Criteria:**
- Alpha prototype: 67M records processed in <24 hours
- Beta load test: 100M records processed in <36 hours
- Linear scaling demonstrated from 10M to 100M records

**Monitoring Plan:**
- **Frequency:** Weekly during Alpha prototype, bi-weekly during Beta
- **Key Indicators:**
  - Processing time per million records
  - Scaling efficiency (time vs. data volume)
  - Resource utilization (CPU, memory, I/O)
- **Escalation Triggers:**
  - Alpha prototype exceeds 30 hours
  - Scaling non-linear (exponential growth)
  - Resource bottleneck identified with no solution

---

### REPUTATIONAL Risks

#### R-012: Cyber Security Breach of Pre-Release Data

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** Head of Cyber Security
**Action Owner:** Security Engineer

##### Risk Identification

**Risk Description:**
Cyber attack successfully breaches ONS platform and exfiltrates pre-release market-sensitive statistics, resulting in insider trading, financial market disruption, and catastrophic reputational damage.

**Root Cause:**
High-value target, nation-state APT capability, insider threat, zero-day exploits.

**Trigger Events:**
- Nation-state APT targets ONS
- Phishing attack compromises credentials (MFA bypass)
- Zero-day exploit in cloud platform
- Insider deliberately exfiltrates data
- Ransomware attack

**Consequences if Realized:**
- Pre-release statistics leaked to financial markets
- Financial market disruption (FCA investigation)
- Parliamentary inquiry / Cabinet Office investigation
- NCSC incident response
- UK Statistics Authority revokes accreditation
- Public trust destroyed

**Affected Stakeholders:**
- **Chief Statistician**: Regulatory accountability
- **National Statistician**: ONS reputation
- **Head of Cyber Security**: Security breach
- **NCSC**: National security

**Related Objectives:**
- NFR-SEC-001 (Zero Trust Architecture)
- Principle 10 (Security by Design)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | High-value target, nation-state APT capability |
| **Impact** | 5 - Catastrophic | National security, public trust destroyed |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

**Risk Zone:** 🟥 Critical (20-25)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Zero Trust architecture**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: Zero Trust design

2. **Multi-factor authentication (MFA)**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: MFA implementation

3. **Network segmentation**
   - Owner: Security Engineer
   - Effectiveness: **Strong**
   - Evidence: Network architecture

4. **Encryption at rest (AES-256) and in transit (TLS 1.3+)**
   - Owner: Security Engineer
   - Effectiveness: **Strong**
   - Evidence: Encryption spec

5. **SIEM real-time monitoring (24/7)**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: SIEM implementation

6. **Penetration testing (annual external, quarterly internal)**
   - Owner: Head of Cyber Security
   - Effectiveness: **Strong**
   - Evidence: PT schedule

7. **Cyber insurance (£10M coverage)**
   - Owner: Chief Data Officer
   - Effectiveness: **Adequate**
   - Evidence: Insurance policy

**Overall Control Effectiveness:** Strong (reduces risk from 20 to 10)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Zero Trust significantly reduces attack surface |
| **Impact** | 5 - Catastrophic | Impact remains catastrophic if occurs |
| **Residual Risk Score** | **10** (Medium) | 2 × 5 = 10 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 50% reduction from inherent (20 → 10)

##### Risk Response (4Ts Framework)

**Primary Response:** TRANSFER (partial via cyber insurance) + TREAT

**Rationale:**
Zero Trust architecture provides strong prevention. Cyber insurance provides financial recovery for breach costs. Combination of treatment and transfer addresses both prevention and recovery.

##### Risk Appetite Assessment

**Organizational Risk Appetite for REPUTATIONAL risks:** Low (Score ≤ 6)
**Current Residual Risk Score:** 10 (Medium)
**Assessment:** ⚠️ **Exceeds Appetite** by 4 points (67% over threshold)

**Justification:**
Cyber breach risk exceeds reputational appetite due to catastrophic impact even with comprehensive controls. Zero Trust and cyber insurance provide maximum practical mitigation. National Statistician has approved proceeding with 24/7 SOC monitoring.

**Escalation Required:** Yes - Immediate escalation to NCSC if breach suspected

##### Action Plan

1. **Zero Trust architecture implementation**
   - Owner: Head of Cyber Security
   - Due Date: Week 66
   - Success Criteria: All controls per NFR-SEC-001

2. **Penetration testing**
   - Owner: Head of Cyber Security
   - Due Date: Weeks 68, 72
   - Success Criteria: Zero critical/high findings

3. **Cyber insurance (£10M coverage)**
   - Owner: Chief Data Officer
   - Due Date: Week 73
   - Success Criteria: Coverage includes breach, interruption, response

4. **SIEM 24/7 monitoring**
   - Owner: Head of Cyber Security
   - Due Date: Week 73
   - Success Criteria: SOC operational 24/7

---

#### R-016: Social Media Backlash from Service Failure

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** Director of Statistical Production
**Action Owner:** Communications Team

##### Risk Identification

**Risk Description:**
High-profile service outage or data error triggers social media backlash, damaging ONS reputation and eroding public trust.

**Root Cause:**
Heightened social media scrutiny, 24/7 news cycle, low tolerance for government failures.

**Consequences if Realized:**
- Social media trending topic
- Media amplification
- Parliamentary questions
- User confidence eroded

**Affected Stakeholders:**
- **National Statistician**: Public trust
- **Director of Statistical Production**: Service delivery
- **Data users**: Public, media, researchers

**Related Objectives:**
- BR-003 (Enhance Public Data Access)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Comprehensive testing reduces outage risk |
| **Impact** | 4 - Major | Reputational damage significant |
| **Inherent Risk Score** | **8** (Medium) | 2 × 4 = 8 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **Comprehensive testing**
   - Owner: QA Engineer
   - Effectiveness: **Strong**
   - Evidence: Test strategy

2. **Availability SLA (99.95%)**
   - Owner: Chief Data Architect
   - Effectiveness: **Strong**
   - Evidence: SLA design

3. **Hypercare support (4 weeks)**
   - Owner: Support team
   - Effectiveness: **Strong**
   - Evidence: Hypercare plan

4. **Incident response plan**
   - Owner: Director of Statistical Production
   - Effectiveness: **Adequate**
   - Evidence: IR plan

**Overall Control Effectiveness:** Strong (reduces risk from 8 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Controls maintain reliability |
| **Impact** | 3 - Moderate | Rapid response reduces impact |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 25% reduction from inherent (8 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for REPUTATIONAL risks:** Low (Score ≤ 6)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

---

#### R-019: Research Community Access Issues

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** Director of Statistical Production
**Action Owner:** Data Engineers

##### Risk Identification

**Risk Description:**
Integration with Secure Research Service (SRS) fails or is delayed, preventing approved researchers from accessing anonymised microdata.

**Root Cause:**
SRS integration complexity, Five Safes framework implementation challenges.

**Consequences if Realized:**
- Research community unable to access data
- Academic publications delayed
- ONS reputation in research community damaged

**Affected Stakeholders:**
- **Director of Statistical Production**: Research access
- **Researchers**: 1,000+ users
- **Research funding bodies**: UKRI, Wellcome

**Related Objectives:**
- INT-004 (Research Access Integration)

##### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | SHOULD_HAVE requirement, lower priority |
| **Impact** | 3 - Moderate | Research impact but not critical |
| **Inherent Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Zone:** 🟨 Medium (6-12)

##### Current Controls and Mitigations

**Existing Controls:**
1. **SRS integration in Sprint 5**
   - Owner: Data Engineers
   - Effectiveness: **Adequate**
   - Evidence: Sprint plan

**Overall Control Effectiveness:** Adequate (reduces risk from 9 to 6)

##### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Sprint 5 allocation sufficient |
| **Impact** | 3 - Moderate | Impact contained |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Zone:** 🟨 Medium (6-12)
**Risk Reduction:** 33% reduction from inherent (9 → 6)

##### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

##### Risk Appetite Assessment

**Organizational Risk Appetite for REPUTATIONAL risks:** Low (Score ≤ 6)
**Current Residual Risk Score:** 6 (Medium)
**Assessment:** ✅ **Within Appetite** (at threshold)

---

## D. Risk Category Analysis

### STRATEGIC Risks (4 risks)

**Total STRATEGIC Risks:** 4
**Average Inherent Score:** 15.3 (High)
**Average Residual Score:** 10.3 (Medium)
**Control Effectiveness:** 33% reduction

**Risk List:**
- R-001: Strategic Direction Change - Residual: 12 (Medium)
- R-002: Vendor Procurement Delays - Residual: 12 (Medium)
- R-013: Vendor Lock-In - Residual: 9 (Medium)
- R-022: Funding Shortfall - Residual: 8 (Medium)

**Key Themes:**
- Policy/ministerial direction changes (R-001)
- Vendor procurement and lock-in (R-002, R-013)
- Funding stability (R-022)

**Category Risk Profile:** ✅ Acceptable - All risks within appetite, monitoring required

---

### OPERATIONAL Risks (5 risks)

**Total OPERATIONAL Risks:** 5
**Average Inherent Score:** 13.6 (High)
**Average Residual Score:** 9.6 (Medium)
**Control Effectiveness:** 29% reduction

**Risk List:**
- R-003: Data Migration Integrity - Residual: 15 (High) ⚠️
- R-008: Legacy Integration - Residual: 12 (Medium)
- R-015: Skills Gap - Residual: 9 (Medium)
- R-018: Statistician Resistance - Residual: 6 (Medium)
- R-020: Key Staff Departure - Residual: 6 (Medium)

**Key Themes:**
- Data migration integrity (R-003 - HIGH residual, critical attention)
- Legacy system integration (R-008)
- Skills and change management (R-015, R-018, R-020)

**Category Risk Profile:** ⚠️ Concerning - R-003 exceeds appetite, requires escalation

---

### FINANCIAL Risks (3 risks)

**Total FINANCIAL Risks:** 3
**Average Inherent Score:** 9.3 (Medium)
**Average Residual Score:** 7.3 (Medium)
**Control Effectiveness:** 22% reduction

**Risk List:**
- R-007: Cloud Cost Overruns - Residual: 12 (Medium) ⚠️
- R-011: DR Costs - Residual: 6 (Medium)
- R-014: API Access Costs - Residual: 4 (Low)

**Key Themes:**
- Cloud cost management (R-007 - exceeds appetite)
- Disaster recovery costs (R-011)
- Integration costs (R-014)

**Category Risk Profile:** ⚠️ Concerning - R-007 exceeds financial appetite (≤9)

---

### COMPLIANCE/REGULATORY Risks (5 risks)

**Total COMPLIANCE Risks:** 5
**Average Inherent Score:** 13.0 (High)
**Average Residual Score:** 9.8 (Medium)
**Control Effectiveness:** 25% reduction

**Risk List:**
- R-006: Statistics Act Breach - Residual: 15 (High) ⚠️
- R-004: GovS 007 ITHC Failure - Residual: 12 (Medium) ⚠️
- R-005: GDS Assessment Failure - Residual: 12 (Medium) ⚠️
- R-017: SDMX Compliance - Residual: 6 (Medium)
- R-021: Judicial Review - Residual: 4 (Low)

**Key Themes:**
- Statistics Act compliance (R-006 - HIGH, critical importance)
- Security and service assessments (R-004, R-005 - exceed appetite)
- Metadata and procurement compliance (R-017, R-021)

**Category Risk Profile:** ❌ Unacceptable - 3 risks exceed compliance appetite (≤9), escalation required

---

### TECHNOLOGY Risks (4 risks)

**Total TECHNOLOGY Risks:** 4
**Average Inherent Score:** 16.0 (High)
**Average Residual Score:** 12.0 (Medium)
**Control Effectiveness:** 25% reduction

**Risk List:**
- R-010: Census Performance - Residual: 15 (High) ⚠️
- R-009: API Traffic Spikes - Residual: 12 (Medium)
- R-013: Vendor Lock-In - Residual: 9 (Medium) (also Strategic)

**Key Themes:**
- Census-scale processing (R-010 - HIGH, strategic importance)
- Traffic handling (R-009)
- Vendor portability (R-013)

**Category Risk Profile:** ⚠️ Concerning - R-010 exceeds technology appetite (≤12)

---

### REPUTATIONAL Risks (3 risks)

**Total REPUTATIONAL Risks:** 3
**Average Inherent Score:** 12.3 (Medium/High)
**Average Residual Score:** 7.3 (Medium)
**Control Effectiveness:** 41% reduction

**Risk List:**
- R-012: Cyber Security Breach - Residual: 10 (Medium) ⚠️
- R-016: Social Media Backlash - Residual: 6 (Medium)
- R-019: Research Access - Residual: 6 (Medium)

**Key Themes:**
- Cyber security (R-012 - exceeds appetite despite strong controls)
- Service reliability (R-016)
- Research community relationship (R-019)

**Category Risk Profile:** ⚠️ Concerning - R-012 exceeds reputational appetite (≤6)

---

## E. Risk Ownership Matrix

**Risk Ownership Distribution by Stakeholder:**

| Stakeholder | Role | Owned Risks | Critical | High | Medium | Low | Total Residual | Risk Concentration |
|-------------|------|-------------|----------|------|--------|-----|----------------|-------------------|
| Chief Data Architect | Technical Lead | R-003, R-008, R-009, R-010, R-011, R-013 | 0 | 2 | 4 | 0 | 63 | ⚠️ High concentration |
| Chief Data Officer | SRO | R-001, R-007, R-022 | 0 | 0 | 3 | 0 | 32 | Moderate |
| Chief Statistician | Regulatory Lead | R-006 | 0 | 1 | 0 | 0 | 15 | Focused - critical risk |
| Head of Cyber Security | Security Lead | R-004, R-012 | 0 | 0 | 2 | 0 | 22 | Moderate |
| Director of Statistical Production | Service Owner | R-005, R-016, R-017, R-018, R-019 | 0 | 0 | 5 | 0 | 30 | Moderate |
| Procurement Specialist | Procurement Lead | R-002, R-021 | 0 | 0 | 1 | 1 | 16 | Low |
| Chief Technology Officer | Skills Lead | R-015 | 0 | 0 | 1 | 0 | 9 | Low |
| Multiple owners | Various | R-014, R-020 | 0 | 0 | 1 | 1 | 10 | Low |

**Risk Concentration Analysis:**
- ⚠️ **Chief Data Architect owns 6 risks totaling 63 points** - Consider delegating R-011 (DR costs) to financial owner
- **Chief Statistician owns 1 HIGH risk (R-006)** - Critical Statistics Act compliance, appropriate ownership
- **Good distribution across categories** - No single owner overwhelmed except technical lead

**Escalation Paths:**
- **Critical/High Strategic Risks** → Chief Data Officer → Programme Board → HM Treasury
- **Critical/High Technology Risks** → Chief Data Architect → Programme Board
- **All Compliance Risks** → Risk Owner → Programme Board → Audit Committee (if exceeds appetite)
- **Statistics Act Risks** → Chief Statistician → National Statistician → UK Statistics Authority

---

## F. 4Ts Response Framework Summary

**Risk Response Distribution:**

| Response | Count | % | Total Residual Score | Key Examples |
|----------|-------|---|----------------------|--------------|
| **TOLERATE** | 4 | 18% | 27 (Low-Medium) | R-014, R-015, R-018, R-020, R-022 - Low risks within appetite |
| **TREAT** | 16 | 73% | 162 (Medium-High) | R-001, R-002, R-003, R-004, R-005, R-006, R-007, R-008, R-009, R-010, R-011, R-013, R-016, R-017, R-019 - Active mitigation |
| **TRANSFER** | 2 | 9% | 18 (Medium) | R-012 (Cyber insurance), R-002 (Vendor liability) - Risk shared with 3rd parties |
| **TERMINATE** | 0 | 0% | 0 | None - No activities require termination |
| **TOTAL** | 22 | 100% | 207 | |

**Response Breakdown by Category:**

| Category | Tolerate | Treat | Transfer | Terminate | Predominant Response |
|----------|----------|-------|----------|-----------|---------------------|
| STRATEGIC | 1 | 3 | 0 | 0 | Treat (75%) |
| OPERATIONAL | 3 | 2 | 0 | 0 | Tolerate (60%) |
| FINANCIAL | 1 | 2 | 0 | 0 | Treat (67%) |
| COMPLIANCE | 1 | 4 | 0 | 0 | Treat (80%) |
| TECHNOLOGY | 0 | 3 | 0 | 0 | Treat (100%) |
| REPUTATIONAL | 0 | 2 | 1 | 0 | Treat (67%) |

**Key Insights:**
- **73% of risks require active treatment** - Significant mitigation effort needed
- **18% can be tolerated** - Indicates manageable risk environment with appropriate controls
- **9% transferred via insurance/contracts** - Appropriate use of risk transfer for catastrophic events
- **Zero terminations** - All risks manageable, no activities require stopping

---

## G. Risk Appetite Compliance

**Organizational Risk Appetite Thresholds:**

| Category | Appetite Level | Threshold Score | Description |
|----------|---------------|-----------------|-------------|
| STRATEGIC | Medium | ≤ 12 | Willing to accept medium strategic risks for transformation |
| OPERATIONAL | Medium | ≤ 12 | Moderate tolerance for operational disruption |
| FINANCIAL | Medium | ≤ 9 | Conservative financial risk for public funds |
| COMPLIANCE | Low | ≤ 9 | Minimal tolerance for regulatory breaches |
| REPUTATIONAL | Low | ≤ 6 | Low tolerance for reputational damage |
| TECHNOLOGY | Medium | ≤ 12 | Willing to adopt new technology with controls |

**Compliance Summary:**

| Category | Appetite | Risks Within | Risks Exceeding | Avg Excess | Action Required |
|----------|----------|--------------|-----------------|------------|-----------------|
| STRATEGIC | ≤ 12 | 4 (100%) | 0 (0%) | N/A | ✅ Compliant |
| OPERATIONAL | ≤ 12 | 4 (80%) | 1 (20%) | +3 points | ⚠️ R-003 escalation required |
| FINANCIAL | ≤ 9 | 2 (67%) | 1 (33%) | +3 points | ⚠️ R-007 CFO approval required |
| COMPLIANCE | ≤ 9 | 2 (40%) | 3 (60%) | +4 points | ❌ Multiple escalations required |
| REPUTATIONAL | ≤ 6 | 2 (67%) | 1 (33%) | +4 points | ⚠️ R-012 escalation required |
| TECHNOLOGY | ≤ 12 | 2 (67%) | 1 (33%) | +3 points | ⚠️ R-010 escalation required |

**Overall Appetite Compliance:** ⚠️ 32% of risks (7 of 22) exceed category appetite

**Risks Significantly Exceeding Appetite (>50% over threshold):**

| Risk ID | Category | Appetite | Actual | Excess | % Over | Escalation |
|---------|----------|----------|--------|--------|--------|------------|
| R-006 | COMPLIANCE | 9 | 15 | +6 | 67% | ❌ UK Statistics Authority validation required |
| R-012 | REPUTATIONAL | 6 | 10 | +4 | 67% | ⚠️ National Statistician approval obtained |
| R-007 | FINANCIAL | 9 | 12 | +3 | 33% | ⚠️ CFO approval required |
| R-004 | COMPLIANCE | 9 | 12 | +3 | 33% | ⚠️ Head of Cyber Security approved |
| R-005 | COMPLIANCE | 9 | 12 | +3 | 33% | ⚠️ Service Owner approved |
| R-003 | OPERATIONAL | 12 | 15 | +3 | 25% | ⚠️ Programme Board review monthly |
| R-010 | TECHNOLOGY | 12 | 15 | +3 | 25% | ⚠️ Programme Board review of Alpha prototype |

**Recommendations:**
1. **URGENT**: Obtain UK Statistics Authority validation for R-006 (Statistics Act) - 67% over appetite
2. **HIGH PRIORITY**: Monthly Programme Board review of R-003, R-010 exceeding operational/technology appetite
3. **MONITOR**: R-012 (Cyber breach) - National Statistician approval obtained, 24/7 SOC monitoring

---

## H. Prioritized Action Plan

### Priority 1: URGENT (Critical Risks or Significant Appetite Exceedance)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Cost | Expected Impact | Status |
|----------|--------|-------------------|-------|----------|------|-----------------|--------|
| 1 | Establish parallel running environment | R-003 (Data Migration - HIGH) | Chief Data Architect | Week 65 | £50K | Reduce from 15 to 10 | Open |
| 2 | UK Statistics Authority validation of pre-release controls | R-006 (Statistics Act - HIGH) | Chief Statistician | Week 65 | Staff time | External assurance | Open |
| 3 | Early census-scale performance prototyping | R-010 (Census - HIGH) | Chief Data Architect | Weeks 20-24 | £50K | Validate architecture | Open |

**Total Urgent Actions:** 3
**Total Cost:** £100K
**Expected Risk Reduction:** 15 points total

### Priority 2: HIGH (High Risks Within Appetite or Significant Treatment Required)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Cost | Expected Impact | Status |
|----------|--------|-------------------|-------|----------|------|-----------------|--------|
| 4 | Start vendor procurement Week 13 | R-002 (Vendor Delay) | Procurement Specialist | Week 13 | Staff time | Prevent delay | Open |
| 5 | Implement FinOps cost monitoring | R-007 (Cloud Costs) | Chief Data Officer | Week 43 | £20K | Cost visibility | Open |
| 6 | STRIDE threat model in Alpha | R-004, R-012 | Head of Cyber Security | Weeks 19-21 | Staff time | Early security | Open |
| 7 | Mock GDS Service Assessment | R-005 (Service Standard) | Service Owner | Week 26 | Staff time | Gap identification | Open |

**Total High Priority Actions:** 4
**Total Cost:** £20K
**Expected Risk Reduction:** 12 points total

### Priority 3: MEDIUM (Medium Risks Requiring Treatment)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Cost | Expected Impact | Status |
|----------|--------|-------------------|-------|----------|------|-----------------|--------|
| 8 | HLD review validates abstraction layers | R-013 (Vendor Lock-in) | Chief Data Architect | Week 24 | Staff time | Portability | Open |
| 9 | Weekly legacy coordination meetings | R-008 (Legacy Integration) | Chief Data Architect | Weeks 37-78 | Staff time | Coordination | Open |
| 10 | Load testing with realistic traffic | R-009, R-010 | QA Engineer | Week 71 | £30K | Performance | Open |
| 11 | Cyber insurance (£10M coverage) | R-012 (Cyber Breach) | Chief Data Officer | Week 73 | £150K/yr | Transfer | Open |
| 12 | Embed 8 ONS engineers with vendor | R-015 (Skills Gap) | Chief Data Architect | Weeks 37-72 | Staff time | Knowledge | Open |
| 13 | Identify 5 change champions | R-018 (User Resistance) | Director of Production | Week 67 | Staff time | Adoption | Open |
| 14 | Internal penetration testing | R-004 (GovS 007) | Head of Cyber Security | Week 68 | £50K | Pre-ITHC | Open |
| 15 | Reserved instance purchasing | R-007 (Cloud Costs) | Chief Data Architect | Week 73 | N/A | 30% saving | Open |
| 16 | Comprehensive data validation framework | R-003 (Data Migration) | Data Engineers | Week 50 | Staff time | Quality | Open |
| 17 | Automate SDMX metadata generation | R-017 (SDMX) | Data Engineers | Weeks 55-58 | Staff time | Compliance | Open |
| 18 | SRS research integration | R-019 (Research Access) | Data Engineers | Weeks 59-62 | Staff time | Access | Open |
| 19 | Quarterly benefits reporting to HMT | R-001, R-022 | Chief Data Officer | Quarterly | Staff time | Assurance | Open |
| 20 | Succession planning for 3 critical roles | R-020 (Key Staff) | Chief Data Officer | Week 37 | Staff time | Continuity | Open |

**Total Medium Priority Actions:** 13
**Total Cost:** ~£230K + £150K/yr insurance
**Expected Risk Reduction:** 35 points total

**Overall Action Plan Summary:**
- **Total Actions:** 20
- **Total Investment:** ~£350K capital + £150K/yr recurring
- **Expected Risk Reduction:** 62 points (30% reduction in total residual risk)
- **Target Completion:** Week 73 (Go-Live)

---

## I. Integration with SOBC

**How this Risk Register feeds into Strategic Outline Business Case (SOBC):**

### SOBC Strategic Case (Part A)
- **"Why Now?" section** uses strategic risks to demonstrate urgency
- **R-001** (Strategic Direction): Demonstrates need for delivery within policy window
- **R-022** (Funding): Justifies immediate action before spending review uncertainty

### SOBC Economic Case (Part B)
- **Risk-adjusted costs** use financial risks + HM Treasury optimism bias
- **R-007** (Cloud Costs): £1.2M cost risk → Add 15% contingency
- **R-011** (DR Costs): £500K budget risk → Add 10% contingency
- **Total risk contingency:** £1.8M (10% of £18M programme)

### SOBC Commercial Case (Part C)
- **Vendor risks** (R-002, R-013) inform procurement strategy
- **G-Cloud framework** selected to mitigate R-002 (procurement delay)
- **Contract exit clauses** required to mitigate R-013 (vendor lock-in)

### SOBC Financial Case (Part D)
- **Cost overrun risks** (R-007) inform contingency allocation
- **Funding risks** (R-022) inform spend profile and HMT engagement

### SOBC Management Case (Part E)
- **Full risk register** (this document) included in Management Case Part E
- **Top 10 risks** highlighted with mitigation plans
- **Risk ownership matrix** demonstrates clear accountability
- **Monitoring framework** shows ongoing risk management capability

### SOBC Recommendation
- **7 risks exceeding appetite** may influence:
  - Additional mitigation investment (£100K urgent actions)
  - Phasing strategy (de-risk Alpha with performance prototype)
  - Go/no-go criteria (Alpha prototype must validate R-010)

---

## J. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Reviewed By | Escalated To | Report Format |
|------------|------------------|-------------|--------------|---------------|
| **Critical (20-25)** | Weekly | Risk Owner + PMO | Steering Committee | Dashboard + narrative |
| **High (13-19)** | Bi-weekly | Risk Owner | Project Board | Dashboard |
| **Medium (6-12)** | Monthly | Risk Owner | Project Manager | Exception report |
| **Low (1-5)** | Quarterly | Action Owner | Risk Owner | Status update |

### Key Risk Indicators (KRIs)

**Leading Indicators** (predict future risk changes):
- Team turnover rate >10% → increases R-015, R-020 (operational risks)
- Vendor SLA breaches → increases R-008 (legacy integration)
- Budget variance >5% → increases R-007 (cloud costs)
- User research negative feedback → increases R-018 (adoption)
- Security scan findings trending up → increases R-004, R-012

**Lagging Indicators** (confirm risk materialization):
- Defect rate >5 per release → R-003 (data migration) materializing
- Schedule delay >2 weeks → R-002 (vendor) materializing
- Cost >10% over budget → R-007 (cloud costs) materializing
- Pre-release access incident → R-006 (Statistics Act) materializing
- API latency >500ms p95 → R-009, R-010 (performance) materializing

### Escalation Criteria

**Automatic Escalation Triggers:**
1. Any risk increases by 5+ points
2. Any new Critical risk (score 20-25) identified
3. Any risk exceeds appetite and no mitigation plan approved
4. Any mitigation action delayed >1 month
5. 3+ risks in same category exceed appetite
6. Any risk materializes (trigger event occurs)

### Reporting Requirements

**Weekly** (Critical/High Risks Only):
- Dashboard to Programme Board
- Narrative update on R-003, R-006, R-010
- Action plan progress for Priority 1 actions

**Monthly** (All Risks):
- Full risk register to Programme Board
- Risk matrix visualization (inherent and residual)
- Risk appetite compliance summary
- Action plan status (all 20 actions)

**Quarterly** (Strategic Review):
- Risk register to Audit Committee
- Risk trend analysis (improving/deteriorating)
- Risk appetite threshold review
- Lessons learned and process improvements
- Orange Book compliance assessment

### Risk Register Maintenance

**Risk Register Owner:** Chief Data Architect, ONS

**Responsibilities:**
- Maintain accuracy of risk register
- Coordinate risk reviews with risk owners
- Update risk scores based on evidence
- Track mitigation action completion
- Escalate risks per criteria
- Produce risk reports

**Update Process:**
1. Risk owners submit updates weekly (critical/high) or monthly (medium/low)
2. Risk register owner validates and updates register
3. PMO reviews for consistency and completeness
4. Programme Board approves material changes

**Version Control:**
- Version increments with each update
- Change log maintained in Revision History
- Previous versions archived for audit trail

**Next Review Date:** 2026-02-26 (Monthly review)

**Next Full Re-Assessment:** 2026-04-26 (Quarterly re-assessment)

---

## K. Orange Book Compliance Checklist

This risk register demonstrates compliance with HM Treasury Orange Book (2023):

### Part I - Risk Management Principles

- ✅ **A. Governance and Leadership**
  - Risk owners assigned from senior stakeholders (from RACI matrix)
  - Escalation paths defined to Programme Board/Audit Committee
  - Risk appetite set and monitored against thresholds

- ✅ **B. Integration**
  - Risks linked to strategic objectives (stakeholder goals)
  - Risks inform business case (SOBC Management Case Part E)
  - Risk management embedded in project governance

- ✅ **C. Collaboration and Best Information**
  - Risks sourced from stakeholder concerns and expert judgment
  - Multiple perspectives considered (stakeholder analysis)
  - Evidence-based assessment (likelihood and impact justified)

- ✅ **D. Risk Management Processes**
  - Systematic identification across 6 Orange Book categories
  - Consistent assessment methodology (5×5 matrix)
  - 4Ts response framework applied
  - Inherent and residual risk tracked

- ✅ **E. Continual Improvement**
  - Regular review schedule (weekly/monthly/quarterly)
  - Key Risk Indicators (leading and lagging) defined
  - Lessons learned process
  - Risk register version control

### Part II - Risk Control Framework

- ✅ **4-Pillar "House" Structure**
  - Risk appetite and tolerance defined per category
  - Risk ownership and governance established
  - Risk assessment methodology documented
  - Control effectiveness measured (inherent vs residual)

---

## Appendices

### Appendix A: Risk Assessment Scales

#### Likelihood Scale (1-5)

| Score | Rating | Probability | Description |
|-------|--------|-------------|-------------|
| 1 | Rare | < 5% | Highly unlikely, exceptional circumstances only |
| 2 | Unlikely | 5-25% | Could happen but probably won't |
| 3 | Possible | 25-50% | Reasonable chance, has happened before |
| 4 | Likely | 50-75% | More likely to happen than not |
| 5 | Almost Certain | > 75% | Expected to occur, highly probable |

#### Impact Scale (1-5)

| Score | Rating | Financial | Schedule | Strategic |
|-------|--------|-----------|----------|-----------|
| 1 | Negligible | < £100K | < 2 weeks | Minimal impact |
| 2 | Minor | £100K-£500K | 2-4 weeks | Manageable |
| 3 | Moderate | £500K-£2M | 1-3 months | Significant effort |
| 4 | Major | £2M-£5M | 3-6 months | Objectives threatened |
| 5 | Catastrophic | > £5M | > 6 months | Project failure |

#### Risk Score Matrix

| | 1 (Neg) | 2 (Min) | 3 (Mod) | 4 (Maj) | 5 (Cat) |
|---|---|---|---|---|---|
| **5 (A.Cert)** | 5 🟩 | 10 🟨 | 15 🟧 | 20 🟥 | 25 🟥 |
| **4 (Likely)** | 4 🟩 | 8 🟨 | 12 🟨 | 16 🟧 | 20 🟥 |
| **3 (Poss)** | 3 🟩 | 6 🟨 | 9 🟨 | 12 🟨 | 15 🟧 |
| **2 (Unlik)** | 2 🟩 | 4 🟩 | 6 🟨 | 8 🟨 | 10 🟨 |
| **1 (Rare)** | 1 🟩 | 2 🟩 | 3 🟩 | 4 🟩 | 5 🟩 |

---

### Appendix B: Stakeholder-Risk Linkage

**Traceability from Stakeholders to Risks:**

| Stakeholder | Driver (from stakeholder-drivers.md) | Risk ID | Risk Title | Category | Residual |
|-------------|-------------------------------------|---------|------------|----------|----------|
| Chief Data Officer | SD-1: Reduce costs by 40% | R-007 | Cloud costs exceed budget | FINANCIAL | 12 |
| Chief Data Officer | SD-1: Reduce costs | R-022 | Funding shortfall | STRATEGIC | 8 |
| Chief Statistician | SD-6: Statistics Act compliance | R-006 | Pre-release access breach | COMPLIANCE | 15 |
| Chief Data Architect | SD-2: Modernize infrastructure | R-003 | Data migration integrity | OPERATIONAL | 15 |
| Chief Data Architect | SD-2: Modernize infrastructure | R-010 | Census performance | TECHNOLOGY | 15 |
| Director of Production | SD-3: Publication efficiency | R-018 | Statistician resistance | OPERATIONAL | 6 |
| Head of Cyber Security | SD-7: Security accreditation | R-004 | ITHC failure | COMPLIANCE | 12 |
| Head of Cyber Security | SD-7: Security accreditation | R-012 | Cyber breach | REPUTATIONAL | 10 |

**Stakeholder Conflicts Mapped to Risks:**

| Stakeholder Conflict | Risk(s) Created | Mitigation |
|---------------------|-----------------|------------|
| CDO (cost reduction) vs CTO (innovation) | R-007 (Cloud costs) | FinOps controls, reserved instances |
| Operations (stability) vs Architecture (modernization) | R-003 (Data migration), R-008 (Legacy) | Parallel running, fallback procedures |
| Compliance (rigor) vs Delivery (speed) | R-004 (ITHC), R-005 (GDS), R-006 (Statistics Act) | Early testing, extended buffers |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Risk Register Owner** | Chief Data Architect | | |
| **Project Manager** | Programme Manager | | |
| **Senior Responsible Owner** | Chief Data Officer | | |
| **Steering Committee Chair** | National Statistician | | |

---

## Next Steps

1. **Immediate Actions** (This Week):
   - [ ] Escalate R-003, R-006, R-010 (HIGH residual risks) to Programme Board
   - [ ] Schedule UK Statistics Authority validation meeting for R-006
   - [ ] Initiate Alpha performance prototype planning for R-010
   - [ ] Establish risk review meeting cadence with all risk owners

2. **Short-term Actions** (This Month):
   - [ ] Integrate risk register into SOBC Management Case Part E
   - [ ] Set up weekly risk dashboard for Programme Board
   - [ ] Implement KRI monitoring (leading indicators)
   - [ ] Complete Priority 1 mitigation planning

3. **Medium-term Actions** (This Quarter):
   - [ ] Quarterly risk appetite compliance review
   - [ ] Lessons learned from Alpha phase risks
   - [ ] Risk register process improvement review
   - [ ] Orange Book compliance self-assessment

---

**END OF RISK REGISTER**

---

*This risk register follows HM Treasury Orange Book (2023) principles and integrates with ArcKit's stakeholder-driven architecture governance framework.*

*For questions or updates, contact: Chief Data Architect, ONS*

---

**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: 2026-01-26
**ArcKit Version**: 0.11.2
**Project**: ONS Data Platform Modernisation (Project 001)
**Model**: claude-opus-4-5-20251101
**Methodology**: HM Treasury Orange Book 2023
**Total Risks**: 22 risks across 6 categories
**Overall Risk Profile**: Concerning but manageable (3 High residual risks, 7 exceeding appetite)
