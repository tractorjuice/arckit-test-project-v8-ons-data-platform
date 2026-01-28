# Office for National Statistics (ONS) - Enterprise Architecture Principles

> **Template Status**: Live | **Version**: 0.11.2 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-PRIN-v1.1 |
| **Document Type** | Enterprise Architecture Principles |
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
| **Distribution** | ONS Architecture Team, Delivery Teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-01 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to align with template v0.11.2: enhanced document control, validation gates, principle summary checklist | PENDING | PENDING |

---

## Executive Summary

This document establishes the immutable principles governing all technology architecture decisions for the Office for National Statistics (ONS) Data Platform. These principles ensure consistency, security, scalability, and alignment with the UK Government's Digital Service Standard and ONS's statutory duty to deliver trusted statistics for public good.

**Scope**: All data platform projects, systems, and initiatives
**Authority**: ONS Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved by Chief Data Officer/CTO

**Philosophy**: These principles are **technology-agnostic** - they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**UK Government Alignment**:
- Government Digital Service (GDS) Service Standard
- UK Government Technology Code of Practice
- Government Functional Standard GovS 007: Security
- Data Ethics Framework
- Statistics and Registration Service Act 2007

---

## I. Strategic Principles

### 1. Open by Default, Secure by Design

**Principle Statement**:
All ONS data MUST be published openly and accessibly by default, while maintaining appropriate security controls for sensitive or unpublished statistics.

**Rationale**:
ONS's statutory duty under the Statistics and Registration Service Act 2007 is to serve the public good by making trusted statistics available to all. Openness increases transparency, enables reuse, and maximizes societal value of public data investments.

**Implications**:
- Default to open data formats (CSV, JSON, Parquet)
- Implement classification-based access controls
- Publish data through open APIs with clear licensing
- Apply security proportionate to data classification
- Separate publishable statistics from sensitive source data
- Pre-release access must comply with statutory restrictions

**Validation Gates**:
- [ ] Eligible datasets assessed for open publication
- [ ] Data classification documented (OFFICIAL/OFFICIAL-SENSITIVE)
- [ ] Open Government Licence applied where appropriate
- [ ] Pre-release access procedures comply with Statistics Act
- [ ] Security controls proportionate to classification

**Common Violations to Avoid**:
- Restricting access to non-sensitive published statistics
- Using proprietary formats that limit accessibility
- Applying excessive security to public data
- Failing to document classification rationale

---

### 2. Scalability and Elastic Capacity

**Principle Statement**:
All data platform systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load.

**Rationale**:
ONS publishes major economic indicators (GDP, CPI, Labour Market) that generate significant traffic spikes. The platform must handle census-scale data volumes (67 million population records) while remaining cost-efficient during quiet periods.

**Implications**:
- Design for stateless, containerized workloads
- Use cloud-native auto-scaling capabilities
- Avoid hard-coded limits or single-instance bottlenecks
- Plan for distributed processing frameworks
- Separate compute from storage for independent scaling
- Implement queue-based load leveling

**Validation Gates**:
- [ ] System can scale horizontally (add more instances)
- [ ] Load testing demonstrates handling of publication spikes
- [ ] Auto-scaling policies defined and tested
- [ ] No single points of failure limiting capacity
- [ ] Cost model accounts for elastic scaling
- [ ] Scaling metrics and triggers defined

**Performance Targets**:
- Peak publication load: 10,000 requests/second
- Auto-scale response time: <5 minutes
- Census data processing: 67M records in <24 hours

**Common Violations to Avoid**:
- Hard-coded capacity limits
- Stateful services that cannot replicate
- Single-instance databases without read replicas
- Monolithic batch jobs that cannot parallelize

---

### 3. Resilience and Fault Tolerance

**Principle Statement**:
The data platform MUST be resilient to component failures, with no single point of failure for critical publication pipelines.

**Rationale**:
ONS releases are scheduled and market-sensitive (GDP, inflation). System failures during release windows damage public trust and can affect financial markets.

**Implications**:
- Deploy across multiple availability zones
- Implement circuit breakers and graceful degradation
- Design for eventual consistency where appropriate
- Maintain operational playbooks for failure scenarios
- Automated failover for critical services
- Regular chaos engineering exercises

