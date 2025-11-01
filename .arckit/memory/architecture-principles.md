# Office for National Statistics (ONS) - Enterprise Architecture Principles

## Document Information

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-PRIN-v1.0 |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Document Type** | Enterprise Architecture Principles |
| **Classification** | OFFICIAL |
| **Version** | 1.0 |
| **Status** | DRAFT |
| **Date** | 2025-11-01 |
| **Owner** | Chief Data Architect, ONS |

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-01 | ArcKit AI | Initial creation from `/arckit.principles` command |

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
- ❌ Restricting access to non-sensitive published statistics
- ❌ Using proprietary formats that limit accessibility
- ❌ Applying excessive security to public data
- ❌ Failing to document classification rationale

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

**Performance Targets**:
- Peak publication load: 10,000 requests/second
- Auto-scale response time: <5 minutes
- Census data processing: 67M records in <24 hours

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

**Service Level Objectives**:
- Publication API availability: 99.95%
- Mean Time To Recovery (MTTR): <30 minutes
- Successful publications without incident: >95%

---

## II. Data Principles

### 4. Single Source of Truth

**Principle Statement**:
Each statistical dataset MUST have ONE authoritative source, version-controlled and traceable to ONS official releases.

**Rationale**:
Conflicting versions of statistics undermine public trust. ONS's credibility depends on consistency between website, APIs, download services, and downstream systems.

**Implications**:
- Centralized data catalog with metadata registry
- Version control for all statistical series
- Immutable published releases (append-only)
- Clear lineage from source data to published statistics
- Deprecation process for superseded datasets
- Canonical URLs for each dataset

**Validation Gates**:
- [ ] Dataset registered in central catalog
- [ ] Lineage documented from source to publication
- [ ] Version history maintained
- [ ] Canonical identifier assigned
- [ ] Supersession relationships documented

**Common Violations to Avoid**:
- ❌ Multiple conflicting copies of same dataset
- ❌ Undocumented dataset modifications
- ❌ Missing version history
- ❌ Unclear which dataset is authoritative

---

### 5. Data Quality by Design

**Principle Statement**:
Data quality checks MUST be automated and applied at ingestion, transformation, and publication stages with clear quality indicators.

**Rationale**:
Statistical accuracy and methodological soundness are core to ONS's reputation as an independent national statistical institute. Manual quality checks don't scale and introduce human error.

**Implications**:
- Implement automated validation rules at each pipeline stage
- Apply statistical disclosure control (SDC) automatically
- Flag data quality issues before publication
- Publish quality indicators alongside statistics
- Automated testing for statistical methodology code
- Data profiling and anomaly detection

**Validation Gates**:
- [ ] Automated quality checks implemented
- [ ] SDC rules verified
- [ ] Quality metadata published with statistics
- [ ] Methodology code has automated tests
- [ ] Data lineage tracked through pipeline

**Quality Metrics**:
- Completeness: >99% for mandatory fields
- Accuracy: Statistical methodology verified
- Timeliness: Published per release calendar
- Consistency: Cross-validation with related series

---

### 6. Privacy by Design and Statistical Disclosure Control

**Principle Statement**:
All data processing MUST implement privacy-preserving techniques and Statistical Disclosure Control (SDC) to prevent identification of individuals or businesses.

**Rationale**:
ONS handles sensitive personal and commercial data under legal privilege. Obligations under GDPR, Data Protection Act 2018, and Statistics and Registration Service Act 2007 require rigorous controls.

**Implications**:
- Apply SDC rules automatically (suppression, perturbation, aggregation)
- Implement differential privacy where appropriate
- Minimize data retention periods
- Encrypt data at rest and in transit
- Privacy Impact Assessments (PIAs) for new processing
- Secure multi-party computation for sensitive linkage

**Validation Gates**:
- [ ] SDC rules applied and verified
- [ ] PIA completed for new processing
- [ ] Re-identification risk assessed
- [ ] Data minimization applied
- [ ] Encryption verified (at rest and in transit)

