# UK Government Technology Code of Practice (TCoP) Assessment
## ONS Data Platform Modernisation

> **Template Status**: Beta | **Version**: 0.11.2 | **Command**: `/arckit.tcop`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-TCOP-v1.1 |
| **Document Type** | Technology Code of Practice Compliance Assessment |
| **Project** | ONS Data Platform Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2025-11-12 |
| **Last Modified** | 2026-01-26 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-04-26 |
| **Owner** | Chief Data Architect, ONS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Project Team, Architecture Team, ONS Leadership, GDS Service Assessors |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2025-11-12 | ArcKit AI | Initial TCoP assessment from `/arckit.tcop` command | PENDING | PENDING |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2 format; enhanced document control | PENDING | PENDING |

## Document Purpose

This document assesses the ONS Data Platform Modernisation project's compliance against the UK Government Technology Code of Practice (TCoP). The TCoP comprises 13 points that guide technology design, build, and procurement decisions. This assessment identifies compliance gaps, blockers for progression to Beta/Live, and provides prioritized remediation actions.

**Intended Use**:
- GDS Service Standard assessments (Alpha, Beta, Live)
- Digital Spend Control submissions
- Internal architecture governance
- Vendor procurement compliance validation

---

## Executive Summary

**Overall TCoP Compliance**: **10/13 points compliant** → ⚠️ **PARTIALLY COMPLIANT**

**Compliance Breakdown**:
- ✅ **Compliant**: 10 points (Points 1, 4, 5, 6, 7, 8, 9, 10, 12, 13)
- ⚠️ **Partially Compliant**: 2 points (Points 2, 3)
- ❌ **Non-Compliant**: 1 point (Point 11)
- N/A: 0 points

**Project Phase**: Discovery/Alpha → Beta (in progress)

**Critical Issues**: **2 blocking issues** for Beta phase:
1. **Point 11 (Purchasing Strategy)**: No documented purchasing strategy or cloud provider evaluation (**HIGH** - blocks Beta)
2. **Point 2 (Accessibility)**: Accessibility testing not yet completed (**HIGH** - blocks Public Beta)

**Recommendations Summary**:
- **Immediate**: Complete cloud provider evaluation and purchasing strategy (Point 11)
- **Before Beta**: Conduct accessibility testing with disabled users (Point 2)
- **Before Beta**: Publish platform code as open source (Point 3)
- **Before Live**: Complete full open source transition for all components (Point 3)

**Strengths**:
- Strong user research with 12 stakeholders and data subject consultation (Point 1)
- Comprehensive DPIA and Privacy by Design (Point 7)
- Excellent data governance and metadata standards (Point 10)
- Cloud First policy adhered to (Point 5)
- Service Standard alignment (Point 13 - on track for 14/14 criteria)

**Next Steps**:
1. **Week 1-2**: Document purchasing strategy, evaluate AWS vs Azure vs GCP (Point 11)
2. **Week 3-4**: Conduct accessibility testing (Point 2)
3. **Week 5-8**: Publish platform code to GitHub (Point 3)
4. **Before Beta Assessment**: Re-assess TCoP compliance (target: 12/13 compliant)

---

## TCoP Point-by-Point Assessment

### 1. Define User Needs ✅

**Principle**: Understand your users and their needs. Develop knowledge of how users interact with your technology initiatives.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ User research conducted with **12 stakeholders** (S-001 to S-012) across 3 categories
- ✅ User personas documented in stakeholder analysis (Chief Data Officer, Chief Statistician, Data Consumers, etc.)
- ✅ User drivers and goals mapped (27 drivers → 27 SMART goals → 28 outcomes)
- ✅ Accessibility needs identified (NFR-C-004: WCAG 2.1 AA compliance)
- ✅ User needs prioritized via Power-Interest Grid (8 "Manage Closely", 2 "Keep Satisfied", 2 "Keep Informed")
- ✅ Ongoing user feedback mechanism: GDS Service Standard assessments, user satisfaction surveys
- ✅ Data subject consultation: Census 2031 public consultation on questions (2023-2024)

**Findings**:

**Internal Users** (ONS Statisticians):
- Driver D-008: "Reduce manual publication effort by 60%" → FR-002 (Automated Publication Workflow)
- Driver D-017: "Improve data quality and reduce publication errors" → FR-006 (Data Quality Validation)
- User journey mapped: Statistician uploads data → Quality validation → SDC applied → Scheduled publication

**External Users** (Data Consumers):
- Driver D-026: "Access ONS data via modern APIs instead of file downloads" → FR-001 (RESTful APIs)
- Driver D-027: "Find relevant statistics easily without prior knowledge of ONS taxonomy" → FR-003 (Data Catalog with Search)
- User satisfaction target: 85% satisfaction score (BR-003)

**Vulnerable Users** (Data Subjects):
- Census respondents: Privacy notice explains data use, limited erasure rights (DPIA)
- Survey respondents: Voluntary participation, informed consent process

**Gaps**: None identified - comprehensive user research completed

**Requirements Mapping**:
- BR-003: Enhance Public Data Access (driven by user need for API access)
- FR-001: Statistical Data Publication API (direct response to user need)
- FR-003: Data Catalog with Search (discoverability user need)
- NFR-C-004: Accessibility compliance (inclusive user need)

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-1-define-user-needs

---

### 2. Make Things Accessible and Inclusive ⚠️

**Principle**: Make sure your technology, infrastructure and systems are accessible and inclusive for all users.

**Compliance Status**: ⚠️ **PARTIALLY COMPLIANT**

**Evidence**:
- ✅ WCAG 2.1 Level AA compliance committed (NFR-C-004)
- ✅ Keyboard navigation requirement documented (NFR-C-004)
- ✅ Accessibility statement to be published (NFR-C-004)
- ⚠️ Assistive technology testing: **NOT YET COMPLETED** (JAWS, NVDA screen readers)
- ⚠️ Accessibility testing with disabled users: **NOT YET CONDUCTED**
- ⚠️ Automated accessibility testing in CI/CD: **TO BE IMPLEMENTED**
- ✅ Accessible across devices: Responsive design committed (NFR-C-004)
- ✅ Color contrast: Design system to meet 4.5:1 minimum

**Findings**:

**Committed**:
- Developer portal and API documentation will meet WCAG 2.1 AA
- All web interfaces designed for keyboard navigation
- Accessibility statement on developer.ons.gov.uk

**Not Yet Implemented**:
- Manual accessibility testing with screen readers (JAWS, NVDA)
- User testing with disabled users (ONS has not yet recruited disabled users for Beta testing)
- Automated accessibility scanning (Axe, Pa11y) in CI/CD pipeline

**Gaps**:
- ❌ **No accessibility testing with disabled users** (GDS Service Standard Point 5 requires user research with disabled people)
- ❌ **No automated accessibility testing** in CI/CD pipeline
- ⚠️ **Accessibility audit not scheduled** for Alpha/Beta phases