**Validation Gates**:
- [ ] Failure modes identified and mitigated
- [ ] Multi-zone deployment verified
- [ ] Disaster recovery tested (RTO/RPO met)
- [ ] Publication pipelines have no single points of failure
- [ ] Operational runbooks documented
- [ ] Chaos engineering or fault injection testing performed
- [ ] Degraded mode behavior documented

**Service Level Objectives**:
- Publication API availability: 99.95%
- Mean Time To Recovery (MTTR): <30 minutes
- Successful publications without incident: >95%

**Common Violations to Avoid**:
- Single availability zone deployments
- Missing circuit breakers on external dependencies
- Untested failover procedures
- Cascading failures due to tight coupling

---

### 4. Security by Design and Zero Trust (NON-NEGOTIABLE)

**Principle Statement**:
Security controls MUST be embedded into every layer of the architecture, following Zero Trust principles with least-privilege access. Security is NOT a feature to be added later—it is a foundational requirement.

**Rationale**:
ONS handles OFFICIAL and OFFICIAL-SENSITIVE data including pre-release market-sensitive statistics. Perimeter security is insufficient; assume breach and verify every access.

**Zero Trust Pillars**:
1. **Identity-Based Access**: No network-based trust; every request authenticated
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest
4. **Continuous Verification**: Monitor, log, and analyze all access patterns

**Mandatory Controls**:
- [ ] Multi-factor authentication (MFA) for all human access
- [ ] Service-to-service authentication (mutual TLS, signed tokens, or equivalent)
- [ ] Secrets management via secure vault (never in code or config files)
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest for all data stores (AES-256)
- [ ] Encrypted transport for all network communication (TLS 1.3+)
- [ ] Structured logging of all authentication/authorization events
- [ ] Regular security testing (penetration testing, vulnerability scanning)

**Compliance Frameworks**:
- NCSC Cyber Assessment Framework (CAF)
- ISO 27001
- Government Functional Standard GovS 007: Security
- UK GDPR / Data Protection Act 2018

**Exceptions**:
- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with compensating controls.

**Validation Gates**:
- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to requirements
- [ ] Security testing plan defined
- [ ] Incident response runbook created
- [ ] RBAC policies defined and tested
- [ ] Audit logs centralized and monitored

**Security Standards**:
- Encryption: TLS 1.3+ in transit, AES-256 at rest
- MFA: Required for all user accounts
- Vulnerability patching: Critical <24hrs, High <7 days
- Penetration testing: Annual external, quarterly internal

---

### 5. Observability and Operational Excellence

**Principle Statement**:
All services MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. Complex distributed systems fail in unpredictable ways. Observability enables teams to understand system behavior in production and meet publication deadlines.

**Telemetry Requirements**:
- **Logging**: Structured JSON logs with correlation IDs
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates
- **Tracing**: Distributed trace context for request flows
- **Alerting**: Service Level Objective (SLO)-based alerting with actionable runbooks

**Required Instrumentation**:
- Request volume, latency distribution, error rate (RED metrics)
- Resource utilization (CPU, memory, I/O, network)
- Business metrics (publications, data downloads, API calls)
- Security events (auth failures, policy violations, suspicious patterns)

**Log Retention**:
- **Security/audit logs**: 7 years (compliance requirement)
- **Application logs**: 90 days online
- **Metrics**: 2 years with aggregation

**Validation Gates**:
- [ ] Structured logging implemented
- [ ] Metrics exported and visualized
- [ ] Distributed tracing configured
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for common failure scenarios
- [ ] Alerting rules configured
- [ ] Capacity planning metrics tracked

**Observability Targets**:
- Mean Time To Detect (MTTD): <5 minutes
- Mean Time To Recovery (MTTR): <30 minutes
- Log retention: 90 days online, 7 years archive

---

## II. Data Principles

### 6. Single Source of Truth

**Principle Statement**:
Each statistical dataset MUST have ONE authoritative source, version-controlled and traceable to ONS official releases. Derived copies must be clearly labeled and synchronized.

**Rationale**:
Conflicting versions of statistics undermine public trust. ONS's credibility depends on consistency between website, APIs, download services, and downstream systems. Multiple authoritative sources create inconsistency, reconciliation overhead, and data integrity issues.