**Common Violations to Avoid**:
- ❌ Publishing small cell counts (<3 individuals)
- ❌ Insufficient aggregation levels
- ❌ Retaining personal data longer than necessary
- ❌ Inadequate anonymization techniques

---

## III. Integration Principles

### 7. API-First Design

**Principle Statement**:
All data products MUST be accessible via well-documented APIs before building user interfaces. APIs are the primary consumption method.

**Rationale**:
APIs enable data reuse by government, business, academia, and civil society. API-first ensures consistency across channels and reduces duplication.

**Implications**:
- Design APIs before web interfaces
- Publish OpenAPI specifications for all APIs
- Consistent authentication for restricted data
- Versioned APIs with deprecation policy (minimum 12 months notice)
- Rate limiting and quotas for fairness
- Developer documentation and sandbox environments

**Validation Gates**:
- [ ] API specification published (OpenAPI 3.0+)
- [ ] Developer documentation available
- [ ] Sandbox environment provided
- [ ] Versioning and deprecation policy documented
- [ ] Rate limiting configured

**API Standards**:
- Response time: p95 <500ms, p99 <2s
- Uptime SLA: 99.9% for production APIs
- Breaking changes: 12-month deprecation notice

---

### 8. Interoperability and Open Standards

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

**Interoperability Standards**:
- SDMX for statistical metadata
- OData v4 for query APIs
- W3C DCAT for catalog metadata
- ISO 19115 for geographic metadata

---

## IV. Cloud and Infrastructure Principles

### 9. Cloud-Native Architecture

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
- [ ] Infrastructure as Code implemented
- [ ] Containers used for compute workloads
- [ ] Deployment automation implemented
- [ ] Vendor lock-in risks assessed

**Common Violations to Avoid**:
- ❌ Self-hosting services with managed alternatives
- ❌ Manual infrastructure provisioning
- ❌ Pet servers vs. cattle approach
- ❌ Tight coupling to proprietary cloud features

---

### 10. Security by Design and Zero Trust

**Principle Statement**:
Security controls MUST be embedded into every layer of the architecture, following Zero Trust principles with least-privilege access.

**Rationale**:
ONS handles OFFICIAL and OFFICIAL-SENSITIVE data including pre-release market-sensitive statistics. Perimeter security is insufficient; assume breach and verify every access.

**Implications**:
- Multi-factor authentication (MFA) for all users
- Service mesh for encrypted service-to-service communication
- Role-Based Access Control (RBAC) with least privilege
- Audit logging for all data access
- Regular penetration testing and security reviews
- Security controls proportionate to classification

**Validation Gates**:
- [ ] MFA enforced for user access
- [ ] Service-to-service encryption verified
- [ ] RBAC policies defined and tested
- [ ] Audit logs centralized and monitored
- [ ] Security scanning in CI/CD pipeline

**Security Standards**:
- Encryption: TLS 1.3+ in transit, AES-256 at rest
- MFA: Required for all user accounts
- Vulnerability patching: Critical <24hrs, High <7 days
- Penetration testing: Annual external, quarterly internal

---

## V. Quality Attributes

### 11. Observability and Operational Excellence

**Principle Statement**:
All services MUST emit structured logs, metrics, and traces to enable rapid diagnosis and resolution of issues.

**Rationale**:
Complex distributed systems fail in unpredictable ways. Observability enables teams to understand system behavior in production and meet publication deadlines.

**Implications**:
- Structured JSON logging with correlation IDs
- Metrics instrumentation (RED: Rate, Errors, Duration)
- Distributed tracing for request flows
- Centralized log aggregation and analysis
- Service Level Objectives (SLOs) with error budgets
- Automated alerting on SLO violations

**Validation Gates**:
- [ ] Structured logging implemented
- [ ] Metrics exported and visualized
- [ ] Distributed tracing configured
- [ ] SLOs defined and monitored
- [ ] Alerting rules configured

