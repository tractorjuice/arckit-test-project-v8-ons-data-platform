# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **ArcKit demonstration project** showcasing enterprise architecture governance artifacts for the **ONS (Office for National Statistics) Data Platform Modernisation** initiative. It demonstrates the systematic generation of architecture documents using ArcKit's 40 slash commands.

**Current Project**: `projects/001-ons-data-platform-modernisation/`

## Using ArcKit Commands

ArcKit slash commands generate architecture artifacts in a structured workflow. Commands follow the pattern `/arckit.{name}` and create markdown files in the project directory.

### Recommended Workflow Order

```
Phase 0: /arckit.plan           → project-plan.md
Phase 1: /arckit.principles     → .arckit/memory/architecture-principles.md (global)
Phase 2: /arckit.stakeholders   → stakeholder-drivers.md
Phase 3: /arckit.risk           → risk-register.md
Phase 4: /arckit.sobc           → sobc.md (Strategic Outline Business Case)
Phase 5: /arckit.requirements   → requirements.md
Phase 5.5: /arckit.data-model   → data-model.md
Phase 5.7: /arckit.dpia         → dpia.md (Data Protection Impact Assessment)
Phase 6: /arckit.research       → research-findings.md
Phase 7: /arckit.wardley        → wardley-maps/*.md
```

### UK Government Compliance Commands

```
/arckit.tcop                    → tcop-review.md (Technology Code of Practice)
/arckit.secure                  → ukgov-secure-by-design.md
/arckit.ai-playbook             → ai-playbook-assessment.md
/arckit.atrs                    → atrs-record.md (Algorithmic Transparency)
/arckit.service-assessment      → service-assessment-{phase}-prep.md
```

### Key Rules for Command Execution

1. **Check prerequisites first** - Many commands require prior artifacts (e.g., requirements needs stakeholders)
2. **Use Write tool for large documents** - Commands should write to file and show summary only to avoid 32K token limit
3. **Read templates before generating** - Templates are in `.arckit/templates/{type}-template.md`
4. **Use helper scripts** - Project creation: `.arckit/scripts/bash/create-project.sh --name "X" --json`

## Repository Structure

```
.arckit/
├── memory/                    # Global architecture principles
├── templates/                 # Document templates (40 templates)
└── scripts/bash/              # Helper scripts (create-project.sh, generate-document-id.sh)

.claude/commands/              # Slash command definitions (arckit.*.md)

projects/
└── 001-ons-data-platform-modernisation/
    ├── stakeholder-drivers.md
    ├── risk-register.md
    ├── sobc.md
    ├── requirements.md
    ├── data-model.md
    ├── dpia.md
    ├── tcop-review.md
    ├── ukgov-secure-by-design.md
    └── PROJECT-STORY.md

docs/
├── guides/                    # Command playbooks (40 guides)
└── index.html                 # Documentation site
```

## Requirement ID Conventions

When generating requirements or reviewing artifacts, use these prefixes:

- **BR-xxx**: Business Requirements
- **FR-xxx**: Functional Requirements
- **NFR-xxx**: Non-Functional Requirements (NFR-P-xxx Performance, NFR-SEC-xxx Security, NFR-A-xxx Availability)
- **INT-xxx**: Integration Requirements
- **DR-xxx**: Data Requirements

## Traceability Chain

ArcKit maintains end-to-end traceability:

```
Stakeholder → Driver → Goal → Requirement → Data Entity → Component → User Story → Sprint
```

## UK Government Context

This project targets UK public sector delivery and should align with:

- **GDS Service Standard** (14 points) - mandatory for government digital services
- **Technology Code of Practice** (13 points) - guidance on technology decisions
- **HM Treasury Green Book** - business case 5-case model (SOBC)
- **HM Treasury Orange Book** - risk management framework
- **NCSC CAF** - cyber security assessment framework
- **UK GDPR / DPA 2018** - data protection requirements