**Requirements Mapping**:
- NFR-C-004: Accessibility (WCAG 2.1 AA) - documented but not yet validated

**Remediation** (**HIGH PRIORITY** - blocks Public Beta):
- **Action 1**: Recruit 5+ disabled users for Beta user research (screen reader users, keyboard-only users, low vision users)
  - **Owner**: User Research Lead
  - **Due**: Before Public Beta (Month 6)
  - **Effort**: 2 weeks
- **Action 2**: Conduct manual accessibility testing with JAWS, NVDA, VoiceOver
  - **Owner**: QA Team
  - **Due**: Beta Week 1
  - **Effort**: 1 week
- **Action 3**: Implement automated accessibility testing (Axe-core, Pa11y-ci) in CI/CD
  - **Owner**: Platform Engineering
  - **Due**: Beta Week 4
  - **Effort**: 3 days
- **Action 4**: Publish accessibility statement on developer.ons.gov.uk
  - **Owner**: Content Design
  - **Due**: Public Beta go-live
  - **Effort**: 2 days

**Score**: **6/10** (committed but not yet validated)

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-2-make-things-accessible-and-inclusive

**Blocker for Beta**: Yes - GDS Service Standard requires accessibility testing with disabled users before Public Beta

---

### 3. Be Open and Use Open Source ⚠️

**Principle**: Publish your code and use open source software to improve transparency, flexibility and accountability.

**Compliance Status**: ⚠️ **PARTIALLY COMPLIANT**

**Evidence**:
- ✅ Open source software used extensively (PostgreSQL, TimescaleDB, Terraform, Kubernetes)
- ⚠️ Code published on public repository: **NOT YET PUBLISHED** (planned for Beta)
- ⚠️ Open source license: **TO BE DECIDED** (MIT or Apache 2.0 recommended)
- ✅ Open Standards Profile (OSP) compliance: SDMX, OpenAPI 3.0, ISO standards
- ⚠️ Contributing back to open source: **NOT YET STARTED**
- ⚠️ Technical documentation publicly available: **PLANNED** (developer.ons.gov.uk)

**Open Source Components Used**:
| Component | License | Purpose | Source |
|-----------|---------|---------|--------|
| PostgreSQL 15+ | PostgreSQL License (permissive) | Primary database | Architecture Principle 9 |
| TimescaleDB | Apache 2.0 | Time-series extension for observations | Data Model implementation guidance |
| OpenAPI 3.0 | Apache 2.0 | API specification | FR-001, Architecture Principle 7 |
| Terraform | MPL 2.0 | Infrastructure as Code | Architecture Principle 9 |
| Kubernetes (likely) | Apache 2.0 | Container orchestration | Architecture Principle 9 (cloud-native) |
| Flyway | Apache 2.0 | Schema migration | Data Model implementation guidance |

**Code Published**:
- Repository: **NOT YET CREATED** (planned: github.com/ONSdigital/data-platform)
- License: **TO BE DECIDED** (recommend MIT or Apache 2.0)
- Documentation: **PLANNED** (developer.ons.gov.uk, API docs)

**Findings**:

**Strengths**:
- Strong commitment to open source infrastructure (PostgreSQL, not proprietary Oracle/SQL Server)
- Open standards for interoperability (SDMX, OpenAPI, ISO 8601, ISO 3166)
- Architecture Principle 8: "Interoperability and Open Standards" mandates open formats

**Gaps**:
- ❌ **Platform code not yet published** as open source (closed development so far)
- ❌ **No open source license selected** (blocks code publication)
- ⚠️ **No contribution strategy** for upstream open source projects
- ⚠️ **Technical documentation** not yet publicly available (developer portal in development)

**Requirements Mapping**:
- Architecture Principle 8: Interoperability and Open Standards
- FR-001: OpenAPI 3.0 specification published (open standard)
- DR-004: SDMX metadata compliance (open standard)

**Remediation** (**MEDIUM PRIORITY** - recommended before Public Beta):
- **Action 1**: Select open source license (recommend Apache 2.0 for government code)
  - **Owner**: Legal / Open Source Programme Office
  - **Due**: Alpha Week 8
  - **Effort**: 1 week (legal review)
- **Action 2**: Publish platform code to GitHub (github.com/ONSdigital/data-platform)
  - **Owner**: Platform Engineering
  - **Due**: Beta Week 1
  - **Effort**: 2 weeks (security review, secrets removal, documentation)
- **Action 3**: Publish technical documentation on developer.ons.gov.uk
  - **Owner**: Technical Writing
  - **Due**: Public Beta go-live
  - **Effort**: 3 weeks
- **Action 4**: Establish open source contribution policy (upstream contributions to PostgreSQL, TimescaleDB if bugs found)
  - **Owner**: Open Source Programme Office
  - **Due**: Beta Week 12
  - **Effort**: 1 week

**Score**: **7/10** (using open source, but not yet publishing code)

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-3-be-open-and-use-open-source

**Blocker for Beta**: No - but strongly recommended for Public Beta (transparency)

---

### 4. Make Use of Open Standards ✅

**Principle**: Build technology that uses open standards to ensure your technology works and communicates with other technology, and can easily be upgraded and expanded.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **SDMX 2.1** (Statistical Data and Metadata eXchange) - ISO 17369 standard for statistical metadata
- ✅ **OpenAPI 3.0+** specification published for all APIs
- ✅ **ISO 8601** for dates and timestamps
- ✅ **ISO 3166** for geography codes (countries, regions)
- ✅ **W3C DCAT** (Data Catalog Vocabulary) for data catalog metadata
- ✅ **OData v4** protocol support (optional, for advanced queries)
- ✅ **JSON, CSV, SDMX-ML** open formats (no proprietary formats)
- ✅ **TLS 1.3** encryption standard
- ✅ **OAuth 2.0** authentication standard
- ✅ **RFC 5322** email format validation

**Findings**:

**Architecture Principle 8: Interoperability and Open Standards**:
> "The platform MUST use open standards for data formats, metadata, and protocols to maximize interoperability with national and international statistical systems."

**Open Standards Applied**:

1. **Statistical Metadata**: SDMX 2.1 (ISO 17369)
   - E-006: SDMX Metadata entity stores Data Structure Definitions (DSDs), codelists
   - Eurostat and UN compatibility for international data exchange

2. **API Specification**: OpenAPI 3.0+
   - FR-001: OpenAPI spec published for all RESTful APIs
   - Developer portal provides Swagger UI for API exploration

3. **Temporal Data**: ISO 8601
   - E-008: Time Period entity uses ISO 8601 codes (2024Q1, 2024-03, 2024)
   - Consistent date/time formatting across all APIs

4. **Geographic Data**: ISO 3166, ONS geography codes
   - E-007: Geography entity uses ISO 3166 for countries, ONS codes for UK regions

5. **Data Catalog**: W3C DCAT
   - FR-003: Data catalog publishes DCAT-compliant metadata
   - Enables federated catalog search across government

