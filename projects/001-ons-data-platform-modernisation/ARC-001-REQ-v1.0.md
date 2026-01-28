# Project Requirements: ONS Data Platform Modernisation

> **Template Status**: Live | **Version**: 0.11.2 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.1 |
| **Document Type** | Business and Technical Requirements |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2025-11-01 |
| **Last Modified** | 2026-01-26 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-04-26 |
| **Owner** | Chief Data Architect, ONS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Project Team, Architecture Team, ONS Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-01 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2: Added User Personas, Use Cases, Requirement Conflicts & Resolutions, Budget sections; Enhanced Document Control with Review Cycle and Next Review Date | PENDING | PENDING |

---

## Executive Summary

### Purpose
This document defines the comprehensive business and technical requirements for the Office for National Statistics (ONS) Data Platform Modernisation project. It establishes the foundation for vendor procurement, architecture design, solution evaluation, acceptance testing, and change control.

### Business Context

The Office for National Statistics (ONS) is the UK's largest independent producer of official statistics and the recognised national statistical institute. ONS serves the public good by collecting, analysing, and disseminating trusted statistics about the UK's economy, population, and society.

The current ONS data platform infrastructure was built incrementally over the past decade, resulting in a fragmented landscape of disparate systems, inconsistent data formats, and manual processes that limit agility and scalability. Recent challenges include:

- **Publication spikes**: Major economic releases (GDP, CPI, Labour Market Statistics) generate traffic spikes that strain infrastructure capacity
- **Census scale**: The 2021 Census demonstrated the need for systems capable of processing 67 million population records
- **Digital expectations**: Users expect modern API access, real-time data, and self-service capabilities rather than static file downloads
- **Operational burden**: Manual publication processes require significant statistician time, delaying releases and increasing error risk
- **Cloud-first mandate**: UK Government Digital Service (GDS) policy requires migration from on-premises to cloud infrastructure

### Objectives

- **Modernise data infrastructure**: Replace legacy on-premises systems with cloud-native data platform capable of census-scale volumes
- **Improve public access**: Provide modern API-first access to ONS statistics for government, business, academia, and civil society
- **Enhance publication efficiency**: Automate statistical publication workflows to reduce manual effort by 60% and time-to-publish by 50%
- **Ensure compliance**: Meet UK Government security standards (GovS 007), Data Protection Act 2018, Statistics Act 2007, and GDS Service Standard
- **Reduce total cost of ownership**: Achieve 40% reduction in infrastructure costs through cloud optimisation and automation

### Expected Outcomes

- **Cost savings**: £4.5M annual savings through infrastructure optimisation and automation (target: Year 2)
- **Publication efficiency**: Reduce average time-to-publish from 4 days to 2 days for major economic indicators
- **API adoption**: 10,000 registered API users within 18 months, driving 50% of data consumption through APIs vs. file downloads
- **Availability**: Achieve 99.95% publication API uptime (max 21.9 minutes downtime per month)
- **Scalability**: Handle census-scale data (67M records) with processing time <24 hours
- **User satisfaction**: Achieve 85% satisfaction score from data users (researchers, journalists, policy makers)

### Requirements Summary

| Category | MUST_HAVE | SHOULD_HAVE | COULD_HAVE | WONT_HAVE | Total |
|----------|-----------|-------------|------------|-----------|-------|
| Business Requirements (BR) | 5 | 0 | 0 | 0 | 5 |
| Functional Requirements (FR) | 6 | 0 | 0 | 0 | 6 |
| Non-Functional - Performance (NFR-P) | 3 | 0 | 0 | 0 | 3 |
| Non-Functional - Security (NFR-SEC) | 3 | 0 | 0 | 0 | 3 |
| Non-Functional - Availability (NFR-A) | 3 | 0 | 0 | 0 | 3 |
| Non-Functional - Scalability (NFR-S) | 2 | 0 | 0 | 0 | 2 |
| Non-Functional - Compliance (NFR-C) | 4 | 0 | 0 | 0 | 4 |
| Non-Functional - Observability (NFR-O) | 2 | 1 | 0 | 0 | 3 |
| Data Requirements (DR) | 5 | 0 | 0 | 0 | 5 |
| Integration Requirements (INT) | 3 | 1 | 0 | 0 | 4 |
| **Total** | **36** | **2** | **0** | **0** | **38** |

### Project Scope

**In Scope**:
- Cloud-native data platform (ingestion, processing, storage, publication)
- RESTful APIs for statistical data access (OpenAPI 3.0 specification)
- Automated data publication workflows with quality validation
- Statistical Disclosure Control (SDC) automation
- Data catalog with metadata registry (SDMX compliance)
- Integration with existing ONS source systems (survey systems, admin data sources)
- Migration of 500+ statistical series to new platform
- User authentication and authorisation for pre-release access
- Observability and operational monitoring
- Developer portal with API documentation and sandbox

**Out of Scope**:
- Statistical methodology or survey design (remains with ONS statistical teams)
- Source data collection systems (surveys, admin data feeds) - integration only
- ONS website redesign (separate Digital Services programme)
- Internal corporate systems (HR, Finance, IT service management)
- Research and analysis tools (separate Data Science programme)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| Chief Data Officer | Executive Sponsor | ONS | Decision maker |
| Chief Statistician | Regulatory Authority | ONS | Compliance oversight |
| Chief Data Architect | Technical Authority | ONS Technology | Architecture oversight |
| Director of Statistical Production | Product Owner | ONS Production | Requirements & acceptance |
| Head of Data Publishing | Business Lead | ONS Publishing | Daily operations |
| National Statistician | Regulatory Compliance | ONS | Statistics Act compliance |
| Head of Cyber Security | Security Authority | ONS Security | Security review & approval |
| Data Protection Officer | Privacy Authority | ONS Compliance | GDPR compliance |
| GDS Service Assessor | Government Assurance | Cabinet Office | Service Standard assessment |
| Data Users Representative | External User Voice | User Research Panel | User acceptance |

---

## User Personas

### UP-1: Data Analyst (Government)

**Name**: Sarah, Policy Analyst at HM Treasury

**Role**: Uses ONS statistics for economic policy analysis and forecasting

**Goals**:
- Access timely economic indicators (GDP, inflation, employment) for policy briefings
- Download large datasets for statistical modelling
- Query historical time-series data programmatically

**Pain Points**:
- Current file download process is slow and manual
- No API access forces copy-paste into analytical tools
- Inconsistent data formats across statistical series

**Technical Proficiency**: Intermediate - comfortable with Excel, R, Python

**Access Patterns**: Daily during publication windows, weekly for analysis

**Requirements Influenced**: FR-001, FR-003, NFR-P-001

---

### UP-2: Data Journalist

**Name**: Marcus, Economics Correspondent at BBC News

**Role**: Reports on economic statistics for public consumption

**Goals**:
- Access data immediately at 9:30 AM publication time
- Get pre-release briefing under embargo (authorised press)
- Quickly verify figures and compare to historical data

**Pain Points**:
- Website crashes during major releases
- Difficult to find historical comparisons quickly
- Pre-release access process is cumbersome

**Technical Proficiency**: Basic - primarily uses web interface and Excel

**Access Patterns**: High intensity during publication windows (9:30-10:00 AM)