**Implications**:
- Centralized data catalog with metadata registry
- Version control for all statistical series
- Immutable published releases (append-only)
- Clear lineage from source data to published statistics
- Deprecation process for superseded datasets
- Canonical URLs for each dataset
- Derived/cached copies are read-only and clearly labeled

**Validation Gates**:
- [ ] Dataset registered in central catalog
- [ ] System of record identified for each data entity
- [ ] Lineage documented from source to publication
- [ ] Version history maintained
- [ ] Canonical identifier assigned
- [ ] Supersession relationships documented
- [ ] No bidirectional sync without conflict resolution strategy

**Common Violations to Avoid**:
- Multiple conflicting copies of same dataset
- Undocumented dataset modifications
- Missing version history
- Unclear which dataset is authoritative

---

### 7. Data Quality by Design

**Principle Statement**:
Data quality checks MUST be automated and applied at ingestion, transformation, and publication stages with clear quality indicators.

**Rationale**:
Statistical accuracy and methodological soundness are core to ONS's reputation as an independent national statistical institute. Manual quality checks don't scale and introduce human error.

**Quality Standards**:
- **Completeness**: >99% for mandatory fields, no unexpected nulls
- **Consistency**: Cross-system data reconciliation, cross-validation with related series
- **Accuracy**: Validation rules and constraints enforced at source, methodology verified
- **Timeliness**: Freshness SLAs defined and monitored, published per release calendar

**Implications**:
- Implement automated validation rules at each pipeline stage
- Apply statistical disclosure control (SDC) automatically
- Flag data quality issues before publication
- Publish quality indicators alongside statistics
- Automated testing for statistical methodology code
- Data profiling and anomaly detection

**Validation Gates**:
- [ ] Data quality rules defined and automated
- [ ] Automated quality checks implemented
- [ ] SDC rules verified
- [ ] Quality metadata published with statistics
- [ ] Methodology code has automated tests
- [ ] Data lineage tracked through pipeline
- [ ] Data contracts between producers and consumers
- [ ] Schema evolution strategy documented

---

### 8. Data Sovereignty and Privacy by Design

**Principle Statement**:
All data processing MUST implement privacy-preserving techniques and Statistical Disclosure Control (SDC) to prevent identification of individuals or businesses. Data classification, residency, retention, and access controls MUST comply with regulatory requirements.

**Rationale**:
ONS handles sensitive personal and commercial data under legal privilege. Obligations under GDPR, Data Protection Act 2018, and Statistics and Registration Service Act 2007 require rigorous controls.

**Data Classification Tiers**:
1. **Public**: No restrictions (published statistics, marketing content)
2. **Internal**: Employee-only access (internal documents, non-sensitive data)
3. **Confidential**: Need-to-know basis (unpublished statistics, PII, business data)
4. **Restricted**: Highest controls (pre-release statistics, sensitive personal data)

**Implications**:
- Apply SDC rules automatically (suppression, perturbation, aggregation)
- Implement differential privacy where appropriate
- Minimize data retention periods
- Encrypt data at rest and in transit
- Privacy Impact Assessments (PIAs) for new processing
- Secure multi-party computation for sensitive linkage
- Personal data must reside in compliant jurisdictions

**Data Retention**:
- Automatic deletion after defined retention period
- Legal hold process for litigation/investigation
- Backup retention aligned with compliance requirements

**Validation Gates**:
- [ ] Data classification performed for all data stores
- [ ] SDC rules applied and verified
- [ ] PIA completed for new processing
- [ ] Re-identification risk assessed
- [ ] Data minimization applied
- [ ] Encryption verified (at rest and in transit)
- [ ] Residency requirements mapped to infrastructure
- [ ] Retention policies configured with automated deletion
- [ ] Access controls enforce least privilege and need-to-know

**Common Violations to Avoid**:
- Publishing small cell counts (<3 individuals)
- Insufficient aggregation levels
- Retaining personal data longer than necessary
- Inadequate anonymization techniques

---

## III. Integration Principles

### 9. API-First Design and Loose Coupling

**Principle Statement**:
All data products MUST be accessible via well-documented APIs before building user interfaces. Systems MUST be loosely coupled through published interfaces, avoiding shared databases, file systems, or tight runtime dependencies.