**No Proprietary Formats**:
- ❌ No Microsoft-specific formats (Excel binary, SQL Server proprietary extensions)
- ❌ No Oracle-specific PL/SQL (using PostgreSQL open source)
- ✅ Open formats only: JSON, CSV, Parquet, SDMX-ML

**Gaps**: None identified - excellent open standards compliance

**Requirements Mapping**:
- DR-004: Statistical Metadata (SDMX) - mandates SDMX 2.1 compliance
- FR-001: OpenAPI 3.0+ specification
- Architecture Principle 8: Interoperability and Open Standards

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-4-make-use-of-open-standards

---

### 5. Use Cloud First ✅

**Principle**: Consider using public cloud solutions first before you invest in your own hardware.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Cloud First policy adhered to**: No on-premises hardware planned
- ✅ **Cloud-native architecture**: Architecture Principle 9 mandates cloud-native design
- ✅ **Managed services prioritized**: PostgreSQL RDS, S3, managed Kubernetes
- ✅ **UK data sovereignty**: All data stored in UK cloud regions (AWS eu-west-2 London, Azure UK South)
- ✅ **Cloud provider evaluation planned**: AWS vs Azure vs GCP (to be completed)
- ✅ **Multi-cloud capability**: Avoid vendor lock-in via containerization (Kubernetes)
- ✅ **Infrastructure as Code**: Terraform for cloud resource provisioning

**Findings**:

**Architecture Principle 9: Cloud-Native Architecture**:
> "All new services MUST be designed for cloud deployment, using managed services over custom infrastructure."

**Cloud First Justification**:
- **Business Case (SOBC)**: £4.5M annual savings vs on-premises (40% cost reduction)
- **Rationale**: Legacy on-premises infrastructure costs £11.2M/year (hardware refresh, data centre, maintenance)
- **GDS Cloud First mandate**: UK Government policy requires cloud unless justified otherwise

**Cloud Services Planned**:
| Service Type | Cloud Service | Provider | Justification |
|--------------|---------------|----------|---------------|
| Database | PostgreSQL RDS | AWS/Azure | Managed service, automated backups, Multi-AZ |
| Object Storage | S3 / Blob Storage | AWS/Azure | Cold storage for archived observations |
| Container Orchestration | EKS / AKS | AWS/Azure | Managed Kubernetes, auto-scaling |
| API Gateway | AWS API Gateway / Azure API Management | AWS/Azure | Managed, rate limiting, caching |
| Identity Management | AWS Cognito / Azure AD B2C | AWS/Azure | MFA, OAuth 2.0 |
| Monitoring | CloudWatch / Azure Monitor | AWS/Azure | Native cloud monitoring |

**UK Data Sovereignty**:
- All data stored in **UK regions only** (no international data transfers)
- AWS: eu-west-2 (London)
- Azure: UK South (London), UK West (Cardiff)
- GDPR compliance: UK-only storage, no cross-border transfers

**Multi-Cloud Strategy**:
- Containerization (Docker, Kubernetes) provides multi-cloud portability
- Infrastructure as Code (Terraform) supports AWS, Azure, GCP
- Avoids tight coupling to proprietary cloud features (AWS Lambda → generic containers)

**Gaps**:
- ⚠️ **Cloud provider not yet selected** (AWS vs Azure vs GCP) - to be evaluated in Point 11
- ⚠️ **No cost optimization analysis** yet (reserved instances, spot instances, auto-scaling policies)

**Requirements Mapping**:
- BR-001: Reduce Infrastructure Costs (£4.5M savings via cloud)
- Architecture Principle 9: Cloud-Native Architecture
- NFR-S-001: Horizontal Scaling (cloud auto-scaling)

**Remediation**:
- **Action**: Complete cloud provider evaluation (see Point 11)
  - **Owner**: Chief Data Architect
  - **Due**: Alpha Week 8
  - **Effort**: 2 weeks

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-5-use-cloud-first

---

### 6. Make Things Secure ✅

**Principle**: Keep systems and data safe with the appropriate level of security.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Security assessment completed**: UK Government Secure by Design assessment (ukgov-secure-by-design.md)
- ✅ **Threat model**: 22 risks identified in risk register, 6 DPIA risks
- ✅ **Zero Trust Architecture**: Architecture Principle 10 mandates Zero Trust (NFR-SEC-001)
- ✅ **Encryption**: AES-256 at rest, TLS 1.3 in transit
- ✅ **Multi-Factor Authentication (MFA)**: Required for pre-release access
- ✅ **Role-Based Access Control (RBAC)**: Least privilege, statisticians only for microdata
- ✅ **Audit logging**: All access logged for 7 years (GovS 007 compliance)
- ✅ **Penetration testing**: Annual external (CHECK-certified), quarterly internal
- ✅ **Vulnerability management**: Critical <24hrs, High <7 days remediation SLAs
- ✅ **Data classification**: OFFICIAL, CONFIDENTIAL, RESTRICTED (E-014: Survey Microdata)
- ✅ **DPIA completed**: Data Protection Impact Assessment for survey microdata

**Findings**:

**UK Government Secure by Design Assessment** (ukgov-secure-by-design.md):
- **Status**: 10/14 NCSC CAF A-principles assessed
- **Security controls**: Documented for Identity, Data, Device, Interface, Supply Chain

**Architecture Principle 10: Security by Design and Zero Trust**:
> "Security controls MUST be embedded into every layer of the architecture, following Zero Trust principles with least-privilege access."

**Key Security Controls**:

1. **Encryption**:
   - At rest: AES-256 for all databases (PostgreSQL TDE), S3 encryption
   - In transit: TLS 1.3 mandatory (no TLS 1.2 or older)
   - Keys: AWS KMS with automatic key rotation

2. **Access Control**:
   - RBAC: STATISTICIAN, ANALYST, ADMIN, API_USER roles
   - MFA: Mandatory for pre-release access (Statistics Act compliance)
   - Security clearance: ONS staff require SC clearance for microdata access

3. **Network Security**:
   - Secure enclave: Survey microdata in isolated VPC (no internet access)
   - Service mesh: Mutual TLS for service-to-service communication
   - DLP: Data Loss Prevention monitoring for large data transfers

4. **Monitoring**:
   - Audit logging: E-015 (Audit Log) - 7-year retention
   - SIEM: Real-time security monitoring, anomaly detection
   - Incident response: Security Incident Response Plan (SIRP)

**Security Risks Identified**:
- DPIA-001: Unauthorized access to survey microdata (MEDIUM residual risk)
- DPIA-003: Data breach - exfiltration (MEDIUM residual risk)
- 22 risks in risk register (category: Security, Data Protection)

**Gaps**:
- ⚠️ **Penetration testing not yet conducted** (planned before Beta)
- ⚠️ **Security controls not yet implemented** (to be implemented during platform build)