**Requirements Influenced**: NFR-P-003, FR-004, NFR-A-001

---

### UP-3: Academic Researcher

**Name**: Dr. Emily Chen, Professor of Economics at University of Edinburgh

**Role**: Conducts research using ONS statistical data

**Goals**:
- Access granular microdata for research (via Secure Research Service)
- Download long time-series for econometric analysis
- Understand methodology and quality indicators

**Pain Points**:
- Metadata often incomplete or hard to find
- Large dataset downloads timeout or fail
- Changes to methodology not clearly documented

**Technical Proficiency**: Advanced - uses R, Stata, Python

**Access Patterns**: Periodic intensive use for research projects

**Requirements Influenced**: INT-004, FR-003, DR-003, DR-004

---

### UP-4: Application Developer

**Name**: Raj, Senior Developer at FinTech startup

**Role**: Builds applications that consume ONS data

**Goals**:
- Integrate ONS data into commercial applications via API
- Receive real-time updates when new data published
- Understand API rate limits and plan accordingly

**Pain Points**:
- No programmatic API currently available
- Data formats inconsistent across datasets
- No developer documentation or sandbox

**Technical Proficiency**: Expert - REST APIs, JSON, modern development practices

**Access Patterns**: Continuous automated polling/streaming

**Requirements Influenced**: FR-001, NFR-P-001, NFR-S-001

---

### UP-5: Statistician (Internal)

**Name**: James, Senior Statistician in ONS Economic Statistics Division

**Role**: Produces and publishes official statistics

**Goals**:
- Publish statistics with minimal manual effort
- Ensure data quality through automated validation
- Control pre-release access for authorised users

**Pain Points**:
- Manual file formatting and upload process
- Quality checks are time-consuming and error-prone
- Pre-release access management is manual and auditable

**Technical Proficiency**: Intermediate - Excel, SAS, some Python

**Access Patterns**: Daily during publication preparation

**Requirements Influenced**: FR-002, FR-005, FR-006, BR-002

---

### UP-6: Citizen (General Public)

**Name**: Lisa, interested member of the public

**Role**: Occasional consumer of statistics for personal interest or local context

**Goals**:
- Find statistics about local area
- Understand what statistics mean
- Share statistics on social media

**Pain Points**:
- Website is difficult to navigate
- Statistical terminology is confusing
- Can't find local-level data easily

**Technical Proficiency**: Basic - web browser, mobile

**Access Patterns**: Occasional, event-driven (news stories, local issues)

**Requirements Influenced**: FR-003, NFR-C-004

---

## Use Cases

### UC-1: Programmatic Data Access via API

**Actor**: Data Analyst (UP-1), Application Developer (UP-4)

**Preconditions**:
- User has registered for API access
- API key has been issued and activated
- Statistical series is published and available

**Main Flow**:
1. User authenticates using API key
2. User queries data catalog to find dataset ID
3. User requests data with filters (time period, geography, breakdown)
4. System validates request against rate limits
5. System retrieves data from data store
6. System returns data in requested format (JSON/CSV/SDMX)
7. System logs access for analytics

**Alternative Flows**:
- **Rate limit exceeded**: Return 429 with retry-after header
- **Dataset not found**: Return 404 with suggested alternatives
- **Invalid parameters**: Return 400 with validation errors

**Postconditions**:
- User receives requested data
- Access logged for analytics and audit

**Related Requirements**: FR-001, NFR-P-001, NFR-SEC-001

---

### UC-2: Automated Statistical Publication

**Actor**: Statistician (UP-5)

**Preconditions**:
- Statistical data validated and approved for publication
- Metadata prepared (methodology, quality indicators)
- Publication date/time scheduled
- Pre-release access list configured

**Main Flow**:
1. Statistician uploads validated data file with metadata
2. System performs automated quality validation
3. System applies Statistical Disclosure Control rules
4. System generates SDMX-compliant metadata
5. System stores data in pre-release state
6. System grants access to pre-release users (up to 24 hours before)
7. At scheduled time, system publishes to public API
8. System invalidates caches and notifies subscribers
9. System logs publication event with audit trail

**Alternative Flows**:
- **Quality validation fails**: Alert statistician, block publication
- **SDC rules triggered**: Suppress cells, alert statistician for review
- **Scheduled time missed**: Alert operations, manual intervention

**Postconditions**:
- Statistics published and available via API
- Pre-release access records auditable
- Publication logged for compliance

**Related Requirements**: FR-002, FR-004, FR-005, FR-006, NFR-C-002

---

### UC-3: Data Discovery and Catalog Search

**Actor**: All user personas

**Preconditions**:
- User has access to data catalog (public for published data)
- Catalog contains metadata for statistical series

**Main Flow**:
1. User enters search query (keywords, topic, geography)
2. System performs full-text and faceted search
3. System returns ranked results with relevance scoring
4. User filters results by facets (topic, time period, geography)
5. User selects dataset to view details
6. System displays metadata (methodology, quality, source)
7. User navigates to API endpoint or download

**Alternative Flows**:
- **No results found**: Suggest related terms, popular datasets
- **Ambiguous query**: Show disambiguation options

**Postconditions**:
- User finds relevant dataset
- Search analytics captured for improvement

**Related Requirements**: FR-003, NFR-P-001

---

### UC-4: Pre-Release Access for Authorised Users

**Actor**: Data Journalist (UP-2), Government Minister

**Preconditions**:
- User is on designated pre-release access list
- MFA credentials configured
- Statistics in pre-release state

**Main Flow**:
1. User authenticates with MFA
2. System validates user against pre-release access list
3. System checks pre-release window (max 24 hours before publication)
4. System grants access to embargoed data
5. User views/downloads data under embargo terms
6. System logs all pre-release access events

**Alternative Flows**:
- **User not authorised**: Deny access, alert security
- **Outside pre-release window**: Deny access with explanation
- **MFA failure**: Deny access, log security event

**Postconditions**:
- Authorised user accesses pre-release data
- Complete audit trail for Statistics Act compliance

**Related Requirements**: FR-004, NFR-SEC-001, NFR-C-002

---

### UC-5: Census-Scale Data Processing

**Actor**: Census Programme, System (automated)

**Preconditions**:
- Census microdata collected and securely transferred
- Processing pipelines configured and tested
- Sufficient compute capacity available

**Main Flow**:
1. Census microdata ingested from secure transfer (67M records)
2. System performs data quality validation at scale
3. System applies Statistical Disclosure Control
4. System aggregates data to publication geographies
5. System generates output tables with metadata
6. System validates against previous census for consistency
7. System stores for statistician review
8. Statistician approves for publication

**Alternative Flows**:
- **Quality issues detected**: Alert statisticians, pause pipeline
- **SDC threshold breached**: Flag for manual review
- **Processing exceeds SLA**: Alert operations, scale resources

**Postconditions**:
- Census statistics ready for publication
- Processing completed within 24-hour SLA
- Full lineage and audit trail available

**Related Requirements**: BR-005, NFR-P-002, NFR-S-002

---

### UC-6: Disaster Recovery Failover

**Actor**: Operations Team, System (automated)

**Preconditions**:
- Primary region experiencing major outage
- DR site synchronised within RPO (1 hour)
- Runbooks approved and tested