**Rationale**:
APIs enable data reuse by government, business, academia, and civil society. API-first ensures consistency across channels and reduces duplication. Loose coupling enables independent deployment, technology diversity, team autonomy, and system evolution.

**Implications**:
- Design APIs before web interfaces
- Publish OpenAPI specifications for all APIs
- Consistent authentication for restricted data
- Versioned APIs with deprecation policy (minimum 12 months notice)
- Rate limiting and quotas for fairness
- Developer documentation and sandbox environments
- No direct database access across system boundaries
- Each system manages its own data lifecycle

**Validation Gates**:
- [ ] Interface specifications published (OpenAPI 3.0+)
- [ ] Developer documentation available
- [ ] Sandbox environment provided
- [ ] Versioning and deprecation policy documented
- [ ] Rate limiting configured
- [ ] Systems communicate via APIs or events, not database
- [ ] No shared mutable state
- [ ] Deployment of one system doesn't require deployment of another

**API Standards**:
- Response time: p95 <500ms, p99 <2s
- Uptime SLA: 99.9% for production APIs
- Breaking changes: 12-month deprecation notice

**Common Violations to Avoid**:
- Direct database access across system boundaries
- Shared databases between services
- Tight runtime coupling requiring synchronized deployments
- Undocumented or unversioned APIs

---

### 10. Interoperability and Open Standards

**Principle Statement**:
The platform MUST use open standards for data formats, metadata, and protocols to maximize interoperability with national and international statistical systems.

**Rationale**:
ONS data is consumed by diverse users globally. Proprietary formats create barriers and reduce interoperability with international statistical community.

**Implications**:
- Adopt Statistical Data and Metadata eXchange (SDMX) for statistical metadata
- Use ISO 8601 for dates, ISO 3166 for geography codes
- Publish in multiple open formats (CSV, JSON, Parquet)
- Implement W3C DCAT for data catalog
- Support OData v4 protocol
- Align with Eurostat and UN statistical standards

**Validation Gates**:
- [ ] SDMX metadata generated for statistical series
- [ ] Multiple open formats available
- [ ] Geographic codes use ISO 3166
- [ ] Temporal data uses ISO 8601
- [ ] DCAT metadata published
- [ ] Authentication and authorization model documented
- [ ] Error handling and retry behavior specified

**Interoperability Standards**:
- SDMX for statistical metadata
- OData v4 for query APIs
- W3C DCAT for catalog metadata
- ISO 19115 for geographic metadata

---

### 11. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous communication for non-real-time interactions to improve resilience and decoupling.

**Rationale**:
Asynchronous patterns reduce temporal coupling, improve fault tolerance, and enable better scalability.

**When to Use Async**:
- Non-real-time business processes (data processing, batch jobs)
- Event notification and pub/sub patterns
- Long-running operations (census processing, bulk data exports)
- Integration with unreliable or slow external systems

**When Synchronous is Acceptable**:
- Real-time user interactions requiring immediate feedback
- Query operations (read-only, idempotent)
- Transactions requiring immediate consistency

**Validation Gates**:
- [ ] Async patterns used for non-real-time flows
- [ ] Message durability and delivery guarantees defined
- [ ] Event schemas versioned and published
- [ ] Dead letter queues and error handling configured

---

## IV. Cloud and Infrastructure Principles

### 12. Cloud-Native Architecture

**Principle Statement**:
All new services MUST be designed for cloud deployment, using managed services over custom infrastructure.

**Rationale**:
Cloud-native design reduces operational burden, improves scalability, and aligns with Government Cloud First policy.

**Implications**:
- Prefer managed services (databases, queues, storage)
- Use Infrastructure as Code (declarative configuration)
- Containerize workloads for portability
- Design for immutable infrastructure
- Multi-cloud capability where vendor lock-in risk is high
- Serverless-first for event-driven workloads

**Validation Gates**:
- [ ] Managed services used where available
- [ ] Infrastructure defined as code
- [ ] Infrastructure code version-controlled
- [ ] Containers used for compute workloads
- [ ] Automated deployment pipeline for infrastructure
- [ ] No manual infrastructure changes in production
- [ ] Vendor lock-in risks assessed

**Common Violations to Avoid**:
- Self-hosting services with managed alternatives
- Manual infrastructure provisioning
- Pet servers vs. cattle approach
- Tight coupling to proprietary cloud features