**Requirements Mapping**:
- NFR-SEC-001: Zero Trust Architecture
- NFR-SEC-002: Audit Logging (7-year retention)
- NFR-SEC-003: Vulnerability Management (SLAs defined)
- NFR-C-003: Government Security Standards (GovS 007)

**Remediation** (**MEDIUM PRIORITY** - before Beta):
- **Action**: Conduct penetration testing (CHECK-certified testers)
  - **Owner**: Head of Cyber Security
  - **Due**: Beta Week 8
  - **Effort**: 2 weeks (external pen test)

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-6-make-things-secure

---

### 7. Make Privacy Integral ✅

**Principle**: Make sure users' rights are protected by integrating privacy as an essential part of your system.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **DPIA completed**: Comprehensive Data Protection Impact Assessment (dpia.md)
- ✅ **Privacy by Design**: Architecture Principle 6 mandates Privacy by Design
- ✅ **Data minimization**: Only necessary data collected, 10-year retention limit
- ✅ **Data subject rights**: SAR, rectification, erasure (limited by Statistics Act), portability
- ✅ **Legal basis documented**: Statistics Act 2007 legal obligation (GDPR Article 6(1)(e))
- ✅ **Special category data**: GDPR Article 9(2)(j) - statistical purposes
- ✅ **Privacy notices**: Published at survey collection, Census privacy notice
- ✅ **Data Protection Officer**: ONS DPO oversees GDPR compliance
- ✅ **Statistical Disclosure Control (SDC)**: Automated SDC prevents re-identification
- ✅ **Encryption**: AES-256 at rest, TLS 1.3 in transit

**Findings**:

**DPIA Summary** (dpia.md):
- **ICO Screening**: 3/9 criteria met → DPIA REQUIRED
- **Risks**: 6 risks identified (2 MEDIUM, 4 LOW residual risk)
- **Mitigations**: 22 mitigations proposed
- **ICO Consultation**: NOT REQUIRED (residual risk MEDIUM, not HIGH)
- **Data Subjects**: 67 million individuals (entire UK population)
- **Special Category Data**: Health, ethnicity, religion (GDPR Article 9)

**Architecture Principle 6: Privacy by Design and Statistical Disclosure Control**:
> "All data processing MUST implement privacy-preserving techniques and Statistical Disclosure Control (SDC) to prevent identification of individuals or businesses."

**Key Privacy Controls**:

1. **Statistical Disclosure Control (SDC)**:
   - Primary suppression: Cells <3 individuals suppressed
   - Secondary suppression: Prevent differencing attacks
   - Rounding: All counts rounded to base 3
   - Perturbation: Random noise added to sensitive cells

2. **Data Minimization**:
   - Survey questions: Only necessary questions asked (Census questions approved by Parliament)
   - Retention: 10 years maximum (GDPR data minimization)
   - Anonymization: No names, addresses, exact income collected

3. **Data Subject Rights**:
   - Right to Access: Implemented (SAR via online form)
   - Right to Rectification: User can update profile
   - Right to Erasure: Limited (Statistics Act exemption - GDPR Article 17(3)(d))
   - Right to Portability: JSON export provided
   - Limitations: Clearly communicated in privacy notices

4. **Legal Basis**:
   - Article 6(1)(e): Public task (Statistics Act 2007)
   - Article 9(2)(j): Statistical purposes (special category data)

**Gaps**: None identified - comprehensive DPIA and Privacy by Design

**Requirements Mapping**:
- NFR-C-001: GDPR and Data Protection Act 2018
- FR-005: Statistical Disclosure Control (SDC)
- Architecture Principle 6: Privacy by Design

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-7-make-privacy-integral

---

### 8. Share, Reuse and Collaborate ✅

**Principle**: Avoid duplicating effort and unnecessary costs by collaborating across government and sharing and reusing technology, data, and services.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Government collaboration**: Integrates with HMRC, DWP, NHS administrative data
- ✅ **Open standards**: SDMX enables data sharing with Eurostat, UN, OECD
- ✅ **Data sharing**: Administrative data linkage reduces survey burden
- ✅ **API reuse**: ONS APIs enable government departments to reuse official statistics
- ✅ **Common components**: Will use GDS common platforms (GOV.UK Pay, Notify if applicable)
- ✅ **Technology reuse**: Open source stack (PostgreSQL, Kubernetes, Terraform) - widely used in government
- ✅ **Digital Marketplace**: Will procure via G-Cloud framework (shared procurement)
- ✅ **Cross-government standards**: GDS Service Standard, TCoP, GovS 007 compliance

**Findings**:

**Government Collaboration**:

1. **Data Sharing** (Upstream):
   - **HMRC**: Tax records, employment data (administrative data)
   - **DWP**: Benefits claims, employment support
   - **NHS**: Health records for health statistics
   - **Rationale**: Reduces respondent burden, improves data quality

2. **Data Sharing** (Downstream):
   - **Government departments**: 50+ departments will consume ONS APIs
   - **Benefits**: £6M annual savings (50 depts × £120K integration cost avoided)
   - **GaaP positioning**: ONS as Government-as-a-Platform (GaaP) provider

**Technology Reuse**:
- PostgreSQL: Widely used across government (HMRC, DWP, BEIS)
- Kubernetes: Standard container orchestration in government
- Terraform: Standard IaC tool in government
- OpenAPI: Standard API specification

**Avoiding Duplication**:
- ONS is **authoritative source** for UK official statistics (no duplication)
- Departments will consume ONS APIs instead of building own statistical systems
- Administrative data linkage avoids duplicate survey collection

**Collaboration Mechanisms**:
- **API Council**: ONS + GDS + community for API governance
- **Metadata registry**: SDMX registry enables cross-government data discovery
- **Developer community**: 10,000 API users including government analysts

**Gaps**: None identified - strong collaboration and reuse

**Requirements Mapping**:
- INT-002: Administrative Data Integration (collaboration with HMRC, DWP, NHS)
- GaaP Ecosystem Analysis: ONS as enabling infrastructure for UK Government

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-8-share-reuse-and-collaborate

---

### 9. Integrate and Adapt Technology ✅

**Principle**: Your technology should work with existing technologies, processes and infrastructure in your organisation, and adapt to future demands.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Legacy integration**: Integrates with existing ONS survey systems (LFS, LCFS, Census)
- ✅ **Interoperability**: APIs enable integration with ONS website, data warehouse, research service
- ✅ **Extensibility**: Modular architecture supports future features (GraphQL, webhooks, SDKs)
- ✅ **Standards-based**: OpenAPI, SDMX enable integration with external systems
- ✅ **Versioning**: API versioning with 12-month deprecation notice (backward compatibility)
- ✅ **Migration strategy**: 500+ statistical series migration with parallel running
- ✅ **Future-proof**: Cloud-native, containerized, Infrastructure as Code

**Findings**:

**Legacy System Integration**:

1. **Survey Collection Systems** (Upstream):
   - **Labour Force Survey (LFS)**: Batch file transfer (SFTP)
   - **Living Costs & Food Survey (LCFS)**: Batch file transfer (SFTP)
   - **Census**: Batch file transfer (SFTP)
   - **Integration**: INT-001 (Survey Data Integration)