**Main Flow**:
1. Monitoring detects primary region failure
2. System alerts operations team
3. Operations initiates DR failover procedure
4. System redirects traffic to secondary region
5. System validates data integrity at DR site
6. System confirms all services operational
7. Operations monitors for stability
8. Communication sent to stakeholders

**Alternative Flows**:
- **Automated failover**: System performs automatic failover if criteria met
- **Data integrity issues**: Alert operations, manual intervention required
- **Partial failure**: Graceful degradation to read-only mode

**Postconditions**:
- Service restored within RTO (4 hours)
- Data loss within RPO (1 hour)
- Incident documented for review

**Related Requirements**: NFR-A-002, NFR-A-003

---

## Business Requirements

### BR-001: Reduce Infrastructure Costs

**Description**: The platform MUST reduce total infrastructure operating costs by 40% compared to current on-premises baseline within 24 months of go-live.

**Rationale**: Taxpayer value requires efficient use of public funds. Current on-premises infrastructure costs £11.2M annually including hardware refresh, data centre, and maintenance. Cloud optimisation and automation can achieve £4.5M annual savings.

**Success Criteria**:
- Infrastructure costs ≤£6.7M/year by Month 24
- Cost per dataset published reduced by 50%
- Cost allocation model implemented with chargeback to statistical divisions
- Monthly cost reports show breakdown by workload and optimisation opportunities

**Priority**: MUST_HAVE

**Stakeholder**: Chief Data Officer (CDO)

**Alignment**: Supports ONS Value for Money strategic objective

**Traceability**:
- Drivers: SD-1 (CDO cost reduction pressure)
- Goals: G-1 (40% infrastructure cost reduction)
- Outcomes: O-1 (£4.5M annual savings)

---

### BR-002: Improve Publication Efficiency

**Description**: The platform MUST reduce statistician manual effort for data publication by 60% through workflow automation.

**Rationale**: Statisticians currently spend 35% of their time on publication mechanics (file formatting, upload, validation) rather than statistical analysis. Automation frees capacity for higher-value work.

**Success Criteria**:
- Automated publication workflow from validated data to public API (zero manual steps)
- Time-to-publish reduced from 4 days average to 2 days
- Publication error rate <0.1% (currently 2.3%)
- Statistician satisfaction score ≥80% for publication tools

**Priority**: MUST_HAVE

**Stakeholder**: Director of Statistical Production

**Alignment**: Supports ONS Operational Excellence priority

**Traceability**:
- Drivers: SD-2 (Director of Statistical Production efficiency needs)
- Goals: G-2 (60% reduction in manual publication effort)
- Outcomes: O-2 (Publication time reduced to 2 days)

---

### BR-003: Enhance Public Data Access

**Description**: The platform MUST provide modern API access to drive 50% of data consumption through APIs within 18 months.

**Rationale**: ONS's statutory duty under Statistics Act 2007 is to maximise accessibility of official statistics. Current file-based distribution limits programmatic access, reducing data reuse in government, business, and research.

**Success Criteria**:
- APIs available for 100% of published statistical series
- 10,000 registered API users within 18 months
- API traffic accounts for ≥50% of data consumption (vs file downloads)
- Developer satisfaction score ≥85%

**Priority**: MUST_HAVE

**Stakeholder**: National Statistician

**Alignment**: Statistics and Registration Service Act 2007 statutory duty

**Traceability**:
- Drivers: SD-3 (National Statistician accessibility mandate)
- Goals: G-3 (API-first data access)
- Outcomes: O-3 (10,000 API users, 50% API consumption)

---

### BR-004: Meet UK Government Digital Standards

**Description**: The platform MUST achieve GDS Service Standard assessment at BETA phase and maintain compliance throughout operation.

**Rationale**: UK Government policy requires all public-facing digital services to meet the Service Standard, ensuring usability, accessibility, and operational excellence.

**Success Criteria**:
- Pass GDS Service Assessment at ALPHA, BETA, and LIVE phases
- Meet all 14 Service Standard criteria
- WCAG 2.1 AA accessibility compliance
- Quarterly service performance reporting published on GOV.UK

**Priority**: MUST_HAVE

**Stakeholder**: GDS Service Assessor

**Alignment**: Mandatory UK Government policy

**Traceability**:
- Drivers: SD-4 (GDS compliance mandate)
- Goals: G-4 (Service Standard compliance)
- Outcomes: O-4 (LIVE assessment passed)

---

### BR-005: Enable Census-Scale Processing

**Description**: The platform MUST process census-scale datasets (67 million records) within 24 hours from source data to published statistics.

**Rationale**: ONS conducts UK Census every 10 years (next: 2031). Current infrastructure required 6 months to process 2021 Census data. Modernisation must enable near-real-time census statistics.

**Success Criteria**:
- 67M record dataset processed end-to-end <24 hours
- Scalability testing demonstrates linear scaling to 100M records
- Automated quality validation for large datasets
- Cost per record processed <£0.0001

**Priority**: MUST_HAVE

**Stakeholder**: Census Programme Director

**Alignment**: Census Act 1920, Statistics Act 2007

**Traceability**:
- Drivers: SD-5 (Census Programme scalability needs)
- Goals: G-5 (Census-scale processing capability)
- Outcomes: O-5 (67M records in <24 hours)

---

## Functional Requirements

### FR-001: Statistical Data Publication API

**Description**: The platform MUST provide RESTful APIs for accessing all published ONS statistical data with query capabilities.

**Rationale**: API-first approach enables programmatic access for data consumers (government analysts, researchers, journalists, businesses).

**Acceptance Criteria**:
- [ ] OpenAPI 3.0+ specification published for all APIs
- [ ] Query by statistical series, time period, geography, breakdown
- [ ] Pagination support for large datasets (>10,000 records)
- [ ] Metadata returned with each dataset (methodology, quality indicators, source)
- [ ] Multiple format support: JSON, CSV, SDMX-ML
- [ ] Rate limiting: 100 requests/minute for anonymous, 1000 requests/minute for authenticated
- [ ] Developer sandbox environment with test data

**Priority**: MUST_HAVE

**Related Principle**: API-First Design (Principle 7)

**User Personas**: UP-1 (Data Analyst), UP-4 (Application Developer)

**Use Cases**: UC-1 (Programmatic Data Access)

---

### FR-002: Automated Publication Workflow

**Description**: The platform MUST provide automated workflow from validated statistical data to published API with zero manual steps.

**Rationale**: Manual publication processes delay releases and introduce human error. Automation ensures consistency and frees statistician capacity.

**Acceptance Criteria**:
- [ ] Workflow triggered by data file upload with metadata
- [ ] Automated quality validation (completeness, range checks, consistency)
- [ ] Automated Statistical Disclosure Control (SDC) rule application
- [ ] Automated metadata generation (SDMX compliance)
- [ ] Scheduled publication with pre-release access control
- [ ] Rollback capability if post-publication issues detected
- [ ] Audit trail for all publication events (who, when, what)

**Priority**: MUST_HAVE

**Related Principle**: Automation and Continuous Delivery (Principle 13)

**User Personas**: UP-5 (Statistician)

**Use Cases**: UC-2 (Automated Statistical Publication)

---

### FR-003: Data Catalog with Search

**Description**: The platform MUST provide searchable data catalog enabling users to discover ONS datasets by keyword, topic, geography, and time period.

