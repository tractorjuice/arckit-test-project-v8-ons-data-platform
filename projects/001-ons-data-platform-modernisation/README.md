# ONS Data Platform Modernisation

Project ID: 001
Created: 2025-11-01

## Overview

[Project description to be added]

## Workflow

Use ArcKit commands to generate project artifacts in the recommended order:

### Discovery Phase
1. `/arckit.stakeholders` - Analyze stakeholder drivers and goals
2. `/arckit.risk` - Create risk register
3. `/arckit.sobc` - Create Strategic Outline Business Case

### Alpha Phase
4. `/arckit.requirements` - Define comprehensive requirements
5. `/arckit.data-model` - Design data model and GDPR compliance
6. `/arckit.wardley` - Create Wardley maps for strategic planning
7. `/arckit.research` - Research technology options (if needed)
8. `/arckit.sow` - Generate Statement of Work for vendor procurement (if needed)
9. `/arckit.evaluate` - Create vendor evaluation framework (if needed)

### Beta Phase
10. `/arckit.hld-review` - Review High-Level Design
11. `/arckit.dld-review` - Review Detailed Design
12. `/arckit.traceability` - Generate requirements traceability matrix

### Compliance (as needed)
- `/arckit.secure` - UK Government Secure by Design review
- `/arckit.tcop` - Technology Code of Practice assessment
- `/arckit.ai-playbook` - AI Playbook compliance (for AI systems)

## Project Structure

Documents will be created in this directory as you run ArcKit commands:

```
001-ons-data-platform-modernisation/
├── README.md (this file)
├── stakeholder-analysis.md (from /arckit.stakeholders)
├── risk-register.md (from /arckit.risk)
├── sobc.md (from /arckit.sobc)
├── requirements.md (from /arckit.requirements)
├── data-model.md (from /arckit.data-model)
├── sow.md (from /arckit.sow)
├── evaluation-criteria.md (from /arckit.evaluate)
├── traceability-matrix.md (from /arckit.traceability)
├── hld-review-YYYYMMDD.md (from /arckit.hld-review)
├── dld-review-YYYYMMDD.md (from /arckit.dld-review)
├── wardley-maps/ (from /arckit.wardley)
└── vendors/ (vendor proposals)
```

## Status

Track your progress through the workflow:

**Discovery Phase:**
- [ ] Stakeholder analysis complete
- [ ] Risk register created
- [ ] Business case approved

**Alpha Phase:**
- [ ] Requirements defined
- [ ] Data model designed
- [ ] Vendor procurement started (if needed)

**Beta Phase:**
- [ ] HLD reviewed and approved
- [ ] DLD reviewed and approved
- [ ] Traceability matrix validated

**Live Phase:**
- [ ] Implementation complete
- [ ] Production deployment