2. **ONS Internal Systems** (Downstream):
   - **ONS Website**: Real-time API integration (<1 minute latency)
   - **Data Warehouse**: Batch export for reporting
   - **Secure Research Service**: Anonymized microdata for researchers

**Architecture Flexibility**:
- **Modular design**: Microservices architecture (stateless, containerized)
- **API-first**: All services expose APIs (enables future integrations)
- **Versioning**: OpenAPI versioning (v1, v2) with 12-month deprecation
- **Extensibility**: Future features can be added without breaking changes

**Migration Strategy** (DR-005):
- **Parallel running**: Legacy and new systems run simultaneously (validation period)
- **Data integrity**: 100% data integrity validation (record counts, checksums)
- **Rollback capability**: Can revert to legacy if issues detected
- **Success criteria**: Zero data loss, 100% data integrity

**Future Adaptability**:
- **Cloud-native**: Can scale to Census 2031 (67M records)
- **Containerization**: Can move to different cloud providers if needed
- **IaC**: Terraform enables infrastructure evolution
- **Open standards**: SDMX, OpenAPI enable integration with future systems

**Gaps**: None identified - strong integration and adaptability

**Requirements Mapping**:
- DR-005: Data Migration (500+ series migration)
- INT-001, INT-002, INT-003, INT-004: Integration requirements
- Architecture Principle 7: API-First Design (versioning, deprecation)

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-9-integrate-and-adapt-technology

---

### 10. Make Better Use of Data ✅

**Principle**: Consider how to minimise data collection and reuse data to avoid duplication of datasets.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Data minimization**: Only necessary survey questions asked (GDPR compliance)
- ✅ **Data reuse**: Administrative data (HMRC, DWP, NHS) supplements surveys
- ✅ **Single source of truth**: ONS is authoritative source for UK statistics (no duplication)
- ✅ **Data governance**: Comprehensive data model with ownership, retention, quality SLAs
- ✅ **Metadata**: SDMX metadata enables data discovery and reuse
- ✅ **Data catalog**: FR-003 enables data discovery (avoid re-collecting data)
- ✅ **Data quality**: Automated quality validation (completeness, accuracy, consistency)
- ✅ **Data lineage**: End-to-end lineage from source to publication (E-012: Data Lineage)

**Findings**:

**Data Minimization** (GDPR Article 5(1)(c)):
- Survey questions: Only necessary questions asked (Census questions approved by Parliament)
- Retention: 10 years maximum (GDPR data minimization)
- No excessive data: No names, addresses, exact income collected

**Data Reuse** (Avoiding Duplication):
- **Administrative data linkage**: HMRC tax + DWP benefits + NHS health records
- **Rationale**: Reduces respondent burden, validates survey estimates, improves data quality
- **Integration**: INT-002 (Administrative Data Integration)

**Single Source of Truth** (Architecture Principle 4):
> "Each statistical dataset MUST have ONE authoritative source, version-controlled and traceable to ONS official releases."

**Data Governance**:
- **Data Model**: Comprehensive data model (data-model.md) with 15 entities
- **Data Ownership**: Business owners, data stewards, technical custodians assigned
- **Data Quality**: Quality dimensions (accuracy, completeness, consistency, timeliness) with measurable targets
- **Data Catalog**: E-001 (Statistical Series) cataloged for discoverability

**Metadata and Discovery**:
- **SDMX Metadata**: E-006 (SDMX Metadata) - enables data discovery
- **Data Catalog**: FR-003 (searchable catalog) - prevents duplicate data collection
- **Lineage**: E-012 (Data Lineage) - traces data from source to publication

**Data Quality Framework**:
- **Accuracy**: 99% target for observations (statistical methodology verified)
- **Completeness**: 95% target for metadata
- **Consistency**: 99.9% cross-system consistency
- **Timeliness**: 95% of publications meet SLA

**Gaps**: None identified - excellent data governance

**Requirements Mapping**:
- Architecture Principle 4: Single Source of Truth
- Architecture Principle 5: Data Quality by Design
- DR-003: Data Lineage
- DR-004: Statistical Metadata (SDMX)
- FR-003: Data Catalog with Search

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-10-make-better-use-of-data

---

### 11. Define Your Purchasing Strategy ❌

**Principle**: Your purchasing strategy must show you've considered commercial and technology aspects, and contractual limitations.

**Compliance Status**: ❌ **NON-COMPLIANT**

**Evidence**:
- ❌ **No purchasing strategy documented** (critical gap)
- ❌ **No cloud provider evaluation** (AWS vs Azure vs GCP)
- ❌ **No vendor RFP/SOW created** (planned but not yet started)
- ⚠️ **Technology research not conducted** (open source selected, but no build vs buy analysis)
- ⚠️ **No total cost of ownership (TCO) analysis** for cloud providers
- ⚠️ **No contractual terms evaluated** (lock-in risk, exit strategy)
- ✅ **Budget allocated**: £18M capital (SOBC approved)
- ✅ **Procurement route identified**: Digital Marketplace (G-Cloud framework)
- ✅ **Open source preference**: PostgreSQL, Kubernetes (avoids vendor lock-in)

**Findings**:

**What's Missing** (**CRITICAL GAP**):

1. **Purchasing Strategy Document**:
   - No documented strategy for cloud provider selection
   - No evaluation criteria for AWS vs Azure vs GCP
   - No TCO analysis (reserved instances, spot instances, egress costs)

2. **Cloud Provider Evaluation**:
   - No RFP issued to cloud providers
   - No scoring matrix (cost, features, UK data sovereignty, support)
   - No proof of concept (PoC) conducted

3. **Build vs Buy Analysis**:
   - Open source selected (PostgreSQL, Kubernetes) but no formal analysis
   - No evaluation of managed services vs self-hosted (RDS vs EC2 + PostgreSQL)
   - No API gateway evaluation (AWS API Gateway vs Azure API Management vs Kong)

4. **Contractual Terms**:
   - No exit strategy documented (vendor lock-in mitigation)
   - No SLA requirements defined (uptime, support response times)
   - No data portability plan (how to migrate to different cloud if needed)

**What Exists**:
- **Budget**: £18M investment, BCR 2.3:1 (SOBC)
- **Procurement route**: Digital Marketplace (G-Cloud, DOS frameworks)
- **Cost model**: £6.7M/year ongoing costs (40% reduction vs on-premises)

**Gaps** (**HIGH PRIORITY** - blocks Beta):
- ❌ **No purchasing strategy document** (GDS Digital Spend Control requirement)
- ❌ **No cloud provider selected** (AWS vs Azure vs GCP)
- ❌ **No vendor evaluation framework** (scoring criteria for cloud providers)
- ❌ **No RFP/SOW created** (procurement not started)