**Rationale**: ONS publishes 500+ statistical series. Discoverability is essential for users to find relevant data without prior knowledge of ONS taxonomy.

**Acceptance Criteria**:
- [ ] Full-text search across titles, descriptions, keywords
- [ ] Faceted search by topic, geography, frequency, source
- [ ] DCAT-compliant metadata for each dataset
- [ ] Links to API endpoints, file downloads, methodology docs
- [ ] Usage analytics (views, downloads, API calls per dataset)
- [ ] Related datasets recommendations
- [ ] Search performance: results returned <500ms p95

**Priority**: MUST_HAVE

**Related Principle**: Interoperability and Open Standards (Principle 8)

**User Personas**: All user personas

**Use Cases**: UC-3 (Data Discovery and Catalog Search)

---

### FR-004: Pre-Release Access Control

**Description**: The platform MUST enforce statutory pre-release access restrictions in compliance with Statistics Act 2007.

**Rationale**: UK Statistics Act mandates that official statistics are published to all users simultaneously, with limited pre-release access (max 24 hours) only for designated government ministers and officials.

**Acceptance Criteria**:
- [ ] Pre-release access window configurable per dataset (typically 24 hours)
- [ ] Designated user list maintained per statistical series
- [ ] Multi-factor authentication (MFA) required for pre-release access
- [ ] Audit log of all pre-release access (who, when, what)
- [ ] Automatic public release at scheduled time (9:30 AM GMT convention)
- [ ] Alert if pre-release period exceeds 24 hours (Statistics Act breach)

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

**User Personas**: UP-2 (Data Journalist), UP-5 (Statistician)

**Use Cases**: UC-4 (Pre-Release Access for Authorised Users)

---

### FR-005: Statistical Disclosure Control (SDC)

**Description**: The platform MUST automatically apply Statistical Disclosure Control rules to prevent identification of individuals or businesses in published statistics.

**Rationale**: ONS processes sensitive personal and commercial data under legal privilege. Publishing small cell counts or insufficiently aggregated data risks re-identification, breaching Data Protection Act 2018 and Statistics Act 2007.

**Acceptance Criteria**:
- [ ] Automated suppression of cells <3 individuals
- [ ] Secondary suppression to prevent differencing attacks
- [ ] Rounding rules applied consistently across tables
- [ ] Perturbation methods for high-risk datasets
- [ ] SDC rule configuration by statistical domain
- [ ] Privacy Impact Assessment (PIA) workflow for new series
- [ ] Re-identification risk assessment reporting

**Priority**: MUST_HAVE

**Related Principle**: Privacy by Design and Statistical Disclosure Control (Principle 6)

**User Personas**: UP-5 (Statistician)

**Use Cases**: UC-2 (Automated Statistical Publication), UC-5 (Census-Scale Data Processing)

---

### FR-006: Data Quality Validation

**Description**: The platform MUST validate data quality at ingestion with automated checks and quality indicators published alongside statistics.

**Rationale**: Statistical accuracy is core to ONS credibility. Automated quality checks scale to census volumes and reduce human error compared to manual review.

**Acceptance Criteria**:
- [ ] Completeness checks (mandatory fields populated, expected record counts)
- [ ] Range validation (values within expected bounds, outlier detection)
- [ ] Consistency checks (cross-table validation, time-series trend analysis)
- [ ] Methodology code automated testing (statistical calculations verified)
- [ ] Quality metadata published with each dataset (coverage, accuracy, timeliness)
- [ ] Configurable quality rules per statistical series
- [ ] Data quality dashboard for statisticians

**Priority**: MUST_HAVE

**Related Principle**: Data Quality by Design (Principle 5)

**User Personas**: UP-5 (Statistician), UP-3 (Academic Researcher)

**Use Cases**: UC-2 (Automated Statistical Publication)

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: API Response Time

**Description**: Publication APIs MUST respond within 500ms for p95 and 2 seconds for p99 latency.

**Rationale**: Data consumers (government analysts, researchers, automated systems) require responsive APIs for analytical workflows. Slow APIs reduce adoption.

**Acceptance Criteria**:
- [ ] p50 latency: <200ms
- [ ] p95 latency: <500ms
- [ ] p99 latency: <2000ms
- [ ] Load testing demonstrates targets met at 10,000 req/s peak load
- [ ] Latency monitoring with alerting on SLO violations

**Priority**: MUST_HAVE

**Related Principle**: Performance and Efficiency (Principle 12)

---

#### NFR-P-002: Publication Processing Time

**Description**: Statistical data processing pipelines MUST complete within SLAs defined per publication type (real-time: <1 hour, daily: <4 hours, census: <24 hours).

**Rationale**: Time-sensitive publications (GDP, inflation, labour market) are market-moving statistics. Delays damage ONS credibility and can affect financial markets.

**Acceptance Criteria**:
- [ ] Real-time indicators (eg flash estimates): <1 hour source to publish
- [ ] Daily publications (eg COVID-19 statistics): <4 hours
- [ ] Monthly publications (eg CPI, Labour Market): <8 hours
- [ ] Census-scale datasets (67M records): <24 hours
- [ ] Pipeline monitoring with SLA tracking
- [ ] Automated alerts on SLA breach risk

**Priority**: MUST_HAVE

**Related Principle**: Performance and Efficiency (Principle 12)

---

#### NFR-P-003: Publication Traffic Handling

**Description**: The platform MUST handle peak publication load of 10,000 requests/second without degradation.

**Rationale**: Major economic releases (GDP, inflation) generate traffic spikes. Platform must handle load without manual intervention or capacity pre-provisioning.

**Acceptance Criteria**:
- [ ] Sustained load: 10,000 requests/second
- [ ] Burst capacity: 20,000 requests/second for 5 minutes
- [ ] Auto-scaling response time: <5 minutes from load trigger to capacity available
- [ ] Latency targets maintained under peak load (NFR-P-001)
- [ ] Load testing performed quarterly with peak scenarios

**Priority**: MUST_HAVE

**Related Principle**: Scalability and Elastic Capacity (Principle 2)

---

### Security Requirements

#### NFR-SEC-001: Zero Trust Architecture

**Description**: The platform MUST implement Zero Trust security with identity-based access control, encrypted communication, and least privilege principles.

**Rationale**: ONS handles OFFICIAL and OFFICIAL-SENSITIVE data including pre-release market-sensitive statistics. Perimeter security is insufficient; must assume breach and verify all access.

**Acceptance Criteria**:
- [ ] Multi-factor authentication (MFA) for all user access
- [ ] Service-to-service authentication (mutual TLS or signed tokens)
- [ ] Role-Based Access Control (RBAC) with least privilege
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest: AES-256 for all data stores
- [ ] Encryption in transit: TLS 1.3+ for all communication
- [ ] Secrets management via secure vault (no secrets in code/config)

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

---

#### NFR-SEC-002: Audit Logging

**Description**: The platform MUST log all authentication, authorisation, and data access events to centralized audit system with tamper-evident storage.

**Rationale**: Audit trails are required for security incident investigation, compliance audits, and Statistics Act pre-release access monitoring.