**Observability Targets**:
- Mean Time To Detect (MTTD): <5 minutes
- Mean Time To Recovery (MTTR): <30 minutes
- Log retention: 90 days online, 7 years archive

---

### 12. Performance and Efficiency

**Principle Statement**:
Data pipelines and APIs MUST meet defined performance targets, with continuous optimization for cost and latency.

**Rationale**:
Taxpayer value requires efficient use of resources. Slow systems reduce productivity and increase infrastructure costs.

**Implications**:
- Define performance requirements early
- Performance testing in CI/CD pipeline
- Query optimization for analytical workloads
- Caching strategies for frequently accessed data
- Regular performance profiling
- Cost allocation and chargeback models

**Validation Gates**:
- [ ] Performance requirements documented
- [ ] Load testing performed
- [ ] Caching strategy implemented
- [ ] Query performance optimized
- [ ] Cost monitoring configured

**Performance Targets**:
- API response: p95 <500ms, p99 <2s
- Batch processing: Cost per GB processed tracked
- Resource utilization: >60% for reserved capacity
- Query optimization: <10s for 90% of queries

---

## VI. Development Practices

### 13. Automation and Continuous Delivery

**Principle Statement**:
All deployment processes MUST be fully automated with continuous integration and continuous delivery (CI/CD) pipelines.

**Rationale**:
Manual deployments are error-prone, slow, and don't scale. Automation ensures consistency and enables rapid iteration while maintaining quality.

**Implications**:
- Git-based source control for all code
- Automated testing (unit, integration, end-to-end)
- Deployment pipelines with approval gates
- Feature flags for controlled rollouts
- Automated rollback on failure
- Blue-green or canary deployments

**Validation Gates**:
- [ ] CI/CD pipeline implemented
- [ ] Automated tests achieve target coverage
- [ ] Deployment requires no manual steps
- [ ] Rollback procedure automated and tested
- [ ] Deployment metrics tracked

**Automation Targets**:
- Deployment frequency: Daily for non-critical, weekly for critical
- Change failure rate: <5%
- Lead time: <4 hours from commit to production
- Rollback time: <15 minutes

---

### 14. Code Quality and Reproducibility

**Principle Statement**:
All analytical code and statistical methods MUST be version-controlled, peer-reviewed, and reproducible.

**Rationale**:
Statistical credibility requires transparency and reproducibility. Code review catches errors before publication. Versioning enables audit trail.

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

**Quality Standards**:
- Code review: 100% for publication-impacting code
- Test coverage: >80% for statistical methods
- Documentation: README with usage examples
- Reproducibility: All published outputs reproducible from code

---

## VII. Exception Process

### When Exceptions Are Permitted

Exceptions to these principles may be granted ONLY when:
1. **Compliance Risk**: Following the principle creates regulatory or legal risk
2. **Technical Constraint**: Legacy system integration prevents compliance
3. **Cost/Benefit**: Demonstrable evidence that cost exceeds benefit by 10x
4. **Time Sensitivity**: Emergency response where principle delays critical capability

### Exception Request Process

1. **Document Rationale**: Written justification with evidence
2. **Propose Mitigation**: How will risks be managed?
3. **Define Sunset Date**: When will the exception be resolved?
4. **Review Board Approval**: Chief Data Architect + CDO/CTO sign-off required
5. **Quarterly Review**: All active exceptions reviewed for closure

### Exception Register

All approved exceptions MUST be logged in the Enterprise Architecture Exception Register with:
- Principle violated
- Business justification
- Risk mitigation plan
- Sunset date
- Approval authority
- Review schedule

---

## VIII. Governance

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

### Compliance Monitoring

Architecture compliance will be measured through:
- Automated architecture fitness functions
- Service assessments at Alpha, Beta, Live phases
- Annual architecture health checks
- Exception register review
- Technical debt tracking

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2025-11-01
**ArcKit Version**: 0.8.1
**Project**: ONS Data Platform Modernisation (Project 001)
**AI Model**: claude-sonnet-4-5-20250929