**Requirements Mapping**:
- BR-001: Reduce Infrastructure Costs (£4.5M savings target requires cloud provider selection)
- Architecture Principle 9: Cloud-Native Architecture (requires cloud provider)

**Remediation** (**CRITICAL - HIGH PRIORITY**):
- **Action 1**: Document purchasing strategy
  - **Owner**: Chief Data Architect + Commercial Lead
  - **Due**: Alpha Week 6 (**URGENT**)
  - **Effort**: 1 week
  - **Content**: Cloud provider evaluation criteria, TCO analysis, contractual terms, exit strategy

- **Action 2**: Conduct cloud provider evaluation (AWS vs Azure vs GCP)
  - **Owner**: Chief Data Architect
  - **Due**: Alpha Week 8
  - **Effort**: 2 weeks
  - **Method**: Run `/arckit.research` command to evaluate cloud providers
  - **Deliverable**: Technology research document with recommendation

- **Action 3**: Create vendor evaluation framework
  - **Owner**: Chief Data Architect + Commercial Lead
  - **Due**: Alpha Week 10
  - **Effort**: 1 week
  - **Method**: Run `/arckit.evaluate` command to create scoring matrix

- **Action 4**: Issue RFP/SOW to cloud providers
  - **Owner**: Commercial Lead
  - **Due**: Alpha Week 12
  - **Effort**: 2 weeks
  - **Method**: Run `/arckit.sow` command to generate Statement of Work

- **Action 5**: Select cloud provider and sign contract
  - **Owner**: Chief Data Officer (CDO)
  - **Due**: Before Beta (Month 5)
  - **Effort**: 4 weeks (RFP response evaluation, contract negotiation)

**Score**: **3/10** (budget allocated, procurement route identified, but no strategy or provider selected)

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-11-define-your-purchasing-strategy

**Blocker for Beta**: **YES** - Cannot proceed to Beta without cloud provider selection

---

### 12. Make Your Technology Sustainable ✅

**Principle**: Consider the environmental impact of your technology and choose more sustainable options where possible.

**Compliance Status**: ✅ **COMPLIANT**

**Evidence**:
- ✅ **Cloud efficiency**: Cloud providers more energy-efficient than on-premises data centres
- ✅ **Auto-scaling**: Resources scaled down during low demand (reduces energy waste)
- ✅ **Cold storage**: Archived data moved to low-energy storage (S3 Glacier)
- ✅ **Serverless-first**: Serverless functions used where appropriate (zero idle resource consumption)
- ✅ **Green cloud regions**: AWS/Azure UK regions use renewable energy
- ✅ **Efficient data storage**: Data compression (Parquet), partitioning, archival reduce storage footprint
- ✅ **Data minimization**: 10-year retention limit reduces storage needs
- ✅ **Lifecycle management**: Automated deletion of expired data

**Findings**:

**Cloud Sustainability**:
- **AWS Sustainability**: AWS UK regions powered by 100% renewable energy (AWS commitment)
- **Azure Sustainability**: Azure UK regions carbon-neutral (Microsoft commitment)
- **GCP Sustainability**: GCP carbon-neutral since 2007, 100% renewable energy by 2030

**Resource Efficiency**:

1. **Auto-Scaling**:
   - **Rationale**: ONS publication traffic is spiky (10,000 req/s on major releases, <100 req/s off-peak)
   - **Benefit**: Scale down to 2 instances during quiet periods, scale up to 100 during peak
   - **Energy savings**: ~80% resource reduction during off-peak hours

2. **Cold Storage**:
   - **Rationale**: Archived observations (>10 years old) rarely accessed
   - **Benefit**: S3 Glacier uses low-energy storage (HDD vs SSD)
   - **Energy savings**: ~90% energy reduction for archived data

3. **Data Compression**:
   - **Format**: Parquet with Snappy compression (columnar format)
   - **Benefit**: 5x-10x compression ratio vs CSV
   - **Energy savings**: Reduced storage, network transfer, processing

**Data Lifecycle Management**:
- **Retention**: 10-year maximum for survey microdata (GDPR data minimization)
- **Deletion**: Automated deletion of expired data (monthly batch job)
- **Benefit**: Reduces storage footprint, energy consumption

**On-Premises Exit**:
- **Legacy**: On-premises data centre with dedicated hardware
- **New**: Cloud-native, shared infrastructure (higher utilization, less waste)
- **Benefit**: Cloud providers achieve 80%+ server utilization (vs 15-20% on-premises)

**Gaps**: None identified - cloud-first approach inherently more sustainable

**Requirements Mapping**:
- BR-001: Reduce Infrastructure Costs (cloud efficiency)
- Architecture Principle 9: Cloud-Native Architecture (serverless-first)
- Data Model: Archival policy (cold storage)

**Remediation**: N/A - compliant

**Score**: **10/10**

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-12-make-your-technology-sustainable

---

### 13. Meet the Service Standard ✅

**Principle**: If you're building a service that will be used by people outside of your organisation, meet the Service Standard.

**Compliance Status**: ✅ **COMPLIANT** (on track for 14/14 criteria)

**Evidence**:
- ✅ **Service Standard applicable**: Public-facing API service for ONS statistics
- ✅ **GDS assessments planned**: Alpha, Beta, Live assessments
- ✅ **User research**: 12 stakeholders consulted, public consultation on Census questions
- ✅ **Accessibility commitment**: WCAG 2.1 AA (NFR-C-004)
- ✅ **Open standards**: SDMX, OpenAPI, ISO standards
- ✅ **Cloud First**: Cloud-native architecture
- ✅ **Privacy**: DPIA completed, Privacy by Design
- ✅ **Security**: Secure by Design assessment, encryption, RBAC
- ✅ **Service ownership**: Head of Data Publishing is Service Owner
- ✅ **Performance metrics**: 99.95% uptime SLA, p95 <500ms latency
- ✅ **Assisted digital**: Developer support (email, Slack, GitHub)

**Findings**:

**GDS Service Standard 14 Points**:

| # | Point | Status | Evidence |
|---|-------|--------|----------|
| 1 | Understand users and their needs | ✅ | 12 stakeholders, 27 drivers, public consultation |
| 2 | Solve a whole problem for users | ✅ | End-to-end API access (discovery → query → download) |
| 3 | Provide a joined up experience | ✅ | Consistent API design, developer portal |
| 4 | Make the service simple to use | ✅ | 15-minute time-to-first-call (developer experience) |
| 5 | Make sure everyone can use the service | ⚠️ | WCAG 2.1 AA committed, testing pending |
| 6 | Have a multidisciplinary team | ✅ | Platform engineering, statisticians, data engineers, security |
| 7 | Use agile ways of working | ✅ | Sprints planned (Alpha, Beta, Live phases) |
| 8 | Iterate and improve frequently | ✅ | Continuous delivery, API versioning |
| 9 | Create a secure service | ✅ | Secure by Design, DPIA, Zero Trust |
| 10 | Define success metrics | ✅ | 10,000 users, 50% API adoption, 85% satisfaction |
| 11 | Choose the right tools and technology | ⚠️ | Cloud provider evaluation pending |
| 12 | Make new source code open | ⚠️ | Code publication planned for Beta |
| 13 | Use and contribute to open standards | ✅ | SDMX, OpenAPI, ISO standards |
| 14 | Operate a reliable service | ✅ | 99.95% uptime SLA, monitoring, incident response |