**Acceptance Criteria**:
- [ ] Structured audit logs (JSON format with correlation IDs)
- [ ] Events logged: authentication, authorisation decisions, data access, configuration changes
- [ ] Tamper-evident log storage (append-only, cryptographic verification)
- [ ] Log retention: 7 years (UK Government compliance requirement)
- [ ] Real-time SIEM integration for security monitoring
- [ ] Audit log search and analysis tools

**Priority**: MUST_HAVE

**Related Principle**: Observability and Operational Excellence (Principle 11)

---

#### NFR-SEC-003: Vulnerability Management

**Description**: The platform MUST identify and remediate security vulnerabilities within defined SLAs (Critical: 24 hours, High: 7 days, Medium: 30 days).

**Rationale**: Government Functional Standard GovS 007: Security requires timely vulnerability patching. Unpatched vulnerabilities expose ONS systems to exploitation.

**Acceptance Criteria**:
- [ ] Automated vulnerability scanning in CI/CD pipeline
- [ ] Dependency scanning for open-source libraries
- [ ] Container image scanning before deployment
- [ ] Vulnerability remediation SLAs:
  - Critical: <24 hours
  - High: <7 days
  - Medium: <30 days
  - Low: <90 days
- [ ] Penetration testing: Annual external, quarterly internal
- [ ] Vulnerability status reporting to security team

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

---

### Availability and Resilience Requirements

#### NFR-A-001: Service Availability

**Description**: Publication APIs MUST achieve 99.95% uptime (maximum 21.9 minutes downtime per month).

**Rationale**: Data consumers rely on API availability for automated systems and time-sensitive analysis. Downtime during major publication releases damages ONS reputation.

**Acceptance Criteria**:
- [ ] 99.95% monthly uptime SLA
- [ ] Planned maintenance windows: max 2 hours/month, scheduled outside business hours
- [ ] Availability monitoring with 5-minute granularity
- [ ] Incident response SLA: acknowledge <15 minutes, resolve <2 hours
- [ ] Monthly SLA reporting published internally
- [ ] Financial penalties for SLA breach (if vendor-operated)

**Priority**: MUST_HAVE

**Related Principle**: Resilience and Fault Tolerance (Principle 3)

---

#### NFR-A-002: Disaster Recovery

**Description**: The platform MUST support disaster recovery with RTO (Recovery Time Objective) of 4 hours and RPO (Recovery Point Objective) of 1 hour.

**Rationale**: Catastrophic failure during scheduled publication window could prevent ONS meeting Statistics Act legal obligations and cause market disruption.

**Acceptance Criteria**:
- [ ] RTO: 4 hours (time to restore service)
- [ ] RPO: 1 hour (maximum data loss)
- [ ] Multi-region deployment across UK availability zones
- [ ] Automated backup: continuous for databases, hourly for files
- [ ] Disaster recovery testing: quarterly full failover exercise
- [ ] Runbooks for failure scenarios documented and tested

**Priority**: MUST_HAVE

**Related Principle**: Resilience and Fault Tolerance (Principle 3)

---

#### NFR-A-003: Fault Tolerance

**Description**: The platform MUST gracefully degrade when non-critical components fail, with no single point of failure for publication pipelines.

**Rationale**: Distributed systems fail unpredictably. Architecture must assume failures occur and maintain core functionality.

**Acceptance Criteria**:
- [ ] Multi-zone deployment for all critical components
- [ ] Circuit breakers for external dependencies
- [ ] Graceful degradation: read-only mode if write path fails
- [ ] Health checks and automated failover (<5 minutes)
- [ ] Chaos engineering tests performed quarterly
- [ ] No single points of failure in publication critical path

**Priority**: MUST_HAVE

**Related Principle**: Resilience and Fault Tolerance (Principle 3)

---

### Scalability Requirements

#### NFR-S-001: Horizontal Scaling

**Description**: The platform MUST scale horizontally to meet demand without manual intervention or architectural changes.

**Rationale**: Publication traffic is unpredictable (spikes on major releases). Manual scaling is slow and error-prone. Auto-scaling ensures capacity meets demand cost-efficiently.

**Acceptance Criteria**:
- [ ] Stateless application design enabling horizontal replication
- [ ] Auto-scaling policies based on CPU, memory, and request rate
- [ ] Scaling range: 2 minimum instances to 100 maximum
- [ ] Scale-out time: <5 minutes from trigger to capacity available
- [ ] Scale-in time: <15 minutes (gradual to avoid traffic disruption)
- [ ] Load testing demonstrates linear scaling to 100 instances

**Priority**: MUST_HAVE

**Related Principle**: Scalability and Elastic Capacity (Principle 2)

---

#### NFR-S-002: Data Volume Scalability

**Description**: The platform MUST handle data growth to 500TB stored data and 10TB monthly ingestion without performance degradation.

**Rationale**: ONS data volumes grow 20% annually. Platform must scale to 5-year projected capacity to avoid costly re-platforming.

**Acceptance Criteria**:
- [ ] Storage capacity: 500TB (5-year projection)
- [ ] Monthly ingestion: 10TB
- [ ] Query performance maintained as data grows (p95 <500ms)
- [ ] Data partitioning strategy for large time-series datasets
- [ ] Archive/retention policies to manage storage costs
- [ ] Capacity planning model with growth projections

**Priority**: MUST_HAVE

**Related Principle**: Scalability and Elastic Capacity (Principle 2)

---

### Compliance Requirements

#### NFR-C-001: GDPR and Data Protection Act 2018

**Description**: The platform MUST comply with GDPR and Data Protection Act 2018 for all personal data processing.

**Rationale**: ONS processes personal data from surveys and administrative sources under legal basis. Non-compliance risks ICO enforcement, reputational damage, and loss of data sharing agreements.

**Acceptance Criteria**:
- [ ] Privacy Impact Assessment (PIA) completed for all data processing
- [ ] Data minimisation: only necessary data retained
- [ ] Retention policies: automated deletion after defined period
- [ ] Right to erasure: capability to delete individual records on request
- [ ] Data breach notification process (<72 hours to ICO)
- [ ] Data Protection Officer (DPO) review and approval

**Priority**: MUST_HAVE

**Related Principle**: Privacy by Design and Statistical Disclosure Control (Principle 6)

---

#### NFR-C-002: Statistics Act 2007 Compliance

**Description**: The platform MUST enforce Statistics Act 2007 requirements including pre-release access restrictions and publication standards.

**Rationale**: ONS operates under Statistics Act legal framework. Non-compliance undermines statistical independence and public trust.

**Acceptance Criteria**:
- [ ] Pre-release access limited to 24 hours maximum
- [ ] Designated user lists maintained and audited
- [ ] Simultaneous public release to all users
- [ ] Publication schedule published in advance
- [ ] Revisions and corrections policy implemented
- [ ] Annual compliance audit by UK Statistics Authority

**Priority**: MUST_HAVE

**Related Principle**: Open by Default, Secure by Design (Principle 1)

---

#### NFR-C-003: Government Security Standards (GovS 007)

**Description**: The platform MUST meet UK Government Functional Standard GovS 007: Security for OFFICIAL classification.

**Rationale**: Mandatory government policy for all public sector technology. Non-compliance prevents accreditation and go-live.

**Acceptance Criteria**:
- [ ] Security risk assessment completed and approved
- [ ] Security controls mapped to GovS 007 requirements
- [ ] Penetration testing by CHECK-certified testers
- [ ] IT Health Check (ITHC) passed before go-live
- [ ] Ongoing security monitoring and incident response
- [ ] Annual assurance review by Government Security Group

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