---

## V. Quality Attributes

### 13. Performance and Efficiency

**Principle Statement**:
Data pipelines and APIs MUST meet defined performance targets under expected load with efficient use of computational resources.

**Rationale**:
Taxpayer value requires efficient use of resources. Slow systems reduce productivity and increase infrastructure costs.

**Performance Targets** (define for each system):
- **Response Time**: p50, p95, p99 latency targets
- **Throughput**: Requests per second, transactions per minute
- **Concurrency**: Simultaneous user/request capacity
- **Resource Efficiency**: CPU/memory utilization targets

**Implications**:
- Performance requirements defined before implementation
- Performance testing in CI/CD pipeline
- Query optimization for analytical workloads
- Caching strategies for frequently accessed data
- Regular performance profiling
- Cost allocation and chargeback models

**Validation Gates**:
- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at expected capacity
- [ ] Performance metrics monitored in production
- [ ] Caching strategy implemented
- [ ] Query performance optimized
- [ ] Cost monitoring configured
- [ ] Capacity planning model defined

**Performance Standards**:
- API response: p95 <500ms, p99 <2s
- Batch processing: Cost per GB processed tracked
- Resource utilization: >60% for reserved capacity
- Query optimization: <10s for 90% of queries

---

### 14. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
ONS releases are scheduled and market-sensitive. Downtime during critical periods damages public trust.

**Availability Targets** (define for each system):
- **Uptime SLA**: e.g., 99.9% (43.8 min downtime/month), 99.95%, 99.99%
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss

**High Availability Patterns**:
- Redundancy across availability zones / data centers
- Automated health checks and failover
- Active-active or active-passive configurations
- Regular disaster recovery testing

**Validation Gates**:
- [ ] Availability SLA defined
- [ ] RTO and RPO requirements documented
- [ ] Redundancy strategy implemented
- [ ] Failover tested regularly
- [ ] Backup and restore procedures validated

---

### 15. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and comprehensive documentation.

**Rationale**:
Software spends most of its lifetime in maintenance. Design decisions should optimize for understandability and modifiability.

**Implications**:
- Modular architecture with clear boundaries
- Separation of concerns (business logic, data access, presentation)
- Code is self-documenting with meaningful names
- Architecture Decision Records (ADRs) for significant choices
- Automated testing to enable confident refactoring

**Validation Gates**:
- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices

---

## VI. Development Practices

### 16. Automation and Continuous Delivery

**Principle Statement**:
All deployment processes MUST be fully automated with continuous integration and continuous delivery (CI/CD) pipelines. All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Manual deployments are error-prone, slow, and don't scale. Automation ensures consistency and enables rapid iteration while maintaining quality.

**Pipeline Stages**:
1. **Source Control**: All changes committed to version control
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution (unit, integration, end-to-end)
4. **Security Scan**: Dependency and code vulnerability scanning
5. **Deployment**: Automated deployment to environments

**Quality Gates**:
- All tests must pass
- No critical security vulnerabilities
- Code review approval required
- Deployment requires production readiness checklist

**Implications**:
- Git-based source control for all code
- Deployment pipelines with approval gates
- Feature flags for controlled rollouts
- Automated rollback on failure
- Blue-green or canary deployments

**Validation Gates**:
- [ ] Automated CI/CD pipeline exists
- [ ] Pipeline includes security scanning
- [ ] Automated tests achieve target coverage
- [ ] Deployment requires no manual steps
- [ ] Deployment is automated and repeatable
- [ ] Rollback procedure automated and tested
- [ ] Deployment metrics tracked

**Automation Targets**:
- Deployment frequency: Daily for non-critical, weekly for critical
- Change failure rate: <5%
- Lead time: <4 hours from commit to production
- Rollback time: <15 minutes

---

### 17. Code Quality and Reproducibility

**Principle Statement**:
All analytical code and statistical methods MUST be version-controlled, peer-reviewed, and reproducible.

**Rationale**:
Statistical credibility requires transparency and reproducibility. Code review catches errors before publication. Versioning enables audit trail.

**Test Pyramid**:
- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions (15-20% of tests)
- **End-to-End Tests**: Critical user journeys (5-10% of tests)