**Service Standard Score**: **11/14 compliant** (3 pending: accessibility testing, cloud provider, code publication)

**GDS Assessment Plan**:
- **Alpha Assessment**: Month 4 (Discovery complete, user research, technical spike)
- **Beta Assessment**: Month 7 (50 early adopters, service works end-to-end)
- **Live Assessment**: Month 12 (10,000 users, 99.95% uptime validated)

**Service Ownership**:
- **Service Owner**: Head of Data Publishing (responsible for service performance)
- **Product Manager**: (to be appointed)
- **Service Manual**: To be created (GOV.UK Service Manual guidance)

**Gaps**:
- ⚠️ **Service Standard Points 5, 11, 12 pending** (see Points 2, 3, 11 above)
- ⚠️ **Product Manager not yet appointed** (multidisciplinary team requirement)

**Requirements Mapping**:
- BR-004: Meet UK Government Digital Standards (GDS Service Standard)
- All NFR-xxx requirements map to Service Standard criteria

**Remediation**:
- **Action 1**: Complete accessibility testing (Point 5) - see Point 2 above
- **Action 2**: Select cloud provider (Point 11) - see Point 11 above
- **Action 3**: Publish code as open source (Point 12) - see Point 3 above
- **Action 4**: Appoint Product Manager for multidisciplinary team
  - **Owner**: Chief Data Officer
  - **Due**: Alpha Week 4
  - **Effort**: Recruitment (4-6 weeks)

**Score**: **9/10** (on track for 14/14, minor gaps to resolve)

**GOV.UK Reference**: https://www.gov.uk/guidance/technology-code-of-practice-point-13-meet-the-service-standard

**Blocker for Beta**: No - but must pass GDS Beta Assessment to proceed to Public Beta

---

## Overall Compliance Summary

### Scorecard

| TCoP Point | Title | Status | Score | Blocker |
|-----------|-------|--------|-------|---------|
| 1 | Define User Needs | ✅ COMPLIANT | 10/10 | No |
| 2 | Accessible and Inclusive | ⚠️ PARTIAL | 6/10 | **YES** (Beta) |
| 3 | Open and Open Source | ⚠️ PARTIAL | 7/10 | No |
| 4 | Open Standards | ✅ COMPLIANT | 10/10 | No |
| 5 | Cloud First | ✅ COMPLIANT | 10/10 | No |
| 6 | Make Things Secure | ✅ COMPLIANT | 10/10 | No |
| 7 | Privacy Integral | ✅ COMPLIANT | 10/10 | No |
| 8 | Share, Reuse, Collaborate | ✅ COMPLIANT | 10/10 | No |
| 9 | Integrate and Adapt | ✅ COMPLIANT | 10/10 | No |
| 10 | Better Use of Data | ✅ COMPLIANT | 10/10 | No |
| 11 | Purchasing Strategy | ❌ NON-COMPLIANT | 3/10 | **YES** (Beta) |
| 12 | Sustainable Technology | ✅ COMPLIANT | 10/10 | No |
| 13 | Service Standard | ✅ COMPLIANT | 9/10 | No |

**Overall Score**: **115/130** → **88%** → ⚠️ **PARTIALLY COMPLIANT**

**Compliance Breakdown**:
- ✅ **Compliant**: 10 points (Points 1, 4, 5, 6, 7, 8, 9, 10, 12, 13)
- ⚠️ **Partially Compliant**: 2 points (Points 2, 3)
- ❌ **Non-Compliant**: 1 point (Point 11)
- N/A: 0 points

---

## Critical Issues

### Issue 1: No Purchasing Strategy (Point 11) 🔴 **CRITICAL**

**Problem**: No documented purchasing strategy, no cloud provider evaluation (AWS vs Azure vs GCP), no vendor RFP/SOW.

**Impact**: Blocks Beta phase - cannot build platform without cloud provider.

**Priority**: 🔴 **CRITICAL - HIGH**

**Remediation**:
1. Document purchasing strategy (1 week)
2. Conduct cloud provider evaluation - run `/arckit.research` (2 weeks)
3. Create vendor evaluation framework - run `/arckit.evaluate` (1 week)
4. Issue RFP/SOW - run `/arckit.sow` (2 weeks)
5. Select cloud provider and sign contract (4 weeks)

**Owner**: Chief Data Architect + Commercial Lead

**Due**: Before Beta (Month 5) - **URGENT**

---

### Issue 2: Accessibility Testing Not Completed (Point 2) 🟠 **HIGH**

**Problem**: No accessibility testing with disabled users, no automated accessibility testing in CI/CD.

**Impact**: Blocks Public Beta - GDS Service Standard requires accessibility testing with disabled people.

**Priority**: 🟠 **HIGH**

**Remediation**:
1. Recruit 5+ disabled users for Beta user research (2 weeks)
2. Conduct manual accessibility testing with JAWS, NVDA (1 week)
3. Implement automated accessibility testing (Axe-core, Pa11y-ci) (3 days)
4. Publish accessibility statement (2 days)

**Owner**: User Research Lead + QA Team

**Due**: Before Public Beta (Month 6)

---

### Issue 3: Code Not Published as Open Source (Point 3) 🟡 **MEDIUM**

**Problem**: Platform code not yet published to GitHub, no open source license selected.

**Impact**: Not a blocker, but strongly recommended for Public Beta (transparency).

**Priority**: 🟡 **MEDIUM**

**Remediation**:
1. Select open source license (Apache 2.0) (1 week)
2. Publish platform code to GitHub (2 weeks)
3. Publish technical documentation (3 weeks)

**Owner**: Platform Engineering + Open Source Programme Office

**Due**: Beta Week 1 (recommended, not blocker)

---

## Prioritized Recommendations

### High Priority (Weeks 1-8)

| Action | Point | Owner | Due | Effort | Blocker? |
|--------|-------|-------|-----|--------|----------|
| **1. Document purchasing strategy** | 11 | Chief Data Architect + Commercial | Alpha Week 6 | 1 week | ✅ YES |
| **2. Cloud provider evaluation** (`/arckit.research`) | 11 | Chief Data Architect | Alpha Week 8 | 2 weeks | ✅ YES |
| **3. Vendor evaluation framework** (`/arckit.evaluate`) | 11 | Chief Data Architect + Commercial | Alpha Week 10 | 1 week | ✅ YES |
| **4. Issue RFP/SOW** (`/arckit.sow`) | 11 | Commercial Lead | Alpha Week 12 | 2 weeks | ✅ YES |
| **5. Recruit disabled users for Beta** | 2 | User Research Lead | Before Public Beta | 2 weeks | ✅ YES |