---

#### NFR-C-004: Accessibility (WCAG 2.1 AA)

**Description**: All user-facing interfaces MUST meet WCAG 2.1 Level AA accessibility standards.

**Rationale**: UK Government Service Standard requires accessibility. Legal obligation under Equality Act 2010 to ensure disabled users can access public services.

**Acceptance Criteria**:
- [ ] WCAG 2.1 AA compliance for all web interfaces
- [ ] Automated accessibility testing in CI/CD pipeline
- [ ] Manual accessibility testing by disabled users
- [ ] Accessibility statement published
- [ ] Screen reader compatibility (JAWS, NVDA)
- [ ] Keyboard navigation support (no mouse required)

**Priority**: MUST_HAVE

**Related Principle**: Interoperability and Open Standards (Principle 8)

---

### Observability Requirements

#### NFR-O-001: Structured Logging

**Description**: All services MUST emit structured logs (JSON format) with correlation IDs for distributed tracing.

**Rationale**: Distributed systems require correlation across services to diagnose issues. Structured logs enable automated analysis and alerting.

**Acceptance Criteria**:
- [ ] JSON-formatted logs with consistent schema
- [ ] Correlation IDs propagated across service calls
- [ ] Log levels: ERROR, WARN, INFO, DEBUG
- [ ] Centralised log aggregation (searchable, indexed)
- [ ] Log retention: 90 days online, 7 years archive
- [ ] Sensitive data excluded from logs (PII, secrets)

**Priority**: MUST_HAVE

**Related Principle**: Observability and Operational Excellence (Principle 11)

---

#### NFR-O-002: Metrics and Monitoring

**Description**: The platform MUST export RED metrics (Rate, Errors, Duration) for all services with real-time dashboards and alerting.

**Rationale**: Proactive monitoring enables issue detection before user impact. SLO-based alerting reduces noise and focuses on user-impacting problems.

**Acceptance Criteria**:
- [ ] RED metrics for all services:
  - Rate: requests per second
  - Errors: error rate percentage
  - Duration: latency percentiles (p50, p95, p99)
- [ ] Service Level Objectives (SLOs) defined and monitored
- [ ] Real-time dashboards for operations team
- [ ] Automated alerting on SLO violations
- [ ] Runbooks linked to alerts (remediation steps)

**Priority**: MUST_HAVE

**Related Principle**: Observability and Operational Excellence (Principle 11)

---

#### NFR-O-003: Distributed Tracing

**Description**: The platform MUST implement distributed tracing for request flows across microservices.

**Rationale**: Debugging latency and errors in distributed systems requires end-to-end visibility of request paths.

**Acceptance Criteria**:
- [ ] Trace context propagated across all service calls
- [ ] Trace sampling: 100% for errors, 1% for successes (configurable)
- [ ] Trace visualisation showing service dependencies
- [ ] Latency breakdown by service and operation
- [ ] Trace retention: 30 days
- [ ] Integration with logging (correlation IDs)

**Priority**: SHOULD_HAVE

**Related Principle**: Observability and Operational Excellence (Principle 11)

---

## Data Requirements

### DR-001: Data Classification

**Description**: All data MUST be classified according to UK Government security classification scheme (OFFICIAL, OFFICIAL-SENSITIVE, SECRET).

**Rationale**: Data classification drives security controls, access restrictions, and handling requirements. Misclassification risks inappropriate access or excessive controls.

**Acceptance Criteria**:
- [ ] Classification assigned to all datasets and data stores
- [ ] Classification metadata stored with data catalog
- [ ] Security controls applied proportionate to classification
- [ ] Classification review process (annually or on data change)
- [ ] Training for data producers on classification criteria

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

---

### DR-002: Data Retention and Deletion

**Description**: Data retention policies MUST be defined per dataset with automated deletion after retention period expires.

**Rationale**: GDPR and Data Protection Act require data minimisation - only retaining data as long as necessary. Excessive retention increases storage costs and privacy risk.

**Acceptance Criteria**:
- [ ] Retention period defined for all datasets (ranging from 1 year to permanent for official statistics)
- [ ] Automated deletion workflows
- [ ] Legal hold process for litigation/investigation
- [ ] Backup retention aligned with data retention policy
- [ ] Audit trail of data deletions

**Priority**: MUST_HAVE

**Related Principle**: Privacy by Design and Statistical Disclosure Control (Principle 6)

---

### DR-003: Data Lineage

**Description**: The platform MUST maintain end-to-end data lineage from source data to published statistics.

**Rationale**: Statistical credibility requires transparent lineage. Impact analysis for schema changes requires understanding data flows.

**Acceptance Criteria**:
- [ ] Source-to-target mapping documented for all pipelines
- [ ] Transformation logic version-controlled
- [ ] Data lineage metadata queryable (API or UI)
- [ ] Impact analysis: identify downstream effects of source changes
- [ ] Lineage visualisation for statisticians and auditors

**Priority**: MUST_HAVE

**Related Principle**: Data Quality by Design (Principle 5)

---

### DR-004: Statistical Metadata (SDMX)

**Description**: All published statistics MUST include SDMX-compliant metadata enabling interoperability with international statistical systems.

**Rationale**: SDMX (Statistical Data and Metadata eXchange) is the ISO standard for statistical data exchange. Compliance enables ONS integration with Eurostat, UN, OECD systems.

**Acceptance Criteria**:
- [ ] SDMX Data Structure Definitions (DSDs) for all series
- [ ] SDMX codelists for dimensions (time, geography, breakdown)
- [ ] SDMX-ML format export supported
- [ ] Metadata includes: methodology, quality, coverage, source
- [ ] SDMX registry integration

**Priority**: MUST_HAVE

**Related Principle**: Interoperability and Open Standards (Principle 8)

---

### DR-005: Data Migration

**Description**: The platform MUST migrate 500+ existing statistical series from legacy systems with data integrity validation.

**Rationale**: Historical data continuity is essential for time-series analysis. Migration errors damage statistical accuracy and user trust.

**Acceptance Criteria**:
- [ ] Migration plan for 500+ statistical series
- [ ] Data integrity validation (record counts, checksums, sample verification)
- [ ] Parallel running: legacy and new systems publishing simultaneously for validation period
- [ ] Rollback capability if migration issues detected
- [ ] Migration success criteria: 100% data integrity, zero data loss

**Priority**: MUST_HAVE

**Related Principle**: Single Source of Truth (Principle 4)

---

## Integration Requirements

### INT-001: Survey Data Integration

**Description**: The platform MUST integrate with ONS survey collection systems to ingest survey microdata.

**Rationale**: ONS conducts 200+ surveys annually. Survey microdata is the primary input for statistical production.

**Acceptance Criteria**:
- [ ] Integration with survey systems: Labour Force Survey (LFS), Living Costs & Food Survey (LCFS), Census
- [ ] Secure file transfer (SFTP, HTTPS) with encryption in transit
- [ ] Automated ingestion triggers on file arrival
- [ ] File format validation (CSV, JSON, Parquet)
- [ ] Error handling and retry logic
- [ ] Audit trail of ingestion events

**Priority**: MUST_HAVE

