# ONS Data Platform

Office for National Statistics data analytics platform

## Overview

This is an ArcKit-managed enterprise architecture governance project.

## Getting Started

This project uses ArcKit for enterprise architecture governance and vendor procurement.

### Available Commands

Once you start your AI assistant, you'll have access to these commands:

#### Project Planning
- `/arckit.plan` - Create project plan with timeline, phases, and gates

#### Core Workflow
- `/arckit.principles` - Create or update architecture principles
- `/arckit.stakeholders` - Analyze stakeholder drivers, goals, and outcomes
- `/arckit.risk` - Create comprehensive risk register (Orange Book)
- `/arckit.sobc` - Create Strategic Outline Business Case (Green Book 5-case)
- `/arckit.requirements` - Define comprehensive requirements
- `/arckit.data-model` - Create data model with ERD, GDPR compliance, data governance
- `/arckit.research` - Research technology, services, and products with build vs buy analysis
- `/arckit.wardley` - Create strategic Wardley Maps for build vs buy and procurement strategy

#### Vendor Procurement
- `/arckit.sow` - Generate Statement of Work (RFP)
- `/arckit.dos` - Digital Outcomes and Specialists (DOS) procurement
- `/arckit.gcloud-search` - Search G-Cloud services on UK Digital Marketplace
- `/arckit.gcloud-clarify` - Validate G-Cloud services and generate clarification questions
- `/arckit.evaluate` - Create vendor evaluation framework and score vendors

#### Design Review
- `/arckit.hld-review` - Review High-Level Design
- `/arckit.dld-review` - Review Detailed Design

#### Architecture Diagrams
- `/arckit.diagram` - Generate visual architecture diagrams using Mermaid

#### Sprint Planning
- `/arckit.backlog` - Generate prioritised product backlog with GDS user stories

#### Service Management
- `/arckit.servicenow` - Generate ServiceNow service design

#### Traceability & Quality
- `/arckit.traceability` - Generate requirements traceability matrix
- `/arckit.analyze` - Comprehensive governance quality analysis

#### UK Government Compliance
- `/arckit.service-assessment` - GDS Service Standard assessment preparation
- `/arckit.tcop` - Technology Code of Practice assessment
- `/arckit.ai-playbook` - AI Playbook compliance for responsible AI
- `/arckit.atrs` - Algorithmic Transparency Recording Standard (ATRS) record

#### Security Assessment
- `/arckit.secure` - UK Government Secure by Design
- `/arckit.mod-secure` - MOD Secure by Design
- `/arckit.jsp-936` - MOD JSP 936 AI assurance documentation

## Project Structure

```
ONS Data Platform/
├── .arckit/
│   ├── memory/           # Global principles
│   ├── templates/        # Document templates
│   └── scripts/bash/     # Helper scripts
├── .claude/commands/     # ArcKit slash commands
├── docs/
│   ├── guides/           # Command usage guides
│   └── README.md         # Documentation index
├── projects/             # Project artifacts
│   └── 001-project-name/
│       ├── requirements.md
│       ├── stakeholder-drivers.md
│       └── vendors/
├── DEPENDENCY-MATRIX.md  # Command dependencies
└── WORKFLOW-DIAGRAMS.md  # Visual workflows
```

## Next Steps

1. Start your AI assistant: `claude`
2. Run `/arckit.principles` to establish architecture governance
3. Create your first project with `/arckit.requirements`

## Documentation

- [ArcKit Documentation](https://github.com/tractorjuice/arc-kit)
- [Command Guides](docs/guides/)
- [Dependency Matrix](DEPENDENCY-MATRIX.md)