**Implications**:
- All R, Python, SAS, SQL code in version control
- Mandatory peer review for methodology changes
- Dependency management (lock files for exact versions)
- Reproducible environments (containers, virtual environments)
- Clear separation of code, configuration, and data
- Automated code quality checks (linting, formatting)

**Validation Gates**:
- [ ] Code in version control
- [ ] Peer review completed for changes
- [ ] Dependencies locked and documented
- [ ] Reproducible environment provided
- [ ] Code quality checks passing
- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical paths have end-to-end tests

**Quality Standards**:
- Code review: 100% for publication-impacting code
- Test coverage: >80% for statistical methods
- Documentation: README with usage examples
- Reproducibility: All published outputs reproducible from code

---

## VII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:
- Technical constraints that prevent compliance
- Regulatory or legal requirements
- Transitional state during migration
- Pilot/proof-of-concept with defined end date
- Cost/benefit: Demonstrable evidence that cost exceeds benefit by 10x

**Exception Request Requirements**:
- [ ] Justification with business/technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound)
- [ ] Remediation plan to achieve compliance

**Approval Process**:
1. Submit exception request to Enterprise Architecture team
2. Review by architecture review board
3. Chief Data Architect + CDO/CTO sign-off required for critical principles
4. Document exception in project architecture documentation
5. Regular review of exceptions (quarterly)

### Exception Register

All approved exceptions MUST be logged in the Enterprise Architecture Exception Register with:
- Principle violated
- Business justification
- Risk mitigation plan
- Sunset date
- Approval authority
- Review schedule

---

## VIII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones:

**Discovery/Alpha**:
- [ ] Architecture principles understood
- [ ] High-level approach aligns with principles
- [ ] No obvious principle violations

**Beta/Design**:
- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Security and data principles validated

**Pre-Production**:
- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified

### Ownership and Accountability

| Role | Responsibility |
|------|-----------------|
| **Chief Data Officer** | Overall accountability for principles compliance |
| **Chief Data Architect** | Maintenance and interpretation of principles |
| **Enterprise Architecture Review Board** | Exception approvals and compliance monitoring |
| **Service Owners** | Compliance within their services |
| **Delivery Teams** | Day-to-day application of principles |

### Review Cycle

- **Quarterly**: Metrics review and exception register audit
- **Annually**: Full principles review for relevance and updates
- **Ad-hoc**: When new GDS guidance or government policy emerges

### Enforcement

- Architecture reviews are **mandatory** for all projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective reviews for compliance on live systems

### Compliance Monitoring

Architecture compliance will be measured through:
- Automated architecture fitness functions
- Service assessments at Alpha, Beta, Live phases
- Annual architecture health checks
- Exception register review
- Technical debt tracking

---

## IX. Appendix

### Principle Summary Checklist

| Principle | Category | Criticality | Validation |
|-----------|----------|-------------|------------|
| Open by Default, Secure by Design | Strategic | HIGH | Classification audit, open data assessment |
| Scalability and Elastic Capacity | Strategic | HIGH | Load testing, scaling metrics |
| Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO |
| Security by Design and Zero Trust | Strategic | CRITICAL | Threat model, pen testing |
| Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces |
| Single Source of Truth | Data | HIGH | Data lineage, catalog audit |
| Data Quality by Design | Data | HIGH | Quality metrics |
| Data Sovereignty and Privacy by Design | Data | CRITICAL | Compliance audit, PIA |
| API-First Design and Loose Coupling | Integration | HIGH | API specs, deployment independence |
| Interoperability and Open Standards | Integration | HIGH | Standards compliance |
| Asynchronous Communication | Integration | MEDIUM | Async patterns used |
| Cloud-Native Architecture | Infrastructure | HIGH | IaC coverage |
| Performance and Efficiency | Quality | HIGH | Load testing |
| Availability and Reliability | Quality | CRITICAL | SLA monitoring |
| Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests |
| Automation and Continuous Delivery | DevOps | HIGH | Pipeline exists |
| Code Quality and Reproducibility | DevOps | HIGH | Test coverage, peer review |

---

**Document Version History**

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-01 | ArcKit AI | Initial creation |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2 |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-01-26
**ArcKit Version**: 0.11.2
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-opus-4-5-20251101