**Related Principle**: Interoperability and Integration (Principle 7)

---

### INT-002: Administrative Data Integration

**Description**: The platform MUST integrate with government administrative data sources (HMRC, DWP, DVLA, NHS) via secure APIs.

**Rationale**: ONS increasingly uses administrative data (tax records, benefits, health) to supplement surveys, reducing respondent burden and improving timeliness.

**Acceptance Criteria**:
- [ ] API integration with government departments: HMRC (tax data), DWP (benefits), NHS (health)
- [ ] OAuth 2.0 or mutual TLS authentication
- [ ] Data sharing agreements implemented in access controls
- [ ] Secure enclave for linkage of sensitive datasets
- [ ] Automated reconciliation: data quality checks on received data

**Priority**: MUST_HAVE

**Related Principle**: Security by Design and Zero Trust (Principle 10)

---

### INT-003: ONS Website Integration

**Description**: The platform MUST provide APIs for ONS website to display latest statistics and enable data downloads.

**Rationale**: ONS.gov.uk is the primary public interface. Website must display up-to-date statistics from platform APIs.

**Acceptance Criteria**:
- [ ] RESTful APIs for website consumption
- [ ] Real-time updates: website reflects published data within 1 minute
- [ ] Caching layer for high-traffic pages
- [ ] File download generation: CSV, Excel, SDMX formats
- [ ] API performance: <200ms p95 for website queries

**Priority**: MUST_HAVE

**Related Principle**: API-First Design (Principle 7)

---

### INT-004: Research Access Integration

**Description**: The platform MUST integrate with ONS Secure Research Service (SRS) for approved researcher access to microdata.

**Rationale**: Researchers require access to anonymised microdata under strict controls. Integration enables secure data provision without manual file transfers.

**Acceptance Criteria**:
- [ ] Secure data transfer to SRS environment
- [ ] Researcher authentication and authorisation
- [ ] Five Safes framework controls: Safe people, projects, settings, data, outputs
- [ ] Audit trail of researcher access
- [ ] Output checking workflow before research dissemination

**Priority**: SHOULD_HAVE

**Related Principle**: Privacy by Design and Statistical Disclosure Control (Principle 6)

---

## Requirement Conflicts & Resolutions

### Conflict RC-1: Cost Reduction vs. Security Investment

**Conflicting Requirements**:
- BR-001: Reduce Infrastructure Costs (40% reduction target)
- NFR-SEC-001 to NFR-SEC-003: Security requirements (Zero Trust, audit logging, vulnerability management)

**Nature of Conflict**: Security implementation requires investment in additional tooling (SIEM, secrets management, vulnerability scanning), dedicated security roles, and security testing which increases costs. This conflicts with aggressive cost reduction targets.

**Resolution Strategy**:
- Security is non-negotiable for government data - implement security requirements fully
- Focus cost reduction on compute/storage optimisation rather than security tooling
- Use cloud-native security services (AWS Security Hub, Azure Security Center) rather than third-party tools where possible
- Accept that security baseline may require adjusting cost reduction target to 35% rather than 40%

**Decision**: Security requirements take precedence. Cost reduction target remains 40% but excludes mandatory security tooling costs.

**Approved By**: Chief Data Officer, Head of Cyber Security

---

### Conflict RC-2: API Performance vs. Comprehensive Audit Logging

**Conflicting Requirements**:
- NFR-P-001: API Response Time (<500ms p95)
- NFR-SEC-002: Audit Logging (all data access events)

**Nature of Conflict**: Synchronous audit logging adds latency to every API request. At high volumes (10,000 req/s), audit log writes could become a bottleneck affecting p95 latency targets.

**Resolution Strategy**:
- Implement asynchronous audit logging using message queue (Kafka/SQS)
- Buffer audit events and write in batches
- Ensure audit logs are guaranteed delivery (at-least-once semantics)
- Accept slight risk of audit log delay (not loss) during peak load

**Decision**: Use asynchronous audit logging with guaranteed delivery. Accept up to 5-minute delay in audit log availability during peak load spikes.

**Approved By**: Head of Cyber Security, Chief Data Architect

---

### Conflict RC-3: Open Data Access vs. Pre-Release Controls

**Conflicting Requirements**:
- BR-003: Enhance Public Data Access (API-first, open access)
- FR-004: Pre-Release Access Control (restrict access before publication)
- NFR-C-002: Statistics Act 2007 Compliance

**Nature of Conflict**: Open by default principle conflicts with statutory requirement to restrict pre-release access to designated users only.

**Resolution Strategy**:
- Implement clear state machine for data lifecycle: DRAFT → PRE_RELEASE → PUBLISHED
- Published data is fully open with no authentication required
- Pre-release data requires authentication and authorisation check
- System enforces automatic transition from PRE_RELEASE to PUBLISHED at scheduled time
- No manual intervention can delay publication once scheduled

**Decision**: Two-tier access model - unrestricted for published data, strictly controlled for pre-release. Statistics Act compliance takes precedence.

**Approved By**: National Statistician, Chief Data Officer

---

### Conflict RC-4: Comprehensive SDC vs. Publication Speed

**Conflicting Requirements**:
- FR-005: Statistical Disclosure Control (comprehensive automated SDC)
- BR-002: Improve Publication Efficiency (reduce time-to-publish)
- NFR-P-002: Publication Processing Time (<24 hours for census scale)

**Nature of Conflict**: Comprehensive SDC analysis, especially secondary suppression and re-identification risk assessment, is computationally intensive. For census-scale data (67M records), thorough SDC could exceed 24-hour processing target.

**Resolution Strategy**:
- Implement tiered SDC approach based on sensitivity classification
- High-sensitivity data (geography <1000 population): comprehensive SDC with risk assessment
- Standard data: automated rule-based SDC without full risk assessment
- Pre-compute SDC during data processing, not at publication time
- Invest in SDC algorithm optimisation and parallel processing

**Decision**: Tiered SDC based on sensitivity. Standard automated SDC for majority of publications, comprehensive SDC reserved for high-risk datasets with extended processing window.

**Approved By**: Chief Statistician, Data Protection Officer

---

## Requirements Traceability

### Business Requirement to Architecture Principle Mapping

| Business Requirement | Architecture Principles |
|---------------------|------------------------|
| BR-001: Reduce Infrastructure Costs | Principle 12 (Performance and Efficiency), Principle 9 (Cloud-Native) |
| BR-002: Improve Publication Efficiency | Principle 13 (Automation and Continuous Delivery) |
| BR-003: Enhance Public Data Access | Principle 1 (Open by Default), Principle 7 (API-First) |
| BR-004: Meet UK Government Digital Standards | All principles (Service Standard alignment) |
| BR-005: Enable Census-Scale Processing | Principle 2 (Scalability), Principle 12 (Performance) |

### Non-Functional Requirement to Architecture Principle Mapping

| NFR Category | Requirements | Architecture Principles |
|-------------|--------------|------------------------|
| Performance | NFR-P-001 to NFR-P-003 | Principle 12 (Performance and Efficiency) |
| Security | NFR-SEC-001 to NFR-SEC-003 | Principle 10 (Security by Design and Zero Trust) |
| Availability | NFR-A-001 to NFR-A-003 | Principle 3 (Resilience and Fault Tolerance) |
| Scalability | NFR-S-001 to NFR-S-002 | Principle 2 (Scalability and Elastic Capacity) |
| Compliance | NFR-C-001 to NFR-C-004 | Principle 6 (Privacy by Design), Principle 1 (Open by Default) |
| Observability | NFR-O-001 to NFR-O-003 | Principle 11 (Observability and Operational Excellence) |