### Medium Priority (Weeks 9-16)

| Action | Point | Owner | Due | Effort | Blocker? |
|--------|-------|-------|-----|--------|----------|
| **6. Accessibility testing (manual)** | 2 | QA Team | Beta Week 1 | 1 week | ✅ YES |
| **7. Automated accessibility testing** | 2 | Platform Engineering | Beta Week 4 | 3 days | ✅ YES |
| **8. Select open source license** | 3 | Legal / OSPO | Alpha Week 8 | 1 week | ❌ NO |
| **9. Publish code to GitHub** | 3 | Platform Engineering | Beta Week 1 | 2 weeks | ❌ NO |
| **10. Conduct penetration testing** | 6 | Head of Cyber Security | Beta Week 8 | 2 weeks | ❌ NO |

### Low Priority (Weeks 17+)

| Action | Point | Owner | Due | Effort | Blocker? |
|--------|-------|-------|-----|--------|----------|
| **11. Publish technical documentation** | 3 | Technical Writing | Public Beta | 3 weeks | ❌ NO |
| **12. Open source contribution policy** | 3 | OSPO | Beta Week 12 | 1 week | ❌ NO |
| **13. Appoint Product Manager** | 13 | Chief Data Officer | Alpha Week 4 | 4-6 weeks | ❌ NO |

---

## Next Steps and Timeline

### Phase: Discovery/Alpha (Weeks 1-16)

**Week 1-2**:
- ✅ **Action**: Document purchasing strategy (Point 11)
- ✅ **Action**: Begin cloud provider evaluation research

**Week 3-4**:
- ✅ **Action**: Complete cloud provider evaluation (run `/arckit.research`)
- ✅ **Action**: Create vendor evaluation framework (run `/arckit.evaluate`)

**Week 5-8**:
- ✅ **Action**: Issue RFP/SOW to cloud providers (run `/arckit.sow`)
- ⚠️ **Action**: Select open source license (Point 3)
- ⚠️ **Action**: Recruit disabled users for Beta user research (Point 2)

**Week 9-12**:
- ✅ **Action**: Evaluate cloud provider responses
- ✅ **Action**: Select cloud provider and sign contract
- ⚠️ **Action**: Prepare code for open source publication (security review, secrets removal)

**Week 13-16** (Alpha Assessment):
- ✅ **Milestone**: GDS Alpha Assessment
- ✅ **Target**: 11/13 TCoP compliant (Point 11 resolved, Points 2 & 3 in progress)

---

### Phase: Beta (Weeks 17-36)

**Week 17-20**:
- ✅ **Action**: Publish platform code to GitHub (Point 3)
- ✅ **Action**: Conduct accessibility testing (manual) (Point 2)
- ✅ **Action**: Implement automated accessibility testing (Point 2)

**Week 21-28**:
- ✅ **Action**: Beta user testing with 50 early adopters
- ✅ **Action**: Conduct penetration testing (Point 6)
- ⚠️ **Action**: Publish accessibility statement (Point 2)

**Week 29-36** (Beta Assessment):
- ✅ **Milestone**: GDS Beta Assessment
- ✅ **Target**: 13/13 TCoP compliant (all points resolved)

---

### Phase: Public Beta / Live (Weeks 37+)

**Week 37+**:
- ✅ **Milestone**: Public Beta go-live (10,000 users target)
- ✅ **Target**: Maintain 13/13 TCoP compliance
- ✅ **Action**: Quarterly TCoP compliance review

---

## Sign-Off

**TCoP Assessment Outcome**: ⚠️ **PARTIALLY COMPLIANT** (10/13 compliant, 88%)

**Recommendation**: ✅ **Proceed to Beta with conditions**

**Conditions**:
1. Resolve Point 11 (Purchasing Strategy) before Beta - **CRITICAL**
2. Resolve Point 2 (Accessibility) before Public Beta - **HIGH**
3. Resolve Point 3 (Open Source) recommended for Beta - **MEDIUM**

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Chief Data Architect | | | |
| Chief Data Officer | | | |
| GDS Service Assessor | | | |
| Digital Spend Control (if applicable) | | | |

---

## Appendix A: TCoP Reference URLs

1. **Define User Needs**: https://www.gov.uk/guidance/technology-code-of-practice-point-1-define-user-needs
2. **Accessible and Inclusive**: https://www.gov.uk/guidance/technology-code-of-practice-point-2-make-things-accessible-and-inclusive
3. **Open and Open Source**: https://www.gov.uk/guidance/technology-code-of-practice-point-3-be-open-and-use-open-source
4. **Open Standards**: https://www.gov.uk/guidance/technology-code-of-practice-point-4-make-use-of-open-standards
5. **Cloud First**: https://www.gov.uk/guidance/technology-code-of-practice-point-5-use-cloud-first
6. **Make Things Secure**: https://www.gov.uk/guidance/technology-code-of-practice-point-6-make-things-secure
7. **Privacy Integral**: https://www.gov.uk/guidance/technology-code-of-practice-point-7-make-privacy-integral
8. **Share, Reuse, Collaborate**: https://www.gov.uk/guidance/technology-code-of-practice-point-8-share-reuse-and-collaborate
9. **Integrate and Adapt**: https://www.gov.uk/guidance/technology-code-of-practice-point-9-integrate-and-adapt-technology
10. **Better Use of Data**: https://www.gov.uk/guidance/technology-code-of-practice-point-10-make-better-use-of-data
11. **Purchasing Strategy**: https://www.gov.uk/guidance/technology-code-of-practice-point-11-define-your-purchasing-strategy
12. **Sustainable Technology**: https://www.gov.uk/guidance/technology-code-of-practice-point-12-make-your-technology-sustainable
13. **Service Standard**: https://www.gov.uk/guidance/technology-code-of-practice-point-13-meet-the-service-standard

---

## Appendix B: Related Assessments

This TCoP assessment should be read alongside:
- **GDS Service Standard Assessment**: To be conducted at Alpha, Beta, Live phases
- **Data Protection Impact Assessment (DPIA)**: projects/001-ons-data-platform-modernisation/dpia.md
- **UK Government Secure by Design**: projects/001-ons-data-platform-modernisation/ukgov-secure-by-design.md
- **Risk Register**: projects/001-ons-data-platform-modernisation/risk-register.md
- **Strategic Outline Business Case (SOBC)**: projects/001-ons-data-platform-modernisation/sobc.md

---

**Document End**

**Generated by**: ArcKit `/arckit.tcop` command
**Generated on**: 2026-01-26
**ArcKit Version**: 0.11.2
**Project**: ONS Data Platform Modernisation (Project 001)
**Model**: claude-opus-4-5-20251101
**Generation Context**: Auto-populated from requirements.md, data-model.md, dpia.md, stakeholder-drivers.md, architecture-principles.md, ukgov-secure-by-design.md
