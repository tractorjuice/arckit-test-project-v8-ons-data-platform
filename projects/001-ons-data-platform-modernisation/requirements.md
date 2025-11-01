# Project Requirements: ONS Data Platform Modernisation

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Business and Technical Requirements |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2025-11-01 |
| **Last Modified** | 2025-11-01 |
| **Review Date** | 2025-12-01 |
| **Owner** | Chief Data Architect, ONS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | Project Team, Architecture Team, ONS Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-01 | ArcKit AI | Initial creation from `/arckit.requirements` command | [PENDING] | [PENDING] |

## Document Purpose

This document defines the comprehensive business and technical requirements for the Office for National Statistics (ONS) Data Platform Modernisation project. It will be used for:
- Vendor RFP/procurement processes
- Architecture design and review
- Solution evaluation and scoring
- Acceptance testing and validation
- Change control and scope management

---

## Executive Summary

### Business Context

The Office for National Statistics (ONS) is the UK's largest independent producer of official statistics and the recognised national statistical institute. ONS serves the public good by collecting, analysing, and disseminating trusted statistics about the UK's economy, population, and society.

The current ONS data platform infrastructure was built incrementally over the past decade, resulting in a fragmented landscape of disparate systems, inconsistent data formats, and manual processes that limit agility and scalability. Recent challenges include:

- **Publication spikes**: Major economic releases (GDP, CPI, Labour Market Statistics) generate traffic spikes that strain infrastructure capacity
- **Census scale**: The 2021 Census demonstrated the need for systems capable of processing 67 million population records
- **Digital expectations**: Users expect modern API access, real-time data, and self-service capabilities rather than static file downloads
- **Operational burden**: Manual publication processes require significant statistician time, delaying releases and increasing error risk
- **Cloud-first mandate**: UK Government Digital Service (GDS) policy requires migration from on-premises to cloud infrastructure

This modernisation will transform ONS's data infrastructure to support the next generation of statistical publishing, improving public access to trusted statistics while reducing operational costs and technical debt.

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

## Generation Metadata

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2025-11-01
**ArcKit Version**: 0.8.1
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-sonnet-4-5-20250929
**Generation Context**: Requirements generated based on ONS Data Platform modernisation scope, aligned with architecture principles defined in ARC-001-PRIN-v1.0