### Full Traceability Matrix

| Stakeholder | Driver | Goal | Requirement | Use Case |
|-------------|--------|------|-------------|----------|
| CDO | SD-1: Cost reduction | G-1: 40% cost reduction | BR-001, NFR-S-001, NFR-S-002 | UC-5, UC-6 |
| Director of Statistical Production | SD-2: Efficiency | G-2: 60% less manual effort | BR-002, FR-002, FR-006 | UC-2 |
| National Statistician | SD-3: Accessibility | G-3: API-first access | BR-003, FR-001, FR-003 | UC-1, UC-3 |
| GDS Service Assessor | SD-4: Standards | G-4: Service Standard | BR-004, NFR-C-004 | All UCs |
| Census Programme Director | SD-5: Scale | G-5: Census processing | BR-005, NFR-P-002, NFR-S-002 | UC-5 |
| Head of Cyber Security | SD-6: Security | G-6: GovS 007 compliance | NFR-SEC-001 to 003, NFR-C-003 | UC-4, UC-6 |
| Data Protection Officer | SD-7: Privacy | G-7: GDPR compliance | FR-005, NFR-C-001, DR-001, DR-002 | UC-2 |
| Data Users | SD-8: Access | G-8: Better data access | FR-001, FR-003, INT-003 | UC-1, UC-3 |

---

## Assumptions and Constraints

### Assumptions

1. **Cloud Provider**: Assumes UK-based cloud regions available from major providers (AWS, Azure, GCP)
2. **Internet Connectivity**: Public API access assumes users have internet connectivity
3. **Source Data Quality**: Assumes survey systems provide data meeting basic quality standards
4. **Resourcing**: Assumes ONS dedicates sufficient statistician time for migration and testing
5. **Legislative Stability**: Assumes no major changes to Statistics Act or Data Protection Act during implementation

### Constraints

1. **Budget**: Total programme budget £18M capital + £6.7M annual operating
2. **Timeline**: 18-month implementation (Alpha: 3 months, Beta: 9 months, Live: 6 months)
3. **Regulatory**: Must maintain Statistics Act compliance throughout migration (no publication disruption)
4. **Security**: All solutions must achieve OFFICIAL accreditation (no cloud services without UK region)
5. **Skills**: ONS has limited cloud engineering expertise (vendor must provide training/knowledge transfer)
6. **Legacy Integration**: Must integrate with legacy systems during transition (5+ years until full decommission)

---

## Budget

### Capital Budget (Implementation)

| Category | Allocation | Notes |
|----------|------------|-------|
| Cloud Infrastructure Setup | £4.0M | Initial provisioning, networking, security controls |
| Software Development | £6.0M | Platform development, API implementation, automation |
| Data Migration | £2.5M | Migration tooling, validation, parallel running |
| Integration Development | £2.0M | Survey systems, admin data, website integration |
| Security Implementation | £1.5M | Zero Trust architecture, SIEM, penetration testing |
| Training & Knowledge Transfer | £1.0M | ONS staff upskilling, documentation |
| Contingency (10%) | £1.0M | Risk buffer |
| **Total Capital** | **£18.0M** | |

### Operating Budget (Annual)

| Category | Year 1 | Year 2 (Target) | Notes |
|----------|--------|-----------------|-------|
| Cloud Compute & Storage | £3.5M | £3.0M | Auto-scaling, reserved instances |
| Software Licenses | £1.0M | £0.8M | SaaS tools, support contracts |
| Operations & Support | £2.0M | £1.9M | L1/L2 support, incident management |
| Security Operations | £0.8M | £0.7M | SOC, vulnerability management |
| Continuous Improvement | £0.5M | £0.3M | Performance optimisation, feature additions |
| **Total Operating** | **£7.8M** | **£6.7M** | Target: 40% reduction from £11.2M baseline |

---

## Open Questions and TBDs

### Technical Decisions Required

1. **Cloud Provider Selection**: AWS, Azure, or GCP? (Resolved through procurement evaluation)
2. **API Rate Limiting**: 100 req/min anonymous sufficient or adjust based on user research?
3. **Data Lake Technology**: Choice of data lake storage and query engine (resolved in design phase)
4. **Microservices Granularity**: How many services? What are service boundaries? (resolved in HLD)

### Business Decisions Required

1. **Charging Model**: Should ONS charge for high-volume API usage? (Policy decision with National Statistician)
2. **Data Catalog Scope**: Include unpublished/internal datasets or only public statistics?
3. **Migration Prioritisation**: Which statistical series migrate first? (Input from statistical divisions)
4. **Deprecation Timeline**: When can legacy systems be decommissioned? (depends on migration success)

### User Research Required

1. **Developer Needs**: Conduct user research with API consumers to validate requirements
2. **Accessibility Testing**: Test with disabled users to validate WCAG compliance
3. **Statistician Workflows**: Shadow statisticians to understand publication workflow pain points

---

## Acceptance and Success Criteria

### Project Success Criteria

The project will be considered successful when:

1. **Go-Live**: Platform operational and serving 100% of targeted statistical series via APIs
2. **Cost Target**: Infrastructure costs ≤£6.7M/year by Month 24 (40% reduction achieved)
3. **Performance**: All NFR targets met (availability, latency, scalability)
4. **Compliance**: GDS Service Standard LIVE assessment passed
5. **User Adoption**: 10,000 registered API users, 50% of consumption via APIs
6. **Statistician Satisfaction**: 80% satisfaction score with publication tools

### Testing and Validation

1. **Functional Testing**: 100% pass rate on acceptance criteria for MUST_HAVE requirements
2. **Performance Testing**: Load testing demonstrates NFR compliance at peak capacity
3. **Security Testing**: Penetration testing and ITHC passed with zero critical/high findings
4. **User Acceptance Testing**: Statisticians validate publication workflows, developers validate APIs
5. **Disaster Recovery Testing**: Successful failover exercise demonstrating RTO/RPO compliance
6. **Migration Testing**: Parallel running validation shows 100% data integrity

---

## Approval

### Requirements Review

| Reviewer | Role | Review Date | Status | Comments |
|----------|------|-------------|--------|----------|
| Chief Data Officer | Executive Sponsor | PENDING | PENDING | |
| Director of Statistical Production | Product Owner | PENDING | PENDING | |
| Chief Data Architect | Technical Authority | PENDING | PENDING | |
| Head of Cyber Security | Security Authority | PENDING | PENDING | |
| Data Protection Officer | Privacy Authority | PENDING | PENDING | |
| GDS Service Assessor | Government Assurance | PENDING | PENDING | |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Sponsor | | | |
| Business Owner | | | |
| Technical Authority | | | |

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-01-26
**ArcKit Version**: 0.11.2
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-opus-4-5-20251101
**Generation Context**: Requirements updated to template v0.11.2, aligned with architecture principles defined in ARC-001-PRIN-v1.1 and stakeholder analysis in ARC-001-STKE-v1.1
